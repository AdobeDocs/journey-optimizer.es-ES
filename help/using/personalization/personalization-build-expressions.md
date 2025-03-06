---
solution: Journey Optimizer
product: journey optimizer
title: Acerca del editor de personalización
description: Aprenda a trabajar con el editor de personalización.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor, about, start
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: ff6619925a36d2687922d1b631d1cabbcb98167e
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 6%

---

# Introducción al editor de personalización {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Acerca del editor de personalización"
>abstract="El editor de personalización permite seleccionar, organizar, personalizar y validar todos los datos para crear una personalización ajustada del contenido."

El editor de personalización es la pieza central de la personalización en [!DNL Journey Optimizer]. Está disponible en todos los contextos en los que necesita definir la personalización, como correos electrónicos, notificaciones push y ofertas.

En la interfaz del editor de personalización, se seleccionan, organizan, personalizan y validan todos los datos para crear una personalización personalizada para el contenido.

![](assets/perso_ee1.png)

## Fuentes de Personalization {#sources}

La parte izquierda de la pantalla muestra un selector de dominio que le permite seleccionar el origen de la personalización. Los orígenes disponibles son:

* **[!UICONTROL Atributos de perfil]** : enumera todas las referencias asociadas al esquema de perfil que se describen en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.
* **[!UICONTROL Audiencias]** : enumera todas las audiencias creadas en el servicio de segmentación de Adobe Experience Platform. Más información sobre la segmentación disponible [aquí](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=es){target="_blank"}.
* **[!UICONTROL Decisiones de oferta]** : enumera todas las ofertas asociadas a una ubicación específica. Seleccione la ubicación e inserte las ofertas en el contenido. Para obtener una documentación completa sobre cómo administrar ofertas, consulte [esta sección](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL Atributos contextuales]**: cuando se utiliza una actividad de acción del canal (correo electrónico, push, SMS) en un recorrido o una campaña, los atributos contextuales relacionados con eventos y propiedades están disponibles para personalización. En [esta sección](personalization-use-case.md) se presenta un ejemplo de personalización que aprovecha atributos contextuales.

