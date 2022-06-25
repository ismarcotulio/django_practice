---
layout: post
title: "Pantallas y flujo de desarrollo"
subtitle: 'Presentacion del proyecto'
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
        width: 60%;
    }

    p{
        text-align: justify;
    }
</style>
El presente documento tiene por finalidad mostrar el diagrama de flujo de proceso y diseño de la aplicación web para la plataforma de Automatización de Canjes de Marcas Propias (Swissfarm-Vitotal) para que los clientes registrados al mismo tengan el beneficio de canjes con los laboratorios, para ello se adjunta las imágenes de cada pantalla del proceso y una breve explicación de las mismas.  

 

## Pantallas de Usuario

### 1. Inicio de sesion.
<img src="{{site.baseurl}}/img/38.png" class="pantalla">

### 2. Recuperar contraseña.
<img src="{{site.baseurl}}/img/39.png" class="pantalla">

### 3. Menu.
<img src="{{site.baseurl}}/img/40.png" class="pantalla">

## Pantallas para la administracion de Puntos de Venta
### 1. Registro de Compras.
<img src="{{site.baseurl}}/img/1.png" class="pantalla">
<p><strong>Funcionalidad</strong>: Esta pantalla se utilizará para realizar el registro de la compra cuando el cliente se presente al punto de venta con la factura en mano. La factura se le mostrará al personal de punto de venta, este a su vez le solicitará al cliente su número de identidad, el cual se deberá introducir en el campo de identificación. Luego al presionar enter desplegará la información del nombre del cliente registrado y desbloqueará los controles de boleta, en caso contrario, desplegará un mensaje que le indicará al operador que tiene que registrar al cliente y en ese caso pasará a una pantalla de registro. Si todo se ha hecho de la manera correcta, se prodecerá a cargar la imagen de la factura. En este caso el documento de la factura se puede escanear o adjuntar manualmente.</p>
<p>Una vez que se carga el documento de factura, el personal del punto de venta hará una búsqueda de los productos relacionados a esa factura, donde se desplegará una pantalla emergente en el cual se hará una búsqueda y selección de los medicamentos de acuerdo a la factura. Estos medicamentos se deberán ir agregando a una lista final de los productos relacionados a la compra.</p>
<p>Una vez que esten cargados los medicamentos a la lista final, la pantalla tendrá una opción que permitira emitir el número de boleta para ese medicamento si el cliente tiene canjes activos. Por último, se procede a realizar la compra la cual tendrá relacionado los números de boleta emitidos.</p>
<p>No obstante también se puede emitir una boleta para un medicamento desde la pantalla <strong>Emitir Boleta</strong>.</p>

### 2. Registro de Canjes.
<img src="{{site.baseurl}}/img/2.png" class="pantalla">
<p><strong>Funcionalidad</strong>: En esta parte del proceso se le solicitará al cliente su número de identidad, esto para hacer la búsqueda y verificar si esta registrado en la plataforma de Canjes y Marcas Propias. Una vez verificada la información se hará una búsqueda de los medicamentos que el cliente tiene disponible para el canje. Teniendo la información verificada se llenará una lista de los medicamentos que tienen disponibilidad de canje. Esta lista posee un apartado de información en el cual desplegará una lista detallada de la boleta a la que pertenece ese medicamento disponible para canje y su estado. Si el estado del canje esta en espera entonces se procederá a añadir a la segunda lista de confirmación de medicamento para ser canjeado. </p>
<p>Por último se procederá a realizar el registro del canje el cual emitirá un documento donde estaran registrados todas las boletas pertenecientes a ese canje.</p>

   - Modal de busqueda de medicamento.  
    <img src="{{site.baseurl}}/img/3.png" class="pantalla">
     

   - Detalles de la boleta.
    <img src="{{site.baseurl}}/img/4.png" class="pantalla">
      

### 3. Registro de Pacientes.
 
<img src="{{site.baseurl}}/img/5.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los pacientes que no se encuentren en la plataforma de Canjes y Marcas propias. Si no existen, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 4. Registro de Pariente.
 
<img src="{{site.baseurl}}/img/6.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los parientes que no se encuentren en la plataforma de Canjes y Marcas propias. Si no existen, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 5. Registro de Parentesco.
 
<img src="{{site.baseurl}}/img/7.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>:  En esta pantalla se hará el registro del parentesco que no se encuentre en la plataforma de Canjes y Marcas propias. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 6. Emision de boleta.
 
