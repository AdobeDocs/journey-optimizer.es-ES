---
solution: Journey Optimizer
product: journey optimizer
title: Lista de componentes
description: Aprenda a utilizar los datos del informe
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: aa060d8e-23e2-4bab-b709-636077eb5d20
source-git-commit: be0a240f73e884fd91798952167e81689aa2ae2f
workflow-type: tm+mt
source-wordcount: '2134'
ht-degree: 2%

---

# Lista de métricas {#list-of-components-global}

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
<td>participación de recorrido</td> 
<td>Número total de individuos únicos que recibieron mensajes enviados a través del recorrido, que representan perfiles distintos que alcanzaron un punto de acción designado en el recorrido.</td> 
</tr> 
<tr> 
<td>el recorrido entra</td> 
<td>Número total de personas que llegaron al evento de entrada del recorrido.</td> 
</tr>
<tr> 
<td>salidas de recorrido</td> 
<td>Número total de personas que salieron del recorrido.</td> 
</tr>
<tr> 
<td>errores de recorrido</td> 
<td>Número total de recorridos individuales que no se ejecutaron correctamente.</td> 
</tr>
<tr> 
<td>Ingresa un Recorrido único</td> 
<td>Número total de individuos que llegaron al evento de entrada del recorrido, sin tener en cuenta varias interacciones del mismo perfil.</td> 
</tr>
<tr> 
<td>Salidas de Recorrido únicas</td> 
<td>Número total de individuos que abandonaron el recorrido, sin tener en cuenta varias interacciones del mismo perfil.</td> 
</tr>
<tr> 
<td>Errores de Recorrido único</td> 
<td>Número total de recorridos individuales que no se ejecutaron correctamente, sin tener en cuenta las interacciones múltiples del mismo perfil.</td> 
</tr>
 </tbody> 
</table>

