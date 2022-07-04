---
layout: post
title: "APIS PARA EL REGISTRO DE USUARIOS EN DISTRIBUIDORES"
subtitle: 'Documentacion utilizando el estandar Open API Specification version 2'
author: "Marco Tulio Ruiz"
header-style: text
tags:
- apis
- open api specification
- backend
---
<style type="text/css">
body {
font-family: Trebuchet MS, sans-serif;
font-size: 15px;
color: #444;
margin-right: 24px;
}

h1	{
font-size: 25px;
}
h2	{
font-size: 20px;
}
h3	{
font-size: 16px;
font-weight: bold;
}
hr	{
height: 1px;
border: 0;
color: #ddd;
background-color: #ddd;
}

.app-desc {
clear: both;
margin-left: 20px;
}
.param-name {
width: 100%;
}
.license-info {
margin-left: 20px;
}

.license-url {
margin-left: 20px;
}

.model {
margin: 0 0 0px 20px;
}

.method {
margin-left: 20px;
}

.method-notes	{
margin: 10px 0 20px 0;
font-size: 90%;
color: #555;
}

pre {
padding: 10px;
margin-bottom: 2px;
}

.http-method {
text-transform: Arribapercase;
}

pre.get {
background-color: #0f6ab4;
}

pre.post {
background-color: #10a54a;
}

pre.put {
background-color: #c5862b;
}

pre.delete {
background-color: #a41e22;
}

.huge	{
color: #fff;
}

pre.example {
background-color: #f3f3f3;
padding: 10px;
border: 1px solid #ddd;
}

code {
white-space: pre;
}

.nickname {
font-weight: bold;
}

.method-path {
font-size: 1.5em;
background-color: #0f6ab4;
}

.Arriba {
float:right;
}

.parameter {
width: 500px;
}

.param {
width: 500px;
padding: 10px 0 0 20px;
font-weight: bold;
}

.param-desc {
width: 700px;
padding: 0 0 0 20px;
color: #777;
}

.param-type {
font-style: italic;
}

.param-enum-header {
width: 700px;
padding: 0 0 0 60px;
color: #777;
font-weight: bold;
}

.param-enum {
width: 700px;
padding: 0 0 0 80px;
color: #777;
font-style: italic;
}

.field-label {
padding: 0;
margin: 0;
clear: both;
}

.field-items	{
padding: 0 0 15px 0;
margin-bottom: 15px;
}

.return-type {
clear: both;
padding-bottom: 10px;
}

.param-header {
font-weight: bold;
}

.method-tags {
text-align: right;
}

.method-tag {
background: none repeat scroll 0% 0% #24A600;
border-radius: 3px;
padding: 2px 10px;
margin: 2px;
color: #FFF;
display: inline-block;
text-decoration: none;
}

</style>
<div class="app-desc">Esta es una descripcion de las APIs necesarias para registrar un usuario en distribuidores los cuales se encuentran en el servidor backend del proyecto Canjes de Marcas Propias propiedad de Farinter. Las peticiones se pueden realizar al servidor de calidad cuya direccion es:
<a href="http://172.16.2.223:8088/api/">http://172.16.2.223:8088/api/</a>.</div>
<div class="app-desc">Informacion de contacto: <a href="marco.ruiz@farinter.com">marco.ruiz@farinter.com</a></div>
<div class="app-desc">Version: 1.0.0</div>


## <a name="__Methods">Metodos</a>
[ Saltar a <a href="#__Models">Modelos</a> ]

### Tabla de Contenidos
<div class="method-summary"></div>

#### <a href="#Distribuidores">Distribuidores</a>
<ul>
<li><a href="#distribuidoresGet"><code><span class="http-method">get</span> /distribuidores</code></a></li>
</ul>

#### <a href="#Roles">Roles</a>
<ul>
<li><a href="#rolesGet"><code><span class="http-method">get</span> /roles</code></a></li>
</ul>