<img src="{{site.baseurl}}/img/8.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: Se le solicitará el número de la identidad al cliente para verificar si se encuentra en la plataforma de Canjes y Marcas Propias se hace una búsqueda por los medicamentos para saber si tiene la disponibilidad de canje y una vez hecha la verificación se procede a emitir una boleta.</p>
 

   - Plantilla boleta.
    <img src="{{site.baseurl}}/img/9.png" class="pantalla">
      

### 7. Reversion de compra.
 
<img src="{{site.baseurl}}/img/10.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: Se deberá verificar que no exista una boleta relacionada a la compra. Si la relación no existe  se podra reversar la compra por medio de su respectivo número de compra. </p>
<p>Al ingresar el número de compra se mostrará la información relacionada a ella.</p>
 

   - Busqueda de compra.
   <img src="{{site.baseurl}}/img/11.png" class="pantalla">
     

### 8. Registrar medico.
 
<img src="{{site.baseurl}}/img/15.png" class="pantalla">
 
<p> <strong>Funcionalidad</strong>: En esta pantalla se hará el registro del médico que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
 

   - Seleccionar especialidad.
   <img src="{{site.baseurl}}/img/16.png" class="pantalla">
    
   <p><strong>Funcionalidad</strong>: En esta pantalla el usuario puede filtrar y seleccionar la especialidad deseada para agregarla en la pantalla  de <strong>Registrar Médico</strong></p>
    

   - Registrar especialidad.
   <img src="{{site.baseurl}}/img/17.png" class="pantalla">
    
   <p> <strong>Funcionalidad</strong>: En esta pantalla se hará el registro de las especialidades medicas que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
     

### 9. Re-impresion de boleta.
 
<img src="{{site.baseurl}}/img/27.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: Esta pantalla será usada para re-imprimir la boleta en caso de que el cliente extravié la boleta fisica. Se le solicitará al cliente que proporcione su número de identidad para buscar las boletas que tiene disponible, el orden en el que se mostraran será de forma ascendente según la fecha, luego se procederá a re-imprimir la boleta con una marca de agua de re-impresion.</p>
  

### 10. Paciente programa.
 
<img src="{{site.baseurl}}/img/49.png" class="pantalla">
<p></p>
 

   - Receta.
    <img src="{{site.baseurl}}/img/50.png" class="pantalla">
      

## Pantallas para la administracion de Cadenas.
### 1. Pedidos rechazados de Cadena.
 
<img src="{{site.baseurl}}/img/12.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En este punto del proceso, el personal del punto de venta verificará la lista de los medicamentos que se le han rechazado su canje y se realizará una búsqueda mediante una fecha de incio y fecha final relacionada al distribuidor del medicamento, el resultado será el detalle del medicamento, la cantidad solicitada, el número de canje y el detalle por el cual fue rechazado ese número de canje. Una vez verificado esto se generará un pedido de reembolso del punto de venta.</p>
  

### 2. Configuracion de solicitudes de reembolso en Cadena.
 
<img src="{{site.baseurl}}/img/47.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: Es una pantalla de configuración donde se parametrizará los valores para generar las solicitudes de reembolso de una manera automatica.</p>
  

## Pantallas para la administracion de Distribuidores.
### 1. Configuracion de solicitudes de reembolso en Distribuidores.
 
<img src="{{site.baseurl}}/img/48.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: Es una pantalla de configuración donde se parametrizará los valores para generar las solicitudes de reembolso de una manera automatica.</p>
  

### 2. Aplicar reembolso.
 
<img src="{{site.baseurl}}/img/26.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>:En esta pantalla el  distribuidor procedera a filtrar la información de las solicitudes a nivel de los puntos de venta de la siguiente forma:</p>

1. Primero se seleccionará el filtro de cadena.
2. Una vez seleccionado el filtro de cadena, desplegará el llenado del filtro del punto de venta, que a su vez también seleccionara una fecha de inicio y fecha final.
3. El resultado será una lista desplegable con la solicitud de reembolso y la fecha en que fue aplicado dicho reembolso en el punto de venta. Cada linea de solicitud tiene un botón de ver detalle, el cual al darle clic nos desplegará la información de manera detallada del medicamento y la cantidad con la que fue solicitado ese reembolso.
<p>Una vez verficada la información se procederá a guardar ese reembolso por parte del distribuidor el cual contiene un panel de mantenimiento donde podra actualizar o borrar el documento generado.</p>
  

### 3. Rechazar Solicitud de reembolso.
 
