---
solution: Journey Optimizer
product: journey optimizer
title: Introducción al Asistente de IA
description: Obtenga información sobre cómo acceder al asistente de IA de Journey Optimizer y trabajar con él
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: b62f8954e09f50896ad5e70784c5a93943617e85
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 43%

---

# Introducción al Asistente de IA {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_content_generation"
>title="Creación de contenido de correo electrónico"
>abstract="El Asistente de IA de Adobe Journey Optimizer ofrece sugerencias proactivas de variación de contenido para textos e imágenes. Está disponible para canales de correo electrónico, push, SMS y web. Esta nueva funcionalidad proporciona una generación de texto e imágenes basada en solicitudes."

>[!BEGINSHADEBOX]

**Tabla de contenido**

* Introducción al Asistente de IA
* [Generación de correo electrónico con el asistente de IA](generative-email.md)
* [Generación de SMS con el asistente de IA](generative-sms.md)
* [Generación push con el asistente de IA](generative-push.md)
* [Experimento de contenido con el asistente de IA](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>El asistente de IA de Adobe Journey Optimizer está disponible actualmente como una versión beta solo para usuarios seleccionados.

El Asistente de IA de Adobe Journey Optimizer ofrece sugerencias proactivas de variación de contenido para textos e imágenes. Está disponible para canales de correo electrónico, push y SMS. Esta nueva funcionalidad proporciona una generación de texto e imágenes basada en solicitudes. La generación de imágenes se administra con Adobe Firefly.

Ahora puede utilizar el Asistente de IA en Journey Optimizer para optimizar el impacto del mensaje experimentando con diferentes títulos e imágenes principales. Genere varias variantes y cree un experimento para compararlas. Con el Experimento de contenido de Journey Optimizer, puede definir varios tratamientos para los mensajes a fin de medir cuál ofrece el mejor rendimiento para su público destinatario. Puede elegir entre variar el contenido del envío o el asunto. El público del mensaje se asigna aleatoriamente a cada tratamiento para determinar cuál funciona mejor en términos de la métrica especificada. Obtenga más información sobre el Experimento de contenido en [esta sección](../campaigns/content-experiment.md).

## Mecanismos de protección y limitaciones {#generative-guardrails}

A continuación, se enumeran las directrices generales para utilizar el asistente de IA en Journey Optimizer para la generación de correo electrónico:

* La calidad del contenido generado se ve fuertemente influida por el objetivo de marketing que defina. Utilice un indicador bien definido para el modelo GenAI para interpretar con precisión. 
* Cargue el recurso de la marca para tener información precisa sobre el contenido de la marca. De lo contrario, el contenido se basa en información disponible públicamente. El contenido cargado puede tener los siguientes formatos: PDF, JPEG, PNG o archivos ZIP (con formatos de archivo compatibles).
* El tamaño máximo del recurso de marca cargado es de 50 MB. Los archivos más grandes o muchas imágenes pueden funcionar, pero el tiempo de procesamiento aumenta.
* Utilice plantillas de correo electrónico creadas por Adobe Campaign, preferiblemente [plantillas de correo electrónico integradas](../email/use-email-templates.md), una plantilla específica de la marca o una plantilla personalizada para crear el contenido del correo electrónico. Se recomienda una plantilla de correo electrónico con hasta 8-10 imágenes.
* Asegúrese de informar de cualquier salida problemática utilizando los iconos de miniatura hacia arriba, pulgar hacia abajo o indicador al seleccionar variantes.
* El uso del asistente de IA está sujeto a las Directrices del usuario de IA generativa de Adobe Experience Cloud. [Más información](https://www.adobe.com/es/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

Las siguientes limitaciones se aplican a AI Assistant en Journey Optimizer:

* El idioma admitido es solo inglés.
* Solo disponible para los canales de correo electrónico, push y SMS.
* Puede que el contenido de GenAI no siempre sea preciso: comparta sus comentarios para que nuestros ingenieros puedan perfeccionar los modelos.
* Puede cargar varios recursos de marca, pero solo puede aprovechar uno para una generación específica.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="Generación de correo electrónico" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong>Generación de correo electrónico</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="Generación de SMS" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong>Generación de SMS</strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="Generación push" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>Generación de notificaciones push</strong></a>
</div>
<p></td>
</tr></table>
