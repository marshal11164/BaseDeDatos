# Replicació: Configuració d'un sistema de rèplica

## Configuració Master

Verifiquem que el paràmetre **server-id** té un valor numèric.


Realitzem un FLUSH dels logs utilitzant la comanda **FLUSH LOGS** dins del MySQL.

Realitzem una comprobació dels logs com a master amb la comanda **SHOW MASTER LOGS**.

## Configuració Slave i Master

Realitzem una còpia de la màquina virtual on tenim el SGBD MySQL. Aquesta nova màquina serà la que farà d'eslau.

Trobem quina IP té cada màquina.

### MASTER

Creem un backup de la BD de la màquina master utilitzant la comanda: **mysqldump –-user=root –-password=vostrepwd -–master-data=2 sakila > /tmp/master_backup.sql**

Editem el fitxer **master_backup.sql** que es troba a /tmp i busquem la línia que comenci per **--CHANGE MASTER TO**. Ens apuntem els valors que trobarem a **MASTER_LOG_FILE** i **MASTER_LOG_POS**.

### SLAVE

Parem el servei de MySQL.
Modifiquem el fitxer de configuració **/etc/my.cnf**. Desactivem el log-bin afegint **disable-log-bin** i li assignem un valor de server_id diferent al del master afegint **server_id = (valor numeric diferent del master)**
Tornem a engegar el servei MySQL.


### MASTER

Afegim l'usuari *slave* amb la IP de la màquina slave.
>mysql> CREATE USER 'slave'@'IP-SERVIDOR-SLAVE'
>       -> IDENTIFIED BY 'P@ssw0rd';

Afegim el permís de REPLICATION SLAVE a l'usuari que acabem de crear.
>mysql> GRANT REPLICATION SLAVE ON \*.\*
>       -> TO 'slave'@'IP-SERVIDOR-SLAVE';
>mysql> FLUSH PRIVILEGES;

### SLAVE

Executem la següent comanda a MySQL:
>mysql> CHANGE MASTER TO
>      -> MASTER_HOST = '<ip-servidor-master>',
>      -> MASTER_USER = 'slave',
>      -> MASTER_PASSWORD = 'P@ssw0rd'
>      -> MASTER_LOG_FILE = '<valor que hem apuntat anteriorment>,
>      -> MASTER_LOG_POS = <valor que hem apuntat anteriorment>;
    
