---
solution: Journey Optimizer
product: journey optimizer
title: Lista de componentes
description: Aprenda a utilizar los datos del informe en directo
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 12168cdf-f517-49b5-958b-ba689ade6982
source-git-commit: c9505b482d2dedc10c4025574cccb662fe149510
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 4%

---

# Lista de componentes {#list-of-components-live}

Las siguientes tablas proporcionan la lista de métricas utilizadas en los informes y sus definiciones según el tipo de envío.

## Métricas de recorrido {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica <br/> </th> 
   <th> Definición <br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>Acciones ejecutadas correctamente<br/> </td> 
   <td> Número total de acciones ejecutadas correctamente para un recorrido.<br/> </td> 
</tr> 
  <tr> 
   <td> Perfiles especificados<br/> </td> 
   <td> Número total de personas que llegaron al evento de entrada del recorrido.<br/> </td> 
</tr>
  <tr> 
   <td> Error en la acción <br/> </td> 
   <td>Número total de errores que se produjeron para las acciones.<br/> </td> 
</tr> 
  <tr> 
   <td> Perfiles abandonados<br/> </td> 
   <td> Número total de personas que salieron del recorrido.<br/> </td> 
</tr> 
  <tr> 
   <td> Error en el recorrido individual <br/> </td> 
   <td> Número total de recorridos individuales que no se ejecutaron correctamente.<br/> </td> 
</tr> 
 </tbody> 
</table>

## Dimensiones y métricas de correo electrónico y SMS {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica <br/> </th> 
   <th> Definición <br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> Devoluciones<br/> </td> 
   <td> Total de errores acumulados durante el envío y el procesamiento automático de devoluciones.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de devoluciones<br/> </td> 
   <td> Porcentaje de correos electrónicos devueltos en comparación con los enviados.<br/> </td> 
</tr>
  <tr> 
   <td> Clics<br/> </td> 
   <td> Número de veces que se hizo clic en un contenido en un mensaje de correo electrónico.<br/> </td> 
</tr> 
  <tr> 
   <td> Entregado <br/> </td> 
   <td> Número de mensajes enviados correctamente.<br/></td> 
</tr> 
  <tr> 
   <td> Tasa de entrega<br/> </td> 
   <td> Porcentaje de mensajes enviados correctamente.<br/> </td> 
</tr>
  <tr> 
   <td> Errores<br/> </td> 
   <td> Número total de errores que se produjeron durante una entrega para evitar que se enviara a los perfiles.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de error <br/> </td> 
   <td> Porcentaje de errores que se produjeron durante un envío y que impiden su envío en comparación con los correos electrónicos enviados.<br/> </td> 
</tr>
  <tr> 
   <td> Excluido<br/> </td> 
   <td> Número de perfiles que Adobe Journey Optimizer ha excluido.<br/> </td> 
</tr>
  <tr> 
   <td> Rechazo duro<br/> </td> 
   <td> Número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.<br/> </td>
</tr>
  <tr> 
   <td> Ignorado<br/> </td> 
   <td> Número total de mensajes temporales, como Fuera de la oficina, o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.<br/> </td> 
</tr>
   <tr> 
   <td>Tasa de clics en ofertas<br/> </td> 
   <td>Porcentaje de usuarios que interactuaron con la oferta.<br/> </td> 
</tr>
   <tr> 
   <td>Tasa de impresión de la oferta<br/> </td> 
   <td>Porcentaje de ofertas abiertas en comparación con el número de ofertas enviadas.<br/> </td> 
</tr>
   <tr> 
   <td>Nombre de oferta<br/> </td> 
   <td> Nombre de la oferta añadida en la entrega. Para obtener más información sobre la ubicación, consulte esta <a href="../offers/offer-library/creating-personalized-offers.md">página</a>.<br/> </td> 
</tr>
   <tr> 
   <td>Se envió la oferta<br/> </td> 
   <td>Número total de envíos para la oferta.<br/> </td> 
</tr> 
  <tr>
   <td>Aperturas<br/> </td> 
   <td> Número de veces que se abrió el mensaje.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de apertura<br/> </td> 
   <td> Número total de correos electrónicos abiertos en comparación con el número de correos electrónicos enviados.<br/> </td> 
</tr>
  <tr> 
   <td>Nombre de ubicación<br/> </td> 
   <td> Nombre de la ubicación utilizada para mostrar la oferta. Para obtener más información sobre la ubicación, consulte esta <a href="../offers/offer-library/creating-placements.md">página</a>. </td> 
</tr> 
  <tr> 
   <td> Reintentos<br/> </td> 
   <td> Número de mensajes de correo electrónico en la cola para reintentos.<br/> </td> 
</tr> 
  <tr> 
   <td> Enviado<br/> </td> 
   <td> Número total de envíos para el envío.<br/> </td> 
</tr>
  <tr> 
   <td> Devolución suave<br/> </td> 
   <td> Número total de errores temporales, como una bandeja de entrada completa.<br/> </td> 