## Métricas de correo electrónico {#email-metrics}

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
   <td> Total de errores acumulados durante el proceso de envío y el procesamiento automático de devolución en relación con el número total de mensajes enviados.<br/> </td> 
  </tr>
  <tr> 
   <td> Tasa de salida hacia otro sitio <br/> </td> 
   <td> Porcentaje de correos electrónicos que resultaron en una devolución, en relación con el número total de correos electrónicos enviados.<br/> </td> 
  </tr> 
  <tr> 
   <td> Tasa de apertura de clics (CTOR)<br/> </td> 
   <td> Número de veces que se abrió el correo electrónico.<br/> </td> 
  </tr>
  <tr> 
   <td> Tasa de clics (CTR)<br/> </td> 
   <td> Porcentaje de usuarios que interactuaron con el correo electrónico.<br/> </td> 
  </tr>
  <tr> 
   <td> Clics<br/> </td> 
   <td> Número de veces que se hizo clic en un contenido en un mensaje de correo electrónico.<br/> </td> 
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
   <td> Motivo del error <br/> </td> 
   <td> Nombre de la causa original específica del error. <a href="exclusion-list.md">Más información sobre los motivos de error</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Aperturas estimadas de correo electrónico<br/> </td> 
   <td>Estimación del total de aperturas de correo electrónico que corresponden a aperturas directas de perfiles y aperturas automatizadas activadas por servidores de correo. Esta métrica ajusta las aperturas activadas por los servidores de correo para el análisis de privacidad o seguridad aplicando una tasa de apertura calculada a partir de los destinatarios que abrieron manualmente el correo electrónico a aquellos cuyos correos electrónicos solo abrieron los servidores de correo.<br/> </td> 
  </tr>
  <tr> 
   <td> Tasa de clics en ofertas<br/> </td> 
   <td> Porcentaje de usuarios que interactuaron con la oferta.<br/> </td> 
  </tr>
  <tr> 
   <td> Tasa de impresión de la oferta<br/> </td> 
   <td> Porcentaje de ofertas abiertas en comparación con el número de ofertas enviadas.<br/> </td> 
  </tr>
  <tr> 
   <td> Nombre de oferta<br/> </td> 
   <td> Nombre de la oferta añadida en la entrega. Para obtener más información sobre la ubicación, consulte esta <a href="../offers/offer-library/creating-personalized-offers.md">página</a>.<br/> </td> 
  </tr>
  <tr> 
   <td> Se envió la oferta<br/> </td> 
   <td> Número total de envíos para la oferta.<br/> </td> 
  </tr> 
  <tr> 
   <td> Aperturas<br/> </td> 
   <td> Número de veces que se abrió el mensaje.<br/> </td> 
  </tr> 
  <tr> 
   <td> Enviar errores<br/> </td> 
   <td> Número total de errores que se produjeron durante el proceso de envío para evitar que se enviara a los perfiles.<br/> </td> 
  </tr> 
  <tr> 
   <td> Enviar exclusiones<br/> </td> 
   <td> Número de perfiles que Adobe Journey Optimizer ha excluido.<br/> </td> 
  </tr>
  <tr> 
   <td> Nombre de ubicación<br/> </td> 
   <td> Nombre de la ubicación utilizada para mostrar la oferta. Para obtener más información sobre la ubicación, consulte esta <a href="../offers/offer-library/creating-placements.md">página</a>. </td> 
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
   <td>Devoluciones únicas<br/> </td> 
   <td> Número de perfiles únicos para los que al menos un correo electrónico resultó en una devolución.</td> 
  </tr>
  <tr> 
   <td>Tasa de devoluciones únicas<br/> </td> 
   <td>Porcentaje de perfiles únicos cuyo correo electrónico rebotó al menos una vez, según el número total de envíos únicos.</td> 
  </tr>
  <tr> 
   <td> Clics únicos<br/> </td> 
   <td> Número de perfiles que hicieron clic en un contenido de un correo electrónico.<br> Tenga en cuenta que al calcular clics únicos, se tienen en cuenta los últimos 10 días. Si un perfil registra varios clics dentro del periodo de 10 días, se contarán como clics únicos. Sin embargo, si un perfil tiene 2 clics separados por más de 10 días, no se considerarán clics únicos.<br/> </td> 
  </tr>
  <tr> 
   <td>Clic único mediante tasa de apertura<br/> </td> 
   <td> Porcentaje de perfiles únicos que hicieron clic en un vínculo después de abrir el correo electrónico, según las aperturas únicas. </td> 
  </tr>
  <tr> 
   <td> Tasa de clics únicos<br/> </td> 
   <td> Porcentaje de perfiles únicos que hicieron clic en al menos un vínculo del correo electrónico, en relación con el número de correos electrónicos enviados únicos. </td> 
  </tr>
  <tr> 
   <td> Entregado(a) único<br/> </td> 
   <td> Número de perfiles únicos que recibieron correctamente al menos un correo electrónico.</td> 
  </tr>
  <tr> 
   <td> Cancelaciones de suscripción de correo electrónico único<br/> </td> 
   <td> Número de perfiles que cancelaron la suscripción a sus correos electrónicos.<br/> </td> 
  </tr>
  <tr> 
   <td> Aperturas de correo electrónico estimadas únicas<br/> </td> 
   <td> Estimación del número de destinatarios de correo electrónico únicos que probablemente abrieron el correo electrónico. Esta métrica tiene como objetivo proporcionar un recuento más preciso de la participación individual desencadenada por los servidores de correo para el análisis de privacidad o seguridad mediante la aplicación de una tasa de apertura única calculada a partir de perfiles únicos que abrieron manualmente el correo electrónico a aquellos cuyos correos electrónicos solo los abrieron los servidores de correo.<br/> </td> 
  </tr>
  <tr> 
   <td> Aperturas únicas<br/> </td> 
   <td> Número de perfiles que abrieron el envío. <br> Tenga en cuenta que al calcular las aperturas únicas, se tienen en cuenta los últimos 10 días. Si un perfil registra varias aperturas dentro del periodo de 10 días, se contarán como aperturas únicas. Sin embargo, si un perfil tiene 2 aperturas separadas por más de 10 días, no se considerarán como aperturas únicas.<br/> </td> 
  </tr> 
  <tr>
  <tr> 
   <td> Envíos únicos<br/> </td> 
   <td>Número de perfiles únicos a los que se intentó enviar al menos un correo electrónico.<br/> </td> 
  </tr>
  <tr> 
   <td> Errores de envío únicos<br/> </td> 
   <td>Número de perfiles únicos que encontraron al menos un error de envío durante el proceso saliente.<br/> </td> 
  </tr>
  <tr> 
   <td> Exclusiones de envío únicas<br/> </td> 
   <td>Número de perfiles únicos excluidos de la recepción de mensajes debido a reglas de idoneidad, segmentación de audiencia o estado del perfil.<br/> </td> 
  </tr>
  <tr> 
   <td>Destino único<br/> </td> 
   <td>Número de perfiles únicos dirigidos durante el proceso de envío.<br/> </td> 
  </tr> 
  <tr> 
   <td> Cancela la suscripción de <br/> </td> 
   <td> Número de clics en el vínculo de baja de suscripción.<br/> </td> 
  </tr> 
 </tbody> 
