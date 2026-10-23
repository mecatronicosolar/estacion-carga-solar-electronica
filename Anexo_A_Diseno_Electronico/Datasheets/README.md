# Hojas de datos y documentación técnica de componentes

## 1. Descripción general

Este directorio contiene las hojas de datos (*datasheets*), fichas técnicas y manuales de los principales componentes utilizados en el diseño y desarrollo de una estación de carga de corriente alterna (AC) para vehículos eléctricos, alimentada mediante un sistema de generación solar fotovoltaica, almacenamiento de energía en baterías y respaldo de la red eléctrica.

La documentación recopilada permite consultar las características eléctricas, especificaciones técnicas, condiciones de operación, interfaces de comunicación y recomendaciones de conexión de los dispositivos seleccionados.

Estos documentos constituyen material de referencia para el diseño, dimensionamiento, integración y validación experimental de los subsistemas de la estación.

## 2. Documentación de componentes

### 2.1. Generación, almacenamiento y conversión de energía

| Componente | Función dentro del sistema |
|---|---|
| Panel solar Suntech 550 W | Generación de energía eléctrica a partir de radiación solar. |
| Controlador de carga MPPT ML2440  | Regulación de la energía proveniente del sistema fotovoltaico y gestión de carga del banco de baterías. |
| Inversor de Corriente Onda Pura 1000W / 12V / 24V | Conversión de corriente continua (DC) a corriente alterna (AC) para alimentar la estación de carga. |

**Documentación disponible:** ficha técnica del panel fotovoltaico, ficha y manual del controlador MPPT, datasheet y manual del inversor.

### 2.2. Control, adquisición de datos y comunicaciones

| Componente | Función dentro del sistema |
|---|---|
| Raspberry Pi Zero 2 W | Unidad central de procesamiento, supervisión y adquisición de información del sistema. |
| ADS1015 | Conversión de señales analógicas a digitales para la adquisición de variables eléctricas. |
| ACS758 | Sensor de corriente basado en efecto Hall, empleado para la medición de corriente del sistema fotovoltaico. |
| DS18B20 | Sensor digital para la supervisión de temperatura. |
| SC16IS740/750 | Interfaz de comunicación que permite integrar puertos UART mediante el bus I²C/SPI. |
| MAX3222 | Circuito integrado de interfaz para comunicación serial RS-232. |
| MAX485 | Transceptor para comunicación serial diferencial RS-485. |

### 2.3. Sistema de carga y medición de energía

| Componente | Función dentro del sistema |
|---|---|
| Controlador de carga EVSE EKEPC2 | Control y supervisión de la interfaz de carga AC del vehículo eléctrico. |
| Medidor de Energía PZEM-016 | Medición de variables eléctricas de corriente alterna y energía consumida durante la operación de la estación. |

### 2.4. Protecciones y maniobra eléctrica

| Componente | Función dentro del sistema |
|---|---|
| EKL6-100B Type B RCCB | Dispositivo de protección diferencial para la detección de corrientes residuales. |
| EKMF AC Modular Contactor | Elemento de maniobra para la conexión y desconexión de circuitos eléctricos de corriente alterna. |

## 3. Organización de los documentos

Los archivos PDF se encuentran almacenados directamente en este directorio.

Para facilitar su consulta, los documentos mantienen nombres relacionados con la referencia comercial del componente, el fabricante o el tipo de equipo.

Se incluyen tanto hojas de datos como manuales de instalación y operación, cuando estos últimos contienen información relevante para la integración del sistema.

## 4. Relación con el diseño electrónico

La selección e integración de los componentes se encuentra representada en los diagramas del sistema y, cuando corresponde, en el esquemático electrónico desarrollado en Altium Designer.

Los archivos del esquemático pueden consultarse en el directorio:

[**Ver esquemático electrónico**](../Esquematico/)

## 5. Consideraciones

- Las especificaciones técnicas deben verificarse de acuerdo con la referencia y versión del componente empleado.
- Los valores eléctricos y las condiciones de operación indicados por los fabricantes constituyen la referencia para la selección e integración de dispositivos.
- Los documentos pertenecen a sus respectivos fabricantes y se incluyen con fines de consulta técnica y académica.
- La presencia de un documento en este directorio no sustituye las pruebas de funcionamiento, las verificaciones de seguridad ni la validación experimental de la estación.

---

**Trabajo de grado — Ingeniería Mecatrónica**

**Pontificia Universidad Javeriana**
