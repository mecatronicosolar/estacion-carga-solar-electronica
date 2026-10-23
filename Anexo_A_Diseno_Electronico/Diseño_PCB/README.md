
# Diseño electrónico y tarjeta de circuito impreso (PCB)



## 1. Descripción general

Este directorio contiene los archivos correspondientes al diseño esquemático y a la tarjeta de circuito impreso (*Printed Circuit Board*, PCB) desarrollados para el sistema de adquisición de datos, supervisión y comunicaciones de la estación de carga vehicular.

El diseño electrónico tiene como finalidad integrar los diferentes dispositivos encargados de adquirir variables eléctricas y térmicas, establecer comunicación con los equipos del sistema y proporcionar las conexiones necesarias para el procesamiento y supervisión de la información.

La tarjeta PCB fue diseñada utilizando **Altium Designer**, herramienta empleada para elaborar el esquemático electrónico, asignar las huellas de los componentes, definir su distribución física y establecer las conexiones eléctricas sobre la tarjeta.

La documentación disponible permite consultar tanto la representación funcional de los circuitos como los archivos editables utilizados durante el desarrollo del diseño.

---

## 2. Archivos disponibles

| Archivo | Descripción |
|---|---|
| [Esquemático electrónico (PDF)](./Esquematico_Trabajo_de_Grado_Estacion_de_Carga_Vehicular.pdf) | Representación gráfica del circuito electrónico, sus componentes y conexiones eléctricas. |
| [Esquemático editable (.SchDoc)](./Esquematico_Tesis.SchDoc) | Archivo fuente del diseño esquemático desarrollado en Altium Designer. |
| [Diseño de PCB (.PcbDoc)](./PCBintento%2022222conintegrado.PcbDoc) | Archivo editable que contiene la distribución de componentes, las huellas y el trazado de conexiones de la tarjeta. |

Los archivos `.SchDoc` y `.PcbDoc` pueden abrirse y modificarse mediante Altium Designer o herramientas compatibles con estos formatos.

El archivo PDF permite visualizar el circuito electrónico sin necesidad de disponer del software de diseño.

---

## 3. Arquitectura del sistema electrónico

El diseño de la tarjeta PCB integra los circuitos de acondicionamiento, adquisición y comunicación necesarios para la supervisión de las variables de operación de la estación.

### 3.1. Unidad central de control

El procesamiento y la supervisión de información se realizan mediante una **Raspberry Pi Zero 2 W**, que actúa como unidad central del sistema electrónico.

La tarjeta incorpora las conexiones necesarias para utilizar diferentes interfaces de la Raspberry Pi, entre ellas:

- Bus I²C para la comunicación con dispositivos de adquisición y expansión de interfaces.
- Comunicación UART para la integración de dispositivos seriales.
- Entradas y salidas digitales GPIO para funciones de control.
- Conexiones de alimentación y referencia de tierra.

### 3.2. Adquisición y acondicionamiento de variables eléctricas

El sistema de adquisición permite supervisar variables eléctricas del arreglo fotovoltaico y del banco de baterías.

Los principales componentes utilizados son:

| Componente | Función dentro del sistema |
|---|---|
| ADS1015 | Conversión analógico-digital de las señales de medición. |
| ACS758 | Medición de corriente del arreglo fotovoltaico mediante efecto Hall. |
| Shunt FL-2 | Medición de corriente del banco de baterías mediante caída de tensión. |
| Divisores resistivos | Acondicionamiento de las señales de voltaje para su adquisición. |

Se emplean dos módulos ADS1015 para la adquisición de variables asociadas al arreglo fotovoltaico y al banco de baterías.

### 3.3. Medición de temperatura

La supervisión térmica se realiza mediante sensores digitales **DS18B20**, destinados al monitoreo de temperatura en puntos definidos del sistema.

Estos dispositivos utilizan el protocolo de comunicación 1-Wire y permiten integrar la información térmica al sistema central de supervisión.

### 3.4. Interfaces de comunicación

La tarjeta incorpora conexiones para dispositivos de comunicación serial, necesarias para intercambiar información con los equipos de la estación de carga.

