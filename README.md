# Publicación de geoservicios del Atlas de Servicios Ecosistémicos de la GAM

Este documento detalla el procedimiento para la publicación de los geoservicios (i.e. servicios web geoespaciales) del [Atlas de Servicios Ecosistémicos de la Gran Área Metropolitana](https://atlas-servicios-ecosistemicos-gam.github.io/). Estos geoservicios son utilizados en la interfaz de usuario del Atlas y también están disponibles para ser consumidos con sistemas de información geográfica (SIG) como, por ejemplo, [ArcGIS](https://www.arcgis.com/) y [QGIS](https://qgis.org/). El documento incluye también una lista de los geoservicios publicados.

Para publicar los geoservicios, se utiliza [ArcGIS API for Python](https://developers.arcgis.com/python/).

## Contenido

## 0. Obtención de programas y datos

### 0.1. Obtención de las capas geoespaciales

### 0.2. Clonación de este repositorio Git
```shell
# Clonación de este repositorio Git
$ git clone https://github.com/atlas-servicios-ecosistemicos-gam/publicacion-geoservicios.git

$ cd publicacion-geoservicios
```

## 1. Publicación de geoservicios
```shell
$ conda activate gam-publicacion-geoservicios
$ jupyter notebook 

# Abrir y ejecutar el notebook publicacion-geoservicios.ipynb

$ conda deactivate
```

## Anexo 1. Creación de un ambiente Conda para publicación de geoservicios
**Actualización de Conda**
```shell
# Actualización de Conda
$ conda update -n base -c defaults conda
```

**Creación del ambiente**
```shell
# Creación del ambiente
$ conda create -n gam-publicacion-geoservicios
```

**Activación del ambiente**
```shell
# Activación del ambiente
$ conda activate gam-publicacion-geoservicios
```

**Instalación de paquetes**
```shell
# Instalación de paquetes
# ArcGIS API for Python
$ conda config --set channel_priority false # fue necesario para instalarlo en Windows
$ conda install -c esri arcgis
# GDAL, Jupyter Notebook
$ conda config --env --add channels conda-forge
$ conda config --env --set channel_priority strict
$ conda install -c conda-forge gdal notebook
```

**Desactivación del ambiente**
```shell
# Desactivación (para el final del proceso)
$ conda deactivate
```
