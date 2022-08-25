---
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 30d197f3eab05e2e38025189a6948a6c0fbd6d54
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 63%

---

# Notas de la versión {#release-notes}

En esta página se enumeran todas las nuevas funciones y mejoras de [!DNL Journey Optimizer]. También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

## Versión de agosto de 2022 {#aug-2022-release}

### Nuevas funciones

<!--table>
<thead>
<tr>
<th><strong>Create and manage campaigns in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use Journey Optimizer campaigns to deliver one-time content to a specific segment using various channels. When using journeys, actions are designed to be executed in sequence. With campaigns actions are performed simultaneously, either immediately, or based on a specified schedule. </p>
<p>For more information, refer to the <a href="../campaigns/get-started-with-campaigns.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Enviar SMS a sus usuarios (disponibilidad general)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear, personalizar y enviar SMS en Journey Optimizer mediante una integración con <b>Sinch</b> o <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Aprenda a crear y enviar un SMS en esta <a href="../messages/create-sms.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->



### Mejoras

**Creación de informes**

* La tabla y el gráfico de políticas de consentimiento ya están disponibles en los informes globales de Recorrido. Estas utilidades permiten rastrear los perfiles excluidos de las políticas en sus acciones personalizadas. [Más información](../reports/journey-global-report.md#journey-global)

   Para tener acceso a las últimas utilidades, tenga en cuenta que tendrá que restablecer los distintos paneles de informes. Para obtener más información sobre la personalización de tableros, consulte [la documentación detallada](../reports/global-report.md).

**Administración**

* Ahora es posible actualizar el número de teléfono principal para utilizarlo en el canal SMS. [Más información](../configuration/primary-email-addresses.md)