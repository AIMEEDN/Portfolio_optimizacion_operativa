# Portfolio_optimizacion_operativa

## Análisis de eficiencia operativa en la empresa telefónica CallMeMaybe

## Introducción
La empresa CallMeMaybe busca mejorar la calidad de su servicio de telefonía virtual al identificar operadores ineficaces dentro de sus equipos. Un operador ineficaz se caracteriza por altos niveles de ineficiencia, como grandes cantidades de llamadas perdidas (entrantes e internas), tiempos de espera prolongados y, en el caso de operadores asignados a realizar llamadas salientes, bajos volúmenes de dichas llamadas. Este análisis tiene como objetivo proporcionar información clave que permita a los supervisores optimizar el desempeño de los operadores, mejorando la experiencia de los clientes finales.

A través de un análisis exhaustivo de los datos históricos proporcionados por CallMeMaybe, se identificarán patrones y métricas clave para evaluar la eficacia de los operadores. Esto permitirá realizar un diagnóstico preciso de las áreas dmee jo mejora y respaldar decisiones estratégicas basadas en evidencias.

## Objetivos específicos
1.Realizar un análisis exploratorio de datos (EDA) para comprender las características principales de las llamadas y operadores dentro de la red CallMeMaybe.

2.Identificar operadores ineficaces basándose en métricas clave como cantidad de llamadas perdidas, tiempos de espera prolongados y número insuficiente de llamadas salientes (cuando aplique).

3.Validar hipótesis estadísticas sobre factores relacionados con la eficacia de los operadores, como la relación entre tiempos de espera y llamadas perdidas, o la influencia de las características del cliente en la distribución de las llamadas.

## Etapas de análisis del proyecto
1.Preparación de Datos

Importar librerías necesarias para ejecutar el proyecto y los datasets requeridos (telecom_dataset_us.csv y telecom_clients_us.csv).

El conjunto de datos ('telecom_dataset_us.csv') contiene las siguientes columnas:

'user_id': ID de la cuenta de cliente
'date': fecha en la que se recuperaron las estadísticas
'direction': "dirección" de llamada (out para saliente, in para entrante)
'internal': si la llamada fue interna (entre los operadores de un cliente o clienta)
'operator_id': identificador del operador
'is_missed_call': si fue una llamada perdida
'calls_count': número de llamadas
'call_duration': duración de la llamada (sin incluir el tiempo de espera)
'total_call_duration': duración de la llamada (incluido el tiempo de espera)
El conjunto de datos ('telecom_clients_us.csv') tiene las siguientes columnas:

'user_id': ID de usuario/a
'tariff_plan': tarifa actual de la clientela
'date_start': fecha de registro de la clientla
2.Análisis Exploratorio de Datos (EDA)

Identificar valores nulos, duplicados y realizar la limpieza de datos. Estandarizar formatos de columnas (fechas, categorías, IDs). Describir las principales métricas de los operadores: número total de llamadas, promedio de duración, tiempo de espera, porcentaje de llamadas perdidas. Identificar patrones generales, como la distribución de llamadas por operador.

3.Definición de Ineficacia

Definir umbrales claros para determinar la ineficacia de un operador: Porcentaje de llamadas perdidas alto (>X%). Tiempo promedio de espera elevado (>X segundos). Volumen bajo de llamadas salientes para operadores asignados a esta tarea. Agrupar operadores con base en su desempeño.

4.Prueba de Hipótesis Estadísticas

Evaluar si los tiempos de espera influyen en el porcentaje de llamadas perdidas. Analizar si las características del cliente (plan tarifario, antigüedad) afectan el desempeño de los operadores.

5.Conclusiones y recomendaciones del Proyecto Final

Conclusiones del Proyecto y estrategias para mejorar el desempeño general de los operadores.

6.Fuentes Consultadas

Documentación, artículos, reportes que sustenten el proyecto.

7.Visualización y Reporte

Generar gráficos y tablas para ilustrar las métricas clave y los resultados del análisis, hacer un dashboard. Crear una presentación en PDF del Proyecto Final.

## Conclusiones y recomendaciones
Conclusión del Proyecto

El análisis realizado permitió identificar factores clave que afectan el desempeño de los operadores, tomando en cuenta métricas específicas, características de los clientes y diferencias significativas en el comportamiento operativo. Las principales conclusiones son:

Distribución de llamadas y desempeño general de los operadores

El 86% de las llamadas realizadas por los operadores fueron salientes, mientras que el 13% fueron entrantes y solo el 0.8% internas. Se establecieron umbrales para clasificar a los operadores como eficientes o ineficientes. Los operadores ineficientes representan casi el doble de los eficientes, lo que señala un posible problema generalizado de productividad o desempeño en el equipo.

Correlación entre tiempos de espera y porcentaje de llamadas perdidas

Existe una correlación significativa, aunque débil, entre estas variables. Esto indica que los tiempos de espera y el porcentaje de llamadas perdidas están relacionados, pero no de manera fuerte o determinante.

Impacto de las características del cliente en el desempeño de los operadores

Plan tarifario: Se encontraron diferencias significativas en las varianzas y medias entre los diferentes planes tarifarios (A, B y C). Esto sugiere que el tipo de plan tarifario del cliente influye en el comportamiento y desempeño de los operadores. Antigüedad del cliente: La antigüedad del cliente afecta significativamente el desempeño de los operadores. Las diferencias en varianzas y promedios sugieren que los clientes más antiguos pueden tener necesidades específicas o estar sujetos a sesgos operativos.

Sugerencias y Recomendaciones

Optimización del desempeño de los operadores

Implementar capacitaciones específicas para los operadores clasificados como ineficientes, enfocándose en la reducción de tiempos de espera y mejora en la atención a clientes. Introducir incentivos para los operadores eficientes y programas de monitoreo continuo que identifiquen áreas de mejora en tiempo real.

Reducción de tiempos de espera y llamadas perdidas

Revisar los flujos operativos y ajustar la distribución de carga laboral entre operadores para reducir el tiempo de espera en picos de alta demanda. Incorporar herramientas tecnológicas, como sistemas de respuesta automática, para atender llamadas entrantes rápidamente cuando no haya disponibilidad inmediata de operadores.

Plan tarifario y personalización del servicio

Analizar en mayor detalle las diferencias entre los planes tarifarios y ajustar las estrategias operativas según las características de cada grupo de clientes.Ofrecer capacitaciones específicas para que los operadores comprendan mejor las necesidades de los clientes según su plan tarifario.

Antigüedad del cliente

Realizar un análisis adicional sobre el impacto de la antigüedad de los clientes en las interacciones con los operadores. Esto podría incluir entrevistas o encuestas con clientes antiguos para identificar áreas de mejora en el servicio. Personalizar el trato hacia los clientes más antiguos, asegurándose de atender sus necesidades específicas y reducir cualquier posible sesgo.

Automatización y redistribución del trabajo

Implementar tecnologías de automatización en procesos operativos recurrentes para reducir la carga de trabajo manual en los operadores. Redistribuir las llamadas entrantes y salientes de manera más equitativa para garantizar una experiencia homogénea para los clientes de diferentes planes tarifarios.

Con estas acciones, se espera no solo mejorar el desempeño de los operadores, sino también optimizar la experiencia del cliente y aumentar la eficiencia operativa general.