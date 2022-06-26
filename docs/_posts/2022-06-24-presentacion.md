---
layout: post
title: "PROYECTO AUTOMATIZACIÓN DE CANJES PARA MARCAS PROPIAS"
subtitle: 'Presentacion de flujo y diseño de pantallas'
author: "Paola Molina, Joaquin valladares, Genesis Aceituno y Marco Tulio Ruiz"
header-style: text
tags:
  - mockups
  - diagramas
  - diseño
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
El presente documento tiene por finalidad mostrar el diagrama de flujo de proceso y diseño de la aplicación web para la plataforma de Automatización de Canjes de Marcas Propias (Swissfarm-Vitotal) para que los clientes registrados al mismo tengan el beneficio de canjes con los laboratorios, para ello se adjunta las imágenes de cada pantalla del proceso y una breve explicación de las mismas.  

## DIAGRAMA DE FLUJO PRINCIPAL
<img src="{{site.baseurl}}/img/1.1.png" class="pantalla">

## PLATAFORMA CADENA - ADMINISTRACION
<img src="{{site.baseurl}}/img/1.2.png" class="pantalla">

### Proceso de pedidos rechazados
<img src="{{site.baseurl}}/img/1.3.png" class="proceso">

## PLATAFORMA CADENA - PUNTO DE VENTA
<img src="{{site.baseurl}}/img/1.4.png" class="pantalla">

### Proceso de Emision de Boleta
<img src="{{site.baseurl}}/img/1.5.png" class="proceso">

### Proceso de Registro de Canje
<img src="{{site.baseurl}}/img/1.6.png" class="proceso">

### Proceso de Registro de Compra
<img src="{{site.baseurl}}/img/1.7.png" class="proceso">

### Proceso de Reversion de Compra
<img src="{{site.baseurl}}/img/1.8.png" class="proceso">

## PLATAFORMA DEL DISTRIBUIDOR
<img src="{{site.baseurl}}/img/1.9.png" class="pantalla">

## PLATAFORMA DEL LABORATORIO
<img src="{{site.baseurl}}/img/1.10.png" class="pantalla">

## PANTALLAS DE USUARIO

### 1. Inicio de sesion.
<img src="{{site.baseurl}}/img/1.11.jpg" class="pantalla">

### 2. Recuperar contraseña.
<img src="{{site.baseurl}}/img/1.12.jpg" class="pantalla">

### 3. Menu.
<img src="{{site.baseurl}}/img/1.13.jpg" class="pantalla">
<b>Nota</b>: El menú puede variar de acuerdo al perfil del usuario.

## PANTALLAS PARA LA ADMINISTRACIÓN DE PUNTOS DE VENTA
### 1. Registro de Compras.
<img src="{{site.baseurl}}/img/1.14.jpg" class="pantalla">
<b>Funcionalidad</b>: Esta pantalla se utilizará para realizar el registro de la compra cuando el cliente se presente al punto de venta con la factura en mano. La factura se le mostrará al personal de punto de venta, este a su vez le solicitará al cliente su número de identidad, el cual se deberá introducir en el campo de identificación. Luego al presionar enter desplegará la información del nombre del cliente registrado y desbloquear los controles de boleta, en caso contrario, desplegará un mensaje que le indicará al operador que tiene que registrar al cliente y en ese caso pasará a una pantalla de registro. Si todo se ha hecho de la manera correcta, se procederá a cargar la imagen de la factura. En este caso el documento de la factura se puede escanear o adjuntar manualmente.

Una vez que se carga el documento de factura, el personal del punto de venta hará una búsqueda de los productos relacionados a esa factura, donde se desplegará una pantalla emergente en el cual se hará una búsqueda y selección de los medicamentos de acuerdo a la factura. Estos medicamentos se deberán ir agregando a una lista final de los productos relacionados a la compra.

Una vez que estén cargados los medicamentos a la lista final, la pantalla tendrá una opción que permitirá emitir el número de boleta para ese medicamento si el cliente tiene canjes activos. Por último, se procede a realizar la compra la cual tendrá relacionado los números de boleta emitidos.

