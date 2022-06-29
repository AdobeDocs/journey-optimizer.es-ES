---
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 108a7aab025aa92fab59c26d0bf5bf5339b81bb3
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 31%

---

# Notas de la versión {#release-notes}

En esta página se enumeran todas las nuevas funciones y mejoras de [!DNL Journey Optimizer]. También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

## Lanzamiento de junio de 2022 {#june-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Enviar SMS a los usuarios (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear, personalizar y enviar SMS en Journey Optimizer mediante una integración con <b>Sinch</b> o <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Actualmente, el canal SMS solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, póngase en contacto con el representante del Adobe.</p>
<p>Aprenda a crear y enviar un SMS en esta <a href="../messages/create-sms.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Encuentre imágenes más impactantes más rápido con la integración con Adobe Stock</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>El complemento de integración de Adobe Stock y Adobe Journey Optimizer Email Designer proporciona a los clientes una forma sencilla de navegar, obtener licencias y guardar imágenes para utilizarlas en la creación de mensajes. </br> El nuevo <b>Buscar fotos similares de Stock</b> también le permite localizar fotos de almacenamiento que coincidan con el contenido, el color y la composición de las imágenes. </p>
<img src="assets/do-not-localize/stock-rn.gif"/>
<p>Para obtener más información, consulte la <a href="../design/stock.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilice el correo electrónico CCO en todos sus correos electrónicos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar la capacidad Email BCC (copia de seguridad ciega) para almacenar correos electrónicos enviados por Adobe Journey Optimizer. Active esta opción en los ajustes preestablecidos de correo electrónico para que cada correo electrónico enviado se copie de forma ciega en su dirección de CCO.</p>
<img src="assets/do-not-localize/bcc-rn.gif"/>
<p>Para obtener más información, consulte la <a href="../configuration/bcc-email.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Copiar objetos entre entornos limitados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede volver a crear las experiencias de un simulador para pruebas de Journey Optimizer a otro, por ejemplo, de un simulador para pruebas que no sean de producción a un simulador para pruebas de producción. Esta nueva funcionalidad copia un Recorrido completo, incluidos los objetos de los que depende el Recorrido, para ejecutarse correctamente, de un entorno a otro. Además de los Recorridos, también puede copiar otros componentes, como Ofertas, Mensajes, Esquemas, Conjuntos de datos, Fuentes de datos, Eventos y Acciones.</p>
<p>Para obtener más información, consulte la <a href="../building-journeys/copy-to-sandbox.md">documentación detallada</a>.
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content. In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Mejoras

**Administración de decisiones**

* **Compatibilidad con archivos HTML y JSON** : Ahora puede arrastrar y soltar archivos HTML y JSON externos de la biblioteca de Adobe Experience Cloud Asset en el contenido de la representación de ofertas. [Más información](../offers/offer-library/add-representations.md#html-json)


**Correo electrónico**

* **Guardar como plantilla** - Ahora puede guardar un contenido de correo electrónico como plantilla y reutilizarlo al crear otros mensajes. [Más información](../design/email-templates.md)

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

-->

**Administración**

<!--* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.-->

* **Vista previa de los parámetros de URL de seguimiento** : Al configurar un ajuste preestablecido de mensaje, si define parámetros de seguimiento de URL, ahora se muestra una vista previa dinámica de la URL de seguimiento resultante. [Más información](../configuration/email-settings.md#url-tracking)

<!--* **Personalize tracking URL parameters** - You can now use the Expression Editor to configure URL tracking parameters in your message presets. [Learn more](../configuration/email-settings.md#url-tracking)-->

<!--
**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.
-->
