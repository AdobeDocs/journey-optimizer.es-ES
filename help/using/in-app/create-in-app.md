---
title: Creación de una notificación en la aplicación en Journey Optimizer
description: Obtenga información sobre cómo crear un mensaje en la aplicación en Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: en la aplicación, mensaje, creación, inicio
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 97e925529f5b61138474d53f7df404ff6ea44ba9
workflow-type: tm+mt
source-wordcount: '1961'
ht-degree: 13%

---

# Creación de un mensaje en la aplicación  {#create-in-app}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_triggers"
>title="Activadores de administración en la aplicación"
>abstract="Controle de forma eficaz sus Activadores seleccionando los eventos y criterios específicos que activarán sus mensajes. Con el Generador de reglas, los usuarios pueden definir condiciones y valores precisos. Cuando se cumplen estas condiciones, inician una serie de acciones, incluido el envío de mensajes en la aplicación."

Puede añadir un mensaje en la aplicación en una campaña o en un recorrido. Siga los pasos detallados a continuación para crear un mensaje en la aplicación en ambos contextos.

Tenga en cuenta que los mensajes en la aplicación no se ven afectados por la opción del usuario de incluirse o excluirse de las notificaciones push en el sistema operativo.

>[!BEGINTABS]

>[!TAB Añadir un mensaje en la aplicación a un recorrido]

Para añadir un mensaje en la aplicación en un recorrido, siga estos pasos:

1. Abra el recorrido y, a continuación, arrastre y suelte un **[!UICONTROL En la aplicación]** actividad desde el **[!UICONTROL Acciones]** de la paleta.

   Cuando un perfil llega al final de su recorrido, los mensajes en la aplicación que se les muestren caducarán automáticamente. Por este motivo, se añade automáticamente una actividad de Espera después de la actividad en la aplicación para garantizar un tiempo de espera adecuado.

   ![](assets/in_app_journey_1.png)

1. Introduzca una **[!UICONTROL Etiqueta]** y **[!UICONTROL Descripción]** para el mensaje.

1. Elija la [Superficie en la aplicación](inapp-configuration.md) para usar.

   ![](assets/in_app_journey_2.png)

1. Ahora puede empezar a diseñar el contenido con **[!UICONTROL Editar contenido]** botón. [Más información](design-in-app.md)

1. Clic **[!UICONTROL Editar déclencheur]** para elegir los eventos y los criterios que almacenarán en déclencheur el mensaje. Los creadores de reglas permiten a los usuarios especificar criterios y valores que, cuando se cumplen, almacenan en déclencheur un conjunto de acciones, como enviar un mensaje en la aplicación.

   ![](assets/in_app_journey_4.png)

   1. Haga clic en el menú desplegable de evento para cambiar el Déclencheur si es necesario.

      +++Consulte los Déclencheur disponibles.

      | Paquete | Activador | Definición |
      |---|---|---|
      | Envío de datos a Platform | Datos enviados a Platform | Se activa cuando la aplicación móvil emite un evento de experiencia Edge para enviar datos a Adobe Experience Platform. Normalmente, la llamada de API [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) desde la extensión AEP Edge. |
      | Seguimiento principal | Seguimiento de acciones | Se activa cuando la funcionalidad heredada se ofrece en la API de código móvil [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction) se llama. |
      | Seguimiento principal | Estado de seguimiento | Se activa cuando la funcionalidad heredada se ofrece en la API de código móvil [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate) se llama. |
      | Seguimiento principal | Recopilar PII | Se activa cuando la funcionalidad heredada se ofrece en la API de código móvil [collectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii) se llama. |
      | Ciclo de aplicación | Inicio de aplicación | Se activa en cada ejecución, incluidos los bloqueos y las instalaciones. También se activa al reanudar desde segundo plano cuando se ha superado el tiempo de espera de la sesión de ciclo vital. |
      | Ciclo de aplicación | Instalación de aplicación | Se activa la primera vez que se ejecuta después de la instalación o reinstalación. |
      | Ciclo de aplicación | Actualización de aplicación | Se activa la primera vez que se ejecuta después de una actualización o cuando cambia el número de versión. |
      | Ciclo de aplicación | Cierre de aplicación | Se activa cuando se cierra la aplicación. |
      | Ciclo de aplicación | Bloqueo de aplicación | Se activa cuando la aplicación no se envía al segundo plano antes de cerrarse. El evento se envía cuando la aplicación se inicia después del bloqueo. Los informes de bloqueo de Adobe Mobile no implementan un controlador global de excepciones no detectadas. |
      | Places | Introducir POI | Se activa mediante el SDK de Places cuando el cliente introduce el punto de interés (POI) que ha configurado. |
      | Places | POI de salida | Se activa mediante el SDK de Places cuando el cliente sale del punto de interés (PDI) que ha configurado. |

