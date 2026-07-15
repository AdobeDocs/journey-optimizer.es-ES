---
solution: Journey Optimizer
product: journey optimizer
title: Personalización del contenido en Journey Optimizer
description: Introducción a la personalización.
feature: Personalization
topic: Personalization
role: Developer
level: Beginner
keywords: expresión, editor, inicio, personalización
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: id: a757b957-83f3-4a4d-9775-a93854f84f77id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1403
ht-degree: 11%

---

# Introducción a la personalización{#add-personalization}

>[!BEGINSHADEBOX]

**En esta página:** Empiece a utilizar la personalización en Adobe Journey Optimizer, incluido cómo funciona el editor de personalización, los datos de perfil que puede utilizar, el área de reproducción de aprendizaje y la edición en línea.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personalización de experiencias"
>abstract="Utilice **Adobe Journey Optimizer** para adaptar los mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Pueden ser sus nombres, intereses, dónde viven, qué compraron, etc."

Las funcionalidades de personalización de [!DNL Adobe Journey Optimizer] le permiten adaptar los mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Pueden ser sus nombres, intereses, dónde viven, qué compraron, etc.

## Funcionamiento de la personalización

Con el **editor de personalización**, puede seleccionar, organizar, personalizar y validar todos los datos para crear una personalización personalizada para el contenido y aprovechar varias herramientas, como funciones de ayuda o expresiones predefinidas, para adaptar los mensajes de forma eficaz.

Journey Optimizer emplea una sintaxis de personalización en línea basada en Handlebars, que le permite crear expresiones con contenido entre llaves dobles **`{{}}`**.

Al procesar el mensaje, Journey Optimizer reemplaza la expresión por los datos contenidos en el conjunto de datos de Experience Platform. Por ejemplo, `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` se convierte dinámicamente en `Hello John Doe`. Con esta sintaxis, puede personalizar los mensajes en varios campos, incluidas las líneas de asunto de los correos electrónicos, los cuerpos de los mensajes, las notificaciones push o las direcciones URL.

## Datos utilizados para la personalización

Personalization se basa en los datos de perfil que administra el esquema **XDM Individual Profile** definido en Adobe Experience Platform. El esquema **XDM Individual Profile** es el único esquema que puede usar para personalizar el contenido en [!DNL Journey Optimizer]. Obtenga más información en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

También puede aprovechar **atributos calculados** para personalizar su contenido. Los atributos calculados permiten resumir eventos de comportamiento individuales en atributos de perfil calculados disponibles en Adobe Experience Platform. [Aprenda a trabajar con atributos calculados](../audience/computed-attributes.md)

Además, [!DNL Journey Optimizer] le permite aprovechar datos de Adobe Experience Platform en el editor de personalización para personalizar su contenido. Para ello, los conjuntos de datos necesarios para la personalización de la búsqueda deben habilitarse primero mediante una llamada de la API. Una vez finalizado, puede utilizar sus datos para personalizar el contenido en Journey Optimizer. Actualmente, esta funcionalidad está disponible en la versión beta. [Más información](../personalization/aep-data-perso.md)

## Aprenda y experimente con la personalización {#playground}

**[!DNL Adobe Journey Optimizer]** incluye una herramienta interactiva diseñada para ayudarle a aprender y experimentar con las capacidades de personalización.

Este área de reproducción proporciona un entorno simulado para escribir y probar código de personalización mediante datos de muestra sin requerir conjuntos de datos en directo. Puede aprovechar muestras de código predefinidas, editar cargas útiles de perfil ficticio y previsualizar la salida del código de personalización en tiempo real.

![área de reproducción de personalización](assets/playground.png)

