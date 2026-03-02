---
solution: Journey Optimizer
product: journey optimizer
title: Acceso al Asesor de contenido de Adobe Experience Manager
description: Obtenga información sobre cómo acceder al Asesor de contenido de Adobe Experience Manager y utilizarlo para descubrir recursos y fragmentos de contenido mediante la búsqueda semántica basada en IA en Adobe Journey Optimizer.
feature: Content Management
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
source-git-commit: 4576362dc6e5cd75fa19a8d4e9403db8f1e025af
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---


# Trabajar con el Asesor de contenido de Adobe Experience Manager {#aem-content-advisor}

>[!AVAILABILITY]
>
>El Asesor de contenido de Adobe Experience Manager solo está disponible en los flujos de trabajo de creación de canales.

El Asesor de contenido de Adobe Experience Manager sustituye la detección determinista por la detección estandarizada por intención desde una superficie unificada. Permite descubrir de forma unificada y con tecnología de IA fragmentos de contenido y Assets directamente en los flujos de trabajo de creación de Journey Optimizer, lo que mejora la productividad de los expertos en marketing y la eficacia de las campañas.

## Funciones disponibles

### Para Assets {#asset-features}

El Asesor de contenido de Adobe Experience Manager proporciona las siguientes funciones de recursos:

* &#x200B;
  +++ Búsqueda semántica de IA

  Busque recursos utilizando un lenguaje natural en lugar de palabras clave o nombres de archivo exactos. Describa lo que necesita en un lenguaje sencillo, por ejemplo, &quot;café en las montañas&quot;, y la IA encontrará recursos relevantes para el contexto en función del significado y el contenido, no solo coincidencias de texto.

  ![](assets/content-advisor-2.png){zoomable="yes"}

  +++

* &#x200B;
  +++ Historial de búsqueda reciente

  Acceda a sus búsquedas recientes para reutilizar rápidamente palabras clave y contextos. Esto ahorra tiempo al trabajar en campañas similares o cuando necesita refinar las búsquedas anteriores.

  ![](assets/content-advisor-4.png){zoomable="yes"}

  +++ 

* &#x200B;
  +++ Cargar informe

  Cargue un documento de información de marketing para que aparezcan automáticamente los recursos que se alinean con el contexto de la campaña. La API analiza el informe y sugiere activos relevantes en función del contenido y los requisitos descritos en el documento.

  ![](assets/content-advisor-5.png){zoomable="yes"}

  +++

* &#x200B;
  +++ Panel de información de recursos

  Vea metadatos y propiedades detallados de cualquier recurso que use el icono **Información**. Esto incluye dimensiones de recursos, tamaño de archivo, fecha de creación, etiquetas y otra información relevante para ayudarle a tomar decisiones informadas.

  ![](assets/content-advisor-6.png){zoomable="yes"}

  +++

* &#x200B;
  +++ Panel de Dynamic Media

  Acceda a representaciones dinámicas, recortes inteligentes y modificaciones sobre la marcha en función de la configuración del repositorio.

  ![](assets/content-advisor-1.png){zoomable="yes"}

  El panel Dynamic Media proporciona acceso a representaciones dinámicas, recortes inteligentes y modificaciones sobre la marcha. Puede introducir modificadores directamente en el panel para crear representaciones personalizadas.

  **Disponibilidad**

  La disponibilidad de Dynamic Media depende de la configuración del repositorio:

   * **Scene7**: disponible para los recursos publicados (excepto Vídeo y PDF). [Más información sobre los modificadores de Scene7 de Dynamic Media](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-is-http-modifiers.html){target="_blank"}

   * **OpenAPI**: disponible para recursos aprobados (excepto vídeo). [Más información sobre Dynamic Media con modificadores OpenAPI](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/image-profiles.html){target="_blank"}

   * **Tanto Scene7 como OpenAPI**: disponibles cuando existen ambas configuraciones y el recurso cumple los criterios.

  **Selección de pila**

  Los botones que vea dependen de la configuración del repositorio:

   * **Solo botón de Scene7**: El repositorio tiene la configuración de Scene7 y el recurso se ha publicado en Dynamic Media.
   * **Solo botón OpenAPI**: El repositorio tiene la configuración OpenAPI y el recurso se ha aprobado.
   * **Ambos botones**: El repositorio tiene ambas configuraciones y el recurso se ha publicado y aprobado.
  +++

