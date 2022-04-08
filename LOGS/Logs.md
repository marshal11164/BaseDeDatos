# LOGS
## Pablo Javega i Reinaldo Calderón


<img src="https://i.imgur.com/wCqEt29.png" alt="mysql" title="percona" width="300"/>

# Index
- [LOGS](#logs)
  - [Pablo Javega i Reinaldo Calderón](#pablo-javega-i-reinaldo-calderón)
- [Index](#index)
- [Logs](#logs-1)
  - [Comprovació dels Logs activats per defecte](#comprovació-dels-logs-activats-per-defecte)
  - [Activació de logs](#activació-de-logs)
  - [Desactivar Log Binary, Slow query i General log](#desactivar-log-binary-slow-query-i-general-log)
  - [Activar Log Binary, Slow query i General log](#activar-log-binary-slow-query-i-general-log)
    - [General Log](#general-log)
    - [Slow Query Log](#slow-query-log)
    - [Binary log](#binary-log)
  - [Sakila](#sakila)
    - [Mirar el nombre de taules creades](#mirar-el-nombre-de-taules-creades)
    - [Comprovar Slow query](#comprovar-slow-query)
    - [Binary Log](#binary-log-1)
      - [Crear taula foo](#crear-taula-foo)
      - [Flush Logs](#flush-logs)
      - [Crear taula bar](#crear-taula-bar)
      - [Borrar binary log](#borrar-binary-log)
      - [mysqlbinlog](#mysqlbinlog)
    - [Desactivar log binary en una sessió concreta](#desactivar-log-binary-en-una-sessió-concreta)

# Logs
## Comprovació dels Logs activats per defecte

<img src="https://i.imgur.com/gb7Mshs.png" alt="mysql" title="percona" width="30000"/>

>Per defecte sempre està activat el log de errors, que es troba a **/var/log/mysqld.log**
## Activació de logs

<img src="https://i.imgur.com/9r6bKTc.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/dnWgm6W.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/b7OiFbe.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/DNU7imA.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/PfRPwlC.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/XPRp7EX.png" alt="mysql" title="percona" width="30000"/>

## Desactivar Log Binary, Slow query i General log

<img src="https://i.imgur.com/FDrAZh5.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/IFp93wp.png" alt="mysql" title="percona" width="30000"/>

## Activar Log Binary, Slow query i General log

### General Log

<img src="https://i.imgur.com/RXrxPq0.png" alt="mysql" title="percona" width="30000"/>

### Slow Query Log

<img src="https://i.imgur.com/Dhn3DkF.png" alt="mysql" title="percona" width="30000"/>

### Binary log

<img src="https://i.imgur.com/t5FTm2z.png" alt="mysql" title="percona" width="30000"/>

>No es pot activar el binary log amb un **Set_Global**, perquè es una variable que només es pot activar per arxiu. A més, ja ve activat de base.
## Sakila
### Mirar el nombre de taules creades

<img src="https://i.imgur.com/2jCZyrY.png" alt="mysql" title="percona" width="30000"/>

### Comprovar Slow query

<img src="https://i.imgur.com/OvEiFEr.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/nXFz8It.png" alt="mysql" title="percona" width="30000"/>

### Binary Log

#### Crear taula foo

<img src="https://i.imgur.com/lWzEJrd.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/tG3yxXt.png" alt="mysql" title="percona" width="30000"/>

#### Flush Logs

<img src="https://i.imgur.com/s4pEQA0.png" alt="mysql" title="percona" width="30000"/>

>Elimina l'interior dels logs

#### Crear taula bar

<img src="https://i.imgur.com/0wNzTHK.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/HiOiNnQ.png" alt="mysql" title="percona" width="30000"/>

#### Borrar binary log

<img src="https://i.imgur.com/jq7dDjt.png" alt="mysql" title="percona" width="30000"/>

#### mysqlbinlog

<img src="https://i.imgur.com/Viga9V9.png" alt="mysql" title="percona" width="30000"/>

### Desactivar log binary en una sessió concreta

<img src="https://i.imgur.com/IcTFBbQ.jpg" alt="mysql" title="percona" width="30000"/>

> No es pot desactivar log binary en una sessió concreta perquè la variable **log_bin** és només de lectura.

