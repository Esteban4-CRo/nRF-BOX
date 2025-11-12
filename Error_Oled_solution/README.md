# 🖥️ Pantalla OLED con ESP32

Configuración completa para conectar una pantalla OLED SSD1306 via I²C a un ESP32.

![Mi OLED 1,3](./Oled.png)

## Conexiones

| OLED | ESP32 |
|------|-------|
| VCC | 3V3 |
| GND | GND |
| SDA | GPIO 21 |
| SCL | GPIO 22 |

## Código Escáner I²C

```cpp
#include <Wire.h>

void setup() {
  Serial.begin(115200);
  Wire.begin(21, 22); // SDA=21, SCL=22
  Serial.println("Escaneando I2C...");
}

void loop() {
  byte error, address;
  int nDevices = 0;

  for (address = 1; address < 127; address++) {
    Wire.beginTransmission(address);
    error = Wire.endTransmission();

    if (error == 0) {
      Serial.print("Dispositivo encontrado en 0x");
      if (address < 16) Serial.print("0");
      Serial.println(address, HEX);
      nDevices++;
    }
  }

  if (nDevices == 0) {
    Serial.println("No se detectaron dispositivos I2C");
  }
  delay(3000);
}
```

## Código de Prueba OLED

```cpp
#include <Wire.h>
#include <Adafruit_GFX.h>
#include <Adafruit_SSD1306.h>

#define SCREEN_WIDTH 128
#define SCREEN_HEIGHT 64
#define OLED_ADDR 0x3C  // Usar 0x3D si es necesario

Adafruit_SSD1306 display(SCREEN_WIDTH, SCREEN_HEIGHT, &Wire, -1);

void setup() {
  if(!display.begin(SSD1306_SWITCHCAPVCC, OLED_ADDR)) {
    Serial.println("Error al inicializar OLED");
    while(true);
  }
  
  display.clearDisplay();
  display.setTextSize(1);
  display.setTextColor(SSD1306_WHITE);
  display.setCursor(0,0);
  display.println("¡OLED Funciona!");
  display.println("ESP32 + SSD1306");
  display.display();
}

void loop() {
  // Mantener mensaje estático
}
```

## 📚 Librerías Requeridas

Instalar via Arduino IDE Library Manager:
- **Adafruit GFX Library**
- **Adafruit SSD1306**

## 🔍 Solución de Problemas

###  No detecta dispositivo I²C
- Verificar conexiones SDA/SCL (GPIO 21/22)
- Confirmar alimentación 3.3V
- Revisar soldaduras y cables

###  Pantalla en blanco
- Probar ambas direcciones: `0x3C` y `0x3D`
- Verificar instalación de librerías
- Confirmar pines correctos

###  Texto distorsionado
- Revisar conexión GND común
- Verificar calidad de cables

##  Resultados Esperados

**Escáner I²C exitoso:**
```
Escaneando I2C...
Dispositivo encontrado en 0x3C
```

**Pantalla OLED funcionando:**
- Texto "¡OLED Funciona!" visible
- Display limpio sin artefactos

##  Configuración Arduino IDE

1. **Seleccionar placa:** `ESP32 Dev Module`
2. **Puerto correcto** (COMx o /dev/ttyUSBx)
3. **Monitor Serial** a 115200 baudios

---
