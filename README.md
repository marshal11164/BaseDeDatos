# Instalació Mysql

## Pablo Javega, Reinaldo Calderón

# índex

- [Instalacion Mysql](#instalacion-mysql)
  - [Pablo Javega, Reinaldo Calderón](#pablo-javega-reinaldo-calderón)
- [Index](#index)
- [Instalacion](#instalacion)
- [Ubicacion de los archivos del msql](#ubicacion-de-los-archivos-del-msql)
  - [Archivos de datos](#archivos-de-datos)
  - [Archivo de configuracion](#archivo-de-configuracion)
- [Cambiar el puerto](#cambiar-el-puerto)
- [Comprovacion](#comprovacion)

<img src="https://i.imgur.com/Zr6ZgP4.png" alt="mysql" title="percona" width="300"/>

# Instal·lació

<img src="https://i.imgur.com/meNeNqr.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/e4oUeJd.png" alt="mysql" title="percona" width="30000"/>

> Instal·lem la versió més recent de mysql i els mòduls necessaris pel seu funcionament amb la comanda: **yum -y install @mysql**.

<img src="https://i.imgur.com/xKuKvYz.png" alt="mysql" title="percona" width="30000"/>

> Iniciem el mysql amb la comanda : **systemctl start mysqld**. I l'habilitem amb: **systemctl enable --now mysqld**.
> Comprovem que està actiu amb la comanda: **systemctl status mysqld**

<img src="https://i.imgur.com/GdDKW2a.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/4N9W3Eo.png" alt="mysql" title="percona" width="30000"/>

>Per a finalitzar la instal·lació, executem una instal·lació de seguretat per establir una contrasenya al root, treure els usuaris anònims i deshabilitar el login remot del root. Utiliitzem la comanda: **mysql_secure_installation**

# Ubicació dels arxius del mysql

## Arxius de dades

<img src="https://i.imgur.com/0MXmWe2.png" alt="mysql" title="percona" width="30000"/>

## Arxiu de configuració

<img src="https://i.imgur.com/9JyBxk8.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/hjYfC5i.png" alt="mysql" title="percona" width="30000"/>

>El arxiu de configuració està dividit en arxius diferents que es troben a: **/etc/my.cnf.d**

<img src="https://i.imgur.com/sCMF76k.png" alt="mysql" title="percona" width="30000"/>

# Cambiar el port

<img src="https://i.imgur.com/UR9ehII.png" alt="mysql" title="percona" width="30000"/>

> Primer hem d'aturar el servei.

<img src="https://i.imgur.com/V54UbRL.png" alt="mysql" title="percona" width="30000"/>

>I afegim el següent a l'arxiu de configuració: **port= 33306**.
> Com l'arxiu de configuració del mysql està vinculat a altres arxius, hem d'afegir-ho en aquest: **/etc/my.cnf.d/mysql-server.cnf**

<img src="https://i.imgur.com/AbZF3sR.png" alt="mysql" title="percona" width="30000"/>

# Comprovació

<img src="https://i.imgur.com/b2OcwCZ.png" alt="mysql" title="percona" width="30000"/>
