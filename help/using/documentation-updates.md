---
title: Actualizaciones de documentación
description: Más información acerca de las últimas actualizaciones de documentación
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: 01313f84dc9d5260388574b3e1eb7e4a7df14d0e
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 25%

---

# Últimas actualizaciones en esta documentación

Esta página lista todas las actualizaciones de documentación de [!DNL Journey Optimizer].


## Octubre de 2021

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 21 de octubre se ha detallado en la documentación. [Más información](release-notes.md)
* Se ha añadido **Date time, función** lista. [Más información](personalization/functions/dates.md)
* Nuevo **Secciones de introducción por usuario**. Tome su propio camino para llegar a sus objetivos más rápido! [Más información](quick-start.md)
* Nuevo **Editar un ajuste preestablecido de mensaje** para obtener más información. [Más información](configuration/message-presets.md#edit-message-preset)
* Nuevo **Editar un registro PTR** para obtener más información. [Más información](configuration/ptr-records.md#edit-ptr-record)
* Nuevo **Desactivar un ajuste preestablecido de mensaje** para obtener más información. [Más información](configuration/message-presets.md#edit-message-preset#deactivate-preset)
* Nuevas limitaciones agregadas a la variable **Guía para desarrolladores de API de administración de decisiones** restricciones de oferta no admitidas con dispositivos móviles [!DNL Experience Edge] flujos de trabajo. [Más información](offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* Nuevo **Creación de simulaciones** para obtener más información. [Más información](offers/offer-activities/simulation.md)
* Actualizado **Agregar ámbitos de decisión** para obtener más información. [Más información](offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Actualizado **Definir contenido para las representaciones** , incluida una nueva [subsección](offers/offer-library/creating-personalized-offers.md#custom-text) sobre cómo definir y personalizar texto personalizado. [Más información](offers/offer-library/creating-personalized-offers.md#content)

## Septiembre de 2021

* Se han actualizado las siguientes páginas de funciones: [sethours](building-journeys/functions/functionsethours.md), [getListItem](building-journeys/functions/functiongetlistitem.md), [inSegment](building-journeys/functions/functioninsegment.md)

* Se han añadido las siguientes funciones: [filter](building-journeys/functions/functionfilter.md), [intersect](building-journeys/functions/functionintersect.md), [toDateOnly](building-journeys/functions/functiontodateonly.md)

* El tipo de fecha dateOnly se ha añadido a la documentación del editor de expresiones. [Más información](building-journeys/expression/data-types.md)

* Se han añadido detalles sobre la duración de la caché de acciones personalizada. [Más información](datasource/external-data-sources.md#section_wjp_nl5_nhb)

* Se ha añadido información sobre los puertos predeterminados de acciones personalizadas. [Más información](action/about-custom-action-configuration.md#url-configuration)

* Se ha agregado información sobre varios casos de uso de eventos comerciales. [Más información](event/about-creating-business.md#multiple-business-events)

* Se han añadido ejemplos de uso común para consultar eventos de pasos de recorrido en un lago de datos. [Más información](reports/query-examples.md)

* Se ha añadido un nuevo **Limitaciones** página. [Más información](limitations.md)

* Se ha mejorado el **Inicio rápido** página con pasos para diferentes personalidades. [Más información](quick-start.md)

* Ahora, todas las funciones de Administración de decisiones descritas en la sección dedicada también se aplican a los usuarios de Adobe Experience Platform que aprovechan el servicio de aplicaciones de Offer decisioning. [Más información](offers/get-started/starting-offer-decisioning.md)

* Se ha añadido una subsección para aclarar las diferencias entre el uso de segmentos y las reglas de decisión al aplicar una restricción para restringir la selección de ofertas para una ubicación determinada. [Más información](offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* Se han añadido ejemplos específicos de fórmula de clasificación para ilustrar algunos casos de uso en la vida real. [Más información](offers/offer-library/create-ranking-formulas.md#ranking-formula-examples)

* Se ha añadido una subsección sobre cómo editar grupos de IP. [Más información](configuration/ip-pools.md#edit-ip-pool)

## Agosto de 2021

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 21 de agosto se ha detallado en la documentación. [Más información](release-notes.md)
* Se han actualizado los permisos de administración de decisiones. [Más información](administration/ootb-product-profiles.md)
* Capturas de pantalla de Diseñador de correo electrónico actualizadas con la IU más reciente.
* Se ha actualizado el procedimiento de configuración para acciones personalizadas con rutas URL dinámicas y encabezados dinámicos. [Más información](action/about-custom-action-configuration.md#url-configuration)
* Se ha añadido una sección sobre las funciones de accesibilidad y los métodos abreviados de teclado. [Más información](user-interface.md#accessibility)
* Se ha añadido una sección acerca de métodos de evaluación de segmentos. [Más información](segment/about-segments.md#evaluation-method-in-journey-optimizer)
* Se han agregado notas a las secciones Lista de supresión, Lista de permitidos y Correo electrónico global/activo para especificar que los perfiles con estados Suprimido y No permitido se excluyen de las métricas Informe de correo electrónico enviado . [Más información](reports/email-global-report.md)
* Se ha añadido una nueva sección para describir cómo recuperar direcciones de correo electrónico o dominios que se excluyeron de un envío porque no estaban en la lista de permitidos. [Más información](allow-list.md#reporting)
* Se ha actualizado la sección Habilitar la lista de permitidos . [Más información](allow-list.md#enable-allow-list)
* Se ha actualizado la sección Monitorizar ajustes preestablecidos de mensaje con los posibles motivos de error de creación preestablecidos y detalles sobre dichos errores. [Más información](configuration/message-presets.md#monitor-message-presets)
* Se ha actualizado la sección Periodo de tiempo de reintento y se le ha cambiado el nombre para reflejar el hecho de que ahora puede ajustar la configuración de reintentos de correo electrónico en los ajustes preestablecidos de mensaje. [Más información](configuration/retries.md#retry-duration)
* Se ha añadido una nueva sección para describir cómo insertar un vínculo de exclusión de un clic en el contenido del correo electrónico. [Más información](message-tracking.md#one-click-opt-out-link)
* Se ha actualizado la sección Delegar un subdominio con información más detallada sobre el proceso de validación realizado por el Adobe. [Más información](configuration/delegate-subdomain.md#subdomain-validation)
* Se ha añadido una sección para describir cómo agregar manualmente direcciones de correo electrónico y dominios a la lista de supresión. [Más información](configuration/manage-suppression-list.md#add-addresses-and-domains)
* Se ha actualizado el [Acceso a la lista de supresión](configuration/manage-suppression-list.md#access-suppression-list) y [Reintentos](configuration/retries.md) para reflejar la nueva interfaz de usuario.
* Se ha documentado el nuevo flujo para añadir y configurar representaciones al crear una oferta. [Más información](offers/offer-library/creating-personalized-offers.md#representations)


## Julio de 2021

* Todas las nuevas funciones y mejoras incluidas [!DNL Journey Optimizer] La versión del 21 de julio se ha detallado en la documentación. [Más información](release-notes.md)
* Se han agregado vínculos directos a la documentación de servicios de Experience Platform en [!DNL Journey Optimizer] página de inicio y tabla de contenido
* Nuevas páginas de aterrizaje para servicios de Experience Platform disponibles en [!DNL Journey Optimizer]
* Se agregaron vínculos a [!DNL Journey Optimizer] descripción del producto en la página de inicio
* Se han añadido vídeos de tutoriales en varias páginas
* Imágenes optimizadas de la página principal
* Se ha movido, mejorado y se ha cambiado el nombre de la sección &quot;Seguimiento de mensajes&quot; a &quot;Añadir vínculos y rastrear mensajes&quot;. [Más información](message-tracking.md)
* Se ha añadido una subsección en las páginas espejo. [Más información](message-tracking.md#mirror-page)
* Se ha cambiado el nombre de &quot;actividades de oferta&quot; por &quot;decisiones&quot; y &quot;decisiones&quot; por &quot;ámbitos de decisión&quot; en la documentación y las pantallas. [Más información](offers/get-started/starting-offer-decisioning.md)
* Nuevo caso de uso: [personalizar un mensaje con funciones de ayuda](personalization/personalization-use-case-helper-functions.md)
* Se ha actualizado la documentación Leer segmento para reflejar los impactos materializados en el segmento. [Más información](building-journeys/read-segment.md)
* Se han actualizado las limitaciones de Recorrido. [Más información](limitations.md)
* Se ha actualizado la sección Configurar ofertas en la sección de decisiones. [Más información](offers/offer-activities/configure-offer-selection.md)
* Se ha añadido una advertencia para indicar que las ofertas basadas en eventos no son compatibles actualmente. [Más información](offers/offer-library/creating-personalized-offers.md#eligibility)
* Se documentó la nueva **[!UICONTROL Overview]** pestaña . [Más información](offers/get-started/user-interface.md#overview)
* Se han añadido nuevas secciones para describir las acciones disponibles en las listas de ofertas y decisiones: [Lista de ofertas](offers/offer-library/creating-personalized-offers.md#offer-list) y [Lista de decisiones](offers/offer-activities/create-offer-activities.md#decision-list).
