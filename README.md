El despliegue de modelos presenta retos del sofware tradicional:
* *Fiabilidad:* Robusto a errores
* *Reusabilidad:* Reusar en diferentes partes de un sistema
* *Mantenibilidad:* Facil de mantener en el tiempo
* *Flexibilidad:* Agregar o remover funcionalidad del sofware

Ademas posee retos especificos del machine learning:
* *Reproducibilidad:* Procudir el mismo resultado dado los mismos datos.

*La reporducibilidad importa ya que permite reducir costos financieros, *

Lo anterior representa un reto porque demanda la coordinación de un gran numero de personas y procesos (Ing de datos, cientificos de datos, ing de calidad de datos). Ademas las versiones de los sofwares tambien peuden ser un problema.

Todos los retos anteriores deben ser solventados a lo largo del pipeline del machine learning:

> Extracción de de base de datos -> ingenieria de caracteristicas -> Selección de caracteristicas -> Creación del modelo -> Predicción

## Ambiente de investigación 

Es un lugar aprovicionado con herramientas, programas y sofwares necsarios para el desarrollo de analisis y modelamiento.

## Ambiente de producción y experimentación
Es el lugar donde se permite tener programas corriendo y configuraciones de hardware donde se operan las operaciones diarias de la empresa, ademas normalmente se tiene el modelo disponible para uso interno. Permite mostrar demos.


## Reproducibilidad
Cuando hablamos de reporducibilidad nos referimos a que cada uno de los pasos involucrados en el pipeline de machine learning deben poder se reproducidos y entregar los mismos resultados.

### Reproducibilidad en los conjuntos de datos

En este caso se proponen dos soluciones para ofrecer reproducibilidad en los conjuntos de datos:

* Guardar una copia del conjunto de entrenamiento lo que no es apropiado en problemas de Big data.
*  Diseñar una conjuntos de datos con registro de tiempo precisos. Ideal

### Reproducibilidad en el proceso de ing de caracteristicas y selección de caracteristicas

La reproducibilidad en esta fase puede verse afectada por aquellos metodos de imputación o estadísticos que dependen de la aleatoriedad o resulytados de los datos, por lo que para segurar la reproducibilidad en esta etapa es importante:

* Crear algoritmos con los proceso de creación de ing de caracteristicas.
* Garantizar la reporducibilidad en los conjuntos de datos.
* Si algun proceso depende de la aleatoriedad definir una semilla aleatoria.

### Reproducibilidad en la creación de modelos

Es normal que los modelos de machine learning dependan de la aleatoriedad o que no tengan en cuenta el nombre de las caracteristicas pasadas para realizar su entrenamiento o predicción. Por lo que es fundamental, realizar una registro de el orden de las caracteristicas, para modelos aleatorios siempre se debe definir una semilla. Ademas se debe registrar la estructura del modelo(Hiperparametros, composición si un modelo de emsamble).

## Contribuidores en un ML system

* Sofwares engineers
* Data sciences
* Products/Business
* DevOps



# Tipos de arquitectura



|                                                   | Patron 1                | Patron 2        | Patron 3                                     | Patron 4                   |
|---------------------------------------------------|-------------------------|-----------------|----------------------------------------------|----------------------------|
| Predicción                                        | Sobre la marcha         | Sobre la marcha | En la marcha                                 | Batch                     |
| Entrega de resultados de la predicción            | En el proceso de la app | Via API         | En tiempo real, por medio de mesajes en cola | Compartiendo DB, API, file |
| Latencia de la predicción                         | Baja                    | Moderada        | Depende del proceso                          | Horas/ dias                |
| Dificultad de adminitración                       | Intermedio              | Facil           | Muy dificil                                  | Intermedio                 |
| Las actualizaciones requieren un nuevo despliegue | Si                      | Si              | No                                           | Si                         |