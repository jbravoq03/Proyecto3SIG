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
- Primero seleccionamos y exportamos como shapefile el canton central de Alajuela, obtenido del shapefile que contenia los cantones. Posteriormente usamos esta capa para aplicar intersecciones con el resto de capas poligonales, lineales y puntuales necesarias para realizar el proyecto.

### 2. Imagen base.
- Para la imagen base se utilizó la capa puntual llamada "geo_hitos", utilizamos interpolacion por distancia inversa ponderada, posteriormente el .TIF generado lo convertimos a .PNG y tomamos las coordenadas x,y del .TIF para colocarlo correctamente con Leaflet.

### 3. Archivos shapefile de polígonos.
- Se utilizaron las capas de poligonos mencionadas en la especificación, además, se extrajo de OpenStreetMap, seleccionando el cantón central de Alajuela, la capa que contenia zonas verdes y parques. Todo esto, posteriormente, se le asigno un estilo en TileMill.

### 4. Archivos shapefile de líneas.
- Se utilizaron las capas de carreteras y ríos, tomadas del archivo Geo_CR ubicado en los documentos del curso. Tambien se extrajo de OpenStreetMap la capa de calles, de esta forma se tomaron estos 3 archivos de líneas y se estilizaron en TileMill, estableciendo que la etiqueta era de una línea, para que apareciera de forma continua en todo su recorrido, se utilizó distintos colores para poder diferenciar carreteras, ríos y calles.

### 5. Archivos shapefile de puntos.
- Se tomaron todas las capas de puntos listadas en la especificación del proyecto (Escuelas, agencias bancarias, hospitales, gasolineras y demás). También, se extrajo de OpenStreetMap los puntos que representaban tiendas y amenidades. Todas estas capas fueron cargadas en TileMill, posteriormente descargamos una colección de íconos del siguiente repositorio: https://github.com/rapideditor/temaki?tab=readme-ov-file. Utilizamos distintos íconos para cada tipo de elemento puntual, así como diferente color tanto para el ícono como para la etiqueta, de esta forma se pueden identificar fácilmente.

### 6. Niveles de zoom en TileMill.
- Primero generamos 5 niveles de zoom (9 a 13) seleccionando todo el país. Posteriormente, seleccionamos solo la zona del cantón, de esta forma, generamos otros 5 niveles más (14 a 18). 
- Seleccionamos solo la zona del canton porque era lo que necesitaba más niveles para mostrar mejor los detalles y también porque que si lo haciamos con todo el país el archivo llegaba a pesar cientos de GB.