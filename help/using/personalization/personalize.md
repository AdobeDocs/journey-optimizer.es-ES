---
solution: Journey Optimizer
product: journey optimizer
title: Personalización del contenido en Journey Optimizer
description: Introducción a la personalización.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: expresión, editor, inicio, personalización
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 5b8d26b4fbc323308b5a49672f9d30298756ccf9
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 25%

---

# Introducción a la personalización{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personalización de experiencias"
>abstract="Utilice **Adobe Journey Optimizer** para adaptar los mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Pueden ser sus nombres, intereses, dónde viven, qué compraron, etc."

Las funcionalidades de personalización de [!DNL Adobe Journey Optimizer] le permiten adaptar los mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Pueden ser sus nombres, intereses, dónde viven, qué compraron, etc.

## Funcionamiento de la personalización

Con el **editor de personalización**, puede seleccionar, organizar, personalizar y validar todos los datos para crear una personalización personalizada para el contenido y aprovechar varias herramientas, como funciones de ayuda o expresiones predefinidas, para adaptar los mensajes de forma eficaz.

Journey Optimizer emplea una sintaxis de personalización en línea basada en Handlebars, que le permite crear expresiones con contenido entre llaves dobles **{{}}{{}}**.

Al procesar el mensaje, Journey Optimizer reemplaza la expresión por los datos contenidos en el conjunto de datos de Experience Platform. Por ejemplo, `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` se convierte dinámicamente en `Hello John Doe`.

Con esta sintaxis, puede personalizar los mensajes en varios campos, incluidas las líneas de asunto de los correos electrónicos, los cuerpos de los mensajes, las notificaciones push o las direcciones URL.

## Datos utilizados para la personalización

Personalization se basa en los datos de perfil que administra el esquema **XDM Individual Profile** definido en Adobe Experience Platform. El esquema **XDM Individual Profile** es el único esquema que puede usar para personalizar el contenido en [!DNL Journey Optimizer]. Obtenga más información en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

También puede aprovechar **atributos calculados** para personalizar su contenido. Los atributos calculados permiten resumir eventos de comportamiento individuales en atributos de perfil calculados disponibles en Adobe Experience Platform. [Aprenda a trabajar con atributos calculados](../audience/computed-attributes.md)

Además, [!DNL Journey Optimizer] le permite aprovechar datos de Adobe Experience Platform en el editor de personalización para personalizar su contenido. Para ello, los conjuntos de datos necesarios para la personalización de la búsqueda deben habilitarse primero mediante una llamada de la API. Una vez finalizado, puede utilizar sus datos para personalizar el contenido en Journey Optimizer. Actualmente, esta funcionalidad está disponible en la versión beta. [Más información](../personalization/lookup-aep-data.md)

## Aprenda y experimente con la personalización {#playground}

**[!DNL Adobe Journey Optimizer]** incluye una herramienta interactiva diseñada para ayudarle a aprender y experimentar con las capacidades de personalización.

Este área de reproducción proporciona un entorno simulado para escribir y probar código de personalización mediante datos de muestra sin requerir conjuntos de datos en directo. Puede aprovechar muestras de código predefinidas, editar cargas útiles de perfil ficticio y previsualizar la salida del código de personalización en tiempo real.

![área de reproducción de personalización](assets/playground.png)

➡️ [Acceso al área de reproducción de personalización](https://experienceleague.adobe.com/en/apps/journey-optimizer/ajo-personalization){target="_blank"}

## Vamos a profundizar

Ahora que comprende la personalización de **[!DNL Journey Optimizer]**, es hora de profundizar en estas secciones de documentación para comenzar a trabajar con la función.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="personalization-build-expressions.md">
<img alt="añadir personalización" src="assets/do-not-localize/add.png">
</a>
<div>
<a href="personalization-build-expressions.md"><strong>Adición de personalización</strong></a>
</div>
<p>
</td>
<td>
<a href="../personalization/personalization-syntax.md">
<img alt="Posible cliente" src="assets/do-not-localize/syntax.png">
</a>
<div><a href="../personalization/personalization-syntax.md"><strong>Sintaxis de Personalization</strong>
</div>
<p>
</td>
<td>
<a href="../personalization/functions/functions.md">
<img alt="Poco frecuente" src="assets/do-not-localize/functions.png">
</a>
<div>
<a href="../personalization/functions/functions.md"><strong>Lista de funciones de ayuda</strong></a>
</div>
<p></td>
<td>
<a href="../personalization/personalization-use-case.md">
<img alt="Poco frecuente" src="assets/do-not-localize/uc.png">
</a>
<div>
<a href="../personalization/personalization-use-case.md"><strong>Casos de uso de Personalization</strong></a>
</div>
<p></td>
</tr></table>

## Vídeotutoriales{#video-perso}

Aprenda a utilizar la información de evento contextual de un recorrido para personalizar un mensaje.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Obtenga información sobre cómo añadir una personalización basada en perfiles a un mensaje y cómo utilizar el abono a un público como condición previa a un bloque de personalización.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

Aprenda a aprovechar el patio del editor de personalización para escribir y probar el código de personalización con datos de ejemplo.

>[!VIDEO](https://video.tv.adobe.com/v/3457868?quality=12)