<img src="{{site.baseurl}}/img/13.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta parte del proceso la persona encargada por parte del distribuidor, rechaza la solicitud de reembolso generada por la cadena referente a un punto de venta. </p>
<p>Este rechazo puede ser de dos formas: parcial o total por las unidades solicitadas. Una vez que el usuario tenga preparado los medicamentos que rechazará se procederá a darle al botón de confirmar, el cual verificará línea por línea si la columna de cantidad rechazada tiene un valor digitado.</p>
 

   - Modal cantidad de rechazo.
   <img src="{{site.baseurl}}/img/14.png" class="pantalla">
    
   <p><strong>Funcionalidad</strong>: Es una pantalla donde se mostrará un espacio, en el cual el usuario podrá digitar la cantidad del producto a rechazar.</p>
     

### 4. Registro de medicamento por distribuidor.
 
<img src="{{site.baseurl}}/img/28.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: Se tomará la data maestra de medicamentos para asociar los productos que manejará el distribuidor.</p>
  

## Pantallas para la admnistracion de Laboratorios.
### 1. Registrar cadena.
 
<img src="{{site.baseurl}}/img/18.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de la cadena que no se encuentre registrada en la plataforma,se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada y modificada mediante la presente pantalla de mantenimiento.</p>
 

- Seleccionar pais cadena.
<img src="{{site.baseurl}}/img/19.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla el usuario puede filtrar y seleccionar el país en donde se encuentra la cadena deseada para agregar en la pantalla  de <strong>Registrar Cadena</strong></p>
  

### 2. Registrar punto de venta.
 
<img src="{{site.baseurl}}/img/20.png" class="pantalla">
 
<p> <strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los puntos de venta que no se encuentren registrados en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
 

   - Seleccion de cadena para registrar punto de venta.
    <img src="{{site.baseurl}}/img/21.png" class="pantalla">
     

- Seleccion de pais para registrar punto de venta.
<img src="{{site.baseurl}}/img/22.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla el usuario puede filtrar y seleccionar el país en donde se encuentra el punto de venta deseado para agregarlo en la pantalla de <strong>Registrar Punto de Venta</strong></p>
  
        
### 3. Registrar pais.
 
<img src="{{site.baseurl}}/img/23.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro del pais que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 4. Registrar region.
 
<img src="{{site.baseurl}}/img/24.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de la region que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 5. Tipo de contacto.
 
<img src="{{site.baseurl}}/img/25.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla el usuario puede agregar o modificar los tipos de contactos.</p>
  

### 6. Registro de medicamento por laboratorio.
 
<img src="{{site.baseurl}}/img/29.png" class="pantalla">
 
<p>Funcionalidad: Se tomará la data maestra de medicamentos para asociar los productos que manejara el laboratorio.</p>
  

### 7. Registrar genero.
 
<img src="{{site.baseurl}}/img/30.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los generos que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 8. Registrar tipo de identificacion.
 
<img src="{{site.baseurl}}/img/31.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los tipos de identificacion que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 9. Registrar Usuario.
 
<img src="{{site.baseurl}}/img/32.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los usuarios. Se procede a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante dicha pantalla de mantenimiento.</p>
   

### 10. Registrar laboratorio.
 
<img src="{{site.baseurl}}/img/33.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los laboratorios que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 11. Registrar distribuidor.
 
<img src="{{site.baseurl}}/img/34.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los distribuidores que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 12. Registrar programa.
 
<img src="{{site.baseurl}}/img/35.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los programas que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 13. Registrar medicamentos.
 
<img src="{{site.baseurl}}/img/36.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los medicamentos que no se encuentre en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

- Busqueda de medicamentos.
<img src="{{site.baseurl}}/img/37.png" class="pantalla">
  

- Listado de medicamentos.
<img src="{{site.baseurl}}/img/41.png" class="pantalla">
  

### 14. Configuracion del laboratorio.
 
<img src="{{site.baseurl}}/img/42.png" class="pantalla">
  

### 15. Configuracion notificaciones.
 
<img src="{{site.baseurl}}/img/43.png" class="pantalla">
  

### 16. Registrar escala.
 
<img src="{{site.baseurl}}/img/44.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de las escalas. Para ello se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 17. Registrar tipo solicitud.
 
<img src="{{site.baseurl}}/img/45.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los tipos de solicitudes que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  

### 18. Registrar tipo recurrencia.
 
<img src="{{site.baseurl}}/img/46.png" class="pantalla">
 
<p><strong>Funcionalidad</strong>: En esta pantalla se hará el registro de los tipos de recurrencia que no se encuentren en la plataforma. Si no existe, se procederá a registrar llenando el siguiente formulario, en el cual la información puede ser agregada o modificada mediante la presente pantalla de mantenimiento.</p>
  










