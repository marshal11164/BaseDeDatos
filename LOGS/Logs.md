# LOGS
## Pablo Javega y Reinaldo Calderon

<img src="https://i.imgur.com/wCqEt29.png" alt="mysql" title="percona" width="300"/>

# Logs
## Comprovacion de Logs activados por defecto

<img src="https://i.imgur.com/gb7Mshs.png" alt="mysql" title="percona" width="30000"/>

>Por defecto siempre viene activado el log de errores, que se ubica en **/var/log/mysqld.log**
## Activacion de logs

<img src="https://i.imgur.com/9r6bKTc.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/dnWgm6W.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/b7OiFbe.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/DNU7imA.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/PfRPwlC.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/XPRp7EX.png" alt="mysql" title="percona" width="30000"/>

## Desactivar Log Binary, Slow query y General log

<img src="https://i.imgur.com/FDrAZh5.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/IFp93wp.png" alt="mysql" title="percona" width="30000"/>

## Activar Log Binary, Slow query y General log

### General Log

<img src="https://i.imgur.com/RXrxPq0.png" alt="mysql" title="percona" width="30000"/>

### Slow Query Log

<img src="https://i.imgur.com/Dhn3DkF.png" alt="mysql" title="percona" width="30000"/>

### Binary log

<img src="https://i.imgur.com/t5FTm2z.png" alt="mysql" title="percona" width="30000"/>

>Para activar el binary log  no se puede con un **Set_Global**, porque ya tiene uno por defecto activado
>Solo se puede modificar por archivos.
## Sakila
### Mirar el numero de tablas que ha creado

<img src="https://i.imgur.com/2jCZyrY.png" alt="mysql" title="percona" width="30000"/>

### Comprobar Slow query

<img src="https://i.imgur.com/OvEiFEr.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/Mk7GWh7.png" alt="mysql" title="percona" width="30000"/>

### Binary Log

#### Crear tabla foo

<img src="https://i.imgur.com/lWzEJrd.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/tG3yxXt.png" alt="mysql" title="percona" width="30000"/>

#### Flush Logs

<img src="https://i.imgur.com/s4pEQA0.png" alt="mysql" title="percona" width="30000"/>

>Elimina el interior de los logs

#### Crear tabla bar

<img src="https://i.imgur.com/0wNzTHK.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/HiOiNnQ.png" alt="mysql" title="percona" width="30000"/>

#### Esborrar binary log

<img src="https://i.imgur.com/jq7dDjt.png" alt="mysql" title="percona" width="30000"/>

#### mysqlbinlog

<img src="https://i.imgur.com/Viga9V9.png" alt="mysql" title="percona" width="30000"/>

### Desactivar log binary en una sesion concreta

<img src="https://i.imgur.com/IcTFBbQ.jpg" alt="mysql" title="percona" width="30000"/>

> No se puede ya que la variable **log_bin** es solo de lectura

