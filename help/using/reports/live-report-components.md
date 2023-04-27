---
solution: Journey Optimizer
product: journey optimizer
title: Lista de componentes
description: Aprenda a utilizar los datos del informe en directo
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 8%

---

# Lista de componentes {#list-of-components-live}

Las tablas siguientes proporcionan la lista de métricas utilizadas en los informes y sus definiciones en función del tipo de envío.

## Métricas de recorrido {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definición<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>Acciones ejecutadas correctamente<br/> </td> 
   <td> Número total de acciones ejecutadas correctamente para un recorrido.<br/> </td> 
</tr> 
  <tr> 
   <td> Perfiles introducidos<br/> </td> 
   <td> Número total de personas que llegaron al evento de entrada del recorrido.<br/> </td> 
</tr>
  <tr> 
   <td> Error en la acción<br/> </td> 
   <td>Número total de errores que se han producido en Acciones.<br/> </td> 
</tr> 
  <tr> 
   <td> Perfiles de salida<br/> </td> 
   <td> Número total de personas que salieron del recorrido.<br/> </td> 
</tr> 
  <tr> 
   <td> Error en el recorrido individual<br/> </td> 
   <td> Número total de recorridos individuales que no se ejecutaron correctamente.<br/> </td> 
</tr> 
 </tbody> 
</table>

## Dimensiones y métricas de correo electrónico y SMS {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definición<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> Devoluciones<br/> </td> 
   <td> Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de devoluciones<br/> </td> 
   <td> Porcentaje de correos electrónicos devueltos en comparación con los correos electrónicos enviados.<br/> </td> 
</tr>
  <tr> 
   <td> Clics<br/> </td> 
   <td> Número de veces que se hizo clic en un contenido en un correo electrónico.<br/> </td> 
</tr> 
  <tr> 
   <td> Entregados <br/> </td> 
   <td> Número de mensajes enviados correctamente.<br/></td> 
</tr> 
  <tr> 
   <td> Tasa de entrega<br/> </td> 
   <td> Porcentaje de mensajes enviados correctamente.<br/> </td> 
</tr>
  <tr> 
   <td> Errores<br/> </td> 
   <td> Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de error<br/> </td> 
   <td> Porcentaje de errores que se produjeron durante una entrega que impiden que se envíe en comparación con los correos electrónicos enviados.<br/> </td> 
</tr>
  <tr> 
   <td> Excluido<br/> </td> 
   <td> Número de perfiles que Adobe Journey Optimizer ha excluido.<br/> </td> 
</tr>
  <tr> 
   <td> Rechazo grave<br/> </td> 
   <td> El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.<br/> </td>
</tr>
  <tr> 
   <td> Ignorado<br/> </td> 
   <td> El número total de mensajes temporales, como fuera de la oficina o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.<br/> </td> 
</tr>
   <tr> 
   <td>Tasa de clics de ofertas<br/> </td> 
   <td>Porcentaje de usuarios que interactuaron con la oferta.<br/> </td> 
</tr>
   <tr> 
   <td>Tasa de impresión de la oferta<br/> </td> 
   <td>Porcentaje de ofertas abiertas comparadas con el número de ofertas enviadas.<br/> </td> 
</tr>
   <tr> 
   <td>Nombre de oferta<br/> </td> 
   <td> Nombre de la oferta añadida en la entrega. Para obtener más información sobre la colocación, consulte esta <a href="../offers/offer-library/creating-personalized-offers.md">página</a>.<br/> </td> 
</tr>
   <tr> 
   <td>Oferta enviada<br/> </td> 
   <td>Número total de envíos para la oferta.<br/> </td> 
</tr> 
  <tr>
   <td>Aperturas<br/> </td> 
   <td> Número de veces que se abrió el mensaje.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de apertura<br/> </td> 
   <td> Número total de correos electrónicos abiertos comparados con el número de correos electrónicos enviados.<br/> </td> 