</tr>
  <tr> 
   <td> Quejas de spam<br/> </td> 
   <td> Número de veces que se declaró un mensaje como correo no deseado.<br/> </td> 
</tr>
  <tr> 
   <td> Segmentado<br/> </td> 
   <td> Número total de mensajes procesados durante el análisis de entregas.<br/> </td> 
</tr> 
  <tr> 
   <td> Clics únicos<br/> </td> 
   <td> Número de destinatarios que hicieron clic en un contenido de un correo electrónico.<br/> </td> 
</tr> 
  <tr> 
   <td>Tasa de clics únicos<br/> </td> 
   <td> Porcentaje de usuarios que interactuaron con el envío.<br/> </td> 
</tr>
  <tr> 
   <td> Aperturas únicas<br/> </td> 
   <td>Número de destinatarios que abrieron la entrega.<br/> </td> 
</tr> 
  <tr> 
   <td> Bajas<br/> </td> 
   <td> Número de clics en el vínculo de baja de suscripción.<br/> </td> 
</tr> 
 </tbody> 
</table>

## Métricas de página de aterrizaje {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica <br/> </th> 
   <th> Definición <br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>Devoluciones<br/> </td> 
   <td>Número de personas que no interactuaron con la página de aterrizaje y no completaron la acción de suscripción.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Clics<br/> </td> 
   <td>Número de veces que se hizo clic en un contenido en la página de aterrizaje.<br/> </td> 
</tr>
<tr>
<td>Conversión<br/> </td> 
   <td>Número de personas que interactuaron con la página de aterrizaje (por ejemplo, se suscribieron a un formulario).<br/> </td> 
</tr>
 <tr> 
   <td>Recorrido(s)<br/> </td> 
   <td>Número de visitas a la página de aterrizaje provenientes de un recorrido.<br/> </td> 
</tr>
 <tr> 
   <td>Otros orígenes<br/> </td> 
   <td>Número de visitas a la página de aterrizaje procedentes de un origen externo en lugar de un recorrido.<br/> </td> 
</tr>
 <tr> 
   <td>Total de visitas<br/> </td> 
   <td> Número total de visitas a la página de aterrizaje procedentes de recorridos y fuentes externas, incluidas las visitas múltiples de un destinatario.<br/> </td> 
</tr>
 <tr> 
   <td>Visitantes únicos<br/> </td> 
   <td>Número de personas que visitaron la página de aterrizaje; no se tienen en cuenta las visitas múltiples de un destinatario.<br/> </td> 
</tr>
 <tr> 
   <td>Visitas<br/> </td> 
   <td>Número de visitas a la página de aterrizaje, incluidas las visitas múltiples de un destinatario.<br/> </td> 
</tr>
 </tbody> 
</table>

## Métricas de notificaciones push {#push-notification-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica <br/> </th> 
   <th> Definición <br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Acciones <br/> </td> 
   <td> Número total de acciones en la notificación push entregada, por ejemplo: clic en el botón o despido.<br/> </td> 
</tr>
  <tr> 
   <td>Devoluciones<br/> </td> 
   <td> Total de errores acumulados durante el envío y el procesamiento automático de devoluciones.<br/> </td> 
</tr> 
  <tr> 
   <td> Entrega<br/> </td> 
   <td> Número de mensajes enviados correctamente.<br/> </td> 
</tr> 
  <tr> 
   <td>Participaciones<br/> </td> 
   <td> Número total de aperturas y acciones para esta notificación push; es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.<br/> </td> 
</tr> 
  <tr> 
   <td> Errores<br/> </td> 
   <td> Número total de errores que se produjeron durante una entrega para evitar que se enviara a los perfiles.<br/> </td> 
</tr>
  <tr> 
   <td> Excluido<br/> </td> 
   <td> Número de perfiles que Adobe Journey Optimizer ha excluido.<br/> </td> 
</tr>
  <tr> 
   <td> Aperturas<br/> </td> 
   <td> Número total de notificaciones push enviadas al dispositivo y en las que los usuarios hicieron clic al abrir la aplicación. Esto es similar al clic push, excepto que una acción push/apertura no se activará si se descarta la notificación.<br/> </td> 
</tr> 
  <tr> 
   <td> Enviado<br/> </td> 
   <td> Número total de envíos para el envío.<br/> </td> 
</tr> 
  <tr> 
   <td> Segmentado<br/> </td> 
   <td> Número total de mensajes push procesados durante el análisis de envío.<br/> </td> 
</tr>  
 </tbody> 
</table>

<!--
## In-app metrics {#inapp-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Clicks<br/> </td> 
   <td>Total number of recipients who interacted with the buttons included in the In-app message.<br/> </td> 
</tr>
  <tr> 
   <td>Impressions<br/> </td> 
   <td> Total number of In-app messages delivered to all users.<br/> </td>
</tr>
  <tr> 
   <td>Unique impressions<br/> </td> 
   <td>Number of unique users to whom the In-app message was delivered.<br/> </td>
</tr>
 </tbody> 
</table>
-->
