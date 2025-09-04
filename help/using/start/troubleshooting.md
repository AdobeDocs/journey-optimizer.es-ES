---
solution: Journey Optimizer
product: journey optimizer
title: Solución de problemas de Journey Optimizer
description: Preguntas de solución de problemas de Journey Optimizer
feature: Get Started
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 3ab8957d0aec6f30853de5537e03f0e7bec2017c
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 2%

---

# Resolución de problemas {#ajo-troubleshooting}


A continuación se muestra una lista de artículos de solución de problemas para Adobe Journey Optimizer. Cada sección de solución de problemas proporciona respuestas a las preguntas más frecuentes y soluciones a los problemas.

Consulte también [Preguntas frecuentes sobre Adobe Experience Platform y la documentación de solución de problemas](https://experienceleague.adobe.com/en/docs/experience-platform/landing/troubleshooting#service-troubleshooting-directory){target="_blank"}.

## Canal de correo electrónico {#ajo-troubleshooting-email}

### Diseño de correo electrónico {#ajo-troubleshooting-design}

+++ ¿Cómo evitar problemas de formato de correo electrónico en Adobe Journey Optimizer al utilizar temáticas?

En Adobe Journey Optimizer (AJO), modificar los bloques CSS predeterminados en el encabezado del correo electrónico puede provocar problemas de formato inesperados, especialmente después de eliminar fragmentos de contenido. Estos problemas son más evidentes en los dispositivos móviles y pueden provocar cambios de diseño o incoherencias en el estilo. Para evitarlo, utilice la función Temáticas para aplicar CSS personalizado de forma segura sin alterar los estilos CSS generados por el sistema.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"} para obtener información sobre cómo resolver este problema.

Obtenga más información acerca del formato de correo electrónico [en esta página](../email/get-started-email-design.md).

+++


+++ ¿Por qué los fragmentos con campos editables no funcionan?

En Adobe Journey Optimizer, es posible que los fragmentos con campos editables no se carguen correctamente o se dupliquen inesperadamente cuando se añaden a las plantillas. El problema suele afectar a fragmentos específicos entre entornos.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"} para obtener información sobre cómo resolver este problema.

Obtenga más información acerca de los fragmentos personalizables [en esta página](../content-management/customizable-fragments.md).

+++

+++ ¿Por qué las plantillas de correo electrónico y el contenido desaparecen de los recorridos no publicados?

Al editar plantillas de correo electrónico en un recorrido sin publicar, el contenido y las plantillas de determinados correos electrónicos pueden desaparecer inesperadamente. Esto puede causar reprocesamiento y retrasos. Para reducir el riesgo de este problema, evite las ediciones simultáneas, limite el número de pestañas abiertas y guarde los cambios con frecuencia.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} para obtener información sobre cómo resolver este problema.

Obtenga más información acerca de las plantillas [en esta página](../email/use-email-templates.md).

+++

+++ ¿Puede un perfil tener varios tokens push en Adobe Journey Optimizer?

Al implementar notificaciones push en Journey Optimizer, un solo perfil puede tener varios tokens push asociados a diferentes dispositivos. Durante una campaña de notificaciones push, Journey Optimizer está diseñado para administrar estos tokens y garantizar que el perfil de destino se pueda alcanzar en todos los dispositivos asociados.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} para obtener más información acerca de la administración de tokens push.

Obtenga más información acerca de la configuración de inserción [en esta página](../push/push-configuration.md).

+++

### Seguimiento y creación de informes de correo electrónico {#ajo-troubleshooting-tracking}

+++ ¿Cómo se evita que falten vínculos de seguimiento de correo electrónico en los informes?

El seguimiento de vínculos que faltan en Adobe Journey Optimizer se produce cuando las direcciones URL de correo electrónico utilizan variables dinámicas y no comienzan con http, o cuando las instrucciones lógicas se colocan en el campo URL. Para resolver esto, asegúrese de que todas las direcciones URL comienzan por http, evite utilizar la lógica en el campo URL y mueva la lógica de personalización compleja al contenido de HTML o a los atributos preprocesados.


Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"} para obtener información sobre cómo resolver este problema.

Obtenga más información acerca del seguimiento de correo electrónico [en esta página](../email/message-tracking.md).

+++

### Envío de correo electrónico {#ajo-troubleshooting-sending}

+++ ¿Cómo resuelvo un error de Mail Exchanger al configurar campañas de correo electrónico transaccionales activadas por API? 

Si encuentra un error de Mail Exchanger (MX) al crear una configuración de canal para una campaña de correo electrónico transaccional activada por API en Adobe Journey Optimizer, puede deberse a **configuraciones incorrectas de DNS** o a **limitaciones de directivas de DMARC**. Para resolver esto, asegúrese de que su DNS esté configurado correctamente y verifique que su dominio cumpla con los requisitos de **Autenticación de mensajes, creación de informes y conformidad basados en el dominio (DMARC)**.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26200){target="_blank"} para obtener información sobre cómo resolver este problema.