#### <a href="#Usuarios">Usuarios</a>
<ul>
<li><a href="#usuariosGet"><code><span class="http-method">get</span> /usuarios</code></a></li>
<li><a href="#usuariosUsuariosIdGet"><code><span class="http-method">get</span> /usuarios/{usuariosId}</code></a></li>
</ul>

#### <a href="#Usuarioxperfilxdistribuidor">Usuarioxperfilxdistribuidor</a>
<ul>
<li><a href="#usuarioxperfilxdistribuidorPost"><code><span class="http-method">post</span> /usuarioxperfilxdistribuidor</code></a></li>
</ul>

# <a name="Distribuidores">Distribuidores</a>
<div class="method"><a name="distribuidoresGet"/>
<div class="method-path">
<a class="Arriba" href="#__Methods">Arriba</a>
<pre class="get"><code class="huge"><span class="http-method">get</span> /distribuidores</code></pre></div>
<div class="method-summary">Devuelve los distribuidores registrados en el sistema (<span class="nickname">distribuidoresGet</span>)</div>
<div class="method-notes">Se obtienen determinados distribuidores registrados de acuerdo a un parametro indicado o sin el.</div>

<b class="field-label">Consulta de Parametros</b>
<div class="field-items">
<div class="param">usuario (opcional)</div>

<div class="param-desc"><span class="param-type">Parametros de Consulta</span> &mdash; Este parametro se envia en conjunto con el parametro &quot;perfil&quot; para retornar distribuidores en los que no se ah registrado con un rol en especifico un usuario. </div><div class="param">perfil (opcional)</div>

<div class="param-desc"><span class="param-type">Parametros de Consulta</span> &mdash; Este parametro se envia en conjunto con el parametro &quot;usuario&quot; para retornar distribuidores en los que no se ah registrado con un rol en especifico un usuario. </div>
</div>  <!-- field-items -->


<b class="field-label">Retornar tipo</b>
<div class="return-type">
array[<a href="#Distribuidores">Distribuidores</a>]

</div>

<!--Todo: process Respuesta Object and its headers, schema, examples -->

<h3 class="field-label">Datos de ejemplo</h3>
<div class="example-data-content-type">Content-Type: application/json</div>
<pre class="example"><code>{}</code></pre>
<h3 class="field-label">Datos de ejemplo</h3>
<div class="example-data-content-type">Content-Type: application/xml</div>
<pre class="example"><code><Roles>
<id>123456789</id>
<nombre>aeiou</nombre>
<fecha_creacion>2000-01-23T04:56:07.000Z</fecha_creacion>
<pais>123</pais>
</Roles></code></pre>

<h3 class="field-label">produccion</h3>
El llamado de esta API produce los siguientes tipos de datos de acuerdo al <span class="header">Accept</span> request header;
 <span class="header">Content-Type</span> Respuesta header.
<ul>
<li><code>application/json</code></li>
<li><code>application/xml</code></li>
</ul>

<h3 class="field-label">Respuestas</h3>
<h4 class="field-label">200</h4>
Operacion exitosa

</div> <!-- method -->
<hr/>

# Roles</a>
<div class="method"><a name="rolesGet"/>
<div class="method-path">
<a class="Arriba" href="#__Methods">Arriba</a>
<pre class="get"><code class="huge"><span class="http-method">get</span> /roles</code></pre></div>
<div class="method-summary">Devuelve los roles de usuario en el sistema (<span class="nickname">rolesGet</span>)</div>
<div class="method-notes">Se obtienen determinados roles de acuerdo a un parametro indicado o sin el.</div>





<h3 class="field-label">Parametros de Consulta</h3>
<div class="field-items">
<div class="param">distribuidor (opcional)</div>

<div class="param-desc"><span class="param-type">Parametros de Consulta</span> &mdash; Permite retornar los roles que estan relacionados unicamente con el modulo de Distribuidor. </div>
</div>  <!-- field-items -->


<h3 class="field-label">Tipo de retorno</h3>
<div class="return-type">
array[<a href="#Roles">Roles</a>]

</div>

<!--Todo: process Respuesta Object and its headers, schema, examples -->