➡️ [Acceso al área de reproducción de personalización](https://experienceleague.adobe.com/en/apps/journey-optimizer/ajo-personalization){target="_blank"}

## El Asistente de IA para expresiones de personalización {#ai-personalization-expressions}

En **[!UICONTROL Personalization Editor]** o en la barra de herramientas de Email Designer (**[!UICONTROL Agregar expresión]**), **[!UICONTROL AI Assistant]** le ayuda a generar nuevas expresiones a partir del lenguaje natural, a explicar qué hace el código existente y a corregir problemas en una selección, y a aplicar la salida cuando coincida con su intención.

![](../content-management/assets/ai-perso-generate.png)

➡️ [Aprenda a trabajar con el Asistente de IA para expresiones Personalization](../content-management/generative-personalization-expressions.md)

## Edición en línea de atributos de perfil {#inline-personalization}

Puede insertar expresiones de atributos de perfil directamente al editar contenido en el editor de **correo electrónico de Designer** o **canal push**, sin abrir el editor de personalización completo.

Para ello, siga estos pasos:

1. Escriba `{{` en cualquier campo de texto. Se abrirá un menú desplegable de autocompletar en línea en la posición del cursor.
1. Empiece a escribir para filtrar los atributos de perfil disponibles.
1. Seleccione el atributo que necesite: se inserta como un token de personalización en la posición del cursor.

![](assets/inline-profile-attributes.png)

## Profundicemos

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
<a href="../personalization/personalization-recipes.md">
<img alt="Poco frecuente" src="assets/do-not-localize/uc.png">
</a>
<div>
<a href="../personalization/personalization-recipes.md"><strong>recetas de Personalization</strong></a>
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

Descubra más tutoriales en vídeo sobre funciones de personalización y prácticas recomendadas en [tutoriales de Personalization](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/personalize-content/personalization-editor-overview){target="_blank"}

## Referencia rápida {#quick-reference}

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

>[!BEGINTABS]

>[!TAB Información general]

**TL;DR**

Esta página presenta la personalización en Journey Optimizer: cómo funciona el editor de personalización basado en Handlebars, qué datos utiliza, el área de reproducción interactiva, el asistente de IA para expresiones y la edición de atributos en línea en el editor de correo electrónico Designer y push.

**Intenciones**

* Descubra cómo funciona la personalización de Journey Optimizer (sintaxis de Handlebars con llaves dobles)
* Identifique las fuentes de datos disponibles para la personalización (esquema de perfil individual XDM, atributos calculados, búsqueda de conjuntos de datos AEP en versión beta)
* Experimente con la personalización mediante el área de reproducción interactiva sin una zona protegida en directo
* Utilice el asistente de IA para generar, explicar o corregir expresiones de personalización a partir del lenguaje natural
* Inserte atributos de perfil en línea en el editor de correo electrónico Designer o push escribiendo `{{`

>[!TAB Glosario]

* **Editor de Personalization**: La herramienta con todas las funciones para crear, personalizar y validar expresiones de personalización; disponible en cualquier campo de Journey Optimizer que admita personalización. *(específico del producto)*
* **Esquema de perfil individual de XDM**: El único esquema que se puede usar para personalizar el contenido en Journey Optimizer; define todos los atributos de perfil disponibles para la personalización. *(específico del producto)*
* **Atributos calculados**: atributos de perfil precalculados que resumen eventos de comportamiento individuales en valores de nivel de perfil; disponibles como datos de personalización junto con campos de perfil XDM estándar. *(específico del producto)*
* **Personalization playground**: un entorno interactivo y simulado en Experience League para escribir y probar código de personalización con datos de muestra; no se requieren conjuntos de datos activos ni zonas protegidas. *(específico del producto)*
* **Edición en línea**: la capacidad de escribir `{{` en cualquier campo de texto del editor de canales push o de correo electrónico para almacenar en déclencheur un menú desplegable de autocompletar e insertar atributos de perfil sin abrir el editor de personalización completo. *(específico del producto)*
* **Asistente de IA (expresiones de personalización)**: herramienta de IA del editor de personalización y Designer de correo electrónico que genera expresiones de personalización a partir del lenguaje natural, explica el código existente y corrige los problemas de una selección. *(específico del producto)*

>[!TAB Terminología]

* **Nombre canónico:** personalización — variantes: personalización de contenido, personalización de mensajes, personalización de expresiones
* **Nombre canónico:** editor de personalización — variantes: funcionalidades de personalización
* **No confundir:** El editor de Personalization (utilizado para generar expresiones de contenido en mensajes y ofertas, admite Handlebars y PQL) ≠ el editor de expresiones avanzadas (utilizado en el recorrido para condiciones en fuentes de datos e información de eventos, actividades de espera personalizadas y asignación de parámetros de acción) proporciona funciones y operadores integrados que difieren de los del editor de personalización
* **No confunda:** edición en línea (escriba `{{` en Email Designer o Push para inserción rápida de atributos sin abrir el editor completo) ≠ editor de personalización (herramienta completa para expresiones complejas, funciones de ayuda, reglas condicionales y fragmentos)
* **No confunda:** esquema de perfil individual XDM (el único esquema utilizable para la personalización en Journey Optimizer) ≠ otros esquemas AEP (no utilizable para la personalización a menos que se exponga mediante la búsqueda de conjuntos de datos)

>[!TAB Protecciones y limitaciones]

* El esquema Perfil individual de XDM es el único esquema que se puede utilizar para personalizar el contenido en Journey Optimizer.
* La búsqueda de conjuntos de datos de AEP para la personalización requiere que los conjuntos de datos se habiliten mediante una llamada de API antes de su uso; esta función está actualmente en fase beta.
* La edición en línea (que escribe `{{` en el Designer de correo electrónico o el editor push) solo admite atributos de perfil.

>[!TAB Preguntas más frecuentes]

**Q: ¿Qué datos se pueden usar para la personalización en Journey Optimizer?**

Los datos de perfil del esquema Perfil individual de XDM, los atributos calculados (eventos de comportamiento resumidos en el nivel de perfil) y la búsqueda de conjuntos de datos de registro de AEP (actualmente beta) requieren que los conjuntos de datos se habiliten mediante API.

**Q: ¿Qué es el área de reproducción de personalización?**

Un entorno interactivo y simulado en Experience League donde puede escribir y probar código de personalización con datos de ejemplo, sin necesidad de una zona protegida de Journey Optimizer activa o conjuntos de datos reales.

**Q: ¿Cómo funciona la edición de atributos en línea?**

Escriba `{{` en cualquier campo de texto del editor de canales push o de correo electrónico de Designer para abrir un menú desplegable de autocompletar en la posición del cursor. Empiece a escribir para filtrar los atributos de perfil y, a continuación, seleccione uno para insertarlo como token de personalización. Solo los atributos de perfil están disponibles en línea.

**Q: ¿Qué puede hacer el Asistente de IA en el editor de personalización?**

Puede generar nuevas expresiones de personalización a partir de descripciones en lenguajes naturales, explicar lo que hace el código existente y corregir problemas en una expresión seleccionada. A continuación, aplique el resultado cuando coincida con la intención.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 248b894f -->
