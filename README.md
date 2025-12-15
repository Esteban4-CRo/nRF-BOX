# nRFBox - Proyecto de Aprendizaje

---

## Descripción

Proyecto educativo basado en el concepto de **nRFBox**, diseñado para el **aprendizaje en entornos controlados**.
Incluye una versión mejorada con correcciones y componentes actualizados.

### Repositorio de referencia

**[https://www.youtube.com/watch?v=fdLniWPArmw&t=619s](https://github.com/cifertech/nRFBox.git)]**

---

## Componentes Requeridos

---

## Electrónicos Principales

| Componente                          | Imagen                                                                                                                                            | Descripción                                   |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- |
| **ESP32 WROOM 32U**                 | <img src="https://cdnx.jumpseller.com/mactornica/image/18172426/H926b1be9ccff47c69563694b726cef17p.webp?1655400654" width="120"/>                 | Microcontrolador principal con WiFi/Bluetooth |
| **ESP32 WROOM 32**                  | <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRRHrFQJuoWDZ9F5hOc4_knXqrqqHQkSiM5YA&s" width="120"/>                             | Alternativa funcional para prototipos         |
| **Antena WiFi SMA**                 | <img src="https://www.sigmaelectronica.net/wp-content/uploads/2020/11/ANTENA-WIFI-SMA-M.jpg" width="120"/>                                        | Mejora de recepción WiFi                      |
| **nRF24L01 PA-LNA (Largo Alcance)** | <img src="https://ae01.alicdn.com/kf/HTB1W9CuUSzqK1RjSZPcq6zTepXag/SPI-nRF24L01-PA-LNA-2-4-GHz-Rf-m-dulo-E01-ML01DP5-2-5-km-de.jpg" width="120"/> | Módulo RF de largo alcance                    |
| **nRF24L01 Estándar (Alcance M)**   | <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQmGQfGSmjzNnnoCHXciU73zUsaSPXnrTgxfQ&s" width="120"/>                             | Comunicación RF estándar                      |

---

## Pantallas e Interfaces

| Componente             | Imagen                                                                                                                                 | Descripción                      |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
| **OLED 1.3" I2C**      | <img src="https://electronilab.co/wp-content/uploads/2020/11/Display-OLED-1.3-128%C3%9764-I2C-Bajo-Consumo-Blanco-2.jpg" width="120"/> | Pantalla grande para información |
| **OLED 0.96" I2C**     | <img src="https://cdnx.jumpseller.com/mactornica/image/12200829/resize/570/765?1658260693" width="120"/>                               | Alternativa compacta             |
| **Botón Pulsador**     | <img src="https://electronilab.co/wp-content/uploads/2019/02/Micro-Boton-Pulsador-Switch-de-4-pines-1.jpg" width="120"/>               | Control básico                   |
| **Módulo LED WS2812B** | <img src="https://naylampmechatronics.com/4090-superlarge_default/modulo-led-rgb-ws2812b.jpg" width="120"/>                            | Indicador RGB programable        |

---

## Conectividad y Alimentación

| Componente             | Imagen                                                                                                                  | Descripción               |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------------------------- |
| **Cables Dupont**      | <img src="https://www.lacasadelabanda.com/wp-content/uploads/2021/12/Jumper-macho-macho-20-cm-x-10-1.jpg" width="120"/> | Conexión para prototipado |
| **Protoboard 400 pts** | <img src="https://sumador.com/cdn/shop/products/Protoboardde400puntos_2048x2048.jpg?v=1588537859" width="120"/>         | Base para pruebas         |

---

## Recursos Descargables

**Drivers y Firmware:**
[https://mega.nz/folder/OQpDnLgY#gKpLGsnu_np7O00hVTvWxg](https://mega.nz/folder/OQpDnLgY#gKpLGsnu_np7O00hVTvWxg)

Incluye:

* Librerías necesarias
* Controladores
* Firmware base
* Documentación técnica

---

## Esquemáticos

### Diagrama preliminar

> *Sujeto a cambios durante el desarrollo.*

<img src="./Esquema.png" width="500"/>

---

## Resultado

### Ensamblaje esperado

> Así debería verse el nRFBox siguiendo el esquemático:

<img src="./MediumR.jpg" width="500"/>

---

### Encendido

<img src="./FinalR.jpg" width="500"/>

---

## Advertencia de Seguridad

Este proyecto es **exclusivamente para fines educativos en ambientes controlados**.
El uso indebido de equipos RF puede vulnerar normativas locales.
