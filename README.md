# Diseño electrónico y pruebas de caracterización — Estación de carga solar

Repositorio de documentación complementaria del trabajo de grado **«Diseño y validación a escala de una estación de carga vehicular con energía solar, almacenamiento en baterías y respaldo de red»**, desarrollado en la **Pontificia Universidad Javeriana**.

Este repositorio reúne los archivos de diseño electrónico de la tarjeta de circuito impreso (PCB) y los protocolos de caracterización propuestos para los dispositivos de medición, acondicionamiento de señales y comunicación del sistema. Su propósito es facilitar la consulta de los documentos técnicos y mantener organizados los archivos que respaldan el desarrollo electrónico descrito en la tesis.

## 1. Contenido del repositorio

| Sección | Contenido | Acceso |
|---|---|---|
| **Anexo A. Diseño electrónico** | Esquemático del circuito, representación en PDF, diagrama de conexiones de hardware y archivos editables del diseño esquemático y de la PCB realizados en Altium Designer. | [Consultar diseño electrónico](<Anexo_A_Diseno_Electronico/Diseño_PCB/README.md>) |
| **Anexo C. Pruebas de caracterización** | Trece protocolos de prueba (P01–P13) para sensores, acondicionamiento de señales, adquisición de datos, comunicaciones e integración de subsistemas. | [Consultar protocolos de caracterización](<Anexo_C_Pruebas_de_Caracterizacion/PRUEBAS_DE_CARACTERIZACION/README.md>) |

### Estructura de carpetas

```text
estacion-carga-solar-electronica-main/
├── README.md
├── Anexo_A_Diseno_Electronico/
│   └── Diseño_PCB/
│       ├── README.md
│       ├──Conexiones hardware Final.pdf
│       ├── Esquematico_Tesis.SchDoc
│       ├── Esquematico_Trabajo_de_Grado_Estacion_de_Carga_Vehicular.pdf
│       └── PCBintento 22222conintegrado.PcbDoc
└── Anexo_C_Pruebas_de_Caracterizacion/
    └── PRUEBAS_DE_CARACTERIZACION/
        ├── README.md
        ├── P01_Divisor_Resistivo.md
        ├── P02_ACS758.md
        ├── P03_Shunt_FL2.md
        ├── P04_ADS1015.md
        ├── P05_Divisor_ADS1015.md
        ├── P06_DS18B20.md
        ├── P07_Dos_DS18B20.md
        ├── P08_PZEM016_Modbus.md
        ├── P09_PZEM016_CT.md
        ├── P10_XY017.md
        ├── P11_MAX3232_SC16IS750.md
        ├── P12_Adquisicion_DC.md
        └── P13_Monitoreo_Integrado.md
```

## 2. Diseño electrónico y PCB

El [Anexo A](<Anexo_A_Diseno_Electronico/Diseño_PCB/README.md>) contiene el esquemático y el archivo de diseño de la PCB utilizada para integrar las conexiones del sistema de adquisición de datos, supervisión y comunicaciones de la estación de carga.

Los archivos disponibles permiten revisar las conexiones eléctricas del circuito mediante un documento PDF y consultar o modificar los diseños originales mediante los archivos de Altium Designer:

- [Esquemático electrónico en PDF](<Anexo_A_Diseno_Electronico/Diseño_PCB/Esquematico_Trabajo_de_Grado_Estacion_de_Carga_Vehicular.pdf>).
- [Esquemático editable (`.SchDoc`)](<Anexo_A_Diseno_Electronico/Diseño_PCB/Esquematico_Tesis.SchDoc>).
- [Diseño editable de PCB (`.PcbDoc`)](<Anexo_A_Diseno_Electronico/Diseño_PCB/PCBintento 22222conintegrado.PcbDoc>).

La documentación de esta sección describe la integración de la Raspberry Pi Zero 2 W con dispositivos de adquisición analógica, medición de temperatura e interfaces de comunicación, entre ellos ADS1015, ACS758, shunt FL-2, DS18B20, SC16IS750 y MAX3232.

## 3. Pruebas de caracterización

El [Anexo C](<Anexo_C_Pruebas_de_Caracterizacion/PRUEBAS_DE_CARACTERIZACION/README.md>) contiene **13 protocolos** organizados por función:

| Grupo | Protocolos | Alcance |
|---|---|---|
| Sensores analógicos y conversión A/D | P01–P05 | Divisores resistivos, sensor ACS758, shunt FL-2 y convertidor ADS1015. |
| Medición de temperatura | P06–P07 | Sensores DS18B20 y comunicación 1-Wire. |
| Medición eléctrica AC | P08–P09 | Protocolos para el medidor PZEM-016 y su transformador de corriente (CT). |
| Interfaces de comunicación | P10–P11 | Conversión TTL–RS-485 mediante XY-017 e interfaz MAX3232 con SC16IS750. |
| Integración de subsistemas | P12–P13 | Verificación conjunta de las cadenas de adquisición y monitoreo. |

Cada archivo presenta un procedimiento propuesto, con objetivos, equipos, metodología y criterios de verificación. **Los resultados esperados descritos en estos protocolos no deben interpretarse como mediciones experimentales ya obtenidas.**

## 4. Consulta y uso de los archivos

- Los documentos `.md` se pueden consultar directamente desde GitHub.
- El esquemático en `.pdf` puede visualizarse sin abrir los archivos de diseño electrónico.
- Los archivos `.SchDoc` y `.PcbDoc` se proporcionan como fuentes editables para su consulta en Altium Designer o una herramienta compatible.
- Los procedimientos de caracterización deben contrastarse con la versión del hardware y las especificaciones de los fabricantes antes de utilizarse en ensayos.

Los README de cada sección contienen información más detallada sobre sus archivos y su propósito. Este repositorio se presenta como **material complementario de la tesis** y no como sustituto de la metodología, los resultados o las conclusiones del documento principal.

## 5. Estado de la documentación

Los archivos incluidos corresponden al diseño electrónico documentado y a **protocolos propuestos de caracterización**. La presencia de un protocolo en el repositorio no confirma que la prueba haya sido ejecutada ni que sus criterios de aceptación se hayan cumplido. Asimismo, la presencia de archivos de PCB no acredita por sí sola una fabricación o validación eléctrica satisfactoria.

---

**Pontificia Universidad Javeriana — Facultad de Ingeniería**  
**Trabajo de grado: Diseño y validación a escala de una estación de carga vehicular con energía solar, almacenamiento en baterías y respaldo de red**