No obstante, también se puede emitir una boleta para un medicamento desde la pantalla <b>Emitir Boleta</b>.


### 2. Registro de Canjes.
<img src="{{site.baseurl}}/img/1.15.jpg" class="pantalla">
<b>Funcionalidad</b>: En esta parte del proceso se le solicitará al cliente su número de identidad, esto para hacer la búsqueda y verificar si está registrado en la plataforma de Canjes Marcas Propias. Una vez verificada la información se hará una búsqueda de los medicamentos que el cliente tiene disponible para el canje. Teniendo la información verificada se llenará una lista de los medicamentos que tienen disponibilidad de canje. Esta lista posee un apartado de información en el cual desplegará una lista detallada de la boleta a la que pertenece ese medicamento disponible para canje y su estado. Si el estado del canje está en espera entonces se procederá a añadir a la segunda lista de confirmación de medicamento para ser canjeado.

Por último, se procederá a realizar el registro del canje el cual emitirá un documento donde estarán registrados todas las boletas pertenecientes a ese canje.


   - Modal de busqueda de medicamento.  
    <img src="{{site.baseurl}}/img/1.16.jpg" class="pantalla">
     

   - Detalles de la boleta.
    <img src="{{site.baseurl}}/img/1.17.jpg" class="pantalla">
      

### 3. Registro de Pacientes.
 
<img src="{{site.baseurl}}/img/1.18.jpg" class="pantalla">
 
<b>Funcionalidad</b>: En esta pantalla se hará el registro de los pacientes que no se encuentren en la plataforma de Canjes y Marcas propias. Si no existen, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.

  

### 4. Registro de Pariente.
 
<img src="{{site.baseurl}}/img/1.19.jpg" class="pantalla">
 
<b>Funcionalidad</b>: En esta pantalla se hará el registro de los parientes que no se encuentren en la plataforma de Canjes Marcas propias. Si no existen, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.

  

### 5. Registro de Parentesco.
 
<img src="{{site.baseurl}}/img/1.20.jpg" class="pantalla">
 
<b>Funcionalidad</b>: En esta pantalla se hará el registro del parentesco que no se encuentre en la plataforma de Canjes Marcas propias. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.

  

### 6. Emision de boleta.
 
<img src="{{site.baseurl}}/img/1.21.jpg" class="pantalla">
 
<b>Funcionalidad</b>: Se le solicitará el número de la identidad al cliente para verificar si se encuentra en la plataforma de Canjes de Marcas Propias se hace una búsqueda por los medicamentos para saber si tiene la disponibilidad de canje y una vez hecha la verificación se procede a emitir una boleta.

 

   - Plantilla boleta.
    <img src="{{site.baseurl}}/img/1.22.png" class="pantalla">
      

### 7. Reversion de compra.
 
<img src="{{site.baseurl}}/img/1.23.jpg" class="pantalla">
 
<b>Funcionalidad</b>: Se deberá verificar que no exista una boleta relacionada a la compra. Si la relación no existe se podra reversar la compra por medio de su respectivo número de compra.

Al ingresar el número de compra se mostrará la información relacionada a ella.
 

   - Busqueda de compra.
   <img src="{{site.baseurl}}/img/1.24.jpg" class="pantalla">
     

### 8. Registrar medico.
 
<img src="{{site.baseurl}}/img/1.25.jpg" class="pantalla">
 
<b>Funcionalidad</b>: En esta pantalla se hará el registro del médico que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento. Se puede seleccionar varias especialidades para el médico.
 

   - Registrar especialidad.
   <img src="{{site.baseurl}}/img/1.26.jpg" class="pantalla">
    
   <b>Funcionalidad</b>: En esta pantalla se hará el registro de las especialidades médicas que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.

### 9. Re-impresion de boleta.
 
<img src="{{site.baseurl}}/img/1.27.png" class="pantalla">
 
