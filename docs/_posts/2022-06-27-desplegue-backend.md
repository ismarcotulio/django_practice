---
layout: post
title: "DESPLIEGUE DE APLICACIONES BACKEND"
subtitle: 'En servidor local, QA y Produccion'
author: "Paola Molina, Wilmer Hernandez y Marco Tulio Ruiz"
header-style: text
tags:
  - despliegue
  - backend
---
<style>
    .pantalla {
        display: block;
        margin-left: auto;
        margin-right: auto;
        width: 80%;
    }

    p{
        text-align: justify;
    }
</style>
El siguiente documento contiene los pasos realizados para desplegar todas las aplicaciones necesarias para trabajar en el proyecto de Automatizacion de Canjes y Marcas Propias del lado del backend. 

## AMBIENTE LOCAL DE DESARROLLO

### 1. Sistema Operativo
La mayoria de pasos descritos en esta documentacion se realizaron utilizando el sistema operativo <u>Ubuntu 20.04</u>. Tambien se puede utilizar cualquier otra distribucion de linux moderna.

### 2. Editor de codigo
En este proyecto el equipo de desarrollo utiliza el editor de codigo <u>Visual Studio Code</u>.

### 3. Preparando Django

Primero creamos la carpeta en donde se encontrara nuestro proyecto. En este caso la carpeta se llama <b>AutomatizacionCanjesMarcasPropias</b>. Luego nos aseguramos de tener instalado el gestor de paquetes de python <u>pip</u>, sino, lo instalamos utilizando el siguiente comando:

<code>sudo apt install python3-pip</code>

Despues instalamos la dependencia de <u>Virtual Environment</u> con el siguiente comando:

<code>pip install virtualenv</code>

o dependiendo de la version de python:

<code>sudo apt install python3.10-venv</code>

Dentro de la carpeta del proyecto creamos un entorno virtual de python utilizando el siguiente comando:

<code>sudo python3 -m venv envautomatizacioncanjesmarcaspropias</code>

Se recomienda dar permisos a la carpeta raiz donde se encuentra nuestro proyecto utilizando el siguiente comando:

<code>sudo chmod 777 -R /home/$USER/documents</code>

Activamos el entorno virtual por medio del siguiente comando:

<code>source $RUTAENV/bin/activate</code>

Una vez activado el entorno virtual, procedemos a instalar django en su ultima version:

<code>pip install django</code>

En este proyecto se instalo <u>django 4.0.5</u>. Luego instalamos las siguientes librerias:

<code>pip install django-cors-headers</code>

<code>pip install django-crontab</code>

<code>pip install djangorestframework</code>

<code>pip install requests</code>

<code>pip install gunicorn</code>

<code>pip install psycopg2-binary</code>

### 4. Preparando Base de Datos

El sistema gestor de base de datos que se utiliza para este proyecto es <u>postgres</u>. La base de datos como tal, se puede gestionar utilizando consola o por medio de un programa gestor con interfaz. En el caso de este proyecto de utilizo el programa gestor con interfaz DBeaver.

En el entorno local se recomienda instalar la version de postgres que se encuentra en los servidores QA y Produccion, en este caso seria <u>postgres 10.21</u>. Para instalar una version especifica de postgres se recomienda descargar el codigo fuente correspondiente desde la documentacion y seguir los pasos para compilar y posteriormente ejecutar. Tambien se puede instalar la version mas reciente, pero hacer esto es menos recomendable ya que puede abrir paso a futuras incompatibilidades con los respectivos gestores de base de datos en los servidores. Para instalar la ultima version de postgres se utiliza el siguiente comando:

<code>sudo apt install -y postgresql postgresql-contrib postgresql-client</code>

Para verificar si se instalo postgres correctamente podemos utilizar el comando:

<code>sudo service postgresql restart</code>

<code>sudo service postgresql status</code>

Una vez instalado postgres, entramos al sistema gestor como usuario administrador:

<code>sudo su - postgres</code>

Estando dentro de postgres, podemos comprobar la version instalada de la siguiente forma:

<code>select version();</code>

En nuestro caso se instalo <u>Postgres 14.3</u>. Luego establecemos una contraseña para el usuario administrador:

<code>\password postgres</code>

Creamos un nuevo usuario:

<code>
CREATE USER desarrollo WITH
    LOGIN
    SUPERUSER
    INHERIT
    CREATEDB
    NOCREATEROLE
    NOREPLICATION
    ENCRYPTED PASSWORD "md55de75376a668539b002512e0bd19dd05";
</code>

Creamos una base de datos:

<code>
CREATE DATABASE "CANJESMARCASPROPIAS"
    WITH
    OWNER = desarrollo
    ENCODING = "UTF8"
    LC_COLLATE = "es_HN.UTF-8"
    LC_CTYPE = "es_HN.UTF-8"
    TABLESPACE = pg_default
    CONNECTION_LIMIT = -1;
    TEMPLATE = template0
</code>

### 5. Creando proyecto

Para crear un nuevo proyecto django, nos colocamos en la carpeta donde se encuentra el virtual environment y escribimos en terminal el siguiente comando:

<code>django-admin startproject canjesmarcaspropiasbackend</code>

Le damos permisos a la carpeta del proyecto

<code>chmod 777 -R canjesmarcaspropiasbackend</code>

### 6. Agregando archivo local_settings.py



## AMBIENTE QA

### 1. Datos para conectar con el sistema gestor de base de datos en el servidor
- Host: 172.16.2.153
- Puerto: 5432
- Username: desarrollo
- Password: 1nfr42018

### 2. Conectando al servidor

Para conectarnos al servidor por secure shell utilizamos el siguiente comando:
<code>ssh infra@172.16.2.223</code>

### 3. Despliegue con Nginx

Estando dentro del servidor, nos vamos a la carpeta /html y clonamos nuestro proyecto de django que fue previamente subido a un repositorio privado en Github:

<code>cd /var/www/html/</code>

<code>git clone https://github.com/PaolaMolinaZeron/canjesmarcaspropiasbackend.git</code>

Luego nos vamos a la carpeta de entornos y en ella creamos un entorno virtual de la misma forma y con las mismas dependencias del entorno local.

<code>cd /var/www/html/Entornos/</code>

<code>python3 -m venv CANJESMARCASPROPIAS</code>

## AMBIENTE PRODUCCION

### 1. Datos para conectar con el sistema gestor de base de datos en el servidor
- Host: 172.16.2.217
- Puerto: 5432
- Username: desarrollo
- Password: 1nfr42018


2:37