+++

   1. Clic **[!UICONTROL Añadir condición]** si desea que el déclencheur considere varios eventos o criterios.

   1. Elija la **[!UICONTROL O]** condición si desea agregar más **[!UICONTROL Déclencheur]** para ampliar aún más la regla.

      ![](assets/in_app_create_3.png)

   1. Elija la **[!UICONTROL Y]** condición si desea agregar **[!UICONTROL Características]** y mejor afina tu regla.

      +++Consulte Características disponibles.

      | Paquete | Características | Definición |
      |---|---|---|
      | Información del dispositivo | Nombre del operador | Se activa cuando se cumple uno de los nombres de operador de la lista. |
      | Información del dispositivo | Nombre del dispositivo | Se activa cuando se cumple uno de los nombres de dispositivo. |
      | Información del dispositivo | Configuración regional | Se activa cuando se cumple uno de los idiomas de la lista. |
      | Información del dispositivo | Versión del SO | Se activa cuando se cumple una de las versiones del sistema operativo especificadas. |
      | Información del dispositivo | Versión anterior del sistema operativo | Se activa cuando se cumple una de las versiones anteriores del sistema operativo especificadas. |
      | Información del dispositivo | Modo de ejecución | Se activa si el modo de ejecución es aplicación o extensión. |
      | Ciclo de aplicación | ID de la aplicación | Se activa cuando se cumple el ID de aplicación especificado. |
      | Ciclo de aplicación | Día de la semana | Se activa cuando se cumple el día de la semana especificado. |
      | Ciclo de aplicación | Día desde el primer uso | Se activa cuando se alcanza el número de días especificado desde que se usó por primera vez. |
      | Ciclo de aplicación | Día desde el último uso | Se activa cuando se cumple el número de días especificado desde el último uso. |
      | Ciclo de aplicación | Día desde la actualización | Se activa cuando se alcanza el número de días especificado desde la última actualización. |
      | Ciclo de aplicación | Fecha de instalación | Se activa cuando se cumple la fecha de instalación especificada. |
      | Ciclo de aplicación | Inicios | Se activa cuando se alcanza el número especificado de inicios. |
      | Ciclo de aplicación | Hora del día | Se activa cuando se cumple la hora del día especificada. |
      | Places | Punto de interés actual | Se activa mediante el SDK de Places cuando el cliente introduce el punto de interés (PDI) especificado. |
      | Places | Último punto de interés | Activado por el SDK de Places en función del último punto de interés (PDI) introducido por el cliente. |
      | Places | Último PDI de salida | Se activa mediante el SDK de Places en función del último punto de interés (PDI) de salida del cliente. |

+++

      ![](assets/in_app_create_8.png)

   1. Clic **[!UICONTROL Crear grupo]** para agrupar déclencheur.

      ![](assets/in_app_journey_3.png)

   1. Elija la frecuencia del déclencheur cuando su mensaje en la aplicación esté activo:

      * **[!UICONTROL Mostrar cada vez]**: Mostrar siempre el mensaje cuando los eventos seleccionados en la **[!UICONTROL Déclencheur de aplicación móvil]** se produce la lista desplegable.
      * **[!UICONTROL Mostrar una vez]**: Mostrar solo este mensaje la primera vez que se seleccionen los eventos en la **[!UICONTROL Déclencheur de aplicación móvil]** se produce la lista desplegable.
      * **[!UICONTROL Mostrar hasta el clic]**: Muestra este mensaje cuando los eventos seleccionados en la **[!UICONTROL Déclencheur de aplicación móvil]** se producen hasta que el SDK envía un evento de interacción con una acción de &quot;clic&quot;.

1. Si es necesario, complete el flujo de recorrido arrastrando y soltando acciones o eventos adicionales. [Más información](../building-journeys/about-journey-activities.md)

1. Una vez que el mensaje en la aplicación esté listo, finalice la configuración y publique el recorrido para activarlo.

Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md).

>[!TAB Añadir un mensaje en la aplicación a una campaña]

Para añadir un mensaje en la aplicación en una campaña, siga estos pasos:

1. Acceda a la **[!UICONTROL Campañas]** y haga clic en **[!UICONTROL Crear campaña]**.