### Para fragmento de contenido {#content-fragment-features}

El Asesor de contenido de Adobe Experience Manager proporciona las siguientes funciones de fragmento de contenido:

* &#x200B;
  +++ Listado de vista de plantilla 

  Cambie entre las vistas de miniaturas y tablas para examinar los fragmentos de contenido en el formato que mejor se adapte a su flujo de trabajo. La vista de miniaturas proporciona un contexto visual, mientras que la vista de tabla muestra información detallada en un formato estructurado.

  ![](assets/content-advisor-7.png){zoomable="yes"}

  +++

* &#x200B;
  +++ Panel Información 

  Haga clic en el icono **[!UICONTROL Información]** para abrir un panel derecho que muestre las variaciones de fragmentos, las propiedades y los detalles de **[!UICONTROL Referido por]**. La sección **[!UICONTROL Referido por]** muestra todas las entidades de Adobe Experience Manager donde se usa el fragmento, con vínculos para ver estas referencias directamente en Adobe Experience Manager.

  ![](assets/content-advisor-8.png){zoomable="yes"}

  +++

* &#x200B;
  +++ Abrir en Adobe Experience Manager

  Abra rápidamente cualquier fragmento de contenido directamente en Adobe Experience Manager para editarlo mediante el icono situado junto al título. Esta integración perfecta le permite cambiar entre Journey Optimizer y Adobe Experience Manager sin perder contexto.

  ![](assets/content-advisor-9.png){zoomable="yes"}

  +++

* &#x200B;
  +++ Previsualización de JSON

  Previsualice la estructura JSON de los fragmentos de contenido en un formato de tabla limpio y organizado. Esto le ayuda a comprender la estructura de datos del fragmento y a verificar el contenido antes de utilizarlo en sus campañas.

  ![](assets/content-advisor-10.png){zoomable="yes"}

  +++

## Acceso al Asesor de contenido de Adobe Experience Manager {#access}

Para acceder al Asesor de contenido de Adobe Experience Manager en Journey Optimizer, siga estos pasos:

1. Cree una campaña en Adobe Journey Optimizer y añada una acción de canal, por ejemplo, Correo electrónico.

1. Haga clic en **[!UICONTROL Editar contenido]** y, a continuación, haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]** para abrir el editor de contenido.

1. Arrastre y suelte un componente HTML o Texto en el contenido del correo electrónico.

1. Pase el ratón sobre el componente y haga clic en **[!UICONTROL Mostrar el código fuente]** (para componentes de HTML) o **[!UICONTROL Agregar Personalization]** (para componentes de texto).

1. En el Editor de Personalization, elija el punto de entrada de contenido:

   * Para agregar un recurso, haga clic en **[!UICONTROL Assets]** y luego en **[!UICONTROL Abrir el selector de recursos]**.

     ![](assets/content-advisor-11.png){zoomable="yes"}

   * Para agregar un fragmento de contenido de Adobe Experience Manager, haga clic en **[!UICONTROL Fragmento de contenido de AEM]** y luego en **[!UICONTROL Abrir el selector de CF de AEM]**.

     ![](assets/content-advisor-12.png){zoomable="yes"}

1. Seleccione el repositorio de Adobe Experience Manager.

   ![](assets/content-advisor-13.png){zoomable="yes"}

1. Explore y seleccione el recurso o el fragmento de contenido que desea utilizar y, a continuación, insértelo en el contenido.


