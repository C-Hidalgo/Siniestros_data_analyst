<p align="center"><img src="./imagenes/ed-vial_732_1296.jpg"></p>

# Proyecto Individual N°2

## Siniestros Viales (Data Analytics)

### CARLOS HIDALGO, DATAPT05

---

## **Tabla de Contenidos**

- [Introducción](#introducción)
- [Desarrollo](#desarrollo)
    - [ETL](#etl-para-análisis-de-homicidios)
    - [EDA](#análisis-exploratorio-de-datos-eda---homicidios)
    - [Estudio](#estudio)
- [Conclusión](#conclusión)
- [Bibliografias](#bibliografias)
- [Contacto](#contacto)

## **Tecnolgías usadas**

![](https://img.shields.io/static/v1?label=Python&message=3.11.6&color=brightgreen)
![](https://img.shields.io/static/v1?label=Pandas&message=2.0.3&color=brightgreen)
![](https://img.shields.io/static/v1?label=Matplotlib&message=3.7.2&color=brightgreen)
![](https://img.shields.io/static/v1?label=Seaborn&message=0.12.2&color=brightgreen)
![](https://img.shields.io/static/v1?label=Power+BI&message=Desktop&color=brightgreen)
![](https://img.shields.io/static/v1?label=MySQL+Workbench&message=8.0&color=brightgreen)
![](https://img.shields.io/static/v1?label=Excel&message=2010&color=brightgreen)

## **Introducción**

**Proyecto de Análisis de Siniestros Viales en Buenos Aires**

Bienvenido al repositorio del proyecto de análisis de datos sobre siniestros viales en la Ciudad de Buenos Aires. Este estudio se llevó a cabo en colaboración con el Observatorio de Movilidad y Seguridad Vial (OMSV), bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires.

**Contexto del Problema:**

Los siniestros viales, o accidentes de tráfico, representan una seria preocupación en áreas urbanas densamente pobladas, y Buenos Aires no es una excepción. Con el objetivo de abordar este desafío y contribuir a la mejora de la seguridad vial, se emprendió un análisis exhaustivo de datos recopilados entre los años 2016 y 2021.

**Objetivo del Proyecto:**

El propósito principal de este proyecto es proporcionar información valiosa que permita a las autoridades locales tomar decisiones informadas para reducir la cantidad de víctimas fatales en siniestros viales. A través de técnicas de análisis de datos y visualización, buscamos identificar patrones, tendencias y factores clave que contribuyen a estos incidentes.

**Estructura del Repositorio:**

1. **Notebooks de Análisis Exploratorio de Datos (EDA):**
   - Documentación detallada de la exploración inicial de los conjuntos de datos.
   - Identificación de valores faltantes, outliers y duplicados.
   - Visualización de patrones y tendencias.

2. **Dashboard Interactivo:**
   - Desarrollo de un tablero interactivo para explorar datos de manera dinámica.
   - Filtros que permiten un análisis detallado.
   - Presentación efectiva de información clave.

3. **Análisis Profundo y Conclusiones:**
   - Interpretación de hallazgos a través de análisis detallado.
   - Conclusiones derivadas de patrones identificados.

4. **KPIs para la Prevención:**
   - Definición, medición y visualización de KPIs clave.
   - Propuestas para la reducción de la tasa de homicidios y accidentes mortales de motociclistas.

Te invito a explorar cada sección, contribuir y aprender de este análisis destinado a impactar positivamente la seguridad vial en Buenos Aires. ¡Gracias por ser parte de este proyecto! 🚗📊


## **Desarrollo**

### **ETL para Análisis de Homicidios**

Este proyecto de ETL se enfoca en la preparación de datos para el análisis de homicidios, abordando inconsistencias y asegurando la calidad de la información. A continuación, se resumen los pasos clave realizados:

Extracción de Datos:

Se cargaron conjuntos de datos 'homicidios.xlsx' y 'lesiones.xlsx' utilizando la biblioteca Pandas de Python.
Exploración del Conjunto de Datos 'hechos':

Se realizó una exploración inicial para comprender la estructura y el contenido del conjunto de datos 'hechos'.
Identificación de Valores Nulos:

Se identificaron valores nulos en las columnas 'Calle', 'Altura', 'Cruce' y 'Dirección Normalizada' del conjunto 'hechos'.
Evaluación y Tratamiento de Columnas:

Se evaluaron y trataron problemas en las columnas 'Calle', 'Altura' y 'Cruce' mediante la identificación de filas con información faltante o incorrecta.
Identificación y Tratamiento de Outliers:

Se identificaron y corrigieron outliers en la columna 'VICTIMA', asegurando la coherencia con el diccionario de hechos.
Corrección de Errores y Limpieza:

Se corrigieron errores en la descripción de víctimas para algunos hechos.
Se eliminaron filas con información insuficiente o incorrecta.
Guardado de Conjuntos de Datos Limpios:

Los conjuntos de datos 'hechos' y 'víctimas' limpios se guardaron en archivos Excel para facilitar su posterior uso en análisis.
Estos pasos garantizaron la integridad y consistencia de los datos, proporcionando un conjunto de datos más fiable y preparado para análisis más avanzados.

## **Análisis Exploratorio de Datos (EDA) - Homicidios**
### **Exploración del Conjunto de Datos 'hechos'**

**Resumen del Conjunto de Datos 'hechos':**
El conjunto de datos 'hechos' consiste en 694 registros de incidentes de homicidios con 21 atributos. Estos atributos incluyen información sobre la fecha, lugar del hecho, participantes, víctima, y acusado.

**Visualización de Hechos por Comuna:**
Se ha realizado un análisis visual utilizando un gráfico de barras para representar la cantidad de hechos por comuna. Se destaca la comuna nº1 como la de mayor incidencia, mientras que las comunas 2, 5 y 6 presentan menos casos.
<p align="center"><img src="./imagenes/output.png"></p>

**Visualización de Hechos según el Tipo de Calle:**
Un gráfico de torta muestra la distribución de hechos según el tipo de calle. Las calles son la categoría principal, seguidas por avenidas y autopistas.
<p align="center"><img src="./imagenes/output_2.png"></p>

**Tendencia Mensual de Accidentes a lo Largo de los Años:**
Se ha explorado la tendencia mensual de los accidentes a lo largo de los años mediante un gráfico de línea. Proporciona una visión de la variación de incidentes a lo largo del tiempo.
<p align="center"><img src="./imagenes/output_3.png"></p>

**Cantidad de Hechos según el Tipo de Víctima:**
Un gráfico de barras indica que las categorías más afectadas son 'MOTO' y 'PEATON', concentrando la mayoría de los incidentes.
<p align="center"><img src="./imagenes/output_4.png"></p>

### **Exploración del Conjunto de Datos 'victimas'**

**Manejo de Datos Faltantes:**
Se ha verificado y gestionado la presencia de datos faltantes en el conjunto de datos 'victimas'. No se identificaron datos faltantes en ninguna columna.

**Distribución de las Víctimas por Edades:**
Se ha creado un histograma para visualizar la distribución de las edades de las víctimas. Proporciona una comprensión rápida de la variabilidad en las edades de las víctimas.
<p align="center"><img src="./imagenes/output_5.png"></p>

**Evaluación de Roles de las Víctimas:**
Un gráfico de torta con agujero ha sido utilizado para evaluar la distribución de roles de las víctimas. Los roles más frecuentes son 'CONDUCTOR' y 'PEATON'.
<p align="center"><img src="./imagenes/output_6.png"></p>

En conjunto, este análisis exploratorio de datos proporciona una visión integral de los homicidios, destacando patrones, tendencias y características clave de los incidentes y sus víctimas.

### **Estudio**

El hilo de estudio se centra en abordar la problemática de los siniestros viales en la Ciudad de Buenos Aires, Argentina. Los siniestros viales, también conocidos como accidentes de tráfico, son eventos que involucran vehículos en las vías públicas y pueden resultar en daños materiales, lesiones o incluso la pérdida de vidas. Este problema es particularmente relevante en Buenos Aires debido al alto volumen de tráfico y la densidad poblacional en la ciudad.

El Observatorio de Movilidad y Seguridad Vial (OMSV), perteneciente a la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires, ha solicitado un proyecto de análisis de datos para proporcionar información que permita a las autoridades locales tomar medidas efectivas para reducir la cantidad de víctimas fatales en siniestros viales.

El análisis se realiza sobre un conjunto de datos que abarca el periodo 2016-2021, con información detallada sobre homicidios en siniestros viales. El objetivo principal es identificar patrones, tendencias y factores contribuyentes a estos incidentes. Se espera que el análisis conduzca a la formulación de KPIs (Indicadores Clave de Desempeño) que orienten las acciones preventivas.

**KPIs**
- Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior 

- Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior .




## Bibliografias
- [Buenos Aires Data](https://data.buenosaires.gob.ar/dataset/victimas-siniestros-viales)
- [Buenos Aires Data](https://data.buenosaires.gob.ar/dataset/victimas-siniestros-viales)
- [DGESYC](https://www.estadisticaciudad.gob.ar/eyc/?p=28146)


## Contacto

<div style="display: flex; align-items: center;">
  <a href="https://www.linkedin.com/in/carlos-hidalgo84/" style="margin-right: 10px;">
    <img src="./imagenes/linkedin.png" alt="LinkedIn" width="40" height="40">
  </a>
  <a href="mailto:hidalgo.carlos1984@gmail.com" style="margin-right: 10px;">
    <img src="./imagenes/gmail.png" alt="Gmail" width="40" height="40">
  </a>
</div>