<h3 class="field-label">Datos de ejemplo</h3>
<div class="example-data-content-type">Content-Type: application/json</div>
<pre class="example"><code>{}</code></pre>
<h3 class="field-label">Datos de ejemplo</h3>
<div class="example-data-content-type">Content-Type: application/xml</div>
<pre class="example"><code><Roles>
<id>123456789</id>
<name>aeiou</name>
</Roles></code></pre>

<h3 class="field-label">produccion</h3>
El llamado de esta API produce los siguientes tipos de datos de acuerdo al <span class="header">Accept</span> request header;
 <span class="header">Content-Type</span> Respuesta header.
<ul>
<li><code>application/json</code></li>
<li><code>application/xml</code></li>
</ul>

<h3 class="field-label">Respuestas</h3>
<h4 class="field-label">200</h4>
Operacion exitosa

</div> <!-- method -->
<hr/>
# Usuarios</a>
<div class="method"><a name="usuariosGet"/>
<div class="method-path">
<a class="Arriba" href="#__Methods">Arriba</a>
<pre class="get"><code class="huge"><span class="http-method">get</span> /usuarios</code></pre></div>
<div class="method-summary">Devuelve los usuarios del sistema (<span class="nickname">usuariosGet</span>)</div>
<div class="method-notes">Se obtienen determinados usuarios de acuerdo a un parametro indicado o sin el.</div>





<h3 class="field-label">Parametros de Consulta</h3>
<div class="field-items">
<div class="param">limit (opcional)</div>

<div class="param-desc"><span class="param-type">Parametros de Consulta</span> &mdash; Permite retornar un limite de usuarios por peticion. format: int64</div>
</div>  <!-- field-items -->


<h3 class="field-label">Tipo de retorno</h3>
<div class="return-type">
array[<a href="#Usuario">Usuario</a>]

</div>

<!--Todo: process Respuesta Object and its headers, schema, examples -->

<h3 class="field-label">Datos de ejemplo</h3>
<div class="example-data-content-type">Content-Type: application/json</div>
<pre class="example"><code>{}</code></pre>
<h3 class="field-label">Datos de ejemplo</h3>
<div class="example-data-content-type">Content-Type: application/xml</div>
<pre class="example"><code><Usuario>
<id>123456789</id>
<groArribas_list>
</groArribas_list>
<password>aeiou</password>
<last_login>2000-01-23T04:56:07.000Z</last_login>
<is_sArribaeruser>true</is_sArribaeruser>
<username>aeiou</username>
<first_name>aeiou</first_name>
<last_name>aeiou</last_name>
<email>aeiou</email>
<is_staff>true</is_staff>
<is_active>true</is_active>
<date_joined>2000-01-23T04:56:07.000Z</date_joined>
<groArribas>
<groArribas>123</groArribas>
</groArribas>
<user_permissions>
<user_permissions>aeiou</user_permissions>
</user_permissions>
</Usuario></code></pre>

<h3 class="field-label">produccion</h3>
El llamado de esta API produce los siguientes tipos de datos de acuerdo al <span class="header">Accept</span> request header;
 <span class="header">Content-Type</span> Respuesta header.
<ul>
<li><code>application/json</code></li>
<li><code>application/xml</code></li>
</ul>

<h3 class="field-label">Respuestas</h3>
<h4 class="field-label">200</h4>
Operacion exitosa

</div> <!-- method -->
<hr/>
<div class="method"><a name="usuariosUsuariosIdGet"/>
<div class="method-path">
<a class="Arriba" href="#__Methods">Arriba</a>
<pre class="get"><code class="huge"><span class="http-method">get</span> /usuarios/{usuariosId}</code></pre></div>
<div class="method-summary">Encuentra usuarios segun su Id (<span class="nickname">usuariosUsuariosIdGet</span>)</div>
<div class="method-notes">Retorna un solo usuario</div>

<h3 class="field-label">Parametros de ruta</h3>
<div class="field-items">
<div class="param">usuariosId (required)</div>

<div class="param-desc"><span class="param-type">Parametros de ruta</span> &mdash; ID del usuario a retornar format: int64</div>
</div>  <!-- field-items -->






