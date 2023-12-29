---
solution: Journey Optimizer
product: journey optimizer
title: Lista de componentes
description: Aprenda a utilizar los datos del informe global
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: c487bb38-49ce-4238-8e94-8364f994cedd
source-git-commit: 82b8c9032d6c377cb76acce4d5cc45afb0ddd6ba
workflow-type: tm+mt
source-wordcount: '1106'
ht-degree: 2%

---

# Lista de componentes {#list-of-components-global}

Las siguientes tablas proporcionan la lista de métricas utilizadas en los informes y sus definiciones según el tipo de envío.

## métricas de recorrido {#journey-metrics}

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
   <td> Error en acción<br/> </td> 
   <td>Número total de errores que se produjeron en las acciones.<br/> </td> 
</tr> 
  <tr> 
   <td> Perfiles abandonados<br/> </td> 
   <td> Número total de personas que salieron del recorrido.<br/> </td> 
</tr> 
  <tr> 
   <td> Recorrido individual fallido<br/> </td> 
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
   <td> Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de devoluciones<br/> </td> 
   <td> Porcentaje de correos electrónicos devueltos en comparación con los enviados.<br/> </td> 
</tr>
  <tr> 
   <td> Clics<br/> </td> 
   <td> Número de veces que se hizo clic en un contenido en un correo electrónico.<br/> </td> 
</tr> 
  <tr> 
   <td> Entregado <br/> </td> 
   <td> Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.<br/></td> 
</tr> 
  <tr> 
   <td> Tasa de entrega<br/> </td> 
   <td> Porcentaje de mensajes enviados correctamente.<br/> </td> 
</tr>
  <tr> 
   <td> Errores<br/> </td> 
   <td> Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de error<br/> </td> 
   <td> Porcentaje de errores que se han producido durante una entrega para evitar que se envíe en comparación con los correos electrónicos enviados.<br/> </td> 
</tr>
</tr> 
  <tr> 
   <td> Motivo del error<br/> </td> 
   <td> Nombre de la causa original específica del error. <a href="error-list.md">Más información sobre los motivos de error</a>.<br/> </td> 
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
   <td>Tasa de pulsaciones de oferta<br/> </td> 
   <td>Porcentaje de usuarios que interactuaron con la oferta.<br/> </td> 
</tr>
   <tr> 
   <td>Tasa de impresiones de oferta<br/> </td> 
   <td>Porcentaje de ofertas abiertas comparadas con el número de ofertas enviadas.<br/> </td> 
</tr>
   <tr> 
   <td>Nombre de oferta<br/> </td> 
   <td> Nombre de la oferta añadida en la entrega. Para obtener más información sobre la ubicación, consulte esta sección <a href="../offers/offer-library/creating-personalized-offers.md">página</a>.<br/> </td> 
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
   <td> Número total de correos electrónicos abiertos en comparación con el número de correos electrónicos enviados.<br/> </td> 
</tr>
  <tr> 
   <td>Nombre de ubicación<br/> </td> 
   <td> Nombre de la ubicación utilizada para mostrar la oferta. Para obtener más información sobre la ubicación, consulte esta sección <a href="../offers/offer-library/creating-placements.md">página</a>. </td> 
</tr> 
  <tr> 
   <td> Reintentos<br/> </td> 
   <td> Número de correos electrónicos en cola para reintentos.<br/> </td> 
</tr> 
  <tr> 
   <td> Enviado<br/> </td> 
   <td> Número total de envíos para el envío.<br/> </td> 
</tr>
  <tr> 
   <td> Rechazo suave<br/> </td> 
   <td> Número total de errores temporales, como una bandeja de entrada llena.<br/> </td> 
</tr>
  <tr> 
   <td> Quejas de spam<br/> </td> 
   <td> Número de veces que un mensaje se ha declarado como correo no deseado.<br/> </td> 
</tr>
  <tr> 
   <td> Objetivos<br/> </td> 
   <td> Número total de mensajes procesados durante el análisis de entregas.<br/> </td> 
</tr> 
  <tr> 
   <td> Clics únicos<br/> </td> 
   <td> Número de destinatarios que hicieron clic en un contenido de un correo electrónico.<br> Tenga en cuenta que al calcular clics únicos, se tienen en cuenta los últimos 10 días. Si un perfil registra varios clics dentro del periodo de 10 días, se contarán como clics únicos. Sin embargo, si un perfil tiene 2 clics con una diferencia de más de 10 días, no se considerarán como clics únicos.<br/> </td> 
</tr> 
  <tr> 
   <td>Tasa de clics únicos<br/> </td> 
   <td> Porcentaje de usuarios que interactuaron con el envío.<br/> </td> 
</tr>
  <tr> 
   <td> Aperturas únicas<br/> </td> 
   <td>Número de destinatarios que abrieron la entrega. <br> Tenga en cuenta que al calcular las aperturas únicas, se tienen en cuenta los últimos 10 días. Si un perfil registra varias aperturas dentro del periodo de 10 días, se contarán como aperturas únicas. Sin embargo, si un perfil tiene 2 aperturas separadas por más de 10 días, no se considerarán como aperturas únicas.<br/> </td> 
</tr> 
  <tr> 
   <td> Bajas<br/> </td> 
   <td> Número de clics en el vínculo de baja de suscripción.<br/> </td> 
</tr> 
 </tbody> 
</table>

<!--
## Experimentation metrics {#experimentation-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td>App installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>App launches<br/> </td> 
   <td><br/> </td> 
</tr>
 <tr> 
   <td>Average lift<br/> </td> 
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../campaigns/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../campaigns/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../campaigns/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>Number of times the email was opened.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td>Number of clicks on the unsubscription link.<br/> </td> 
</tr>
  <tr> 
   <td>First app launches<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Outbound Clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Profiles<br/> </td> 
   <td>Number of profiles targeted for this treatment.<br/> </td> 