</table>

## Métricas de SMS

<table> 
  <thead> 
    <tr> 
      <th> Métrica de SMS </th> 
      <th> Definición </th> 
    </tr>
  </thead> 
  <tbody> 
    <tr> 
      <td>Entregados</td> 
      <td>Número de mensajes SMS enviados correctamente en relación con el número total de mensajes SMS.</td> 
    </tr>
    <tr> 
      <td>Clics</td> 
      <td>Número de veces que se hizo clic en un vínculo de un mensaje SMS.</td> 
    </tr>
    <tr> 
      <td>Devoluciones para mensajes SMS salientes</td> 
      <td>Número total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes SMS enviados.</td> 
    </tr>
    <tr> 
      <td>Errores de SMS salientes</td> 
      <td>Número total de errores que se han producido para evitar que el mensaje SMS se envíe a los destinatarios.</td> 
    </tr>
    <tr> 
      <td>Exclusiones de SMS salientes</td> 
      <td>Número de perfiles que Adobe Journey Optimizer excluyó de la recepción de mensajes SMS.</td> 
    </tr>
    <tr> 
      <td>Clics únicos</td> 
      <td>Número de destinatarios únicos que hicieron clic en un vínculo de un mensaje SMS.</td> 
    </tr>
    <tr> 
      <td>Visualizaciones</td> 
      <td>Número de veces que se ha mostrado o abierto un mensaje SMS.</td> 
    </tr>
    <tr> 
      <td>Pantallas únicas</td> 
      <td>Número de destinatarios únicos que abrieron el mensaje SMS, excluidas varias interacciones del mismo usuario.</td> 
    </tr>
    <tr> 
      <td>Personas</td> 
      <td>Número de perfiles de usuario únicos que recibieron o interactuaron con un mensaje SMS.</td> 
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
   <td>Number of profiles who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of profiles who clicked on the unsubscription link.<br/> </td>
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
   <th> Métrica <br/> </th> 
   <th> Definición <br/> </th> 
  </tr>
 </thead> 
 <tbody>
  <tr> 
   <td>Clics<br/> </td> 
   <td>Número total de perfiles que interactuaron con los botones incluidos en el mensaje en la aplicación.<br/> </td> 
  </tr>
  <tr> 
   <td>Tasa de clics<br/> </td> 
   <td>Porcentaje de usuarios que interactuaron con los botones incluidos en el mensaje en la aplicación en comparación con los usuarios que vieron el mensaje.<br/> </td> 
  </tr>
  <tr> 
   <td>Tasa de descarte <br/> </td> 
   <td>Porcentaje de mensajes en la aplicación cuyos perfiles se descartaron.<br/> </td> 
  </tr>
  <tr> 
   <td>Impresiones<br/> </td> 
   <td>Número total de mensajes en la aplicación entregados a todos los usuarios.<br/> </td>
  </tr>
  <tr> 
   <td>Impresiones únicas<br/> </td> 
   <td>Número de usuarios únicos a los que se entregó el mensaje en la aplicación.<br/> </td>
  </tr>
  <tr> 
   <td>Muestra<br/> </td>
   <td>Número de veces que se abrió el mensaje en la aplicación.<br/> </td>
  </tr>
  <tr> 
   <td>Visualizaciones únicas<br/> </td>
   <td>Número de veces que se abrió el mensaje en la aplicación, excluidas varias interacciones del mismo perfil.<br/> </td>
  </tr>
  <tr> 
   <td>Clics únicos<br/> </td>
   <td>Número de perfiles que hicieron clic en el contenido de sus mensajes en la aplicación.<br/> </td>
  </tr>
  <tr> 
   <td>Clics<br/> </td>
   <td>Número de veces que se hizo clic en el contenido en los mensajes en la aplicación.<br/> </td>
  </tr>
  <tr> 
   <td>Tasa de clics (CTR)<br/> </td>
   <td>Porcentaje de usuarios que interactuaron con los mensajes en la aplicación.<br/> </td>
  </tr>
  <tr> 
   <td>Tasa de apertura de clics (CTOR)<br/> </td>
   <td>Número de veces que se abrió el mensaje en la aplicación.<br/> </td>
  </tr>
  <tr> 
   <td>Envíos<br/> </td>
   <td>Número total de mensajes en la aplicación enviados.<br/> </td>
  </tr>
  <tr> 
   <td>Activado entrante<br/> </td>
   <td>Número de veces que un mensaje en la aplicación se activó por una interacción del usuario o un evento predefinido.<br/> </td>
  </tr>
  <tr> 
   <td>Rechazos entrantes<br/> </td>
   <td>Cantidad de veces que los usuarios descartaron el mensaje en la aplicación sin interactuar con él.<br/> </td>
  </tr>
 </tbody> 
