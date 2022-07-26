---
title: Notas de la versión
description: Notas de la versión de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 88%

---

# Notas de la versión {#release-notes}

En esta página se enumeran todas las nuevas funciones y mejoras de [!DNL Journey Optimizer]. También puede consultar la página de las [últimas actualizaciones de la documentación](documentation-updates.md) para ver más cambios.

[!DNL Adobe Journey Optimizer] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Regístrese para la [Newsletter trimestral de Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoy y reciba las últimas actualizaciones de productos, artículos interesantes, casos de uso, sugerencias y mucho más directamente en su bandeja de entrada cada trimestre.

>[!CAUTION]
>
>El 25 de julio, Adobe Journey Optimizer lanzará un [nueva función](../rn/inline-messages.md) que mejora la forma en que se crea contenido para canales de Journey Optimizer (correo electrónico, push, SMS). Como profesional de Journey Optimizer, ahora [crear y crear](../messages/get-started-content.md) sus mensajes directamente desde un recorrido. Se realiza una conversión automática de recorridos. Dicho esto, necesitamos su ayuda con algunos pasos. Obtenga más información sobre [pasos necesarios](../rn/inline-messages-steps.md).

## Lanzamiento de junio de 2022 {#june-2022-release}

### Nuevas funciones

<table>
<thead>
<tr>
<th><strong>Envío de SMS a los usuarios (disponibilidad limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede crear, personalizar y enviar SMS en Journey Optimizer mediante una integración con <b>Sinch</b> o <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Ahora mismo, el canal SMS solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.</p>
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
<p>El complemento de integración del Diseñador de correo electrónico de Adobe Journey Optimizer y Adobe Stock proporciona a los clientes una forma sencilla de navegar, obtener licencias y guardar imágenes para utilizarlas en la creación de mensajes. </br> La nueva opción <b>Buscar fotografías similares de Stock</b> también le permite localizar fotos de Stock que coincidan con el contenido, el color y la composición de sus imágenes. </p>
<img src="assets/do-not-localize/stock-rn.gif"/>
<p>Para obtener más información, consulte la <a href="../design/stock.md">documentación detallada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Uso de CCO del correo electrónico en todos los correos electrónicos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede utilizar la capacidad CCO del correo electrónico (copia de carbón oculta) para almacenar correos electrónicos enviados por Adobe Journey Optimizer. Active esta opción en los ajustes preestablecidos de correo electrónico para que cada correo electrónico enviado se copie de forma oculta en su dirección de CCO.</p>
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
<th><strong>Copia de objetos entre zonas protegidas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ahora puede recrear las experiencias de una zona protegida de Journey Optimizer en otra, por ejemplo, de una que no sea de producción a una de producción. Esta nueva funcionalidad copia un recorrido completo, incluidos los objetos de los que depende para ejecutarse correctamente, de un entorno a otro. Además de los recorridos, también puede copiar otros componentes, como Ofertas, Mensajes, Esquemas, Conjuntos de datos, Fuentes de datos, Eventos y Acciones.</p>
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
<p>You can now create conditional content blocks across different authoring services to personalize your content. In addition to the Personalization Expression Library, the Expression editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Mejoras

**Gestión de decisiones**

* **Compatibilidad con archivos HTML y JSON**: ahora puede arrastrar y soltar archivos HTML y JSON externos de la biblioteca de recursos de Adobe Experience Cloud en el contenido de la representación de la oferta. [Más información](../offers/offer-library/add-representations.md#html-json)


**Correo electrónico**

* **Guardar como plantilla**: ahora puede guardar un contenido de correo electrónico como plantilla y reutilizarlo al crear otros mensajes. [Más información](../design/email-templates.md)

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

-->

**Administración**

<!--* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.-->

* **Previsualizar parámetros de URL de seguimiento**: al configurar un ajuste preestablecido de mensaje, si define parámetros de seguimiento de URL, ahora se muestra la vista previa dinámica de la URL de seguimiento resultante. [Más información](../configuration/email-settings.md#url-tracking)

* **Edición de ajustes preestablecidos de mensajes**: ahora, al actualizar un ajuste preestablecido de mensaje, el tiempo de procesamiento solo puede ser de hasta tres horas. [Más información](../configuration/message-presets.md#edit-message-preset)

* **Edición de grupos de IP**: ahora, al actualizar un grupo de IP, el tiempo de procesamiento solo puede ser de hasta tres horas. [Más información](../configuration/ip-pools.md#edit-ip-pool)

<!--* **Personalize tracking URL parameters** - You can now use the Expression editor to configure URL tracking parameters in your message presets. [Learn more](../configuration/email-settings.md#url-tracking)-->

<!--
**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.
-->