1. En el **[!UICONTROL Propiedades]** , seleccione cuando el tipo de ejecución de la campaña: Programada o activada por API. Obtenga más información acerca de los tipos de campañas en [esta página](../campaigns/create-campaign.md#campaigntype).

1. En el **[!UICONTROL Acciones]** , seleccione la **[!UICONTROL Mensaje en la aplicación]** y el **[!UICONTROL Superficie de aplicación]** previamente configurado para su mensaje en la aplicación. A continuación, haga clic en **[!UICONTROL Crear]**.

   Obtenga más información acerca de la configuración en la aplicación en [esta página](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Desde el **[!UICONTROL Propiedades]** , introduzca la **[!UICONTROL Título]** y el **[!UICONTROL Descripción]** descripción.

1. Para asignar etiquetas de uso de datos personalizadas o principales al mensaje en la aplicación, seleccione **[!UICONTROL Administrar acceso]**. [Más información](../administration/object-based-access.md).

1. Haga clic en **[!UICONTROL Seleccionar audiencia]** para definir la audiencia de destino a partir de la lista de audiencias de Adobe Experience Platform disponibles. [Más información](../audience/about-audiences.md).

   ![](assets/in_app_create_2.png)

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a los individuos de la audiencia seleccionada. [Más información](../event/about-creating.md#select-the-namespace).

1. Clic **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido y crear tratamientos para medir su rendimiento e identificar la mejor opción para la audiencia de destino. [Más información](../campaigns/content-experiment.md)

1. Clic **[!UICONTROL Editar déclencheur]** para elegir los eventos y los criterios que almacenarán en déclencheur el mensaje. Los creadores de reglas permiten a los usuarios especificar criterios y valores que, cuando se cumplen, almacenan en déclencheur un conjunto de acciones, como enviar un mensaje en la aplicación.

   1. Haga clic en el menú desplegable de evento para cambiar el Déclencheur si es necesario.

      +++Consulte los Déclencheur disponibles.

      | Paquete | Activador | Definición |
      |---|---|---|
      | Envío de datos a Platform | Datos enviados a Platform | Se activa cuando la aplicación móvil emite un evento de experiencia Edge para enviar datos a Adobe Experience Platform. Normalmente, la llamada de API [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) desde la extensión AEP Edge. |
      | Seguimiento principal | Seguimiento de acciones | Se activa cuando la funcionalidad heredada se ofrece en la API de código móvil [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction) se llama. |
      | Seguimiento principal | Estado de seguimiento | Se activa cuando la funcionalidad heredada se ofrece en la API de código móvil [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate) se llama. |
      | Seguimiento principal | Recopilar PII | Se activa cuando la funcionalidad heredada se ofrece en la API de código móvil [collectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii) se llama. |
      | Ciclo de aplicación | Inicio de aplicación | Se activa en cada ejecución, incluidos los bloqueos y las instalaciones. También se activa al reanudar desde segundo plano cuando se ha superado el tiempo de espera de la sesión de ciclo vital. |
      | Ciclo de aplicación | Instalación de aplicación | Se activa la primera vez que se ejecuta después de la instalación o reinstalación. |
      | Ciclo de aplicación | Actualización de aplicación | Se activa la primera vez que se ejecuta después de una actualización o cuando cambia el número de versión. |
      | Ciclo de aplicación | Cierre de aplicación | Se activa cuando se cierra la aplicación. |
      | Ciclo de aplicación | Bloqueo de aplicación | Se activa cuando la aplicación no se envía al segundo plano antes de cerrarse. El evento se envía cuando la aplicación se inicia después del bloqueo. Los informes de bloqueo de Adobe Mobile no implementan un controlador global de excepciones no detectadas. |
      | Places | Introducir POI | Se activa mediante el SDK de Places cuando el cliente introduce el punto de interés (POI) que ha configurado. |
      | Places | POI de salida | Se activa mediante el SDK de Places cuando el cliente sale del punto de interés (PDI) que ha configurado. |

+++

   1. Clic **[!UICONTROL Añadir condición]** si desea que el déclencheur considere varios eventos o criterios.

   1. Elija la **[!UICONTROL O]** condición si desea agregar más **[!UICONTROL Déclencheur]** para ampliar aún más la regla.

      ![](assets/in_app_create_3.png)

   1. Elija la **[!UICONTROL Y]** condición si desea agregar **[!UICONTROL Características]** y mejor afina tu regla.

      +++Consulte Características disponibles.

      | Paquete | Características | Definición |
      |---|---|---|
      | Información del dispositivo | Nombre del operador | Se activa cuando se cumple uno de los nombres de operador de la lista. |
      | Información del dispositivo | Nombre del dispositivo | Se activa cuando se cumple uno de los nombres de dispositivo. |
      | Información del dispositivo | Configuración regional | Se activa cuando se cumple uno de los idiomas de la lista. |
      | Información del dispositivo | Versión del SO | Se activa cuando se cumple una de las versiones del sistema operativo especificadas. |
      | Información del dispositivo | Versión anterior del sistema operativo | Se activa cuando se cumple una de las versiones anteriores del sistema operativo especificadas. |
      | Información del dispositivo | Modo de ejecución | Se activa si el modo de ejecución es aplicación o extensión. |
      | Ciclo de aplicación | ID de la aplicación | Se activa cuando se cumple el ID de aplicación especificado. |
      | Ciclo de aplicación | Día de la semana | Se activa cuando se cumple el día de la semana especificado. |
      | Ciclo de aplicación | Día desde el primer uso | Se activa cuando se alcanza el número de días especificado desde que se usó por primera vez. |
      | Ciclo de aplicación | Día desde el último uso | Se activa cuando se cumple el número de días especificado desde el último uso. |
      | Ciclo de aplicación | Día desde la actualización | Se activa cuando se alcanza el número de días especificado desde la última actualización. |
      | Ciclo de aplicación | Fecha de instalación | Se activa cuando se cumple la fecha de instalación especificada. |
      | Ciclo de aplicación | Inicios | Se activa cuando se alcanza el número especificado de inicios. |
      | Ciclo de aplicación | Hora del día | Se activa cuando se cumple la hora del día especificada. |
      | Places | Punto de interés actual | Se activa mediante el SDK de Places cuando el cliente introduce el punto de interés (PDI) especificado. |
      | Places | Último punto de interés | Activado por el SDK de Places en función del último punto de interés (PDI) introducido por el cliente. |
      | Places | Último PDI de salida | Se activa mediante el SDK de Places en función del último punto de interés (PDI) de salida del cliente. |

+++

      ![](assets/in_app_create_8.png)

   1. Clic **[!UICONTROL Crear grupo]** para agrupar déclencheur.

1. Elija la frecuencia del déclencheur cuando su mensaje en la aplicación esté activo. Las opciones disponibles son las siguientes:

   * **[!UICONTROL Siempre]**: Mostrar siempre el mensaje cuando los eventos seleccionados en la **[!UICONTROL Déclencheur de aplicación móvil]** se produce la lista desplegable.
   * **[!UICONTROL Una]**: Mostrar solo este mensaje la primera vez que se seleccionen los eventos en la **[!UICONTROL Déclencheur de aplicación móvil]** se produce la lista desplegable.
   * **[!UICONTROL Hasta el clic]**: Muestra este mensaje cuando los eventos seleccionados en la **[!UICONTROL Déclencheur de aplicación móvil]** se producen hasta que el SDK envía un evento de interacción con una acción de &quot;clic&quot;.
   * **[!UICONTROL X número de veces]**: muestra este mensaje X vez.

1. Si es necesario, elija cuál **[!UICONTROL Día de la semana]** o **[!UICONTROL Hora del día]** se muestra el mensaje en la aplicación.

1. Las campañas están diseñadas para ejecutarse en una fecha específica o en una frecuencia recurrente. Obtenga información sobre cómo configurar el **[!UICONTROL Programación]** de la campaña en [esta sección](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Ahora puede empezar a diseñar el contenido con **[!UICONTROL Editar contenido]** botón. [Más información](design-in-app.md)

   ![](assets/in_app_create_4.png)

>[!ENDTABS]

## Vídeotutoriales{#video}

* El siguiente vídeo muestra cómo crear, configurar y publicar mensajes en la aplicación en sus campañas.

  +++Consulte el vídeo

  >[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)

+++

* El siguiente vídeo muestra cómo configurar y analizar experimentos de contenido para probar mensajes en la aplicación A/B.

  +++Consulte el vídeo

  >[!VIDEO](https://video.tv.adobe.com/v/3419898)

+++

* El siguiente vídeo muestra cómo crear un mensaje en la aplicación en un recorrido y cómo probar y publicar el recorrido.

  +++Consulte el vídeo

  >[!VIDEO](https://video.tv.adobe.com/v/3423077)

+++

**Temas relacionados:**

* [Diseño de un mensaje en la aplicación](design-in-app.md)
* [Prueba y envío de un mensaje en la aplicación](send-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report.md#inapp-report)
* [Configuración en la aplicación](inapp-configuration.md)