---
solution: Journey Optimizer
product: journey optimizer
title: Informe global
description: Aprenda a utilizar los datos del informe global
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: ee2c3c5d356bddf622da2d9313ad7e0511be3092
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 5%

---

# Introducción al informe global {#global-report}

>[!NOTE]
>
> Si las consultas personalizadas se realizan a través de API al utilizar el servicio de Consulta, espere un cierto retraso para los informes.

Utilice la variable **[!UICONTROL Informe global]** para medir el impacto de los recorridos y envíos durante un período de tiempo seleccionado.

* Si desea dirigirse a un recorrido o envíos en el contexto de un recorrido, desde el **[!UICONTROL Recorridos]** , acceda al recorrido y haga clic en el botón **[!UICONTROL Ver informe]** botón. A continuación, puede encontrar los informes globales Recorrido, Correo electrónico, SMS y Push .

   ![](assets/report_journey.png)

* Si desea dirigir una campaña, desde la **[!UICONTROL Campañas]** , acceda a la campaña y haga clic en el botón **[!UICONTROL Informes]** botón.

   ![](assets/report_campaign.png)

* Si desea cambiar del **[!UICONTROL Informe activo]** a **[!UICONTROL Informe global]** para la entrega, haga clic en **[!UICONTROL Todo]** del conmutador de pestañas.

   ![](assets/report_5.png)

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](#list-of-components-global)

## Personalizar tablero {#modify-dashboard}

Cada tablero de informes se puede modificar cambiando el período de tiempo y cambiando el tamaño o eliminando las utilidades. Cambiar las utilidades solo afecta al tablero del usuario actual. Otros usuarios verán sus propios tableros o los que estén configurados de forma predeterminada.

1. En el informe Global , seleccione una Hora de inicio y una de finalización para dirigirse a datos específicos.

   ![](assets/report_modify_1.png)

1. Elija si desea excluir los eventos de prueba de los informes con la barra de alternancia. Para obtener más información sobre los eventos de prueba, consulte [esta página](../building-journeys/testing-the-journey.md).

   Tenga en cuenta que **[!UICONTROL Excluir eventos de prueba]** solo está disponible para informes de Recorrido.

   ![](assets/report_modify_2.png)

1. Haga clic en **[!UICONTROL Modificar]** para comenzar a personalizar el tablero.

   ![](assets/report_modify_3.png)

1. Ajuste el tamaño de los widgets arrastrando su esquina inferior derecha.

   ![](assets/report_modify_4.png)

1. Haga clic en **[!UICONTROL Eliminar]** para quitar cualquier utilidad que no necesite.

   ![](assets/report_modify_5.png)

1. Una vez que esté satisfecho con el orden de visualización y el tamaño de sus widgets, haga clic en **[!UICONTROL Guardar]**.

El tablero se ha guardado. Los diferentes cambios se volverán a aplicar para un uso posterior de los informes activos. Si es necesario, use la variable **[!UICONTROL Restablecer]** para restaurar el orden predeterminado de las utilidades y utilidades.

## Lista de componentes {#list-of-components-global}

Las tablas siguientes proporcionan la lista de métricas utilizadas en los informes y sus definiciones en función del tipo de envío.

### Métricas de recorrido {#journey-metrics}

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

### Dimensiones y métricas de correo electrónico y SMS {#email-and-sms-metrics}

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
   <td> Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.<br/> </td> 
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
   <td> Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.<br/></td> 
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

<!--
### Experimentation metrics {#experimentation-metrics}
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
   <td>.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td><br/> </td> 
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
   <td><br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td><br/> </td>
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

### Métricas de notificaciones push

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
   <td> Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de devoluciones<br/> </td> 
   <td> Porcentaje de notificaciones push que rebotaron en comparación con las notificaciones push enviadas.<br/> </td>
</tr>
  <tr> 
   <td> Entregados<br/> </td> 
   <td> Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de entrega<br/> </td> 
   <td> Porcentaje de notificaciones push enviadas correctamente.<br/> </td> 
</tr>
  <tr> 
   <td>Participaciones<br/> </td> 
   <td> Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasa de participación<br/> </td> 
   <td> Porcentaje de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.<br/> </td> 
</tr>
  <tr> 
   <td> Errores<br/> </td> 
   <td> Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.<br/> </td> 
</tr>
  <tr> 
   <td> Tasa de error<br/> </td> 
   <td> Porcentaje de errores que se produjeron durante una entrega que impiden que se envíe comparado con las notificaciones push enviadas.<br/> </td> 
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
   <td> Tasa de apertura<br/> </td> 
   <td> Porcentaje de notificaciones push abiertas.<br/> </td> 
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

### Métricas de la página de aterrizaje {#landing-page-metrics}

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
   <td>Porcentaje de rebote<br/> </td> 
   <td>Número de personas que no interactuaron con la página de aterrizaje y no completaron la acción de suscribirse, en relación con el número total de visitas.<br/> </td> 
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
   <td>Número de personas que interactuaron con la página de aterrizaje, por ejemplo, suscritas a un formulario.<br/> </td> 
</tr>
<tr>
   <td>Tasa de conversión<br/> </td> 
   <td>Número de personas que interactuaron con la página de aterrizaje, por ejemplo, suscritas a un formulario, en relación con el número total de visitas.<br/> </td> 
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

<!--
### In-app metrics {#inapp-metrics}
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
   <td>Click rate<br/> </td> 
   <td>Percentage of users who interacted with the buttons included in the In-app message compared to users who saw the message.<br/> </td> 
</tr> 
  <tr> 
   <td>Dismiss rate<br/> </td> 
   <td> Percentage of In-app messages that recipients dismissed.<br/> </td> 
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