</table>

## Métricas de notificaciones push

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
   <td> Total de errores acumulados durante el envío y el procesamiento automático de devolución en relación con el número total de mensajes enviados.<br/> </td> 
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
   <td> Tasa de entrega <br/> </td> 
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
   <td> Número total de errores que se produjeron durante una entrega para evitar que se enviara a los perfiles.<br/> </td> 
</tr>
  <tr> 
   <td> Tasa de error <br/> </td> 
   <td> Porcentaje de errores que se produjeron durante una entrega para evitar que se enviara en comparación con las notificaciones push enviadas.<br/> </td> 
</tr>
  <tr> 
   <td> Motivo del error <br/> </td> 
   <td> Nombre de la causa original específica del error. <a href="exclusion-list.md">Más información sobre los motivos de error</a>.<br/> </td> 
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
   <td> Tasa de apertura<br/> </td> 
   <td> Porcentaje de notificaciones push abiertas.<br/> </td> 
</tr>
  <tr> 
   <td> Acciones personalizadas push<br/> </td> 
   <td>Número de acciones personalizadas realizadas por perfiles en respuesta a las notificaciones push.<br/> </td> 
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
   <td>Tasa de salida hacia otro sitio <br/> </td> 
   <td>Porcentaje de personas que vieron la página de aterrizaje pero no interactuaron ni se suscribieron, en relación con el número total de visitas.<br/> </td> 
</tr>
 <tr> 
   <td>Clics<br/> </td> 
   <td>Número de veces que se hizo clic en un contenido en la página de aterrizaje.<br/> </td> 
</tr>

<tr> 
   <td>Conversión de página de aterrizaje<br/> </td> 
   <td>Número de personas que interactuaron con la página de aterrizaje; por ejemplo, se suscribieron a un formulario.<br/> </td> 
</tr>
<tr> 
   <td>Tasa de conversión de página de aterrizaje<br/> </td> 
   <td>Porcentaje de personas que interactuaron con la página de aterrizaje (por ejemplo, suscritas a un formulario) en relación con el número total de visitas.<br/> </td> 
