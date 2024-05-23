---
solution: Journey Optimizer
product: journey optimizer
title: Introducción al asistente de IA
description: Obtenga información sobre cómo acceder al asistente de IA de Journey Optimizer y trabajar con él
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 644e0959ee0d0ec8ee0c4ec54c3bcd1cc3c4dda9
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 67%

---

# Introducción al asistente de IA {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Asistente de IA"
>abstract="Una vez que haya creado y personalizado su envío, puede utilizar el asistente de IA para mejorar su contenido. Esta función simplifica el proceso de personalización y mejora de contenido, ya que le permite ajustar el contenido al describir lo que desea generar."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Definir contexto con el asistente de IA"
>abstract="Para utilizar el contenido seleccionado como entrada para la generación de contenido, active la variable **Usar contenido original** alternar. También puede cargar los recursos de su marca para utilizarlos como fuente. Si no utiliza el contenido seleccionado, es obligatorio cargar y seleccionar recursos de una marca."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe Términos de IA generativa"
>abstract="El acceso a esta función está sujeto a su acuerdo con las Directrices de usuario de IA generativa de Adobe Experience Cloud. Cualquier solicitud, contexto, información complementaria u otra información que proporcione a esta función debe estar vinculada a un contexto específico, que puede incluir materiales de promoción de la marca, contenido del sitio web, datos, esquemas para dichos datos, plantillas u otros documentos de confianza y no debe contener información personal (la información personal incluye cualquier cosa que pueda vincularse de nuevo a una persona específica). Debe revisar cualquier resultado de esta función para comprobar su precisión y asegurarse de que sea adecuado para su caso de uso"
>additional-url="https://www.adobe.com/es/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Adobe Directrices del usuario de IA generativa"

>[!BEGINSHADEBOX]

**Tabla de contenido**

* Introducción al asistente de IA
* [Generación de correo electrónico con el asistente de IA](generative-email.md)
* [Generación de SMS con el asistente de IA](generative-sms.md)
* [Generación de push con el asistente de IA](generative-push.md)
* [Experimento de contenido con el asistente de IA](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>El asistente de IA de Adobe Journey Optimizer está disponible actualmente en versión Beta solo para los usuarios seleccionados.

El asistente de IA de Adobe Journey Optimizer ofrece sugerencias proactivas de variación de contenido para texto e imágenes. Está disponible para canales de correo electrónico, push y SMS. Esta nueva funcionalidad proporciona una generación de texto e imágenes basada en solicitudes. La generación de imágenes se administra con Adobe Firefly.

Ahora puede utilizar el Asistente de IA en Journey Optimizer para optimizar el impacto del mensaje experimentando con diferentes títulos e imágenes principales. Genere varias variantes y cree un experimento para compararlas. Con el Experimento de contenido de Journey Optimizer, puede definir varios tratamientos para los mensajes a fin de medir cuál ofrece el mejor rendimiento para su público destinatario. Puede elegir entre variar el contenido del envío o el asunto. El público del mensaje se asigna aleatoriamente a cada tratamiento para determinar cuál funciona mejor en términos de la métrica especificada. Obtenga más información sobre el Experimento de contenido en [esta sección](../campaigns/content-experiment.md).

## Mecanismos de protección y limitaciones {#generative-guardrails}

A continuación, se indican las directrices generales para utilizar el asistente de IA en Journey Optimizer para la generación de correos electrónicos:

* La calidad del contenido generado depende en gran medida del objetivo de marketing o indicación que se defina. Utilice indicaciones bien definidas para que el modelo GenAI las interprete con precisión. 
* Cargue el recurso de marca para disponer de contenido preciso y acorde con el contenido de la marca. Si no, el contenido se basa en información pública. El contenido cargado puede estar en los siguientes formatos: archivos PDF, JPEG, PNG o ZIP (con formatos de archivo compatibles).
* El tamaño máximo del recurso de marca cargado es de 50 MB.Los archivos más grandes o muchas imágenes pueden funcionar, pero aumenta el tiempo de procesamiento.
* Utilice las plantillas de correo electrónico creadas por Adobe Campaign, preferiblemente las [plantillas de correo electrónico integradas](../email/use-email-templates.md), una plantilla específica de la marca o una personalizada para crear el contenido de su correo electrónico. Se recomienda una plantilla de correo electrónico con un máximo de 8 a 10 imágenes.
* Asegúrese de notificar cualquier salida problemática utilizando los iconos de pulgar hacia arriba, pulgar hacia abajo o bandera al seleccionar variantes.
* El uso que se haga del asistente de IA está sujeto a las Directrices del usuario de IA generativa de Adobe Experience Cloud. [Más información](https://www.adobe.com/es/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

Las siguientes limitaciones se aplican al asistente de IA en Journey Optimizer:

* Solo se admite el idioma inglés.
* Solo está disponible para los canales de correo electrónico, push y SMS.
* El contenido de GenAI podría no ser siempre preciso: comparta sus comentarios para que nuestros ingenieros puedan perfeccionar los modelos.
* Puede cargar varios recursos de marca, pero solo puede utilizar uno para una generación específica.

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
<img alt="Generación de push" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>Generación de notificaciones push</strong></a>
</div>
<p></td>
</tr></table>
