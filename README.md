# Carga_Incremental_Diaria_Con_Parametro:

Se tiene un conjunto de dataset en archivos de Excel. Lo que se requiere es que se carguen solo algunos Archivos de Excel, para ello se necesita que se pasen como parámetro las fechas de los archivos que se van a cargar a la Base de Datos.

-----------------------------------------------------------------------------------------------------

1. En una carpeta alojaremos los archivos de Excel, estos los puedes enconntrar en el repositorio:

<p align="center">
<img src="https://github.com/csantamaria89/Carga_Incremental_Diaria_Con_Parametro/blob/main/assets/Imagen1.png"  height=150>
</p>
   

```shell
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