<b>Funcionalidad</b>: Esta pantalla será usada para imprimir la boleta en caso de que el cliente extravíe la boleta física. Se le solicitará al cliente que proporcione su número de identidad para buscar las boletas que tiene disponible, el orden en el que se mostraran será de forma ascendente según la fecha, luego se procederá a imprimir la boleta con una marca de agua de reimpresión.
  

### 10. Paciente programa.
 
<img src="{{site.baseurl}}/img/1.28.jpg" class="pantalla">
<b>Funcionalidad</b>: En esta pantalla se realiza el registro del paciente a un programa en específico, en el cual tendremos la información de la receta y los medicamentos disponibles según el plan de registro.
 

   - Receta.
    <img src="{{site.baseurl}}/img/1.29.png" class="pantalla">
      

## PANTALLAS PARA LA ADMINISTRACIÓN DE CADENAS.
### 1. Pedidos rechazados de Cadena.
 
<img src="{{site.baseurl}}/img/1.30.jpg" class="pantalla">
 
<b>Funcionalidad</b>: En este punto del proceso, el personal del punto de venta verificará la lista de los medicamentos que se le han rechazado su canje y se realizará una búsqueda mediante una fecha de inicio y fecha final relacionada al distribuidor del medicamento, el resultado será el detalle del medicamento, la cantidad solicitada, el número de canje y el detalle por el cual fue rechazado ese número de canje. Una vez verificado esto se generará un pedido de reembolso del punto de venta.
  

### 2. Configuracion de solicitudes de reembolso en Cadena.
 
<img src="{{site.baseurl}}/img/1.31.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: Es una pantalla de configuración donde se parametrizará los valores para generar las solicitudes de reembolso de una manera automatica.</p>
  

## PANTALLAS PARA LA ADMINISTRACIÓN DE DISTRIBUIDORES.

### 1. Configuracion de solicitudes de reembolso en Distribuidores.
 
<img src="{{site.baseurl}}/img/1.32.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: Es una pantalla de configuración donde se parametrizará los valores para generar las solicitudes de reembolso de una manera automatica.</p>
  

### 2. Aplicar reembolso.
 
<img src="{{site.baseurl}}/img/1.33.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>:En esta pantalla el  distribuidor procedera a filtrar la información de las solicitudes a nivel de los puntos de venta de la siguiente forma:</p>

1. Primero se seleccionará el filtro de cadena.
2. Una vez seleccionado el filtro de cadena, desplegará el llenado del filtro del punto de venta, que a su vez también seleccionara una fecha de inicio y fecha final.
3. El resultado será una lista desplegable con la solicitud de reembolso y la fecha en que fue aplicado dicho reembolso en el punto de venta. Cada linea de solicitud tiene un botón de ver detalle, el cual al darle clic nos desplegará la información de manera detallada del medicamento y la cantidad con la que fue solicitado ese reembolso.
<p>Una vez verficada la información se procederá a guardar ese reembolso por parte del distribuidor el cual contiene un panel de mantenimiento donde podra actualizar o borrar el documento generado.</p>
  

### 3. Rechazar Solicitud de reembolso.
 
<img src="{{site.baseurl}}/img/1.34.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta parte del proceso la persona encargada por parte del distribuidor, rechaza la solicitud de reembolso generada por la cadena referente a un punto de venta. </p>
<p>Este rechazo puede ser de dos formas: parcial o total por las unidades solicitadas. Una vez que el usuario tenga preparado los medicamentos que rechazará se procederá a darle al botón de confirmar, el cual verificará línea por línea si la columna de cantidad rechazada tiene un valor digitado.</p>
 

   - Modal cantidad de rechazo.
   <img src="{{site.baseurl}}/img/1.35.jpg" class="pantalla">
    
   <p><strong>Funcionalidad</strong>: Es una pantalla donde se mostrará un espacio, en el cual el usuario podrá digitar la cantidad del producto a rechazar.</p>
     