Obtenga más información acerca de las directivas de DMARC de correo electrónico [en esta página](../configuration/dmarc-record-update.md).

Consulte también [documentación de campañas activadas por API](../campaigns/api-triggered-campaigns.md).
+++

## Canal push {#ajo-troubleshooting-push}

+++ ¿Puede un perfil tener varios tokens push en Adobe Journey Optimizer?

Al implementar notificaciones push en Journey Optimizer, un solo perfil puede tener varios tokens push asociados a diferentes dispositivos. Durante una campaña de notificaciones push, Journey Optimizer está diseñado para administrar estos tokens y garantizar que el perfil de destino se pueda alcanzar en todos los dispositivos asociados.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} para obtener más información acerca de la administración de tokens push.

Obtenga más información acerca de la configuración de inserción [en esta página](../push/push-configuration.md).

+++

+++ ¿Por qué hacer clic en un mensaje push no me redirige a la URL web configurada?  

Si los mensajes push no redirigen a la URL web deseada, puede deberse a una configuración de acción de clic incorrecta o a que se deshabilitó la configuración de notificaciones push. Asegúrese de que la **acción de clic** para el mensaje push esté configurada correctamente y que la **visualización y el seguimiento automáticos** de las notificaciones push estén habilitados para resolver este problema.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26226){target="_blank"} para obtener más información sobre este problema.

Obtenga más información acerca de la configuración de inserción [en esta página](../push/push-configuration.md).

+++


## Canal de SMS {#ajo-troubleshooting-sms}

+++ ¿Por qué no se entregan mis SMS transaccionales aunque el consentimiento esté establecido en `marketing.sms.value=y`?

Si un destinatario responde **STOP** a un SMS, todos los mensajes futuros de ese número corto se bloquearán, incluidos los mensajes transaccionales. Para garantizar el envío ininterrumpido de SMS transaccionales, configúrelos y envíelos a través de un **número corto independiente** del que los destinatarios no se hayan excluido anteriormente.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26258){target="_blank"} para obtener más información sobre este problema.

Obtenga más información acerca de la configuración de exclusión de SMS [en esta página](../sms/sms-opt-out.md).

+++


## Gestión de datos {#ajo-troubleshooting-data-management}

+++ ¿Cómo se aplica la configuración del tiempo de vida (TTL) a los conjuntos de datos del perfil y del lago de datos al crear una nueva zona protegida?

Las organizaciones que aprovisionan nuevos entornos limitados en Adobe Journey Optimizer han planteado preguntas sobre cómo se aplica la configuración del tiempo de vida (TTL) a los conjuntos de datos de perfiles y lagos de datos. Este artículo aclara que la configuración de TTL no afecta a las zonas protegidas existentes y se aplica automáticamente solo a las recién aprovisionadas.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} para obtener información sobre cómo administrar TTL.

Obtenga más información acerca del tiempo de vida del conjunto de datos [en esta página](../data/datasets-ttl.md).

+++


## Administración de perfiles y audiencias {#ajo-troubleshooting-audiences}

+++ ¿Cómo se resuelven las discrepancias de recuento de audiencias?

El número de entradas procesadas en la característica **Leer audiencia** de Adobe Journey Optimizer puede ser inferior al recuento de audiencias esperado. Este problema suele deberse a configuraciones de área de nombres incorrectas, lo que provoca que los perfiles se excluyan de los recorridos. La resolución implica comprobar y corregir las configuraciones del área de nombres, revisar la documentación relevante y ajustar las prioridades para garantizar operaciones más fluidas en Adobe Journey Optimizer.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} para obtener información sobre cómo resolver este problema.

Vea también [este artículo sobre recuentos de audiencias obsoletas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}.

Obtenga más información acerca de la actividad **Leer audiencia** en los recorridos [de esta página](../building-journeys/read-audience.md).

+++

+++ ¿Por qué fallan las actualizaciones de perfil?

En Adobe Journey Optimizer, es posible que algunos valores de campo no se actualicen correctamente después de ejecutar una actividad **Actualizar perfil** en un recorrido. En algunos casos, los campos actualizados pueden desaparecer o volver a su estado anterior. Para solucionarlo, compruebe si hay reglas o condiciones en conflicto, revise la configuración de permisos, utilice un conjunto de datos único para la actividad **Actualizar perfil** y asegúrese de que ningún otro proceso de ingesta esté escribiendo en el mismo perfil al mismo tiempo.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"} para conocer los pasos que debe seguir para resolver este problema.

Obtenga más información acerca de la actividad **Actualizar perfil** en los recorridos [de esta página](../building-journeys/update-profiles.md).