| Componente | Función dentro del sistema |
|---|---|
| SC16IS750 | Expansión de interfaces UART a través del bus I²C. |
| MAX3232 | Adaptación de niveles eléctricos entre señales UART TTL y comunicación RS-232. |
| Interfaz RS-485 | Comunicación diferencial con dispositivos externos compatibles. |

Estas interfaces permiten integrar dispositivos de control, regulación y medición que utilizan diferentes protocolos de comunicación.

### 3.5. Alimentación e interconexión

El diseño contempla conexiones de alimentación y distribución de señales para los circuitos electrónicos.

Entre sus principales elementos se encuentran:

- Conexiones de alimentación de 3,3 V y 5 V.
- Referencias de tierra (GND).
- Conectores para dispositivos de medición y comunicaciones.
- Resistencias y capacitores asociados al acondicionamiento de señales.
- Conexiones digitales destinadas a funciones de control.

---

## 4. Diseño de la tarjeta PCB

El diseño físico de la tarjeta de circuito impreso se desarrolló a partir del esquemático electrónico elaborado en Altium Designer.

El proceso de diseño comprende las siguientes etapas:

### 4.1. Elaboración del esquemático

Representación de los componentes electrónicos y definición de las conexiones eléctricas necesarias para integrar los diferentes subsistemas.

### 4.2. Asignación de componentes y huellas

Asociación de los componentes del esquemático con sus respectivas huellas físicas (*footprints*), considerando las dimensiones y características de montaje.

### 4.3. Distribución de componentes

Ubicación de los componentes electrónicos sobre la tarjeta, considerando la organización funcional de los circuitos de adquisición, comunicaciones y alimentación.

### 4.4. Enrutamiento de conexiones

Definición de las pistas conductoras que interconectan los componentes electrónicos.

El diseño contempla diferentes tipos de conexiones:

- Señales digitales de comunicación I²C, UART y GPIO.
- Señales analógicas provenientes de los sensores.
- Líneas de alimentación eléctrica.
- Referencias y planos de tierra.

### 4.5. Verificación del diseño

La revisión del diseño debe contemplar:

- Correspondencia entre el esquemático y la PCB.
- Verificación de las conexiones eléctricas.
- Comprobación de las huellas y dimensiones de los componentes.
- Revisión de anchos de pista y separaciones eléctricas.
- Ejecución de las verificaciones de reglas de diseño (*Design Rule Check*, DRC).

Estas verificaciones permiten identificar posibles inconsistencias antes de la fabricación de la tarjeta.

---

## 5. Relación con los componentes del sistema

Los componentes representados en el esquemático y utilizados en el diseño de la tarjeta se seleccionaron considerando sus características eléctricas, requerimientos de alimentación e interfaces de comunicación.

Las hojas de datos, fichas técnicas y manuales correspondientes se encuentran disponibles en el directorio:

[Consultar documentación técnica de componentes](../Datasheets/)

Esta documentación constituye la referencia para la selección de dispositivos, identificación de terminales, revisión de niveles eléctricos y definición de condiciones de operación.

---

## 6. Consideraciones técnicas

- Los archivos de diseño corresponden a la documentación electrónica de la estación de carga vehicular.
- El esquemático representa las conexiones funcionales de los circuitos de adquisición, supervisión y comunicaciones.
- El archivo `.PcbDoc` contiene la implementación física del circuito sobre la tarjeta de circuito impreso.
- Los niveles de voltaje, corrientes admisibles y conexiones deben verificarse según las especificaciones de cada componente.
- Antes de fabricar la tarjeta deben comprobarse las reglas de diseño eléctrico y las características físicas de los componentes.
- Los archivos editables permiten realizar modificaciones y mantener la trazabilidad del diseño electrónico.
- Cualquier modificación posterior debe reflejarse tanto en el esquemático como en el diseño de la PCB.

---

**Trabajo de grado para optar por el título de Ingeniero Mecatrónico**

**Diseño y validación a escala de una estación de carga vehicular con energía solar, almacenamiento en baterías y respaldo de red**

**Pontificia Universidad Javeriana**

**Facultad de Ingeniería — Ingeniería Mecatrónica**

