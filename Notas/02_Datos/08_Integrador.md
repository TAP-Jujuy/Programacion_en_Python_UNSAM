[Contenidos](../Contenidos.md) \| [Anterior (7 El módulo collections)](07_Contadores.md) \| [Próximo (9 Cierre de la segunda clase)](09_CierreClase.md)

# 2.8 Integración

En esta sección haremos algunos ejercicios integradores manejando archivos, diccionarios y el comando `zip`, entre otras cosas.

## Ejercicios

Vamos a repasar las herramientas que vimos en esta clase aplicándolas a una base de datos sobre árboles en parques de la Ciudad de Buenos Aires. Para empezar, descargá el [archivo csv](https://data.buenosaires.gob.ar/dataset/arbolado-espacios-verdes) sobre arbolado de espacios verdes de la Ciudad a tu carpeta `Data`. Vamos a estudiar esta base de datos y responder algunas preguntas. Guardá este trabajo en un archivo `arboles.py`.

### Ejercicio 2.28: Lectura de los árboles de un parque
Definí una función `leer_parque(nombre_archivo, parque)` que abra el archivo incidicado y devuelva una **lista de diccionarios** con la información sobre los árboles del parque especificado. La función debe devolver una lista que, por cada árbol (cada fila) del archivo, contenga un diccionario con toda la información sobre el árbol. 

_Sugerencia: basate en la función `leer_camion()` y usá también el comando `zip` como hiciste en el_ [Ejercicio 2.25](../02_Datos/06_Secuencias.md#ejercicio-225-la-función-zip) _para combinar el encabezado del archivo con los datos de cada fila. Por ahora te preocupes por los tipos de datos de cada columna._

_Observación: La columna que indica el nombre del parque se llama `'espacio_ve'`._

Probá con el parque "GENERAL PAZ" para tener un ejemplo de trabajo.

### Ejercicio 2.29: Contar ejemplares por especie
Escribí una función `especies(lista)` que tome una lista de árboles como la generada en el Ejercicio anterior y devuelva el conjunto de especies (columna `'nombre_com'` del archivo) que figuran en la lista.

_Ṣegurencia: Usá el comando `set` como en la \ref{secc_conjuntos})._

### Ejercicio 2.30: Contar ejemplares por especie
Usando contadores como en el Ejercicio ?, escribí una función `contar_ejemplares(lista_arboles,especie)` que dada una lista como la que generada con `leer_parque()` devuelva un diccionario en el que las especies (columna `'nombre_com'` del archivo) sean las claves y tengan como valores asociados la cantidad de ejemplares en esa especie en la lista dada.

Luego, combiná estas dos funciones con el método `most_common()` para informar las cinco especies más frecuentes en cada uno de los siguientes parques:

- 'GENERAL PAZ'
- 'ANDES, LOS'
- 'CENTENARIO'

### Ejercicio 2.31: Alturas de una especie en una lista
Escribí una función `obtener_alturas(especie,larboles)` que, dada una especie de árbol (columna `'nombre_com'` del archivo) y una lista de árboles como la anterior, devuelva una lista con las alturas (columna `'altura_tot'`) de los ejemplares de esa especie. 

_Observación: Acá sí, fijate de devolver las alturas como números (de punto flotante) y no como cadenas de caracteres_.

Calculá la altura promedio y altura máxima de los 'Jacarandá'en los tres parques mencionados.

### Ejercicio 2.32: Inclinación promedio por especie de una lista
Escribí una función `obtener_inclinaciones(especie,lista)` que, dada una especie de árbol y una lista de árboles como la anterior, devuelva una lista con las inclinaciones (columna `'inclinacio'`) de los ejemplares de esa especie. 

### Ejercicio 2.33: Especies con ejemplares más inclinados
Combinando la función `especies()` con `obtener_inclinaciones()` escribí una función `especies_inclinadas(lista)` que, dada una lista de árboles devuelva la especie que tiene el ejemplar más inclinado así como la especie que tiene mayor promedio de inclinación entre las que figuran en la lista.

Correlo para loa tres parques mencionados anteriormente.

[](OTRA: lista de lat lon de una especie en una lista)









[Contenidos](../Contenidos.md) \| [Anterior (7 El módulo collections)](07_Contadores.md) \| [Próximo (9 Cierre de la segunda clase)](09_CierreClase.md)