Consulte también la [documentación de Adobe Experience Platform sobre la Ingesta de datos](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/tutorials/ingest-batch-data?lang=en#dataset-activity){target="_blank"}.

+++

+++ ¿Por qué hay una discrepancia en el recuento de perfiles al introducir un recorrido frente a en la audiencia asociada?

La discrepancia puede producirse cuando el recorrido utiliza una instantánea de perfil del día anterior si la instantánea del día actual no está disponible en el momento de ejecutar el recorrido.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"} para conocer los pasos que debe seguir para resolver este problema.

Más información en [esta publicación de la comunidad de Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998){target="_blank"}.

Consulte también la [Documentación de la API de horarios de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/api/schedules?lang=en){target="_blank"} para comprobar cuándo se ha programado su trabajo diario.

+++


+++ ¿Cómo se resuelven los problemas de población de audiencia?

Pueden producirse problemas de población de audiencias cuando faltan componentes o recursos, a menudo debido a errores de configuración de derechos, aprovisionamiento o permisos. Para solucionar estos problemas, comience por verificar las autorizaciones, garantizar el aprovisionamiento correcto y revisar los permisos. Si el problema persiste, escale el caso y coordine con los equipos de asistencia para una solución completa.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"} para conocer los pasos que debe seguir para resolver este problema.

Obtenga más información acerca de la actividad **Actualizar perfil** en los recorridos [de esta página](../building-journeys/update-profiles.md).

Consulte también la [documentación del perfil de Adobe Real-Time CDP](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide?lang=en#profile-detail){target="_blank"}.

+++

+++ ¿Cómo puedo resolver los problemas de déclencheur de recorrido después de los cambios de audiencia en Adobe Journey Optimizer? 

Si un recorrido deja de activarse después de realizar modificaciones en su audiencia asociada (como cambios en la política de combinación), puede que se interrumpan los flujos de campaña. Para resolver esto, **duplique y vuelva a publicar el recorrido** con la configuración de audiencia actualizada para garantizar que los déclencheur funcionen correctamente.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} para conocer los pasos que debe seguir para resolver este problema.

Aprenda a duplicar un recorrido [en esta página](../building-journeys/journey-ui.md#duplicate-a-journey).

+++


## Recorridos

### Eventos

+++ ¿Por qué mi evento no activa el recorrido deseado?  

Es posible que los eventos no almacenen en déclencheur un recorrido aunque se cumplan todos los criterios cuando se **crean mediante los servicios de consulta** en lugar de transmitirse al **Servicio principal de recopilación de datos (DCCS)**. Para resolver esto, revise la configuración del evento, asegúrese de que los eventos se **transmiten directamente a DCCS** y compruebe la funcionalidad mediante **modo de prueba**.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} para conocer los pasos que debe seguir para resolver este problema.

Más información sobre los eventos [en esta página](../event/about-events.md).

Consulte también [protecciones de eventos de Recorrido](../start/guardrails.md#events).

+++

## Toma de decisiones {#ajo-troubleshooting-decisioning}

+++ ¿Cómo puedo resolver los problemas al crear colecciones de ofertas?

Las dificultades para crear colecciones de ofertas suelen ocurrir cuando no se han aprovisionado **catálogos** para su organización. Para resolver esto, compruebe que todos los catálogos requeridos estén aprovisionados correctamente antes de intentar crear colecciones de ofertas.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} para conocer los pasos que debe seguir para resolver este problema.

Obtenga más información acerca de las colecciones de ofertas [en esta página](../offers/offer-library/creating-collections.md).

+++


## Multilingüe {#ajo-troubleshooting-multilingual}

+++ ¿Cómo resolver este problema `Message validation error (CJMMAS - 1069-500)`?

En Adobe Journey Optimizer, un error de validación de mensaje (CJMMAS - 1069-500) vinculado a la función multilingüe evita que las recorridos se establezcan en el modo de prueba o publiquen.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} para conocer los pasos que debe seguir para resolver este problema.

Obtenga más información acerca del contenido multilingüe [en esta página](../content-management/multilingual-gs.md).

++


## Configuración {#ajo-troubleshooting-config}

### Seguridad {#ajo-troubleshooting-security}

+++ ¿Cómo habilito TLS v1.3 para acciones personalizadas?  

Para mantener la **integridad y seguridad de los datos** al conectarse a sistemas de terceros, asegúrese de que Transport Layer Security (**TLS**) v1.3 esté habilitado para sus acciones personalizadas. Esto ayuda a proteger las comunicaciones y evita posibles vulnerabilidades de seguridad.


Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"} para obtener más información.

Obtenga más información acerca del contenido multilingüe [en esta página](../action/about-custom-action-configuration.md).

+++

### Paneles de control {#ajo-troubleshooting-dashboards}

+++ ¿Por qué no puedo crear un tablero directamente a partir de una consulta en Adobe Journey Optimizer? 

En Adobe Journey Optimizer, los paneles no se pueden crear directamente a partir de consultas. Para crear paneles, use las **funcionalidades de creación de paneles** disponibles en Adobe Experience Platform, que le permiten visualizar y analizar los datos de las consultas de forma eficaz.

Consulte [este artículo de solución de problemas](https://experienceleague.adobe.com/es/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"} para obtener más información.

++