---
title: Creación de tarjetas de contenido
description: Aprenda a crear tarjetas de contenido y editar su contenido en Journey Optimizer
topic: Content Management
feature: Content Cards
role: User
level: Beginner
exl-id: a26bb3bd-d593-466b-9852-94e194d6d2b7
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: cc5c44e2-54a1-4927-b794-442cd87d8f74
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
source-git-commit: e41af203a353dd0c5f34c5c9f1915892e7c95999
workflow-type: tm+mt
source-wordcount: 1755
ht-degree: 10%

---

# Creación de tarjetas de contenido {#create-content-card}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_content_card"
>title="Acción de tarjeta de contenido"
>abstract="Una acción de entrada de tarjeta de contenido muestra una tarjeta de contenido a los perfiles cuando llegan a este paso del recorrido. La etiqueta identifica la actividad en el lienzo de recorrido y la acción hace referencia a una configuración de tarjeta de contenido que define el contenido mostrado. La sección **Optimization** puede incluir experimentos de contenido o reglas de segmentación. Se inserta automáticamente un nodo **Wait** después de esta actividad (de forma predeterminada, 3 días), lo que da a los perfiles tiempo para ver la tarjeta de contenido."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/about-journey-building/journey-action#add-action" text="Introducción a las acciones del canal"


Las tarjetas de contenido son experiencias entrantes en la aplicación que muestran contenido personalizado (como promociones, anuncios o recomendaciones) directamente en una superficie dedicada de la aplicación móvil. A diferencia de los mensajes interrumpidos, permanecen disponibles en la aplicación hasta que el usuario los descarta o las reglas de envío los ocultan.

En esta página se explica cómo crear una tarjeta de contenido y definir su contenido, ya sea como parte de un [recorrido](../building-journeys/journey-gs.md) o una [campaña](../campaigns/create-campaign.md). Una vez añadida, puede diseñar la tarjeta, establecer reglas de envío adicionales que controlen cuándo se muestra, se descarta o se oculta de forma permanente y ejecutar experimentos de contenido para optimizar su rendimiento.

>[!IMPORTANT]
>
>De forma predeterminada, el botón Cerrar oculta la tarjeta. Para añadir más funciones, puede definir manualmente reglas de despido o descalificación.

>[!BEGINTABS]

>[!TAB Agregar tarjetas de contenido a un recorrido]

Para añadir una tarjeta de contenido a un recorrido, siga estos pasos:

1. Abra el [recorrido](../building-journeys/journey-gs.md) y, a continuación, arrastre y suelte una actividad **[!UICONTROL Acción]** desde la sección **[!UICONTROL Acciones]** de la paleta. Más información sobre la [actividad de acción](../building-journeys/journey-action.md).

   >[!IMPORTANT]
   >
   >Las actividades heredadas de canales nativos (correo electrónico, push, SMS, en la aplicación, web, experiencia basada en código y tarjeta de contenido) quedaron obsoletas a partir de la versión de marzo de 2026. Los recorridos existentes que utilizan estas actividades siguen funcionando sin ningún cambio; no se requiere ninguna migración.

