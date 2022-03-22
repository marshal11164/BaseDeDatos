# Instalació De Percona Server
## Pablo Javega y Reinaldo Calderon
<img src="https://i.imgur.com/Da0DSyG.png" alt="percona" title="percona" width="300"/>

# Index

- [Instalació De Percona Server](#instalació-de-percona-server)
  - [Pablo Javega y Reinaldo Calderon](#pablo-javega-y-reinaldo-calderon)
- [Index](#index)
    - [Instalacion de Percona Server](#instalacion-de-percona-server)
      - [Possible solució en cas de que no deixi executar la comanda de instal·lació](#possible-solució-en-cas-de-que-no-deixi-executar-la-comanda-de-installació)
    - [Informació Addicional](#informació-addicional)
      - [Instalació de Seguretat](#instalació-de-seguretat)
      - [Comandes per verificar l'estat del servidor](#comandes-per-verificar-lestat-del-servidor)
        - [Iniciar Server](#iniciar-server)
        - [Veure l'estat](#veure-lestat)
        - [Parar el Server](#parar-el-server)
      - [Arxiu de configuració del Percona Server](#arxiu-de-configuració-del-percona-server)
      - [Ubicació dels arxius de dades](#ubicació-dels-arxius-de-dades)
      - [Crear Usuari](#crear-usuari)
        - [A màquina](#a-màquina)
        - [A mysql](#a-mysql)
        - [AutoLogin](#autologin)
      - [Cambiar el port](#cambiar-el-port)
      - [Links de interès](#links-de-interès)



### Instalacion de Percona Server
<img src="https://i.imgur.com/9se8QTU.png" alt="percona" title="percona" width="3000"/>

> Obtenim el repositori amb la comanda seguent:

> **sudo yum install https://repo.percona.com/yum/percona-release-latest.noarch.rpm**


<img src="https://i.imgur.com/jSWbA3Z.png" alt="percona" title="percona" width="3000"/>

>Activem el repositori.

> **sudo percona-release setup ps80**

<img src="https://i.imgur.com/cnD3lGb.png" alt="percona" title="percona" width="3000"/>
<img src="https://i.imgur.com/iVzXRil.png" alt="percona" title="percona" width="3000"/>

>Instal·lem els paquets.

> **sudo yum install percona-server-server**

#### Possible solució en cas de que no deixi executar la comanda de instal·lació
<img src="https://i.imgur.com/8oOJfCe.png" alt="percona" title="percona" width="3000"/>

>**dnf clean all**

<img src="https://i.imgur.com/q7j7SJa.png" alt="percona" title="percona" width="3000"/>

>**rm -frv /var/cache/dnf**

<img src="https://i.imgur.com/YWE2K9j.png" alt="percona" title="percona" width="3000"/>

>**subscription-manager refresh**

<img src="https://i.imgur.com/gZfpbA6.png" alt="percona" title="percona" width="3000"/>

>**dnf update**
### Informació Addicional
#### Instalació de Seguretat

<img src="https://i.imgur.com/PN1aXjC.png" alt="percona" title="percona" width="3000"/>

<img src="https://i.imgur.com/wQdOqrH.png" alt="percona" title="percona" width="3000"/>

<img src="https://i.imgur.com/2mCL4hB.png" alt="percona" title="percona" width="3000"/>

**No es pot posar "patata" perquè no cumpleix els requisits mínims establerts**

#### Comandes per verificar l'estat del servidor
##### Iniciar Server
<img src="https://i.imgur.com/J87B1w7.png" alt="percona" title="percona" width="3000"/>

##### Veure l'estat
<img src="https://i.imgur.com/9MnjvHF.png" alt="percona" title="percona" width="3000"/>

##### Parar el Server
<img src="https://i.imgur.com/x09sUT9.png" alt="percona" title="percona" width="3000"/>

#### Arxiu de configuració del Percona Server

<img src="https://i.imgur.com/HHXSnb4.png" alt="percona" title="percona" width="30000"/>

#### Ubicació dels arxius de dades

<img src="https://i.imgur.com/civySf8.png" alt="percona" title="percona" width="30000"/>

<img src="https://i.imgur.com/wroWRlA.png" alt="percona" title="percona" width="30000"/>

#### Crear Usuari

##### A màquina

<img src="https://i.imgur.com/tI5uN3F.png" alt="percona" title="percona" width="30000"/>

<img src="https://i.imgur.com/v5DswT1.png" alt="percona" title="percona" width="30000"/>

##### A mysql

<img src="https://i.imgur.com/cmIKHJZ.png" alt="percona" title="percona" width="30000"/>

<img src="https://i.imgur.com/ZWLR98c.png" alt="percona" title="percona" width="30000"/>

<img src="https://i.imgur.com/KgZmEfC.png" alt="percona" title="percona" width="30000"/>

<img src="https://i.imgur.com/egmbNu2.png" alt="percona" title="percona" width="30000"/>

##### AutoLogin

<img src="https://i.imgur.com/Q07SmoA.png" alt="percona" title="percona" width="30000"/>

> Entramos al archivo de configuracion ubicado en : /etc/my.cnf. Y colocamos el siguiente codigo:

>**[Client]**

>**user = asix**

>**password = patata**

#### Cambiar el port

<img src="https://i.imgur.com/UR9ehII.png" alt="percona" title="percona" width="30000"/>

<img src="https://i.imgur.com/V54UbRL.png" alt="percona" title="percona" width="30000"/>

#### Links de interès
https://www.percona.com/doc/percona-server/8.0/installation/yum_repo.html
https://www.percona.com/doc/percona-server/LATEST/installation/post-installation.html
https://tecadmin.net/change-mysql-password-policy-level/
https://www.a2hosting.com.co/kb/developer-corner/mysql/reset-mysql-root-password
https://www.linkedin.com/pulse/how-change-mysql-default-port-3306-secure-piyush-diwakar?trk=public_profile_article_view
