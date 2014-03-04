pyql-weather
=================
### Yahoo Weather para Python


Instalación:
------------------------------------------------------------

(1) Descarga el paquete y ejecutar:

```bash
python setup.py install
```

(2) A disfrutar de las consultas del clima en Yahoo!!!!


### Ejemplo de uso: (1)

```python
from pyql.weather.models import Weather

# Pasamos el WOEID:
w = Weather(24553062)
# Leemos el resultado:
print "Temperatura: %sc. Estatus: (%s) %s"%(w.get_temperature(), w.get_status_code(), w.get_status_text())

```

### Ejemplo de uso: (2)

```python
from pyql.weather.models import Weather, GeoData

# Conseguimos una lat y long
latitude = "20.982994"
longitude = "-89.617710"


# Obtenemos datos de una latitud y longitud dada:
geo = GeoData(latitude, longitude) # Inicializamos el objeto
# Pasamos en WOEID:
w = Weather(geo.get_woeid())
# Leemos el resultado:
print "Temperatura: %sc. Estatus: %s"%(w.get_temperature(), w.get_status_text())

```

Yahoo utiliza como valor importante el WOEID ( Where On Earth Identifiers).
Si no contamos con esta información, pero sí tenemos nuestra latitud y longitud, entonces la pasamos
para obtener el WOEID que desconocemos y posteriormente ya podremos consultar el clima.



Autor:
-------------------------------------------------------------
Alex Dzul.
Python / Django Sr. Developer.

Página web: [alexdzul.com] (http://alexdzul.com)
Canal de Youtube: [youtube.com/alexexc2] (http://youtube.com/alexexc2)
Twitter: [@lexjs88] (http://twitter.com/alexjs88)


### Nota:

La versión de este paquete aún se encuentra en alfa por lo que
se recomienda no utilizar en entornos de producción hasta la liberación
de una versión estable.