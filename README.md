## Caso Técnico
* Se tiene una Pantalla de Actualización de Datos la cual sirve para registrar las direcciones electrónicas de Clientes Persona Jurídica.

* La pantalla tiene hasta 5 correos electrónicos los cuales pueden  ser registrados, actualizados o eliminados

* Se requiere un proceso Batch que se ejecute todos los días y exporte la información de las direcciones de los Clientes


## Consideraciones Específicas
* Requisito #01: Se requiere un proceso diario de las actualizaciones (delta) y en caso no se llegara a ejecutar el proceso, se tenga la posibilidad de re*ejecutar y se procesen los días faltantes. Ejemplo: El proceso empieza a fallar desde el Martes, se soluciona el el Jueves y se tiene que reprocesar con la información del Martes, Miercoles y Jueves.

* Requisito #02: El equipo de Negocio ha identificado que un anterior sistema de información se tiene una base histórica de correos de Clientes y los desea cargar en el nuevo modelo y que el proceso de descarga los considere, los correos los va enviar en un archivo Excel teniendo como llave el ID del Cliente

* Requisito #03: El equipo de Negocio quiere que se informe en un campo adicional de la BROAD cuando el correo sea nuevo, modificado o eliminado, ya que son 5 posiciones máximas

* Requisito #04: El equipo de Negocio solicita que el proceso informe no solo los nuevos correos (delta) sino todos los correos del Cliente, es decir si al Cliente "Juan Perez" se le modifico 1 de sus 5 correos, se informen todos los correos no solo el modificado


## Entregables
* Diagramar el modelo de datos de soporte las necesidad de negocio

* Diagramar los procesos principales y flujos alternos

* Especificar reglas de validacion y limpieza de datos

* Especificar lógicas de reproceso y cargas externas AdHoc
