# Replicació: Configuració d'un sistema de rèplica

## Configuració Master

Verifiquem que el paràmetre **server-id** té un valor numèric.
<img src="https://imgur.com/MyijcG9" alt="mysql" title="percona" width="30000"/>

Realitzem un FLUSH dels logs utilitzant la comanda **FLUSH LOGS** dins del MySQL.
<img src="https://imgur.com/IhIdUvJ" alt="mysql" title="percona" width="30000"/>

Realitzem una comprobació dels logs com a master amb la comanda **SHOW MASTER LOGS**.
<img src="https://imgur.com/4Hyqplj" alt="mysql" title="percona" width="30000"/>

## Configuració Slave i Master

Realitzem una còpia de la màquina virtual on tenim el SGBD MySQL. Aquesta nova màquina serà la que farà d'eslau.
<img src="https://imgur.com/RSBz3tZ" alt="mysql" title="percona" width="30000"/>

Trobem quina IP té cada màquina.
<img src="https://imgur.com/HbjtbqN" alt="mysql" title="percona" width="30000"/>
<img src="https://imgur.com/icv803P" alt="mysql" title="percona" width="30000"/>

### MASTER

Creem un backup de la BD de la màquina master utilitzant la comanda: **mysqldump –-user=root –-password=vostrepwd -–master-data=2 sakila > /tmp/master_backup.sql**
<img src="https://imgur.com/WOEEVa4" alt="mysql" title="percona" width="30000"/>

Editem el fitxer **master_backup.sql** que es troba a /tmp i busquem la línia que comenci per **--CHANGE MASTER TO**. Ens apuntem els valors que trobarem a **MASTER_LOG_FILE** i **MASTER_LOG_POS**.
<img src="https://imgur.com/b0ylJ3j" alt="mysql" title="percona" width="30000"/>

### SLAVE

Parem el servei de MySQL.
Modifiquem el fitxer de configuració **/etc/my.cnf**. Desactivem el log-bin afegint **disable-log-bin** i li assignem un valor de server_id diferent al del master afegint **server_id = (valor numeric diferent del master)**
<img src="https://imgur.com/dk7ehph" alt="mysql" title="percona" width="30000"/>

Borrem el fitxer **auto.cnf** per generar una nova UUID i que no coincideixi amb la del master.
<img src="https://imgur.com/eocfVcu" alt="mysql" title="percona" width="30000"/>

Tornem a engegar el servei MySQL.


### MASTER

Afegim l'usuari *slave* amb la IP de la màquina slave.
>mysql> CREATE USER 'slave'@'IP-SERVIDOR-SLAVE'
>       -> IDENTIFIED BY 'P@ssw0rd';
<img src="https://imgur.com/dXswz8N" alt="mysql" title="percona" width="30000"/>

Afegim el permís de REPLICATION SLAVE a l'usuari que acabem de crear.
>mysql> GRANT REPLICATION SLAVE ON \*.\*
>       -> TO 'slave'@'IP-SERVIDOR-SLAVE';
>mysql> FLUSH PRIVILEGES;
<img src="https://imgur.com/uifJL7L" alt="mysql" title="percona" width="30000"/>

### SLAVE

Executem la següent comanda a MySQL:
>mysql> CHANGE MASTER TO
>      -> MASTER_HOST = '<ip-servidor-master>',
>      -> MASTER_USER = 'slave',
>      -> MASTER_PASSWORD = 'P@ssw0rd'
>      -> MASTER_LOG_FILE = '<valor que hem apuntat anteriorment>,
>      -> MASTER_LOG_POS = <valor que hem apuntat anteriorment>;

<img src="https://imgur.com/WJmp796" alt="mysql" title="percona" width="30000"/>
