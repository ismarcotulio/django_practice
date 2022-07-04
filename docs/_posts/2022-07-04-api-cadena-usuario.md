---
layout: post
title: "APIs para el registro de usuarios en Cadena"
subtitle: 'Documentacion utilizando Open API Estandar version 2'
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
text-transform: uppercase;
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

.up {
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
<div class="app-desc">Esta es una descripcion de las APIs de Usuario que se encuentran en el servidor backend del proyecto Canjes de Marcas Propias propiedad de Farinter. Las peticiones se pueden realizar al servidor de calidad cuya direccion es:
<a href="http://172.16.2.223:8088/api/">http://172.16.2.223:8088/api/</a>.</div>
<div class="app-desc">Informacion de contacto: <a href="marco.ruiz@farinter.com">marco.ruiz@farinter.com</a></div>
<div class="app-desc">Version: 1.0.0</div>

## <a name="__Methods">Metodos</a>
[ Jump to <a href="#__Models">Modelos</a> ]

<b>Tabla de contenido </b>
<div class="method-summary"></div>
Roles
<ul>
<li><a href="#cadenasGet"><code><span class="http-method">get</span> /cadenas</code></a></li>
<li><a href="#rolesGet"><code><span class="http-method">get</span> /roles</code></a></li>
</ul>
Usuarios
<ul>
<li><a href="#usuariosGet"><code><span class="http-method">get</span> /usuarios</code></a></li>
<li><a href="#usuariosUsuariosIdGet"><code><span class="http-method">get</span> /usuarios/{usuariosId}</code></a></li>
</ul>
Usuarioxperfilxcadena
<ul>
<li><a href="#usuarioxperfilxcadenaPost"><code><span class="http-method">post</span> /usuarioxperfilxcadena</code></a></li>
</ul>

# <a name="Roles">Roles</a>
<div class="method"><a name="cadenasGet"/>
<div class="method-path">
<a class="up" href="#__Methods">Up</a>
<pre class="get"><code class="huge"><span class="http-method">get</span> /cadenas</code></pre></div>
<div class="method-summary">Devuelve las cadenas del sistema (<span class="nickname">cadenasGet</span>)</div>
<div class="method-notes">Se obtienen determinadas cadenas de acuerdo a un parametro indicado o sin el.</div>





<b>Query parameters</b>
<div class="field-items">
<div class="param">usuario (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> &mdash; Este parametro se envia en conjunto con el parametro &quot;perfil&quot; para retornar cadenas en las que no se ah registrado con un rol en especifico un usuario. </div><div class="param">perfil (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> &mdash; Este parametro se envia en conjunto con el parametro &quot;usuario&quot; para retornar cadenas en las que no se ah registrado con un rol en especifico un usuario. </div>
</div>  <!-- field-items -->


<b>Retornar tipo</b>
<div class="return-type">
array[<a href="#Cadenas">Cadenas</a>]

</div>

<!--Todo: process Response Object and its headers, schema, examples -->

<b>Datos de ejemplo</b>
<div class="example-data-content-type">Content-Type: application/json</div>
<pre class="example"><code>{}</code></pre>
<b>Datos de ejemplo</b>
<div class="example-data-content-type">Content-Type: application/xml</div>
<pre class="example"><code><Roles>
<id>123456789</id>
<nombre>aeiou</nombre>
<fecha_creacion>2000-01-23T04:56:07.000Z</fecha_creacion>
<pais>123</pais>
</Roles></code></pre>

<b>Produce</b>
Esta API produce los siguientes tipos de datos al <span class="header">Accept</span> request header;
the media type will be conveyed by the <span class="header">Content-Type</span> response header.
<ul>
<li><code>application/json</code></li>
<li><code>application/xml</code></li>
</ul>

<b>Respuestas</b>
200
Operacion exitosa

</div> <!-- method -->
<hr/>
<div class="method"><a name="rolesGet"/>
<div class="method-path">
<a class="up" href="#__Methods">Up</a>
<pre class="get"><code class="huge"><span class="http-method">get</span> /roles</code></pre></div>
<div class="method-summary">Devuelve los roles de usuario en el sistema (<span class="nickname">rolesGet</span>)</div>
<div class="method-notes">Se obtienen determinados roles de acuerdo a un parametro indicado o sin el.</div>





<b>Query parameters</b>
<div class="field-items">
<div class="param">cadena (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> &mdash; Permite retornar los roles que estan relacionados unicamente con el modulo de Cadena. </div>
</div>  <!-- field-items -->


<b>Retornar tipo</b>
<div class="return-type">
array[<a href="#Roles">Roles</a>]

</div>

<!--Todo: process Response Object and its headers, schema, examples -->

<b>Datos de ejemplo</b>
<div class="example-data-content-type">Content-Type: application/json</div>
<pre class="example"><code>{}</code></pre>
<b>Datos de ejemplo</b>
<div class="example-data-content-type">Content-Type: application/xml</div>
<pre class="example"><code><Roles>
<id>123456789</id>
<name>aeiou</name>
</Roles></code></pre>

<b>Produce</b>
Esta API produce los siguientes tipos de datos al <span class="header">Accept</span> request header;
the media type will be conveyed by the <span class="header">Content-Type</span> response header.
<ul>
<li><code>application/json</code></li>
<li><code>application/xml</code></li>
</ul>

<b>Respuestas</b>
200
Operacion exitosa

</div> <!-- method -->
<hr/>
# <a name="Usuarios">Usuarios</a>
<div class="method"><a name="usuariosGet"/>
<div class="method-path">
<a class="up" href="#__Methods">Up</a>
<pre class="get"><code class="huge"><span class="http-method">get</span> /usuarios</code></pre></div>
<div class="method-summary">Devuelve los usuarios del sistema (<span class="nickname">usuariosGet</span>)</div>
<div class="method-notes">Se obtienen determinados usuarios de acuerdo a un parametro indicado o sin el.</div>





<b>Query parameters</b>
<div class="field-items">
<div class="param">limit (optional)</div>

<div class="param-desc"><span class="param-type">Query Parameter</span> &mdash; Permite retornar un limite de usuarios por peticion. format: int64</div>
</div>  <!-- field-items -->


<b>Retornar tipo</b>
<div class="return-type">
array[<a href="#Usuario">Usuario</a>]

</div>

<!--Todo: process Response Object and its headers, schema, examples -->

<b>Datos de ejemplo</b>
<div class="example-data-content-type">Content-Type: application/json</div>
<pre class="example"><code>{}</code></pre>
<b>Datos de ejemplo</b>
<div class="example-data-content-type">Content-Type: application/xml</div>
<pre class="example"><code><Usuario>
<id>123456789</id>
<groups_list>
</groups_list>
<password>aeiou</password>
<last_login>2000-01-23T04:56:07.000Z</last_login>
<is_superuser>true</is_superuser>
<username>aeiou</username>
<first_name>aeiou</first_name>
<last_name>aeiou</last_name>
<email>aeiou</email>
<is_staff>true</is_staff>
<is_active>true</is_active>
<date_joined>2000-01-23T04:56:07.000Z</date_joined>
<groups>
<groups>123</groups>
</groups>
<user_permissions>
<user_permissions>aeiou</user_permissions>
</user_permissions>
</Usuario></code></pre>

<b>Produce</b>
Esta API produce los siguientes tipos de datos al <span class="header">Accept</span> request header;
the media type will be conveyed by the <span class="header">Content-Type</span> response header.
<ul>
<li><code>application/json</code></li>
<li><code>application/xml</code></li>
</ul>

<b>Respuestas</b>
200
Operacion exitosa

</div> <!-- method -->
<hr/>
<div class="method"><a name="usuariosUsuariosIdGet"/>
<div class="method-path">
<a class="up" href="#__Methods">Up</a>
<pre class="get"><code class="huge"><span class="http-method">get</span> /usuarios/{usuariosId}</code></pre></div>
<div class="method-summary">Encuentra usuarios segun su Id (<span class="nickname">usuariosUsuariosIdGet</span>)</div>
<div class="method-notes">Retorna un solo usuario</div>

<b>Path parameters</b>
<div class="field-items">
<div class="param">usuariosId (required)</div>

<div class="param-desc"><span class="param-type">Path Parameter</span> &mdash; ID del usuario a retornar format: int64</div>
</div>  <!-- field-items -->






<b>Retornar tipo</b>
<div class="return-type">
<a href="#Usuario">Usuario</a>

</div>

<!--Todo: process Response Object and its headers, schema, examples -->

<b>Datos de ejemplo</b>
<div class="example-data-content-type">Content-Type: application/json</div>
<pre class="example"><code>{"empty": false}</code></pre>
<b>Datos de ejemplo</b>
<div class="example-data-content-type">Content-Type: application/xml</div>
<pre class="example"><code><Usuario>
<id>123456789</id>
<groups_list>
</groups_list>
<password>aeiou</password>
<last_login>2000-01-23T04:56:07.000Z</last_login>
<is_superuser>true</is_superuser>
<username>aeiou</username>
<first_name>aeiou</first_name>
<last_name>aeiou</last_name>
<email>aeiou</email>
<is_staff>true</is_staff>
<is_active>true</is_active>
<date_joined>2000-01-23T04:56:07.000Z</date_joined>
<groups>
<groups>123</groups>
</groups>
<user_permissions>
<user_permissions>aeiou</user_permissions>
</user_permissions>
</Usuario></code></pre>

<b>Produce</b>
Esta API produce los siguientes tipos de datos al <span class="header">Accept</span> request header;
the media type will be conveyed by the <span class="header">Content-Type</span> response header.
<ul>
<li><code>application/json</code></li>
<li><code>application/xml</code></li>
</ul>

<b>Respuestas</b>
200
Operacion exitosa
<a href="#Usuario">Usuario</a>
400
Invalid ID supplied
<a href="#"></a>
404
Pet not found
<a href="#"></a>
</div> <!-- method -->
<hr/>
# <a name="Usuarioxperfilxcadena">Usuarioxperfilxcadena</a>
<div class="method"><a name="usuarioxperfilxcadenaPost"/>
<div class="method-path">
<a class="up" href="#__Methods">Up</a>
<pre class="post"><code class="huge"><span class="http-method">post</span> /usuarioxperfilxcadena</code></pre></div>
<div class="method-summary">Registra a un usuario en cadena con un rol especifico. (<span class="nickname">usuarioxperfilxcadenaPost</span>)</div>
<div class="method-notes"></div>


<b>Consumes</b>
This API call consumes the following media types via the <span class="header">Content-Type</span> request header:
<ul>
<li><code>application/json</code></li>
</ul>

<b>Request body</b>
<div class="field-items">
<div class="param">usuarioxperfilxcadena <a href="#UsuarioxPerfilxCadena">UsuarioxPerfilxCadena</a> (optional)</div>

<div class="param-desc"><span class="param-type">Body Parameter</span> &mdash; Datos de registro. </div>

</div>  <!-- field-items -->





<!--Todo: process Response Object and its headers, schema, examples -->



<b>Respuestas</b>
201
Created
<a href="#"></a>
</div> <!-- method -->
<hr/>

## <a name="__Models">Models</a>
[ Jump to <a href="#__Methods">Methods</a> ]

<h3>Tabla de contenidos</h3>
<ol>
<li><a href="#ApiResponse"><code>ApiResponse</code> - </a></li>
<li><a href="#Cadenas"><code>Cadenas</code> - </a></li>
<li><a href="#Group"><code>Group</code> - </a></li>
<li><a href="#Roles"><code>Roles</code> - </a></li>
<li><a href="#Usuario"><code>Usuario</code> - </a></li>
<li><a href="#UsuarioxPerfilxCadena"><code>UsuarioxPerfilxCadena</code> - </a></li>
</ol>

<div class="model">
<h3><a name="ApiResponse"><code>ApiResponse</code> - </a> <a class="up" href="#__Models">Up</a></h3>
<div class='model-description'></div>
<div class="field-items">
<div class="param">code (optional)</div><div class="param-desc"><span class="param-type"><a href="#integer">Integer</a></span>  format: int32</div>
<div class="param">type (optional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">message (optional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
</div>  <!-- field-items -->
</div>
<div class="model">
<h3><a name="Cadenas"><code>Cadenas</code> - </a> <a class="up" href="#__Models">Up</a></h3>
<div class='model-description'></div>
<div class="field-items">
<div class="param">id (optional)</div><div class="param-desc"><span class="param-type"><a href="#long">Long</a></span>  format: int64</div>
<div class="param">nombre (optional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">fecha_creacion (optional)</div><div class="param-desc"><span class="param-type"><a href="#DateTime">Date</a></span>  format: date-time</div>
<div class="param">pais (optional)</div><div class="param-desc"><span class="param-type"><a href="#integer">Integer</a></span>  </div>
</div>  <!-- field-items -->
</div>
<div class="model">
<h3><a name="Group"><code>Group</code> - </a> <a class="up" href="#__Models">Up</a></h3>
<div class='model-description'></div>
<div class="field-items">
<div class="param">id (optional)</div><div class="param-desc"><span class="param-type"><a href="#long">Long</a></span>  format: int64</div>
<div class="param">name (optional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
</div>  <!-- field-items -->
</div>
<div class="model">
<h3><a name="Roles"><code>Roles</code> - </a> <a class="up" href="#__Models">Up</a></h3>
<div class='model-description'></div>
<div class="field-items">
<div class="param">id (optional)</div><div class="param-desc"><span class="param-type"><a href="#long">Long</a></span>  format: int64</div>
<div class="param">name (optional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
</div>  <!-- field-items -->
</div>
<div class="model">
<h3><a name="Usuario"><code>Usuario</code> - </a> <a class="up" href="#__Models">Up</a></h3>
<div class='model-description'></div>
<div class="field-items">
<div class="param">id (optional)</div><div class="param-desc"><span class="param-type"><a href="#long">Long</a></span>  format: int64</div>
<div class="param">groups_list (optional)</div><div class="param-desc"><span class="param-type"><a href="#Group">array[Group]</a></span>  </div>
<div class="param">password (optional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">last_login (optional)</div><div class="param-desc"><span class="param-type"><a href="#DateTime">Date</a></span>  format: date-time</div>
<div class="param">is_superuser (optional)</div><div class="param-desc"><span class="param-type"><a href="#boolean">Boolean</a></span>  </div>
<div class="param">username (optional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">first_name (optional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">last_name (optional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">email (optional)</div><div class="param-desc"><span class="param-type"><a href="#string">String</a></span>  </div>
<div class="param">is_staff (optional)</div><div class="param-desc"><span class="param-type"><a href="#boolean">Boolean</a></span>  </div>
<div class="param">is_active (optional)</div><div class="param-desc"><span class="param-type"><a href="#boolean">Boolean</a></span>  </div>
<div class="param">date_joined (optional)</div><div class="param-desc"><span class="param-type"><a href="#DateTime">Date</a></span>  format: date-time</div>
<div class="param">groups (optional)</div><div class="param-desc"><span class="param-type"><a href="#integer">array[Integer]</a></span>  </div>
<div class="param">user_permissions (optional)</div><div class="param-desc"><span class="param-type"><a href="#string">array[String]</a></span>  </div>
</div>  <!-- field-items -->
</div>
<div class="model">
<h3><a name="UsuarioxPerfilxCadena"><code>UsuarioxPerfilxCadena</code> - </a> <a class="up" href="#__Models">Up</a></h3>
<div class='model-description'></div>
<div class="field-items">
<div class="param">id (optional)</div><div class="param-desc"><span class="param-type"><a href="#long">Long</a></span>  format: int64</div>
<div class="param">cadena (optional)</div><div class="param-desc"><span class="param-type"><a href="#integer">Integer</a></span>  </div>
<div class="param">usuario (optional)</div><div class="param-desc"><span class="param-type"><a href="#integer">Integer</a></span>  </div>
<div class="param">perfil (optional)</div><div class="param-desc"><span class="param-type"><a href="#integer">Integer</a></span>  </div>
</div>  <!-- field-items -->
</div>