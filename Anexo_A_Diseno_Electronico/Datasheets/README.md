
# Hojas de datos y documentación técnica de componentes

---

## 1. Descripción general

Este directorio contiene las hojas de datos (*datasheets*), fichas técnicas y manuales de los principales componentes utilizados en el diseño y desarrollo de una estación de carga de corriente alterna (AC) para vehículos eléctricos, alimentada mediante un sistema de generación solar fotovoltaica, almacenamiento de energía en baterías y respaldo de la red eléctrica.

La documentación recopilada permite consultar las características eléctricas, especificaciones técnicas, condiciones de operación, interfaces de comunicación y recomendaciones de conexión de los dispositivos seleccionados.

Estos documentos constituyen material de referencia para el diseño, dimensionamiento, integración y validación experimental de los subsistemas de la estación.

---

## 2. Documentación de componentes

### 2.1. Generación, almacenamiento y conversión de energía

| Componente | Función dentro del sistema | Documentación |
|---|---|---|
| Panel solar Suntech 550 W | Generación de energía eléctrica a partir de radiación solar. | [Ficha técnica](./Panel Solar Suntech 550W.pdf) |
| Controlador de carga MPPT ML2440 | Regulación de la energía proveniente del sistema fotovoltaico y gestión de carga del banco de baterías. | [Ficha técnica](./Ficha_tecnica_Controlador_MPPT_sr_ml_12_24-LCD.pdf) / [Manual](./manual-Controlador-mppt-12-24.pdf) |
| Inversor de onda sinusoidal pura 1000 W | Conversión de corriente continua (DC) a corriente alterna (AC) para alimentar la estación de carga. | [Ficha técnica](./datasheet-inversor-belttt.pdf) / [Manual](./manual-de-usuario-inversor-onda-pura-1000w-12v-belttt.pdf) |

### 2.2. Control, adquisición de datos y comunicaciones

| Componente | Función dentro del sistema | Documentación |
|---|---|---|
| Raspberry Pi Zero 2 W | Unidad central de procesamiento, supervisión y adquisición de información del sistema. | [Ficha técnica](./RP-008359-DS-1-raspberry-pi-zero-2-w-product-brief.pdf) |
| ADS1015 | Conversión de señales analógicas a digitales para la adquisición de variables eléctricas. | [Datasheet](./ads1015.pdf) |
| ACS758 | Sensor de corriente basado en efecto Hall, empleado para la medición de corriente del sistema fotovoltaico. | [Datasheet](./ACS758.PDF) |
| Shunt FL-2 | Resistencia de precisión para la medición de corriente del banco de baterías mediante la caída de tensión en sus terminales. | [Datasheet](./FL2-shunt.pdf) |
| DS18B20 | Sensor digital para la supervisión de temperatura mediante comunicación 1-Wire. | [Datasheet](./DS18B20.PDF) |
| SC16IS740/750 | Interfaz de comunicación que permite integrar puertos UART mediante el bus I²C/SPI. | [Datasheet](./SC16IS740%20%281%29.PDF) |
| MAX3222 | Circuito integrado para la adaptación de niveles de comunicación serial RS-232. | [Datasheet](./MAX3222.PDF) |
| MAX485 | Transceptor para comunicación serial diferencial RS-485. | [Datasheet](./MAX485.PDF) |

### 2.3. Sistema de carga y medición de energía

| Componente | Función dentro del sistema | Documentación |
|---|---|---|
| Controlador de carga EVSE EKEPC2 | Control y supervisión de la interfaz de carga AC del vehículo eléctrico. | [Ficha técnica](./Controlador_de_Carga_EVSE_EKEPC2.pdf) |
| Medidor de energía PZEM-016 | Medición de voltaje, corriente, potencia y energía eléctrica en corriente alterna mediante comunicación RS-485/Modbus. | [Ficha técnica](./Medidor-de-Energia-Potencia-Voltaje-Corriente-RS485-Modbus-PZEM-016.pdf) |

### 2.4. Protecciones y maniobra eléctrica

| Componente | Función dentro del sistema | Documentación |
|---|---|---|
| EKL6-100B Type B RCCB | Dispositivo de protección diferencial para la detección de corrientes residuales. | [Ficha técnica](./EKL6-100B_Type_B_RCCB.pdf) |
| EKMF AC Modular Contactor | Elemento de maniobra para la conexión y desconexión de circuitos eléctricos de corriente alterna. | [Ficha técnica](./EKMF%20Din%20AC%20Modular%20Contactor.pdf) |

---

## 3. Organización de los documentos

Los archivos PDF se encuentran almacenados directamente en este directorio.

Para facilitar su consulta, los documentos mantienen nombres relacionados con la referencia comercial del componente, el fabricante o el tipo de equipo.

La documentación se encuentra organizada conceptualmente en cuatro categorías:

1. **Generación, almacenamiento y conversión de energía:** componentes relacionados con la generación fotovoltaica, regulación de carga y conversión de energía eléctrica.

2. **Control, adquisición de datos y comunicaciones:** dispositivos electrónicos utilizados para el procesamiento, adquisición, acondicionamiento y transmisión de señales.

3. **Sistema de carga y medición de energía:** componentes destinados al control de la carga vehicular y a la medición de variables eléctricas.

4. **Protecciones y maniobra eléctrica:** dispositivos destinados a la protección de los circuitos y al control de conexión y desconexión de cargas.

Se incluyen tanto hojas de datos como manuales de instalación y operación cuando estos últimos contienen información relevante para la integración del sistema.

---


## 4. Consideraciones técnicas

- Las especificaciones técnicas deben verificarse de acuerdo con la referencia y versión del componente empleado.
- Los valores eléctricos y las condiciones de operación indicados por los fabricantes constituyen la referencia para la selección e integración de dispositivos.
- La configuración de los equipos debe corresponder con los parámetros eléctricos establecidos durante el dimensionamiento del sistema.
- Los dispositivos de protección deben verificarse conforme a las condiciones de operación y a la normativa eléctrica aplicable.
- Los documentos pertenecen a sus respectivos fabricantes y se incluyen con fines de consulta técnica y académica.
- La presencia de un documento en este directorio no sustituye las pruebas de funcionamiento, las verificaciones de seguridad ni la validación experimental de la estación.

---

**Trabajo de grado para optar por el título de Ingeniero Mecatrónico**

**Diseño y validación a escala de una estación de carga vehicular con energía solar, almacenamiento en baterías y respaldo de red**

**Pontificia Universidad Javeriana**

**Facultad de Ingeniería — Ingeniería Mecatrónica**
