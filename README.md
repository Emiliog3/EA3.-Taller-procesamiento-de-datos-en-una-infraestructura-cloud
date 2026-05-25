# EA3 - Taller: procesamiento de datos en una infraestructura cloud

Este repositorio contiene la entrega de la Unidad 3, Evidencia de Aprendizaje EA3, correspondiente al taller de procesamiento de datos en una infraestructura cloud mediante Databricks Community Edition, Apache Spark, Spark SQL y tabla Delta.

Aunque la plataforma conserva la nomenclatura `Actividad_2` para el archivo del notebook, el desarrollo corresponde conceptualmente a la Actividad 3 / EA3 de Big Data.

## Archivo principal

- `Gomez_Pablo_Actividad_2.ipynb`

Este es el notebook exportado desde Databricks Community Edition y constituye el archivo principal de entrega solicitado para cargar en GitHub y compartir en el LMS.

## Planteamiento del problema

En los procesos de análisis de datos, una dificultad frecuente consiste en pasar de un archivo plano, como un CSV descargado desde una fuente pública, a una estructura de datos organizada, consultable y validada dentro de una infraestructura de procesamiento cloud. Cuando los datos se conservan únicamente como archivos aislados, su análisis queda limitado a revisiones manuales o a procesos poco trazables. Además, se dificulta verificar tipos de datos, campos clave, valores nulos, consultas agregadas y resultados comparables entre diferentes enfoques de procesamiento.

La situación abordada en esta práctica parte de esa necesidad: tomar un conjunto de datos conocido, estructurarlo técnicamente, cargarlo en una plataforma cloud y comprobar que puede ser procesado tanto con PySpark como con Spark SQL. Para ello se trabajó con el dataset Titanic, que contiene información de pasajeros, clase del tiquete, edad, sexo, tarifa, puerto de embarque y variable de supervivencia. Este conjunto de datos permite construir un caso académico claro: organizar información histórica de pasajeros para responder preguntas básicas de análisis, por ejemplo, cuántos registros existen, cómo están distribuidos los pasajeros por clase, qué diferencias aparecen en la supervivencia por sexo y qué comportamiento presenta la tarifa promedio por grupo.

El problema, por tanto, no consiste solamente en cargar un archivo, sino en demostrar cómo una infraestructura cloud permite convertir datos iniciales en una tabla Delta consultable, documentada y validada. Esto resulta importante porque en escenarios reales de Big Data las entidades y empresas requieren almacenar datos de forma confiable, consultarlos con rapidez, reutilizarlos en procesos analíticos y mantener evidencia del flujo realizado, desde la ingesta hasta la validación de resultados.

## Objetivo general

Implementar un flujo básico de procesamiento de datos en Databricks Community Edition, a partir de la ingesta del dataset Titanic, la definición de su esquema, la creación de una tabla Delta y la validación de resultados mediante PySpark y Spark SQL.

## Objetivos específicos

1. Diseñar el esquema de almacenamiento del dataset Titanic, definiendo campos, tipos de datos, llaves, nulabilidad y diccionario de datos.

2. Configurar y evidenciar el entorno de trabajo en Databricks Community Edition, incluyendo información del runtime, versión de Python, versión de Spark, catálogo, esquema y almacenamiento utilizado.

3. Ingerir el conjunto de datos en Databricks, convertirlo en un DataFrame de Spark y persistirlo como tabla Delta dentro del esquema de trabajo definido.

4. Ejecutar validaciones técnicas y analíticas mediante PySpark y Spark SQL, incluyendo metadatos, descripción estadística, conteos, filtros, consultas SELECT y agrupaciones GROUP BY.

5. Comparar el uso de SQL y PySpark a partir de la experiencia práctica, identificando ventajas, limitaciones y escenarios recomendados para cada enfoque.

## Relación entre Databricks, Visual Studio Code y GitHub

El desarrollo de la actividad se apoyó en tres espacios diferentes, cada uno con una función concreta dentro del flujo de trabajo.

Databricks Community Edition fue la plataforma principal de ejecución. Allí se creó el notebook, se consultó la configuración del entorno cloud, se definió el esquema de datos, se cargó el dataset, se creó la tabla Delta y se realizaron las validaciones con PySpark y Spark SQL. En otras palabras, Databricks fue el lugar donde realmente se procesaron los datos.

Visual Studio Code se utilizó como entorno local de organización y apoyo. Desde allí se prepararon carpetas, archivos auxiliares, evidencias, documentación y comandos de trabajo. VS Code no reemplazó a Databricks en esta actividad; funcionó como una herramienta de soporte para ordenar el proyecto, revisar archivos y preparar la entrega.

GitHub se empleó como repositorio final de publicación. Allí se cargó el notebook exportado desde Databricks, de manera que la evidencia quedara disponible mediante una URL pública, verificable y apta para ser registrada en el LMS.

En resumen:

- Databricks CE: ejecución real del procesamiento cloud.
- Visual Studio Code: organización local del proyecto y apoyo documental.
- GitHub: publicación final del notebook para la entrega académica.

## Dataset utilizado

El trabajo se desarrolló con el dataset Titanic, disponible públicamente y ampliamente usado en prácticas de analítica de datos. Para efectos académicos, se trabajó como un conjunto de datos equivalente al consultado desde Kaggle, con campos suficientes para diseñar un esquema, crear una tabla, ejecutar consultas y comparar resultados entre SQL y Spark.

Campos principales del dataset:

- `PassengerId`: identificador único del pasajero.
- `Survived`: variable de supervivencia, donde 0 indica que no sobrevivió y 1 indica que sobrevivió.
- `Pclass`: clase del tiquete.
- `Name`: nombre del pasajero.
- `Sex`: sexo registrado del pasajero.
- `Age`: edad.
- `SibSp`: número de hermanos o cónyuge a bordo.
- `Parch`: número de padres o hijos a bordo.
- `Ticket`: código del tiquete.
- `Fare`: tarifa pagada.
- `Cabin`: cabina asignada.
- `Embarked`: puerto de embarque.


## Resultado esperado

El notebook permite evidenciar que el dataset fue cargado correctamente, que el esquema fue diseñado y aplicado, que la tabla Delta quedó disponible en Databricks y que las consultas ejecutadas en PySpark y SQL producen resultados útiles para validar el procesamiento de datos en una infraestructura cloud.
