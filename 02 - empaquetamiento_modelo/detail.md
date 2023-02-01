# Organización del proyecto

------------

    ├── Makefile            <- Makefile con comandos como `hacer datos` o `traer datos`
    ├── README.md           <- El README de nivel superior para los desarrolladores que utilizan este proyecto.
    ├── prepare_data        <- Estructuración de los datos, creación y ajuste de consultas. Unificación de datos.
    │
    ├── vectorize_data      <- Reestructuración de los datos en formato valido para modelos, proceso de ing de caracteristicas.
    |
    ├── train               <- Experimentación y entremaniento de modelos, selección del mejor modelo.
    │
    ├── requirements.txt    <- El archivo de requerimientos para reproducir el ambiente.
    │                         genrado con `pip freeze > requirements.txt`
    │
    ├── setup.py            <- makes project pip installable (pip install -e .) so src can be imported
    ├── regression_model   <- Carpeta con procesos de ingenieria de datos, modelamiento y predicción. 
    |   |
    |   ├── 
    ├── src                 <- Source code for use in this project.
    |   |
    │   ├── __init__.py      <- Makes src a Python module
    │   │
    │   ├── data          
    │   │   ├── prepare.py   <- Script con el proceso de vectorización de datos (Creación de caracteristicas).
    │   │   └── queries.py   <- Script con con todas las consultas consolidadas en formato string.
    │   │
    │   ├── features       
    │   │   └── vectorize.py <- Script con el proceso de creación de caracteristicas y consolidación entrada del modelo.
    │   │
    │   ├── models           <- Consolidación de datos los archivos .py con las predicciones del o de los modelos.
    │   │   └── predict_model.py  <- Script con proceso para crear predicciones desde el mejor modelo.
    |
    ├── pipeline.py        <- Archivo con que consolida la ejecución del modelo. Ejecutando el proceso de modelación de principio
    |                         proceso de modelación de principio a fin.
    |                        
    └── tox.ini            <- Archivo tox con configuraciones para ejecutar tox.


--------