>[!NOTE]
>
>Si va a segmentar una audiencia con atributos de enriquecimiento generados mediante un flujo de trabajo de composición, puede aprovechar estos atributos de enriquecimiento para personalizar el mensaje. [Aprenda a utilizar los atributos de enriquecimiento de audiencias](../audience/about-audiences.md#enrichment)

## Adición de personalización {#add}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="Autocompletar"
>abstract="Alternar esta opción permite al sistema sugerir y completar automáticamente el código mientras escribe. Esta función solo está disponible para formatos HTML y Texto y admite atributos de Perfil y Contexto. Si se deshabilita mediante la opción, el editor proporcionará finalización automática de código HTML nativo en su lugar."

En el espacio de trabajo central se crea la sintaxis de personalización. Para utilizar un atributo para personalizar el mensaje, localícelo en el panel de navegación izquierdo y haga clic en el botón `+` para agregarlo a la expresión.

El menú de los tres puntos situado junto al icono `+` le permite obtener más información sobre cada atributo y agregar a los favoritos los atributos utilizados con más frecuencia. Se puede acceder a los atributos agregados a favoritos desde el menú **[!UICONTROL Favoritos]** del panel de navegación izquierdo.

Además, puede definir el texto de reserva predeterminado que se mostrará si un atributo de perfil de tipo cadena está vacío. Para ello, haga clic en el botón de puntos suspensivos situado junto al atributo y seleccione **[!UICONTROL Insertar con texto de reserva]**. Escriba el texto que debería mostrarse de forma predeterminada si el valor del atributo está vacío para un perfil y, a continuación, haga clic en **[!UICONTROL Agregar]**.

![](assets/attribute-details.png)

En el siguiente ejemplo, el editor de personalización le permite seleccionar los perfiles que tienen su cumpleaños hoy y luego completar la personalización insertando una oferta específica correspondiente a este día.

![](assets/perso_ee2.png)

## Herramientas para editar expresiones

El espacio de trabajo central proporciona varias herramientas para ayudarle a escribir su expresión de personalización.

![](assets/perso-workspace.png)

Entre las opciones disponibles se encuentran:

1. **[!UICONTROL Buscar]** / **[!UICONTROL Buscar y reemplazar]**: Busca a través de tu expresión y reemplaza automáticamente partes de código.
1. **[!UICONTROL Deshacer]** / **[!UICONTROL Rehacer]**: Deshacer / Rehacer la última operación.
1. **[!UICONTROL Completar automáticamente]**: sugiere y completa automáticamente el código mientras escribe. Esta función solo está disponible para formatos HTML y Texto y admite atributos de Perfil y Contexto. Si se deshabilita mediante la opción, el editor proporcionará finalización automática de código HTML nativo en su lugar.

   ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"}

1. **[!UICONTROL HTML]** / **[!UICONTROL JSON]** / **[!UICONTROL Text]**: identifique el formato de su código. Esto permite al sistema adaptar la función de validación y autocompletar en función del idioma seleccionado.
1. **[!UICONTROL Validar]**: compruebe la sintaxis de su expresión. Obtenga más información en [esta sección](personalization-validation.md).
1. **[!UICONTROL Guardar como fragmento]**: guarde la expresión como un fragmento de expresión. Obtenga más información en [esta sección](../content-management/save-fragments.md#save-as-expression-fragment)
1. **[!UICONTROL Tamaño de fuente]**: Ajusta el tamaño de fuente del contenido dentro del editor para mejorar la legibilidad.
1. **[!UICONTROL Ajuste de palabras]**: habilita o deshabilita el ajuste de palabras, lo que permite que las expresiones largas se muestren en una sola línea o se ajusten dentro del editor. Las opciones incluyen:
   * **Desactivado** (Predeterminado) - Sin ajuste de palabras. Las líneas largas se extienden más allá de la vista del editor y requieren un desplazamiento horizontal.
   * **Activado**: ajusta líneas en la anchura del editor.
   * **Columna de ajuste de línea**: ajusta las líneas cuando los caracteres de una línea alcanzan los 80 caracteres.
   * **Redondeado**: ajusta las líneas en la anchura del editor o en 80 caracteres, el valor que sea menor.

En el panel de navegación, hay disponibles funciones adicionales que le ayudarán a crear su expresión de personalización.

![](assets/perso-features.png)

* **[!UICONTROL Funciones de ayuda]**: las funciones de ayuda le permiten realizar operaciones en los datos, como cálculos, conversiones o formato de datos, condiciones y manipularlos en el contexto de la personalización. [Más información sobre las funciones de ayuda disponibles](functions/functions.md)

* **[!UICONTROL Favoritos]**: los atributos que agregó a los favoritos se muestran en esta lista. Esto le permite acceder rápidamente a los elementos utilizados con más frecuencia. Para agregar un atributo a tus favoritos, haz clic en el menú de los tres puntos y elige **[!UICONTROL Agregar a favoritos]**.

* **[!UICONTROL Condiciones]**: aproveche las reglas condicionales creadas en la biblioteca para agregar contenido dinámico a los mensajes. Esto le permite crear varias variantes del mensaje en función de las condiciones. [Aprenda a crear contenido dinámico](../personalization/get-started-dynamic-content.md)

* **[!UICONTROL Fragmentos]**: aproveche los fragmentos de expresiones que se han creado o guardado en la zona protegida actual. Un fragmento es un componente reutilizable al que se puede hacer referencia en [!DNL Journey Optimizer] campañas y recorridos. Esta funcionalidad permite generar previamente varios bloques de contenido personalizados que los usuarios de marketing pueden utilizar para ensamblar contenido rápidamente en un proceso de diseño mejorado. [Aprenda a utilizar fragmentos de expresiones para la personalización](../personalization/use-expression-fragments.md)

Una vez que la expresión personalizada está lista, el editor de personalización debe validarla. Obtenga más información en [esta sección](personalization-validation.md).