1. Seleccione **[!UICONTROL Tarjeta]** como tipo de acción.

   ![](assets/content-card-jo-1.png)

   >[!NOTE]
   >
   >Como **Card** es una actividad de experiencia entrante, viene con una actividad de **Espera** de 3 días. [Más información](../building-journeys/wait-activity.md#auto-wait-node)

1. Escriba una **[!UICONTROL etiqueta]** para identificar la acción en el lienzo de recorrido.

1. Haga clic en el botón **[!UICONTROL Configurar acción]**.

1. Se le dirigirá a la ficha **[!UICONTROL Acciones]**. A partir de ahí, seleccione o cree la configuración de la tarjeta de contenido que desea utilizar. [Más información](content-card-configuration.md)

   ![](assets/content-card-jo-2.png)

1. Ahora puedes empezar a diseñar tu contenido con el botón **[!UICONTROL Editar contenido]**. [Más información](design-content-card.md)

1. Habilite la opción **[!UICONTROL Habilitar reglas de envío adicionales]** y, a continuación, seleccione **[!UICONTROL Editar reglas]** para definir cuándo se debe mostrar, rechazar o ocultar el mensaje de forma permanente.

   ![](assets/content-card-jo-3.png)

   1. Haga clic en **[!UICONTROL Agregar condición]** para seleccionar el evento.

      +++ Ver eventos disponibles

      | Paquete | Déclencheur | Definición |
      |---|---|---|
      | Envío de datos a Platform | Datos enviados a Platform | Se activa cuando la aplicación móvil emite un evento de experiencia Edge para enviar datos a Adobe Experience Platform. Normalmente, la llamada de API [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) procede de la extensión de AEP Edge. |
      | Seguimiento principal | Seguimiento de acciones | Se activa cuando se llama a la funcionalidad heredada ofrecida en la API de código móvil [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction). |
      | Seguimiento principal | Estado de seguimiento | Se activa cuando se llama a la funcionalidad heredada ofrecida en la API de código móvil [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate). |
      | Seguimiento principal | Recopilar PII | Se activa cuando se llama a la funcionalidad heredada ofrecida en la API de código móvil [collectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii). |
      | Ciclo de aplicación | Inicio de aplicación | Se activa en cada ejecución, incluidos los bloqueos y las instalaciones. También se activa al reanudar desde segundo plano cuando se ha superado el tiempo de espera de la sesión de ciclo vital. |
      | Ciclo de aplicación | Instalación de aplicación | Se activa la primera vez que se ejecuta después de la instalación o reinstalación. |
      | Ciclo de aplicación | Actualización de aplicación | Se activa la primera vez que se ejecuta después de una actualización o cuando cambia el número de versión. |
      | Ciclo de aplicación | Cierre de aplicación | Se activa cuando se cierra la aplicación. |
      | Ciclo de aplicación | Bloqueo de aplicación | Se activa cuando la aplicación no se envía al segundo plano antes de cerrarse. El evento se envía cuando la aplicación se inicia después del bloqueo. Los informes de bloqueo de Adobe Mobile no implementan un controlador global de excepciones no detectadas. |

      +++

   1. Elija la condición **[!UICONTROL Or]** si desea agregar más **[!UICONTROL Déclencheur]** para expandir aún más la regla.

   1. Elija la condición **[!UICONTROL And]** si desea agregar **[!UICONTROL características]** y ajustar mejor la regla.

      +++ Ver características disponibles

      | Paquete | Rasgos | Definición |
      |---|---|---|
      | Información del dispositivo | Nombre de operador | Se activa cuando se cumple uno de los nombres de operador de la lista. |
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
      | Ciclo de aplicación | Lanzamientos | Se activa cuando se alcanza el número especificado de inicios. |
      | Ciclo de aplicación | Hora del día | Se activa cuando se cumple la hora del día especificada. |

      +++

   1. Haga clic en **[!UICONTROL Crear grupo]** para agrupar los déclencheur.

1. Puede agregar una o más acciones entrantes a su tarjeta de contenido si hace clic en el botón **[!UICONTROL Agregar acción]**. [Más información](../building-journeys/journey-action.md#multi-action)

1. Volver al lienzo de recorrido. Si es necesario, complete el flujo de recorrido arrastrando y soltando acciones o eventos adicionales. [Más información](../building-journeys/about-journey-activities.md)

Para obtener más información sobre cómo crear, configurar y publicar un recorrido, consulte [esta página](../building-journeys/journey-gs.md).

>[!TAB Agregar tarjetas de contenido a una campaña]

Para empezar a crear sus tarjetas de contenido a través de una campaña, siga los pasos a continuación.

1. Cree una campaña. [Más información](../campaigns/create-campaign.md)

1. Seleccione el tipo de campaña que desea ejecutar

   * **[!UICONTROL Programado - Marketing]**: ejecute la campaña inmediatamente o en una fecha especificada. Las campañas programadas están destinadas a enviar **marketing** mensajes. Se configuran y ejecutan desde la interfaz de usuario de.

   * **[!UICONTROL Activado por API - Marketing/Transaccional]**: ejecute la campaña mediante una llamada de API. Las campañas activadas por API están destinadas a enviar **marketing** o **mensajes transaccionales**, es decir, mensajes enviados después de una acción realizada por un individuo: restablecimiento de contraseña, compra en el carro de compras, etc. [Aprenda a almacenar en déclencheur una campaña mediante API](../campaigns/api-triggered-campaigns.md)

   ![](assets/content-card-create-1.png)

1. En la sección **[!UICONTROL Propiedades]**, especifique un nombre y una descripción para la campaña.

1. En la sección **Audiencia**, haga clic en el botón **[!UICONTROL Seleccionar audiencia]** para mostrar la lista de audiencias de Adobe Experience Platform disponibles. [Más información sobre los públicos](../audience/about-audiences.md)

1. En el campo **[!UICONTROL Área de nombres de identidad]**, elija el área de nombres que desea utilizar para identificar a los individuos del segmento seleccionado. [Más información sobre áreas de nombres](../event/about-creating.md#select-the-namespace)

1. Seleccione la acción **[!UICONTROL Tarjeta de contenido]**.

   ![](assets/content-card-create-2.png)

1. Seleccione o cree una nueva [configuración de la tarjeta de contenido](content-card-configuration.md).

1. Seleccione una [configuración de la bandeja de entrada](../inbox/inbox-configuration.md) que defina la superficie de la bandeja de entrada para esta **tarjeta de contenido**.

   ![](assets/content-card-create-2.png)

1. Para probar el contenido del mensaje, haga clic en **[!UICONTROL Crear experimento]**. Esto le permite probar varias variables de un envío en poblaciones de muestra para determinar qué tratamiento tiene el mayor impacto en la audiencia de destino. [Más información sobre el experimento de contenido](../content-management/content-experiment.md).

1. Habilite la opción **[!UICONTROL Habilitar reglas de envío adicionales]** y, a continuación, seleccione **[!UICONTROL Editar reglas]** para definir cuándo se debe mostrar, rechazar o ocultar el mensaje de forma permanente.

   Utilice los creadores de reglas para establecer condiciones específicas que almacenen en déclencheur estas acciones.

   1. Haga clic en **[!UICONTROL Agregar condición]** para seleccionar el evento.

      +++ Ver eventos disponibles

      | Paquete | Déclencheur | Definición |
      |---|---|---|
      | Envío de datos a Platform | Datos enviados a Platform | Se activa cuando la aplicación móvil emite un evento de experiencia Edge para enviar datos a Adobe Experience Platform. Normalmente, la llamada de API [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) procede de la extensión de AEP Edge. |
      | Seguimiento principal | Seguimiento de acciones | Se activa cuando se llama a la funcionalidad heredada ofrecida en la API de código móvil [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction). |
      | Seguimiento principal | Estado de seguimiento | Se activa cuando se llama a la funcionalidad heredada ofrecida en la API de código móvil [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate). |
      | Seguimiento principal | Recopilar PII | Se activa cuando se llama a la funcionalidad heredada ofrecida en la API de código móvil [collectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii). |
      | Ciclo de aplicación | Inicio de aplicación | Se activa en cada ejecución, incluidos los bloqueos y las instalaciones. También se activa al reanudar desde segundo plano cuando se ha superado el tiempo de espera de la sesión de ciclo vital. |
      | Ciclo de aplicación | Instalación de aplicación | Se activa la primera vez que se ejecuta después de la instalación o reinstalación. |
      | Ciclo de aplicación | Actualización de aplicación | Se activa la primera vez que se ejecuta después de una actualización o cuando cambia el número de versión. |
      | Ciclo de aplicación | Cierre de aplicación | Se activa cuando se cierra la aplicación. |
      | Ciclo de aplicación | Bloqueo de aplicación | Se activa cuando la aplicación no se envía al segundo plano antes de cerrarse. El evento se envía cuando la aplicación se inicia después del bloqueo. Los informes de bloqueo de Adobe Mobile no implementan un controlador global de excepciones no detectadas. |

      +++

   1. Elija la condición **[!UICONTROL Or]** si desea agregar más **[!UICONTROL Déclencheur]** para expandir aún más la regla.

   1. Elija la condición **[!UICONTROL And]** si desea agregar **[!UICONTROL características]** y ajustar mejor la regla.

      +++ Ver características disponibles

      | Paquete | Rasgos | Definición |
      |---|---|---|
      | Información del dispositivo | Nombre de operador | Se activa cuando se cumple uno de los nombres de operador de la lista. |
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
      | Ciclo de aplicación | Lanzamientos | Se activa cuando se alcanza el número especificado de inicios. |
      | Ciclo de aplicación | Hora del día | Se activa cuando se cumple la hora del día especificada. |

      +++

   1. Haga clic en **[!UICONTROL Crear grupo]** para agrupar los déclencheur.

   ![](assets/content-card-rules.png)

1. Puede programar la campaña para una fecha específica o configurarla para que se repita a intervalos regulares. [Más información](../campaigns/create-campaign.md#schedule)

1. Ahora puedes empezar a diseñar tu contenido con **[!UICONTROL Editar contenido]**. [Más información](design-content-card.md)

   ![](assets/content-card-create-4.png)

>[!ENDTABS]