<h3 class="field-label">Tipo de retorno</h3>
<div class="return-type">
<a href="#Usuario">Usuario</a>

</div>

<!--Todo: process Respuesta Object and its headers, schema, examples -->

<h3 class="field-label">Datos de ejemplo</h3>
<div class="example-data-content-type">Content-Type: application/json</div>
<pre class="example"><code>{"empty": false}</code></pre>
<h3 class="field-label">Datos de ejemplo</h3>
<div class="example-data-content-type">Content-Type: application/xml</div>
<pre class="example"><code><Usuario>
<id>123456789</id>
<groArribas_list>
</groArribas_list>
<password>aeiou</password>
<last_login>2000-01-23T04:56:07.000Z</last_login>
<is_sArribaeruser>true</is_sArribaeruser>
<username>aeiou</username>
<first_name>aeiou</first_name>
<last_name>aeiou</last_name>
<email>aeiou</email>
<is_staff>true</is_staff>
<is_active>true</is_active>
<date_joined>2000-01-23T04:56:07.000Z</date_joined>
<groArribas>
<groArribas>123</groArribas>
</groArribas>
<user_permissions>
<user_permissions>aeiou</user_permissions>
</user_permissions>
</Usuario></code></pre>

<h3 class="field-label">produccion</h3>
El llamado de esta API produce los siguientes tipos de datos de acuerdo al <span class="header">Accept</span> request header;
 <span class="header">Content-Type</span> Respuesta header.
<ul>
<li><code>application/json</code></li>
<li><code>application/xml</code></li>
</ul>

<h3 class="field-label">Respuestas</h3>
<h4 class="field-label">200</h4>
Operacion exitosa
<a href="#Usuario">Usuario</a>
<h4 class="field-label">400</h4>
Invalid ID sArribaplied
<a href="#"></a>
<h4 class="field-label">404</h4>
Pet not found
<a href="#"></a>
</div> <!-- method -->
<hr/>
# Usuarioxperfilxdistribuidor</a>
<div class="method"><a name="usuarioxperfilxdistribuidorPost"/>
<div class="method-path">
<a class="Arriba" href="#__Methods">Arriba</a>
<pre class="post"><code class="huge"><span class="http-method">post</span> /usuarioxperfilxdistribuidor</code></pre></div>
<div class="method-summary">Registra a un usuario en distribuidor con un rol especifico. (<span class="nickname">usuarioxperfilxdistribuidorPost</span>)</div>
<div class="method-notes"></div>


<h3 class="field-label">Consumo</h3>
This API call Consumo the following media types via the <span class="header">Content-Type</span> request header:
<ul>
<li><code>application/json</code></li>
</ul>

<h3 class="field-label">Cuerpo de la peticion</h3>
<div class="field-items">
<div class="param">usuarioxperfilxdistribuidor <a href="#UsuarioxPerfilxDistribuidor">UsuarioxPerfilxDistribuidor</a> (opcional)</div>

<div class="param-desc"><span class="param-type">Parametro de cuerpo</span> &mdash; Datos de registro. </div>

</div>  <!-- field-items -->





<!--Todo: process Respuesta Object and its headers, schema, examples -->



<h3 class="field-label">Respuestas</h3>
<h4 class="field-label">201</h4>
Created
<a href="#"></a>
</div> <!-- method -->
<hr/>

<h2><a name="__Models">Modelos</a></h2>
[ Saltar a <a href="#__Methods">Methods</a> ]

<h3>Tabla de contenido</h3>
<ol>
<li><a href="#Distribuidores"><code>Distribuidores</code> - </a></li>
<li><a href="#GroArriba"><code>GroArriba</code> - </a></li>
<li><a href="#Roles"><code>Roles</code> - </a></li>
<li><a href="#Usuario"><code>Usuario</code> - </a></li>
<li><a href="#UsuarioxPerfilxDistribuidor"><code>UsuarioxPerfilxDistribuidor</code> - </a></li>
</ol>

