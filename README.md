# Carga_Incremental_Diaria_Con_Parametro:

Se tiene un conjunto de dataset en archivos de Excel. Lo que se requiere es que se carguen solo algunos Archivos de Excel, para ello se necesita que se pasen como parámetro las fechas de los archivos que se van a cargar a la Base de Datos.

-----------------------------------------------------------------------------------------------------

1. En una carpeta alojaremos los archivos de Excel, estos los puedes enconntrar en el repositorio y copiaremos la dirección completa:

<p align="center">
<img src="https://github.com/csantamaria89/Carga_Incremental_Diaria_Con_Parametro/blob/main/Assets/Imagen2.png"  height=250>
</p>

2. Creamos un nuevo paquete en el SSIS y posterior se crearán las siguientes variables:

<p align="center">
<img src="https://github.com/csantamaria89/Carga_Incremental_Diaria_Con_Parametro/blob/main/Assets/Imagen1.png"  height=150>
</p>

Nota: Para la variable Ruta, agregamos la ruta completa dónde guardamos los tres archivos de excel.

4. Para el desarrollo de este ejercicio utilizaremos la DB MONROE, Copio el código por si la quieren utilizar:

```shell
CREATE DATABASE MONROE
GO

USE MONROE
GO

CREATE TABLE ACCIDENTES(
Periodo INT,
NumeroRegistro INT,
Semana VARCHAR(MAX),
Colision VARCHAR(MAX),
TipoLesion VARCHAR(MAX),
FactorPrimario VARCHAR(MAX),
ReporteLocasion VARCHAR(MAX),
Latitud VARCHAR(MAX),
Longitud VARCHAR(MAX)
)
```
En la ventana de Control Flow agregamos una caja de Execute SQL Task, la cual llamaremos Limpiar Fecha de Carga. Posteriormente configuraremos la conexión con la BD MONROE.

<p align="center">
<img src="https://github.com/csantamaria89/Carga_Incremental_Diaria_Con_Parametro/blob/main/Assets/Imagen3.png"  height=450>
</p>