### 4. Registro de medicamento por distribuidor.
 
<img src="{{site.baseurl}}/img/1.36.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: Se tomará la data maestra de medicamentos para asociar los productos que manejará el distribuidor.</p>
  

## PANTALLAS PARA LA ADMINISTRACIÓN DE LABORATORIOS.

### 1. Registrar cadena.
 
<img src="{{site.baseurl}}/img/1.37.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de la cadena que no se encuentre registrada en la plataforma,se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada y modificada mediante la presente pantalla de mantenimiento.</p>
 

- Seleccionar pais cadena.
<img src="{{site.baseurl}}/img/1.38.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla el usuario puede filtrar y seleccionar el país en donde se encuentra la cadena deseada para agregar en la pantalla  de <strong>Registrar Cadena</strong></p>
  

### 2. Registrar punto de venta.
 
<img src="{{site.baseurl}}/img/1.39.jpg" class="pantalla">
 
<p> <strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los puntos de venta que no se encuentren registrados en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
 

   - Seleccion de cadena para registrar punto de venta.
    <img src="{{site.baseurl}}/img/1.40.jpg" class="pantalla">
     

- Seleccion de pais para registrar punto de venta.
<img src="{{site.baseurl}}/img/1.41.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla el usuario puede filtrar y seleccionar el país en donde se encuentra el punto de venta deseado para agregarlo en la pantalla de <strong>Registrar Punto de Venta</strong></p>
  
        
### 3. Registrar pais.
 
<img src="{{site.baseurl}}/img/1.42.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro del pais que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 4. Registrar region.
 
<img src="{{site.baseurl}}/img/1.43.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de la region que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 5. Tipo de contacto.
 
<img src="{{site.baseurl}}/img/1.44.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla el usuario puede agregar o modificar los tipos de contactos.</p>
  

### 6. Registro de medicamento por laboratorio.
 
<img src="{{site.baseurl}}/img/1.45.png" class="pantalla">
 
<p>Funcionalidad: Se tomará la data maestra de medicamentos para asociar los productos que manejara el laboratorio.</p>
  

### 7. Registrar genero.
 
<img src="{{site.baseurl}}/img/1.46.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los generos que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 8. Registrar tipo de identificacion.
 
<img src="{{site.baseurl}}/img/1.47.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los tipos de identificacion que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 9. Registrar Usuario.
 
<img src="{{site.baseurl}}/img/1.48.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los usuarios. Se procede a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante dicha pantalla de mantenimiento.</p>
   

### 10. Registrar laboratorio.
 
<img src="{{site.baseurl}}/img/1.49.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los laboratorios que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 11. Registrar distribuidor.
 
<img src="{{site.baseurl}}/img/1.50.jpg" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los distribuidores que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 12. Registrar programa.
 
<img src="{{site.baseurl}}/img/1.51.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los programas que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 13. Registrar medicamentos.
 
<img src="{{site.baseurl}}/img/1.52.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los medicamentos que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

- Busqueda de medicamentos.
<img src="{{site.baseurl}}/img/1.53.png" class="pantalla">
  

- Listado de medicamentos.
<img src="{{site.baseurl}}/img/1.54.png" class="pantalla">
  

### 14. Configuracion del laboratorio.
 
<img src="{{site.baseurl}}/img/1.55.png" class="pantalla">
  

### 15. Rechazar solicitud de reembolso.
 
<img src="{{site.baseurl}}/img/1.56.png" class="pantalla">

### 16. Aplicar pedido.
 
<img src="{{site.baseurl}}/img/1.57.png" class="pantalla">
  

### 17. Registrar escala.
 
<img src="{{site.baseurl}}/img/1.58.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de las escalas. Para ello se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 18. Registrar tipo solicitud.
 
<img src="{{site.baseurl}}/img/1.59.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los tipos de solicitudes que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 19. Registrar tipo recurrencia.
 
<img src="{{site.baseurl}}/img/1.60.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los tipos de recurrencia que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  