</tr>
 <tr> 
   <td>Vistas de página de aterrizaje<br/> </td> 
   <td>Número total de visitas a la página de aterrizaje desde recorridos y fuentes externas, incluidas varias visitas desde el mismo perfil.<br/> </td> 
</tr>
<tr> 
   <td>Conversiones de página de aterrizaje únicas<br/> </td> 
   <td>Número de personas únicas que interactuaron con la página de aterrizaje, excluidas varias interacciones del mismo perfil.<br/> </td> 
</tr>
 <tr> 
   <td>Vistas de página de aterrizaje únicas<br/> </td> 
   <td>Número de personas únicas que visitaron su página de aterrizaje, excluidas las visitas múltiples del mismo perfil.<br/> </td> 
</tr>
 </tbody> 
</table>

## Correo directo {#direct-mail}

<table> 
 <thead> 
  <tr> 
   <th> Métrica <br/> </th> 
   <th> Definición <br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Entrega<br/> </td> 
   <td>Número de mensajes de correo postal que se entregaron correctamente a los destinatarios.<br/> </td> 
</tr>
<tr> 
   <td>Errores de salida <br/> </td> 
   <td>Número de mensajes de correo postal que detectaron errores durante el procesamiento o el envío, lo que impide el envío correcto.<br/> </td> 
</tr>
<tr> 
   <td>Exclusiones salientes<br/> </td> 
   <td>Número de perfiles excluidos de la recepción de correo postal debido a criterios predefinidos o al filtrado por Adobe Journey Optimizer.<br/> </td> 
</tr>
<tr> 
   <td>Perfiles<br/> </td> 
   <td>Número de perfiles de usuario identificados como audiencia de destino para la campaña de correo postal.<br/> </td> 
</tr>
<tr> 
   <td>Enviado<br/> </td> 
   <td>Número total de mensajes de correo postal enviados correctamente como parte de la campaña.<br/> </td> 
</tr>
<tr> 
   <td>Segmentado<br/> </td> 
   <td>Número total de mensajes de correo postal preparados y procesados para su envío.<br/> </td> 
</tr>
 </tbody> 
</table>


## Métricas de tarjeta de contenido {#content-based}

<table> 
 <thead> 
  <tr> 
   <th> Métrica <br/> </th> 
   <th> Definición <br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Tasa de clics (CTR)<br/> </td> 
   <td>Porcentaje de usuarios que interactuaron con la tarjeta de contenido.<br/> </td> 
</tr>
<tr> 
   <td>Clics<br/> </td> 
   <td>Número de veces que se hizo clic en un contenido de su tarjeta de contenido.<br/> </td> 
</tr>
<tr> 
   <td>Muestra<br/> </td> 
   <td>Número de veces que se abrió el mensaje.<br/> </td> 
</tr>
<tr> 
   <td>Personas<br/> </td> 
   <td>Número de perfiles de usuario que cumplen los requisitos como perfiles de destino para las tarjetas de contenido.<br/> </td> 
</tr>
<tr> 
   <td>Clics únicos<br/> </td> 
   <td>Número de perfiles que hicieron clic en un contenido de su tarjeta de contenido.<br/> </td> 
</tr>
<tr> 
   <td>Visualizaciones únicas<br/> </td> 
   <td>Número de veces que se abrió el mensaje; no se tienen en cuenta las interacciones múltiples de un perfil.<br/> </td> 
</tr>
 </tbody> 
</table>

## Métricas de páginas web {#web}

<table> 
 <thead> 
  <tr> 
   <th> Métrica <br/> </th> 
   <th> Definición <br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Clics<br/> </td> 
   <td>Número de veces que se hizo clic en un contenido de sus páginas Web.<br/> </td> 
</tr>
<tr> 
   <td>Tasa de clics (CTR)<br/> </td> 
   <td>Porcentaje de usuarios que interactuaron con las páginas Web.<br/> </td> 
