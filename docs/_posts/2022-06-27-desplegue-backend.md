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

1:08

