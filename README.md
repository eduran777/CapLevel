# CapLevel
Adquisición de nivel por capacitancia 🌊⚡

Bienvenido al repositorio de **CapLevel**, un sistema de medición de nivel de líquido basado en sensores capacitivos, desarrollado como parte del curso de **Sensores y Actuadores 2024-II** de la Universidad Nacional de Colombia 🎓🇨🇴.

## 📌 Descripción del Proyecto

CapLevel permite estimar el nivel de un líquido en un recipiente utilizando un sensor capacitivo conectado a un microcontrolador **PIC18F4550**. El sistema convierte la señal analógica en datos digitales mediante un **ADC** de 10 bits y transmite los valores por **UART** hacia una interfaz gráfica desarrollada en **Python con Tkinter**, que muestra el voltaje, el nivel estimado y el estado de conexión.  

La interfaz también permite al usuario seleccionar el tipo de líquido y la configuración del condensador, brindando flexibilidad y personalización del sistema.

---

## ⚙️ Características Técnicas

- 🔌 **Sensor capacitivo:** Detecta variaciones de capacitancia según el nivel de líquido.
- 📟 **Microcontrolador PIC18F4550:**
  - ADC de 10 bits.
  - Comunicación serial UART.
- 🖥️ **Interfaz gráfica en Python (Tkinter):**
  - Selección de tipo de líquido y configuración del sensor.
  - Muestra de voltaje, nivel estimado y estado de conexión.
- 🧮 **Promedio digital:** Se promedian 10 muestras para reducir ruido y obtener valores estables.
- 📡 **Resolución del ADC:** 4.89 mV por unidad digital.
- ⏱️ **Frecuencia de muestreo estimada:** ~9.6 Hz.

---

## 🧪 Resultados de Prueba

Se realizaron pruebas para comparar el nivel real con el nivel medido por el sistema, obteniendo errores absolutos menores al 6% en todos los casos. El tiempo de estabilización varía según el nivel y condiciones del líquido.

---

## 🛠️ Tecnologías Usadas

- Lenguaje C (para microcontrolador)
- MPLAB X + XC8
- Python 3 + Tkinter
- Comunicación UART (serial)
- Sensor capacitivo personalizado
- Fuente de voltaje regulada 5V 🔋

---

## 🧰 Cómo Usar

1. Conectar el sensor capacitivo al canal **AN0** del PIC18F4550.
2. Alimentar el sistema con 5V.
3. Ejecutar el programa Python en un computador conectado por USB.
4. Seleccionar el tipo de líquido y tipo de condensador.
5. Observar en pantalla el voltaje y nivel estimado en tiempo real 📈.

---

## 📁 Estructura del Repositorio

# 📁 Estructura del Repositorio

```plaintext
CapLevel/
├── firmware/             # Código en C para el PIC18F4550
│   ├── main.c
│   ├── config_bits.c
│   └── uart_adc.c
│
├── interface/            # Interfaz gráfica desarrollada en Python
│   ├── gui.py
│   └── utils.py
│
├── data/                 # Tablas de resultados y mediciones
│   ├── tabla_mediciones.csv
│   └── resultados.xlsx
│
├── images/               # Capturas de pantalla y diagramas del sistema
│   ├── interfaz.png
│   ├── pruebas_sensor.png
│   └── esquematico_sensor.png
│
└── README.md             # Documento principal del proyecto




---

## 🧑‍🔬 Autores

- Esteban Durán Jiménez 👨‍💻
- Juan Ángel 🔧
- Stewart ⚙️
- Ariadna 🧪
- Universidad Nacional de Colombia – Sede Bogotá
---

## 📢 Nota Final

Este proyecto fue desarrollado con fines académicos para demostrar la aplicación práctica de sensores capacitivos en la medición de nivel. Para implementaciones industriales se recomienda realizar pruebas de calibración rigurosas y considerar el tipo de líquido y el entorno operativo.

---

¡Gracias por visitar este repositorio! 🌟 Si encuentras útil este proyecto, no dudes en darle ⭐ en GitHub.
