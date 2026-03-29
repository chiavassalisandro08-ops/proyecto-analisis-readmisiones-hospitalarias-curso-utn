# Proyecto final – Análisis de readmisiones hospitalarias

## Contexto

El índice de readmisiones hospitalarias posteriores a procedimientos quirúrgicos es uno de los parámetros que más influye en los costos de gestión y uno de los más demandantes en recursos institucionales.

Como referencia, puede señalarse su presencia en sistemas de salud tan diversos como Medicare en Estados Unidos y PAMI en Argentina, donde existen mecanismos de penalización o débitos vinculados a estas readmisiones. En algunos casos, esto puede hacer que no solo no generen ganancias, sino que incluso deriven en pérdidas económicas importantes y en complicaciones logísticas y de gestión superiores a las de los procedimientos primarios. Identificar los procedimientos con mayor injerencia en estos parámetros de readmisión y costos es de vital importancia en la administración económica de un centro de salud.

Su análisis motiva el siguiente proyecto.

Los datasets de salud reales se encuentran restringidos por políticas de privacidad; por lo tanto, se utilizó un dataset ficticio que respeta parámetros estándar para un hospital de considerables dimensiones.

## Fuente directa del dataset

Maven Hospital Challenge

## Objetivo del proyecto

Explorar un conjunto de procedimientos quirúrgicos para identificar cuáles presentan mayor volumen de casos, mayor tasa de readmisión a 30 días y mayor costo promedio, buscando detectar patrones relevantes desde el punto de vista clínico y de gestión.

## Pregunta de análisis

¿Existen procedimientos quirúrgicos con un peso particular en la tasa de readmisión a 30 días? ¿Cuál es la relevancia de cada uno de ellos en términos de gastos de gestión, recursos materiales, logística y costos hospitalarios?

## Datos utilizados

Se trabajó con una tabla final resumida de procedimientos quirúrgicos que incluye las siguientes variables:

- `DESCRIPTION`
- `total_casos`
- `readmisiones_30d`
- `tasa_readmision_30d`
- `costo_promedio`

El archivo de datos finales se encuentra en la carpeta `data/`.

## Herramientas utilizadas

- Python
- pandas
- matplotlib
- Google Colab
- Power BI
- GitHub

## Estructura del repositorio

- `notebooks/` → notebook principal del análisis
- `data/` → datos finales utilizados
- `dashboard/` → visualizaciones y material del dashboard en Power BI

## Hallazgo principal

Se encontró que, dentro del grupo de procedimientos quirúrgicos con mayor tasa de readmisiones, el conjunto de procedimientos gastroenterológicos (**Colonoscopy** y **Rectal polypectomy**) no aparece como un hallazgo aislado, sino como un núcleo con peso propio dentro del análisis.

Su importancia radica en que una readmisión a 30 días no tendría en este grupo el mismo carácter esperable que en otros procedimientos con dinámica clínica diferente, ya que se trata de procedimientos que habitualmente no presentan readmisiones significativas dentro de ese plazo. Sumado a esto, en muchos casos se trata de procedimientos de control protocolizado dentro de la mayor parte de los programas de salud, lo que les confiere un carácter significativo tanto en volumen como en su rol dentro de la mecánica hospitalaria.

Un hallazgo de estas características tiene un efecto relevante, haciendo necesaria la auditoría de todos los procesos comprometidos en su realización.

## Cómo revisar el proyecto

1. Abrir la carpeta `notebooks/` para ver el desarrollo del análisis en Python.
2. Revisar la carpeta `data/` para consultar la tabla final utilizada.
3. Revisar la carpeta `dashboard/` para ver el resumen visual construido en Power BI.

## Acceso al notebook en Google Colab
https://colab.research.google.com/drive/1TPS3wn0nr3QDDYLpEswQAm65DG_SBGFF?usp=sharing

## Autor

Lisandro Chiavassa
Proyecto académico realizado en el marco del curso Herramientas básicas para el Análisis de Datos (UTN)