</tr>
  <tr> 
   <td>Nombre de colocación<br/> </td> 
   <td> Nombre de la ubicación utilizada para mostrar la oferta. Para obtener más información sobre la colocación, consulte esta <a href="../offers/offer-library/creating-placements.md">página</a>. </td> 
</tr> 
  <tr> 
   <td> Reintentos<br/> </td> 
   <td> Número de correos electrónicos en cola para reintentos.<br/> </td> 
</tr> 
  <tr> 
   <td> Enviados<br/> </td> 
   <td> Número total de envíos para la entrega.<br/> </td> 
</tr>
  <tr> 
   <td> Rechazo suave<br/> </td> 
   <td> Número total de errores temporales, como una bandeja de entrada completa.<br/> </td> 
</tr>
  <tr> 
   <td> Reclamaciones por correo no deseado<br/> </td> 
   <td> Número de veces que un mensaje se declaró como correo no deseado o no deseado.<br/> </td> 
</tr>
  <tr> 
   <td> Segmentado<br/> </td> 
   <td> Número total de mensajes procesados durante el análisis de entregas.<br/> </td> 
</tr> 
  <tr> 
   <td> Clics únicos<br/> </td> 
   <td> Número de destinatarios que hicieron clic en un contenido en un correo electrónico.<br/> </td> 
</tr> 
  <tr> 
   <td>Tasa de clics únicos<br/> </td> 
   <td> Porcentaje de usuarios que interactuaron con la entrega.<br/> </td> 
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

## Métricas de la página de aterrizaje {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definición<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>Devoluciones<br/> </td> 
   <td>Número de personas que no interactuaron con la página de aterrizaje y que no completaron la acción de suscribirse.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Clics<br/> </td> 
   <td>Número de veces que se hizo clic en un contenido en la página de aterrizaje.<br/> </td> 
</tr>
<tr>
<td>Conversión<br/> </td> 
   <td>Número de personas que interactuaron con la página de aterrizaje, por ejemplo, suscritas a un formulario.<br/> </td> 
</tr>
 <tr> 
   <td>Recorridos<br/> </td> 
   <td>Número de visitas a la página de aterrizaje procedentes de un recorrido.<br/> </td> 
</tr>
 <tr> 
   <td>Otras fuentes<br/> </td> 
   <td>Número de visitas a la página de aterrizaje procedentes de una fuente externa en lugar de un recorrido.<br/> </td> 
</tr>
 <tr> 
   <td>Visitas totales<br/> </td> 
   <td> Número total de visitas a la página de aterrizaje procedentes de recorridos y fuentes externas, incluidas las visitas múltiples de un destinatario.<br/> </td> 
</tr>
 <tr> 
   <td>Visitantes únicos<br/> </td> 
   <td>Número de personas que visitaron la página de aterrizaje y no se tienen en cuenta las visitas múltiples de un destinatario.<br/> </td> 
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
   <th> Métrica<br/> </th> 
   <th> Definición<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Acciones<br/> </td> 
   <td> Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.<br/> </td> 
</tr>
  <tr> 
   <td>Devoluciones<br/> </td> 
   <td> Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.<br/> </td> 
</tr> 
  <tr> 
   <td> Entregados<br/> </td> 
   <td> Número de mensajes enviados correctamente.<br/> </td> 
</tr> 
  <tr> 
   <td>Participaciones<br/> </td> 
   <td> Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.<br/> </td> 
</tr> 
  <tr> 
   <td> Errores<br/> </td> 
   <td> Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.<br/> </td> 
</tr>
  <tr> 
   <td> Excluido<br/> </td> 
   <td> Número de perfiles que Adobe Journey Optimizer ha excluido.<br/> </td> 
</tr>
  <tr> 
   <td> Aperturas<br/> </td> 
   <td> Número total de notificaciones push enviadas al dispositivo y en las que los usuarios han hecho clic para abrir la aplicación. Esto es similar al clic push , excepto que no se activará un push Open si se descarta la notificación.<br/> </td> 
</tr> 
  <tr> 
   <td> Enviados<br/> </td> 
   <td> Número total de envíos para la entrega.<br/> </td> 
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