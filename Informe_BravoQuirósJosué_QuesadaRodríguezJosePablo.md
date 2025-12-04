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
    - [1. Imagen base.](#1-imagen-base)
    - [2. Archivos shapefile de polígonos.](#2-archivos-shapefile-de-polígonos)
    - [3. Archivos shapefile de líneas.](#3-archivos-shapefile-de-líneas)
    - [4. Archivos shapefile de puntos.](#4-archivos-shapefile-de-puntos)


## Enlace al sitio web.
https://jbravoq03.github.io/Proyecto3SIG/

## Descripción del proceso de creación del mapa.

### 1. Imagen base.
- Para la imagen base se utilizó la capa puntual llamada "geo_hitos", utilizamos interpolacion por distancia inversa ponderada, posteriormente el .TIF generado lo convertimos a .PNG y tomamos las coordenadas x,y del .TIF para colocarlo correctamente con Leaflet.

### 2. Archivos shapefile de polígonos.
- Se utilizaron las capas de poligonos mencionadas en la especificación, además, se extrajo de OpenStreetMap, seleccionando el cantón central de Alajuela, la capa que contenia zonas verdes y parques. Todo esto, posteriormente, se le asigno un estilo en TileMill.
- 
### 3. Archivos shapefile de líneas.

### 4. Archivos shapefile de puntos.
- 