</tr>
  <tr> 
   <td>Unique email opens<br/> </td> 
   <td>Number of recipients who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of recipients who clicked on the unsubscription link.<br/> </td>
</tr>
  <tr> 
   <td>Unique installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique launches<br/> </td> 
   <td><br/> </td> 
</tr> 
  <tr> 
   <td>Unique outbound clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique upgrades<br/> </td> 
   <td><br/> </td> 
</tr>
   <td>Upgrades<br/> </td> 
   <td><br/> </td> 
</tr> 
</tbody> 
</table>
-->

## Métricas en la aplicación {#inapp-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Métrica<br/> </th> 
   <th> Definición<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Clics<br/> </td> 
   <td>Número total de destinatarios que interactuaron con los botones incluidos en el mensaje en la aplicación.<br/> </td> 
</tr>
  <tr> 
   <td>Tasa de clics<br/> </td> 
   <td>Porcentaje de usuarios que interactuaron con los botones incluidos en el mensaje en la aplicación comparados con los usuarios que vieron el mensaje.<br/> </td> 
</tr> 
  <tr> 
   <td>Tasa de descarte<br/> </td> 
   <td> Porcentaje de mensajes en la aplicación que los destinatarios descartaron.<br/> </td> 
</tr> 
  <tr> 
   <td>Impresiones<br/> </td> 
   <td> Número total de mensajes en la aplicación enviados a todos los usuarios.<br/> </td>
</tr>
  <tr> 
   <td>Impresiones únicas<br/> </td> 
   <td>Número de usuarios únicos a los que se entregó el mensaje en la aplicación.<br/> </td>
</tr>
 </tbody> 
</table>

## Métricas de notificaciones push

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
   <td> Número total de acciones en la notificación push entregada; por ejemplo, clic en el botón o despido.<br/> </td> 
</tr>
  <tr> 
   <td>Devoluciones<br/> </td> 
   <td> Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de devoluciones<br/> </td> 
   <td> Porcentaje de notificaciones push que rebotaron en comparación con las notificaciones push enviadas.<br/> </td>
</tr>
  <tr> 
   <td> Entrega<br/> </td> 
   <td> Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de entrega<br/> </td> 
   <td> Porcentaje de notificaciones push enviadas correctamente.<br/> </td> 
</tr>
  <tr> 
   <td>Participaciones<br/> </td> 
   <td> Número total de aperturas y acciones para esta notificación push; es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de participación<br/> </td> 
   <td> Porcentaje de aperturas y acciones para esta notificación push; es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.<br/> </td> 
</tr>
  <tr> 
   <td> Errores<br/> </td> 
   <td> Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.<br/> </td> 
</tr>
  <tr> 
   <td> Tasa de error<br/> </td> 
   <td> Porcentaje de errores que se han producido durante una entrega para evitar que se envíe en comparación con las notificaciones push enviadas.<br/> </td> 
</tr>
  <tr> 
   <td> Motivo del error<br/> </td> 
   <td> Nombre de la causa original específica del error. <a href="error-list.md">Más información sobre los motivos de error</a>.<br/> </td> 
</tr>
  <tr> 
   <td> Excluido<br/> </td> 
   <td> Número de perfiles que Adobe Journey Optimizer ha excluido.<br/> </td> 
</tr>
  <tr> 
   <td> Aperturas<br/> </td> 
   <td> Número total de notificaciones push enviadas al dispositivo y en las que los usuarios hicieron clic al abrir la aplicación. Esto es similar al clic push, excepto que una apertura push no se activa si se descarta la notificación.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de apertura<br/> </td> 
   <td> Porcentaje de notificaciones push abiertas.<br/> </td> 
</tr> 
  <tr> 
   <td> Enviado<br/> </td> 
   <td> Número total de envíos para el envío.<br/> </td> 
</tr> 
  <tr> 
   <td> Objetivos<br/> </td> 
   <td> Número total de mensajes push procesados durante el análisis de envío.<br/> </td> 
</tr>  
 </tbody> 
</table>

## Métricas de página de aterrizaje {#landing-page-metrics}

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
   <td>Número de personas que no interactuaron con la página de aterrizaje y no completaron la acción de suscripción.<br/> </td> 
</tr>
 <tr> 
   <td>Tasa de devoluciones<br/> </td> 
   <td>Número de personas que no interactuaron con la página de aterrizaje y no completaron la acción de suscripción en relación con el número total de visitas.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Clics<br/> </td> 
   <td>Número de veces que se hizo clic en un contenido en la página de aterrizaje.<br/> </td> 
</tr>
 <tr> 
   <td>Tasa de clics<br/> </td> 
   <td>Porcentaje de clics en la página de aterrizaje.<br/> </td>
</tr>
<tr>
<td>Conversión<br/> </td> 
   <td>Número de personas que interactuaron con la página de aterrizaje (por ejemplo, suscritas a un formulario).<br/> </td> 
</tr>
<tr>
   <td>Tasa de conversión<br/> </td> 
   <td>Número de personas que interactuaron con la página de aterrizaje (por ejemplo, suscritas a un formulario) en relación con el número total de visitas.<br/> </td> 
</tr>
 <tr> 
   <td>Recorrido(s)<br/> </td> 
   <td>Número de visitas a la página de aterrizaje procedentes de un recorrido.<br/> </td> 
</tr>
 <tr> 
   <td>Otras fuentes<br/> </td> 
   <td>Número de visitas a la página de aterrizaje procedentes de un origen externo en lugar de un recorrido.<br/> </td> 
</tr>
 <tr> 
   <td>Visitas totales<br/> </td> 
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
