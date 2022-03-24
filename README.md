# Instalacion Mysql

## Pablo Javega, Reinaldo Calderón

<img src="https://i.imgur.com/Zr6ZgP4.png" alt="mysql" title="percona" width="300"/>

# Instalacion

<img src="https://i.imgur.com/meNeNqr.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/e4oUeJd.png" alt="mysql" title="percona" width="30000"/>

> Utilizamos el comando: **yum -y install @mysql**. Para que instale la version mas reciente del mysql y todas sus dependencia.

<img src="https://i.imgur.com/xKuKvYz.png" alt="mysql" title="percona" width="30000"/>

> Despues iniciamos el mysql con : **systemctl start mysqld**. Y despues lo habilitamos con : **systemctl enable --now mysqld**.
> Ahora comprobamos que esta activo con: **systemctl status mysqld**

<img src="https://i.imgur.com/GdDKW2a.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/4N9W3Eo.png" alt="mysql" title="percona" width="30000"/>

>Para finalizar la instalacion ejecutamos una instalacion de seguridad para establecer una contraseña al root, quitar los usuarios anonimos y deshabilitar el login desde remoto del root. Comando: **mysql_secure_installation**

# Ubicacion de los archivos del msql

## Archivos de datos

<img src="https://i.imgur.com/0MXmWe2.png" alt="mysql" title="percona" width="30000"/>

## Archivo de configuracion

<img src="https://i.imgur.com/9JyBxk8.png" alt="mysql" title="percona" width="30000"/>

<img src="https://i.imgur.com/hjYfC5i.png" alt="mysql" title="percona" width="30000"/>

>El archivo de configuracion esta como dividido en distintos archivos, que estan en esta ruta: **/etc/my.cnf.d**

<img src="https://i.imgur.com/sCMF76k.png" alt="mysql" title="percona" width="30000"/>

# Cambiar el puerto