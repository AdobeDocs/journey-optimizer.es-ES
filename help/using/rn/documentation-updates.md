---
solution: Journey Optimizer
product: journey optimizer
title: Actualizaciones de documentación
description: Más información sobre las últimas actualizaciones de la documentación
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: 3adcd750089d81e6216316dc3d39f6a7982033f4
workflow-type: tm+mt
source-wordcount: '2246'
ht-degree: 0%

---

# Actualizaciones de documentación {#latest-updates}

Esta página enumera todas las actualizaciones de documentación de [!DNL Journey Optimizer].

## Diciembre de 2022 {#december-2022}

* La guía Mensajes se ha reorganizado y dividido en guías específicas para cada canal:

   * [Canal de correo electrónico](../email/get-started-email.md)
   * [Canal de notificaciones push](../push/get-started-push.md)
   * [Canal de SMS](../sms/get-started-sms.md)

* La guía de configuración se ha reorganizado para mejorar la legibilidad. [Más información](../configuration/get-started-configuration.md)

## Noviembre de 2022 {#november-2022}

* Se ha añadido una nueva página sobre las integraciones de Journey Optimizer. [Más información](../start/ajo-integrations.md)
* Se agregó una recomendación sobre la longitud de las direcciones URL de las páginas espejo. [Más información](../email/message-tracking.md)
* Se ha añadido una nueva subsección en la configuración de configuración de correo electrónico en la respuesta a la dirección de correo electrónico, incluidas las recomendaciones para garantizar una administración de respuestas adecuada. [Más información](../email/email-settings.md#reply-to-email)
* Se ha añadido una sección sobre cómo modificar el contenido de un mensaje en un recorrido en directo. [Más información](../building-journeys/journeys-message.md#update-live-content)

## Octubre de 2022 {#october-2022}

* Se ha añadido un caso de uso de recorrido sobre cómo limitar el rendimiento mediante Fuentes de datos externas y Acciones personalizadas. [Más información](../building-journeys/limit-throughput.md)
* La sección de casos de uso del recorrido se ha reorganizado en dos categorías: [Casos de uso empresarial](../building-journeys/journeys-uc.md) y [Casos de uso técnico](../building-journeys/collections.md).
* La variable **Conjunto de datos de entidad** se ha actualizado con más detalles. [Más información](../data/datasets-query-examples.md#entity-dataset)
* Se han reorganizado las secciones de administración de exclusión y políticas de consentimiento. [Más información](../privacy/opt-out.md)
* La sección sobre parámetros avanzados en mensajes de recorrido se ha aclarado y ahora especifica que la anulación de direcciones de correo electrónico solo debe utilizarse para casos de uso específicos. La mayoría de las veces, el valor definido como la dirección principal en la variable **Campos de ejecución** es el que debe usarse.
* Se ha añadido una nota al **Configurar subdominios de página de aterrizaje** para especificar que no se permiten mayúsculas en los subdominios de la página de aterrizaje. [Más información](../landing-pages/lp-subdomains.md)

## Septiembre de 2022 {#september-2022}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 22 de septiembre se ha detallado en la documentación. [Más información](release-notes.md)
* Se ha añadido una práctica recomendada relacionada con el uso de actividades de espera en recorridos recurrentes de segmentos de lectura. [Más información](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Se han añadido nuevos ejemplos de consultas de eventos de paso, así como información sobre la diferencia entre id, instanceid y profileid. [Más información](../reports/query-examples.md).
* Se han actualizado las páginas relacionadas con la variable [toDateOnly](../building-journeys/functions/functiontodateonly.md) y [toString](../building-journeys/functions/functiontostring.md) funciones.
* Se agregaron detalles sobre los parámetros de condición horaria. [Más información](../building-journeys/condition-activity.md#time_condition)
* Se ha añadido información sobre conjuntos de datos integrados. [Más información](../data/get-started-datasets.md#access-datasets)
* Se han mejorado y reorganizado las secciones Informe global y Informe en directo . [Más información](../reports/global-report.md)
* Se ha añadido una lista de todas las métricas de informes disponibles en Adobe Journey Optimizer.
   [Más información](../reports/global-report.md#email-and-sms-metrics)
* La sección de correo electrónico de CCO se ha trasladado a la nueva página Asistencia para el archivado . [Más información](../configuration/archiving-support.md)

## Agosto de 2022 {#august-2022}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 22 de agosto se ha detallado en la documentación. [Más información](release-notes.md)
* La sección de reglas de frecuencia se ha actualizado para reflejar el nuevo flujo de mensajería en línea. [Más información](../configuration/frequency-rules.md#apply-frequency-rule)
* Ahora se hace referencia a un vídeo que muestra cómo configurar suscripciones y crear páginas de aterrizaje en la sección Introducción a las páginas de aterrizaje . [Más información](../landing-pages/get-started-lp.md#video)
* Se ha añadido una limitación para los recorridos que utilizan actividades Leer segmento . [Más información](../building-journeys/read-segment.md)
* Se ha mejorado la página de operadores del editor de expresiones. [Más información](../building-journeys/expression/operators.md)
* Se ha añadido una sección sobre cómo programar una campaña. [Más información](../campaigns/create-campaign.md)
* Se ha actualizado la sección de reglas de sintaxis generales del editor de expresiones para tener en cuenta la nueva regla con respecto al escape del símbolo de barra invertida en funciones literales. Los mensajes publicados existentes no se ven afectados por este cambio. Solo se deben actualizar los mensajes nuevos o borrador. [Más información](../personalization/personalization-syntax.md#general-rules)

## Julio de 2022 {#july-2022}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 22 de julio se ha detallado en la documentación. [Más información](release-notes.md)
* La variable **Configuración de superficies de canal** se ha aclarado y actualizado con vínculos a la página que describe cómo configurar el canal SMS. [Más información](../configuration/channel-surfaces.md#create-channel-surface)
* En las propiedades del recorrido, la variable **Zona horaria del perfil** ahora está desactivada de forma predeterminada. [Más información](../building-journeys/timezone-management.md#timezone-from-profiles)
* En el **Espera** actividad, **Fecha fija** ya no está disponible. [Más información](../building-journeys/wait-activity.md)
* Se ha añadido más información sobre la variable **Lectura incremental** en la **Leer segmento** actividad. [Más información](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Se han añadido recomendaciones sobre la variable **Límite de perfiles** tipo de condición. [Más información](../building-journeys/condition-activity.md#profile_cap)
* Se ha agregado una limitación en los eventos comerciales. [Más información](../start/guardrails.md#events-g)

## Junio de 2022 {#june-2022}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 22 de junio se ha detallado en la documentación. [Más información](release-notes.md)
* Se ha añadido una nueva sección sobre solicitudes de privacidad a la documentación. [Más información](../privacy/requests.md)
* Se ha añadido a la documentación una nueva sección sobre los registros de auditoría de los recursos. [Más información](../privacy/audit-logs.md)
* Se ha añadido a la documentación una nueva sección sobre cómo añadir contenido HTML o JSON procedentes de la biblioteca de recursos de Adobe Experience Cloud a una representación de oferta. [Más información](../offers/offer-library/add-representations.md#html-json)
* Se ha añadido una nueva página sobre el ciclo de vida del recorrido. [Más información](../building-journeys/journey.md#journey-versions)
* Se ha actualizado la página de actividad Espera . [Más información](../building-journeys/wait-activity.md)
* Se ha añadido la lista de conjuntos de datos de Adobe Journey Optimizer con ejemplos de consultas. [Más información](../data/datasets-query-examples.md)
* La página Lista permitida se ha movido a la sección Configuración . [Más información](../configuration/allow-list.md)
* La página de la lista de supresión se ha actualizado para aclarar cierta información, incluido el hecho de que todos los caracteres ASCII comprendidos entre 32 y 126 están permitidos en el campo de motivos de supresión. [Más información](../configuration/manage-suppression-list.md)
* Se ha añadido el vínculo a las barreras y los límites estáticos para la gestión de la Decisión. [Más información](../start/guardrails.md)
* La optimización del tiempo de envío ya está disponible para todos los clientes. Se ha eliminado la mención beta. [Más información](../building-journeys/journeys-message.md#send-time-optimization)
* La API de decisiones por lotes se ha agregado a la lista de API disponibles para enviar ofertas personalizadas. [Más información](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## Mayo de 2022 {#may-2022}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 22 de mayo se ha detallado en la documentación. [Más información](release-notes.md)
* Nuevos ejemplos de consultas relacionados con [calificación de segmentos](../reports/query-examples.md#segment-qualification-queries) y [events](../reports/query-examples.md#event-based-queries) se han añadido.
* La sección de diseño de correo electrónico ahora menciona nuevas plantillas integradas disponibles para iniciar contenido. Se han actualizado las capturas de pantalla relacionadas. [Más información](../email/get-started-email-design.md)
* Los vínculos a recursos clave se han actualizado en la página de inicio de la documentación de Journey Optimizer.
* Se han actualizado las capturas de pantalla de la página de aterrizaje y los informes de suscripción. [Más información](../reports/live-report.md)
* Se ha añadido una nota que indica que el método Delete no es compatible con las acciones personalizadas. [Más información](../action/about-custom-action-configuration.md)
* Se han actualizado los vínculos a vídeos explicativos.
* La variable [Configuración de correo electrónico](../configuration/about-subdomain-delegation.md), [Ajustes preestablecidos de mensajes](../configuration/channel-surfaces.md) y [Configurar páginas de aterrizaje](../landing-pages/lp-subdomains.md) se han reorganizado para mejorar la legibilidad.
* La sección de seguimiento de URL se ha actualizado y mejorado con ejemplos. [Más información](../email/email-settings.md#url-tracking)
* Se ha añadido una nueva subsección sobre la configuración de una dirección de correo electrónico de reenvío. Tenga en cuenta que no puede hacerlo a través de la interfaz de usuario. [Más información](../email/email-settings.md#forward-email)

## Abril de 2022 {#april-2022}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 22 de abril se ha detallado en la documentación. [Más información](release-notes.md)
* La variable **reacciones** se ha actualizado la página de documentación del evento. [Más información](../building-journeys/reaction-events.md)
* Se han actualizado los vídeos de las funciones de administración de decisiones para que reflejen la interfaz de usuario de Journey Optimizer. [Más información](../offers/get-started/starting-offer-decisioning.md)
* La variable **Introducción a los conjuntos de datos** se ha mejorado para detallar cómo acceder y crear conjuntos de datos. [Más información](../data/get-started-datasets.md)
* Se han agregado vínculos a guías de ayuda y notas de la versión del producto al **Documentación de Adobe Journey Optimizer** página principal. [Más información](https://experienceleague.adobe.com/docs/journey-optimizer.html)
* La variable **Crear ajustes preestablecidos de mensaje** ahora especifica que no puede continuar con la creación de ajustes preestablecidos mientras el grupo de IP seleccionado está en edición (**[!UICONTROL Processing]** ) y nunca se ha asociado con el subdominio seleccionado. [Más información](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* Los ajustes preestablecidos de mensaje **Seguimiento de URL** se ha actualizado para reflejar cambios menores en la interfaz de usuario. [Más información](../configuration/channel-surfaces.md#url-tracking)

## Marzo de 2022 {#march-2022}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 22 de marzo se ha detallado en la documentación. [Más información](release-notes.md)
* Se ha añadido una nueva página sobre cómo empezar a usar modelos de IA a la **Offer decisioning** , incluida una descripción detallada del [modelo de optimización automática](../offers/ranking/auto-optimization-model.md), el algoritmo que utiliza y más detalles técnicos. [Más información](../offers/ranking/ai-models.md)
* La página de creación del perfil de prueba se ha trasladado a la  **Segmento, perfiles e identidad** para obtener más información. [Más información](../segment/creating-test-profiles.md)
* Se ha añadido un ejemplo sobre cómo añadir una expresión como valor predeterminado en el editor de expresiones. [Más información](../building-journeys/expression/field-references.md#default-value)
* La variable **Creación de ofertas personalizadas** se ha reorganizado para mejorar la legibilidad. [Más información](../offers/offer-library/creating-personalized-offers.md)
* Se ha añadido una nueva sección para describir el impacto que puede tener el cambio de las fechas de inicio y/o finalización de una oferta en el límite de frecuencia de esta oferta. [Más información](../offers/offer-library/add-constraints.md#capping-change-date)
* La variable **Cambiar las direcciones de correo electrónico principales** se ha actualizado para reflejar los cambios en la interfaz de usuario. [Más información](../configuration/primary-email-addresses.md)

## Febrero de 2022 {#feb-2022}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 22 de febrero se ha detallado en la documentación. [Más información](release-notes.md)
* La variable [replace](../building-journeys/functions/functionreplace.md#example_2) y [replaceAll](../building-journeys/functions/functionreplaceall.md#example) las páginas de documentación de funciones se han actualizado con información y ejemplos adicionales relacionados con el parámetro target .
* Se han añadido las prácticas recomendadas al [Operadores](../building-journeys/expression/operators.md#important-notes) página.

## Enero de 2022 {#january-2022}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 22 de enero se ha detallado en la documentación. [Más información](release-notes.md)
* La variable **Clasificación de IA de Offer Decisioning** se ha actualizado con una descripción más detallada del modelo de optimización automática. [Más información](../offers/ranking/auto-optimization-model.md)
* Se ha añadido una nueva sección sobre los requisitos de esquema necesarios para poder enviar en tipos de evento al utilizar una estrategia de clasificación. [Más información](../offers/ranking/schema-requirement.md)
* La sección relacionada con [!DNL Journey Optimizer] las funcionalidades de personalización se han reorganizado para mejorar la legibilidad. [Más información](../personalization/personalize.md)
* La variable **Crear ajustes preestablecidos de mensaje** se ha dividido en varias secciones para mejorar la claridad. [Más información](../configuration/channel-surfaces.md#create-channel-surface)
* La variable **Administración de la exclusión** se ha aclarado y se ha reorganizado ligeramente. [Más información](../privacy/opt-out.md#opt-out-management)
* La variable **Insertar vínculos** se ha actualizado para reflejar los cambios recientes en la interfaz de usuario. [Más información](../email/message-tracking.md#insert-links)

## Noviembre de 2021 {#november-2021}

* Una descripción completa del **editor de expresiones avanzadas** ya está disponible para su uso en recorridos. [Más información](../building-journeys/expression/expressionadvanced.md)
* Una nueva sección sobre **método de delegación de subdominios CNAME** se ha añadido. [Más información](../configuration/delegate-subdomain.md#cname-subdomain-delegation)


## Octubre de 2021 {#october-2021}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 21 de octubre se ha detallado en la documentación. [Más información](release-notes.md)
* Se ha añadido **Date time, función** lista. [Más información](../personalization/functions/dates.md)
* Nuevo **Secciones de introducción por usuario**. Tome su propio camino para llegar a sus objetivos más rápido! [Más información](../start/quick-start.md)
* Nuevo **Editar un ajuste preestablecido de mensaje** para obtener más información. [Más información](../configuration/channel-surfaces.md#edit-channel-surface)
* Nuevo **Editar un registro PTR** para obtener más información. [Más información](../configuration/ptr-records.md#edit-ptr-record)
* Nuevo **Desactivar un ajuste preestablecido de mensaje** para obtener más información. [Más información](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
* Nuevas limitaciones agregadas a la variable **Guía para desarrolladores de API de administración de decisiones** restricciones de oferta no admitidas con dispositivos móviles [!DNL Experience Edge] flujos de trabajo. [Más información](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* Nuevo **Creación de simulaciones** para obtener más información. [Más información](../offers/offer-activities/simulation.md)
* Actualizado **Agregar ámbitos de decisión** para obtener más información. [Más información](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Actualizado **Definir contenido para las representaciones** , incluida una nueva [subsección](../offers/offer-library/creating-personalized-offers.md#custom-text) sobre cómo definir y personalizar texto personalizado. [Más información](../offers/offer-library/creating-personalized-offers.md#content)

## Septiembre de 2021 {#september-2021}

* Se han actualizado las siguientes páginas de funciones: [sethours](../building-journeys/functions/functionsethours.md), [getListItem](../building-journeys/functions/functiongetlistitem.md), [inSegment](../building-journeys/functions/functioninsegment.md)

* Se han añadido las siguientes funciones: [filter](../building-journeys/functions/functionfilter.md), [intersección](../building-journeys/functions/functionintersect.md), [toDateOnly](../building-journeys/functions/functiontodateonly.md)

* El tipo de fecha dateOnly se ha agregado en la documentación del editor de expresiones. [Más información](../building-journeys/expression/data-types.md)

* Se agregaron detalles sobre la duración de la caché de acciones personalizada. [Más información](../datasource/external-data-sources.md#custom-authentication-mode)

* Se ha añadido información sobre los puertos predeterminados de acciones personalizadas. [Más información](../action/about-custom-action-configuration.md#url-configuration)

* Se ha agregado información sobre varios casos de uso de eventos comerciales. [Más información](../event/about-creating-business.md#multiple-business-events)

* Se han añadido ejemplos de uso común para consultar eventos de pasos de recorrido en Data Lake. [Más información](../reports/query-examples.md)

* Se ha añadido un nuevo **Limitaciones** página. [Más información](../start/guardrails.md)

* Se ha mejorado el **Inicio rápido** página con pasos para diferentes personalidades. [Más información](../start/quick-start.md)

* Ahora, todas las funciones de Administración de decisiones descritas en la sección dedicada también se aplican a los usuarios de Adobe Experience Platform que aprovechan el servicio de aplicación Offer Decisioning . [Más información](../offers/get-started/starting-offer-decisioning.md)

* Se ha añadido una subsección para aclarar las diferencias entre el uso de segmentos y las reglas de decisión al aplicar una restricción para restringir la selección de ofertas para una ubicación determinada. [Más información](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* Se han añadido ejemplos específicos de fórmula de clasificación para ilustrar algunos casos de uso en la vida real. [Más información](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Se ha añadido una subsección sobre cómo editar grupos de IP. [Más información](../configuration/ip-pools.md#edit-ip-pool)


## Agosto de 2021 {#august-2021}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 21 de agosto se ha detallado en la documentación. [Más información](release-notes.md)
* Se han actualizado los permisos de administración de decisiones. [Más información](../administration/ootb-product-profiles.md)
* Capturas de pantalla de Diseñador de correo electrónico actualizadas con la IU más reciente.
* Se ha actualizado el procedimiento de configuración para acciones personalizadas con rutas URL dinámicas y encabezados dinámicos. [Más información](../action/about-custom-action-configuration.md#url-configuration)
* Se ha añadido una sección sobre las funciones de accesibilidad y los métodos abreviados de teclado. [Más información](../start/user-interface.md#accessibility)
* Se ha añadido una sección sobre métodos de evaluación de segmentos. [Más información](../segment/about-segments.md#evaluation-method-in-journey-optimizer)
* Se han agregado notas a las secciones Lista de supresión, Lista permitida e Informe global/activo de correo electrónico para especificar que los perfiles con estados suprimidos y no permitidos se excluyen de las métricas Informe de correo electrónico enviado . [Más información](../reports/global-report.md)
* Se ha añadido una nueva sección para describir cómo recuperar direcciones de correo electrónico o dominios que se excluyeron de un envío porque no estaban en la lista de permitidos. [Más información](../configuration/allow-list.md#reporting)
* Se ha actualizado la sección Habilitar la lista de permitidos . [Más información](../configuration/allow-list.md#enable-allow-list)
* Se ha actualizado la sección Monitorizar ajustes preestablecidos de mensaje con los posibles motivos de error de creación preestablecidos y detalles sobre dichos errores. [Más información](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Se ha actualizado la sección Periodo de tiempo de reintento y se le ha cambiado el nombre para reflejar el hecho de que ahora puede ajustar la configuración de reintentos de correo electrónico en los ajustes preestablecidos de mensaje. [Más información](../configuration/retries.md#retry-duration)
* Se ha añadido una nueva sección para describir cómo insertar un vínculo de exclusión de un clic en el contenido del correo electrónico. [Más información](../privacy/opt-out.md#one-click-opt-out-link)
* Se ha actualizado la sección Delegar un subdominio con información más detallada sobre el proceso de validación realizado por Adobe. [Más información](../configuration/delegate-subdomain.md#subdomain-validation)
* Se ha añadido una sección para describir cómo agregar manualmente direcciones de correo electrónico y dominios a la lista de supresión. [Más información](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Se ha actualizado el [Acceso a la lista de supresión](../configuration/manage-suppression-list.md#access-suppression-list) y [Reintentos](../configuration/retries.md) para reflejar la nueva interfaz de usuario.
* Se ha documentado el nuevo flujo para añadir y configurar representaciones al crear una oferta. [Más información](../offers/offer-library/creating-personalized-offers.md#representations)


## Julio de 2021 {#july-2021}

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 21 de julio se ha detallado en la documentación. [Más información](release-notes.md)
* Se han agregado vínculos directos a la documentación de servicios de Experience Platform en [!DNL Journey Optimizer] página de inicio y tabla de contenido
* Nuevas páginas de aterrizaje para los servicios de Experience Platform disponibles en [!DNL Journey Optimizer]
* Se agregaron vínculos a [!DNL Journey Optimizer] descripción del producto en la página de inicio
* Se han añadido vídeos de tutoriales en varias páginas
* Imágenes optimizadas de la página principal
* Se ha movido, mejorado y se ha cambiado el nombre de la sección &quot;Seguimiento de mensajes&quot; a &quot;Añadir vínculos y rastrear mensajes&quot;. [Más información](../email/message-tracking.md)
* Se ha añadido una subsección en las páginas espejo. [Más información](../email/message-tracking.md#mirror-page)
* Se ha cambiado el nombre de &quot;actividades de oferta&quot; por &quot;decisiones&quot; y &quot;decisiones&quot; por &quot;ámbitos de decisión&quot; en la documentación y las pantallas. [Más información](../offers/get-started/starting-offer-decisioning.md)
* Nuevo caso de uso: [personalizar un mensaje con funciones de ayuda](../personalization/personalization-use-case-helper-functions.md)
* Se ha actualizado la documentación Leer segmento para reflejar los impactos materializados en el segmento. [Más información](../building-journeys/read-segment.md)
* Se han actualizado las limitaciones de recorrido. [Más información](../start/guardrails.md)
* Se ha actualizado la sección Configurar ofertas en la sección de decisiones. [Más información](../offers/offer-activities/configure-offer-selection.md)
* Se ha añadido una advertencia para indicar que las ofertas basadas en eventos no son compatibles actualmente. [Más información](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Se documentó la nueva **[!UICONTROL Overview]** pestaña . [Más información](../offers/get-started/user-interface.md#overview)
* Se han añadido nuevas secciones para describir las acciones disponibles en las listas de ofertas y decisiones: [Lista de ofertas](../offers/offer-library/creating-personalized-offers.md#offer-list) y [Lista de decisiones](../offers/offer-activities/create-offer-activities.md#decision-list).