</tr>
<tr> 
   <td>Muestra<br/> </td> 
   <td>Número de veces que se abrió la página web.<br/> </td> 
</tr>
<tr> 
   <td>Personas<br/> </td> 
   <td>Número de perfiles que cumplen los requisitos de los perfiles de destino para las páginas web.<br/> </td> 
</tr>
<tr> 
   <td>Clics únicos<br/> </td> 
   <td>Número de perfiles que hicieron clic en un contenido de sus páginas web.<br/> </td> 
</tr>
<tr> 
   <td>Visualizaciones únicas<br/> </td> 
   <td>Número de veces que se abrió la página web; no se tienen en cuenta las interacciones múltiples de un perfil.<br/> </td> 
</tr>
 </tbody> 
</table>

## Métricas de experiencias basadas en código {#code-based}

<table> 
 <thead> 
  <tr> 
   <th> Métrica <br/> </th> 
   <th> Definición <br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Clics<br/> </td> 
   <td>Cantidad total de veces que los usuarios hicieron clic en experiencias personalizadas que se les mostraron.<br/> </td> 
</tr>
<tr> 
   <td>Tasa de clics (CTR)<br/> </td> 
   <td>Porcentaje de usuarios que hacen clic en un vínculo, anuncio o recomendación en comparación con el número de veces que se mostró.<br/> </td> 
</tr>
<tr> 
   <td>Tasa de conversión <br/> </td> 
   <td>Porcentaje de pantallas que dieron como resultado acciones del usuario (por ejemplo, clics), que indican el éxito del modelo en la participación de usuarios.<br/> </td> 
</tr>
<tr> 
   <td>Rendimiento de elementos de decisión<br/> </td> 
   <td>Evalúa el rendimiento de cada elemento para atraer usuarios e impulsar las acciones deseadas, como compras, clics u otras respuestas.<br/> </td> 
</tr>
<tr> 
   <td>KPI de decisiones<br/> </td> 
   <td>Información clave sobre la participación de los visitantes con las experiencias, incluidos los elementos totales, los clics totales, las visualizaciones totales y la tasa de reserva.<br/> </td> 
</tr>
<tr> 
   <td>Muestra<br/> </td> 
   <td>Número total de veces que se mostraron o presentaron experiencias personalizadas a los usuarios en varios puntos de contacto.<br/> </td> 
</tr>
<tr> 
   <td>Canal de participación<br/> </td> 
   <td>Supervisa el rendimiento de las experiencias personalizadas mediante la evaluación de la eficacia con que cada fase del canal impulsa las interacciones del usuario.<br/> </td> 
</tr>
<tr> 
   <td>Canal de participación por estrategia de selección<br/> </td> 
   <td>Supervisa y analiza la eficacia con la que las distintas estrategias de selección atraen a usuarios con experiencias personalizadas.<br/> </td> 
</tr>
<tr> 
   <td>Personas<br/> </td> 
   <td>Número de perfiles de usuario que se califican como perfiles de destino para sus experiencias basadas en código.<br/> </td> 
</tr>
<tr> 
   <td>Estrategia de clasificación <br/> </td> 
   <td>Perspectivas del rendimiento de los modelos de clasificación impulsados por IA que comparan dos tipos de tráfico: Impulsado por modelo y Retenido.<br/> </td> 
</tr>
<tr> 
   <td>Elementos de decisión principales por CTR<br/> </td> 
   <td>Destaca el rendimiento de los elementos individuales en función de su tasa de clics (CTR), lo que ayuda a evaluar qué elementos son los más eficaces para atraer usuarios.<br/> </td> 
</tr>
<tr> 
   <td>Clics únicos<br/> </td> 
   <td>Número de perfiles que hicieron clic en un contenido de sus experiencias basadas en código.<br/> </td> 
</tr>
<tr> 
   <td>Visualizaciones únicas<br/> </td> 
   <td>Número de veces que se abrió la experiencia; no se tienen en cuenta las interacciones múltiples de un perfil.<br/> </td> 
</tr>
 </tbody> 
</table>
