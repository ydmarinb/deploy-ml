# Organización del proyecto

------------
    ├── regression_model       <- Carpeta con procesos de ingenieria de datos, modelamiento y predicción. 
    |  ├── config            
    │  |  ├── __init__.py      <- Archivo que primero se lee al importar el folder config
    |  |  └── core.py          <- Se definen las rutas de los directorios, configuraciones del modelo como 
    |  |                          tipos de   variables , ademas se crean funciones de validaciones para
    |  |                          la existencia de yml con las configuraciones y su previa lectura.
    |  |                     
    |  ├── datasets            <- Carpeta donde se almacean las bases de datos despues de realizar ing de 
    |  |   |                      caracteristicas  y quedan listas para entrenar el modelo. 
    |  |   └── __init__.py     <-  Archivo que primero de lee al importar el folder datasets.
    |  |
    |  ├── processing   
    |  |  ├── __init__.py      <- Archivo que primero de lee al importar el folder config.
    |  |  ├── data_manager.py  <- Archivo con procesos de carga de datos y procesos de guardado, carga
    |  |  |                       y eliminación de pipelines.
    |  |  ├── features.py      <- Se agregan procesos de transformación e ing de caracteristicas de impli-
    |  |  |                       mentación propia.
    |  |  └── validation.py    <- Se agregan procesos de validación de variables, tipo de datos, eliminación
    |  |                          de variables nulas no identificadas en el proceso de analisis.
    |  |
    |  ├── trained_models      <- Carpeta donde se almacenan los binarios de los modelos construines.
    |  |   └── __init__.py     <- Archivo que primero de lee al importar el folder config
    |  |
    |  ├── VERSION             <- Archivo con la versión del proceso(ejemplo 0.0.1)
    |  |
    |  ├── config.yml          <- Se agregan todas aquellas constantes o parametros de nombres que se usaran
    |  |                          a lo largo del proceso, nombre de las variables, nombre variables categoricas, 
    |  |                          nombres variables numericas, ..., nombres variables a alguna transformación. 
    |  ├── pipeline.py         <- Pipeline de que integra todo lo que es limpieza, transformación y predicción.
    |  ├── predict.py          <- Funciones para predecir con los modelos guardados en binario.
    |  └── train_pipeline.py   <- Funciones para entrenar el pipeline con los datos en entrenamiento.
    |
    ├── requirements           <- Carpeta con archivos requeriments.txt para las fases del proceso.
    |  ├── requirements.txt    <- Archivos con las versiones de los paquetes necesarios.
    |  ├── test_requirements.txt <- Archivos con paquetes en requirements.txt mas  pytest.
    |  └── typing_requirements.txt <- Archivo con librerias involucradas en el proceso de buenas
    |                                 practicas ce codificación.
    |
    ├── tests                   <- Carpeta con scripts de testing.
    |   ├── conftest.py         <- Carga y creación de variables de testeo usadas en pytest.
    |   ├── test_features.py    <- Validación de los valores en las variables y sus transformaciones.
    |   └── test_prediction.py  <- Validación de los direferentes caracteristicas de la predicción tipo
    |                              de dato, transformación, tamaño,.....
    |
    ├── MANIFEST.in             <- Similar a .gitignore.  Se especifican las carpetas, archivos a incluir en el 
    |                              paquete.
    |
    ├── mypy.ini                <- Definir configuración para el archivo mypy.
    |
    ├── pyproject.toml          <- Este archivo contiene información y requisitos del sistema de compilación, 
    |                              que pip utiliza para compilar el paquete.
    |
    ├── pyproject.toml          <- Archivos de metados y configuración el paquete.
    |
    | tox.ini                    <- Es una herramienta de línea de comando de prueba y administración de  
    └──                             entornos virtuales genérica.  

--------;
