# Informe - Proyecto 3

Instituto Tecnológico de Costa Rica.

Escuela de Ingeniería en Computación.

**Estudiantes:** Josué Bravo Quirós. C.2022067969. José Pablo Quesada Rodríguez. C.2020211670.

**Curso:** Sistemas de Información Geográfica. 

**Profesor:** Armando Arce Orozco.

**Fecha:** 8 de diciembre de 2025. 

---
Tabla de Contenido.
- [Informe - Proyecto 3](#informe---proyecto-3)
  - [Enlace al sitio web.](#enlace-al-sitio-web)
  - [Descripción del proceso de creación del mapa.](#descripción-del-proceso-de-creación-del-mapa)
    - [1. Capa del cantón central de Alajuela.](#1-capa-del-cantón-central-de-alajuela)
    - [2. Imagen base.](#2-imagen-base)
    - [3. Archivos shapefile de polígonos.](#3-archivos-shapefile-de-polígonos)
    - [4. Archivos shapefile de líneas.](#4-archivos-shapefile-de-líneas)
    - [5. Archivos shapefile de puntos.](#5-archivos-shapefile-de-puntos)
    - [6. Niveles de zoom en TileMill.](#6-niveles-de-zoom-en-tilemill)


## Enlace al sitio web.
https://jbravoq03.github.io/Proyecto3SIG/

## Descripción del proceso de creación del mapa.
### 1. Capa del cantón central de Alajuela.

- Se inició seleccionando el cantón central de Alajuela a partir de la capa general de cantones (shapefile geo_cantones). Una vez identificado, Esta capa funcionó como base para aplicar operaciones de intersección con las demás capas poligonales, de líneas y de puntos incluidas en el proyecto, manteniendo únicamente los datos correspondientes al territorio del cantón central.

### 2. Imagen base.
- Para la creación de la imagen base del mapa, se utilizó la capa puntual denominada “geo_hitos”. A partir de esos puntos se aplicó interpolación mediante el método de distancia inversa ponderada (IDW), con lo cual se generó un archivo 
.TIF Este archivo se convirtió posteriormente a formato .PNG para poder integrarlo correctamente con Leaflet. Además, se tomaron las coordenadas X y Y del archivo original para asegurar que la imagen quedara alineada y georreferenciada en su posición correspondiente dentro del visor web.

### 3. Archivos shapefile de polígonos.
- Se trabajó con todas las capas poligonales mencionadas en la especificación del proyecto. Además, se incorporó una capa adicional obtenida desde OpenStreetMap, correspondiente al cantón central de Alajuela (incluyendo: zonas verdes y parques dentro del área) . Luego de cargarlas, se aplicaron estilos en TileMill, asignando colores y propiedades visuales adecuadas para permitir su correcta diferenciación y visualización en el mapa.

### 4. Archivos shapefile de líneas.
- Se utilizaron las capas de carreteras y ríos, tomadas del archivo Geo_CR ubicado en los documentos del curso. Tambien se extrajo de OpenStreetMap la capa de calles, de esta forma se tomaron estos 3 archivos de líneas y se estilizaron en TileMill, estableciendo que la etiqueta era de una línea, para que apareciera de forma continua en todo su recorrido, se utilizó distintos colores para poder diferenciar carreteras, ríos y calles.

### 5. Archivos shapefile de puntos.
- Se tomaron todas las capas de puntos listadas en la especificación del proyecto (Escuelas, agencias bancarias, hospitales, gasolineras y demás). También, se extrajo de OpenStreetMap los puntos que representaban tiendas y amenidades. Todas estas capas fueron cargadas en TileMill, posteriormente descargamos una colección de íconos del siguiente repositorio: https://github.com/rapideditor/temaki?tab=readme-ov-file. Utilizamos distintos íconos para cada tipo de elemento puntual, así como diferente color tanto para el ícono como para la etiqueta, de esta forma se pueden identificar fácilmente.

### 6. Niveles de zoom en TileMill.
- La generación de los niveles de zoom se realizó en dos etapas. Primero, se crearon los niveles de zoom del 9 al 13 considerando toda la extensión del país. Posteriormente, se limitaron los niveles del 14 al 18 únicamente al área del cantón central de Alajuela. Esta decisión permitió representar con mayor detalle la zona de estudio sin provocar un incremento excesivo en el tamaño del archivo, ya que si se hubieran aplicado los niveles de zoom altos al país completo, el tamaño del proyecto habría alcanzado cientos de gigabytes.