<div class="model">
<h3><a name="Distribuidores"><code>Distribuidores</code> - </a> <a class="Arriba" href="#__Models">Arriba</a></h3>
<div class='model-description'></div>
<div class="field-items">
<div class="param">id (opcional)</div><div class="param-desc"><span class="param-type"><a href="#long">Long</a></span>  format: int64</div>
<div class="param">nombre (opcional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">fecha_creacion (opcional)</div><div class="param-desc"><span class="param-type"><a href="#DateTime">Date</a></span>  format: date-time</div>
<div class="param">pais (opcional)</div><div class="param-desc"><span class="param-type"><a href="#integer">Integer</a></span>  </div>
</div>  <!-- field-items -->
</div>
<div class="model">
<h3><a name="GroArriba"><code>GroArriba</code> - </a> <a class="Arriba" href="#__Models">Arriba</a></h3>
<div class='model-description'></div>
<div class="field-items">
<div class="param">id (opcional)</div><div class="param-desc"><span class="param-type"><a href="#long">Long</a></span>  format: int64</div>
<div class="param">name (opcional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
</div>  <!-- field-items -->
</div>
<div class="model">
<h3><a name="Roles"><code>Roles</code> - </a> <a class="Arriba" href="#__Models">Arriba</a></h3>
<div class='model-description'></div>
<div class="field-items">
<div class="param">id (opcional)</div><div class="param-desc"><span class="param-type"><a href="#long">Long</a></span>  format: int64</div>
<div class="param">name (opcional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
</div>  <!-- field-items -->
</div>
<div class="model">
<h3><a name="Usuario"><code>Usuario</code> - </a> <a class="Arriba" href="#__Models">Arriba</a></h3>
<div class='model-description'></div>
<div class="field-items">
<div class="param">id (opcional)</div><div class="param-desc"><span class="param-type"><a href="#long">Long</a></span>  format: int64</div>
<div class="param">groArribas_list (opcional)</div><div class="param-desc"><span class="param-type"><a href="#GroArriba">array[GroArriba]</a></span>  </div>
<div class="param">password (opcional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">last_login (opcional)</div><div class="param-desc"><span class="param-type"><a href="#DateTime">Date</a></span>  format: date-time</div>
<div class="param">is_sArribaeruser (opcional)</div><div class="param-desc"><span class="param-type"><a href="#boolean">Boolean</a></span>  </div>
<div class="param">username (opcional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">first_name (opcional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">last_name (opcional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">email (opcional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">is_staff (opcional)</div><div class="param-desc"><span class="param-type"><a href="#boolean">Boolean</a></span>  </div>
<div class="param">is_active (opcional)</div><div class="param-desc"><span class="param-type"><a href="#boolean">Boolean</a></span>  </div>
<div class="param">date_joined (opcional)</div><div class="param-desc"><span class="param-type"><a href="#DateTime">Date</a></span>  format: date-time</div>
<div class="param">groArribas (opcional)</div><div class="param-desc"><span class="param-type"><a href="#integer">array[Integer]</a></span>  </div>
<div class="param">user_permissions (opcional)</div><div class="param-desc"><span class="param-type"><a href="#string">array[String]</a></span>  </div>
</div>  <!-- field-items -->
</div>
<div class="model">
<h3><a name="UsuarioxPerfilxDistribuidor"><code>UsuarioxPerfilxDistribuidor</code> - </a> <a class="Arriba" href="#__Models">Arriba</a></h3>
<div class='model-description'></div>
<div class="field-items">
<div class="param">id (opcional)</div><div class="param-desc"><span class="param-type"><a href="#long">Long</a></span>  format: int64</div>
<div class="param">distribuidor (opcional)</div><div class="param-desc"><span class="param-type"><a href="#integer">Integer</a></span>  </div>
<div class="param">usuario (opcional)</div><div class="param-desc"><span class="param-type"><a href="#integer">Integer</a></span>  </div>
<div class="param">perfil (opcional)</div><div class="param-desc"><span class="param-type"><a href="#integer">Integer</a></span>  </div>
</div>  <!-- field-items -->
</div>