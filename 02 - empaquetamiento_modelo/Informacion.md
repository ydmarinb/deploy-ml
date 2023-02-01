# Empaquetamiento del modelo

El proposito de construir codigo es producción para entegar lso resultados a los usarios finales.
Las consideraciones para poder llevar un codigo a producción es que debe ser:

* Testeable
* Mantenible
* Escalable
* Optimo
* Reproducible

# TOX

Tene como objetivo automatizar y estandarizar las pruebas en Python. Es parte de una visión más amplia de facilitar el proceso de empaquetado, prueba y lanzamiento del software Python.

`tox` es una herramienta de línea de comando de prueba y administración de entornos virtuales genérica que puede usar para: verificar que su paquete se compila e instala correctamente en diferentes entornos (como diferentes implementaciones de Python, versiones o dependencias de instalación), ejecutando sus pruebas en cada uno de los entornos con la herramienta de prueba de su elección, actuando como una interfaz para servidores de integración continua, reduciendo en gran medida el modelo estándar y fusionando CI y pruebas basadas en shell. (Para conocer mas sobre tox visite su pagina <https://tox.wiki/en/latest/>)

Para empezar usar el comando solo se debe usar `pip install tox`.
[EOF]