# Practica Instalacion De Percona Server
## Pablo Javega y Reinaldo Calderon
<img src="https://i.imgur.com/Da0DSyG.png" alt="percona" title="percona" width="300"/>





### Instalacion de Percona Server
<img src="https://i.imgur.com/9se8QTU.png" alt="percona" title="percona" width="3000"/>

> Primero descarga el repositorio con la siguiente comando:

> **sudo yum install https://repo.percona.com/yum/percona-release-latest.noarch.rpm**


<img src="https://i.imgur.com/jSWbA3Z.png" alt="percona" title="percona" width="3000"/>

>Activamos el repositorio

> **sudo percona-release setup ps80**

<img src="https://i.imgur.com/cnD3lGb.png" alt="percona" title="percona" width="3000"/>
<img src="https://i.imgur.com/iVzXRil.png" alt="percona" title="percona" width="3000"/>

>Ahora instalamos los paquetes

> **sudo yum install percona-server-server**

#### Posible solucion por si no deja ejecutar el comando de instalacion
<img src="https://i.imgur.com/8oOJfCe.png" alt="percona" title="percona" width="3000"/>

>**dnf clean all**

<img src="https://i.imgur.com/q7j7SJa.png" alt="percona" title="percona" width="3000"/>

>**rm -frv /var/cache/dnf**

<img src="https://i.imgur.com/YWE2K9j.png" alt="percona" title="percona" width="3000"/>

>**subscription-manager refresh**

<img src="https://i.imgur.com/gZfpbA6.png" alt="percona" title="percona" width="3000"/>

>**dnf update**
### Informacion Adicional
#### Instalacion de Seguridad

<img src="https://i.imgur.com/PN1aXjC.png" alt="percona" title="percona" width="3000"/>

<img src="https://i.imgur.com/wQdOqrH.png" alt="percona" title="percona" width="3000"/>

<img src="https://i.imgur.com/2mCL4hB.png" alt="percona" title="percona" width="3000"/>

**No se puede poner "patata" porque no cumple los requisitos minimos establecidos**

#### Comandos para verificar el estado del servidor
##### Iniciar Server
<img src="https://i.imgur.com/J87B1w7.png" alt="percona" title="percona" width="3000"/>

##### Ver el estado
<img src="https://i.imgur.com/9MnjvHF.png" alt="percona" title="percona" width="3000"/>

##### Parar el server
<img src="https://i.imgur.com/x09sUT9.png" alt="percona" title="percona" width="3000"/>

#### Archivo de configuracion del Percona Server

<img src="https://i.imgur.com/HHXSnb4.png" alt="percona" title="percona" width="30000"/>

#### Localizacion de los archivos de datos

<img src="https://i.imgur.com/civySf8.png" alt="percona" title="percona" width="30000"/>

<img src="https://i.imgur.com/wroWRlA.png" alt="percona" title="percona" width="30000"/>

#### Crear Usuario

##### En maquina

<img src="https://i.imgur.com/tI5uN3F.png" alt="percona" title="percona" width="30000"/>

<img src="https://i.imgur.com/v5DswT1.png" alt="percona" title="percona" width="30000"/>

##### En mysql

<img src="https://i.imgur.com/cmIKHJZ.png" alt="percona" title="percona" width="30000"/>

#### Links de interes
https://www.percona.com/doc/percona-server/8.0/installation/yum_repo.html
https://www.percona.com/doc/percona-server/LATEST/installation/post-installation.html
https://tecadmin.net/change-mysql-password-policy-level/
https://www.a2hosting.com.co/kb/developer-corner/mysql/reset-mysql-root-password
https://www.linkedin.com/pulse/how-change-mysql-default-port-3306-secure-piyush-diwakar?trk=public_profile_article_view

