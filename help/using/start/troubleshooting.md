---
solution: Journey Optimizer
product: journey optimizer
title: Artículos de solución de problemas de Journey Optimizer
description: Artículos de solución de problemas de Journey Optimizer
feature: Get Started, Monitoring
role: User
level: Intermediate
exl-id: f8acb987-5c6e-4545-93b9-fdfc0d74db57
source-git-commit: 7755e29c4ad07319dadfb3426c8093199b4f843b
workflow-type: tm+mt
source-wordcount: '4652'
ht-degree: 0%

---

# Preguntas frecuentes sobre solución de problemas {#ajo-troubleshooting}

A continuación se muestra una lista de artículos de solución de problemas para Adobe Journey Optimizer. Cada sección de solución de problemas proporciona respuestas a las preguntas más frecuentes y soluciones a los problemas.

Al ponerse en contacto con el servicio de asistencia de Adobe por problemas sin resolver, incluya detalles del entorno, nivel de impacto, pasos de replicación, registros o capturas de pantalla e ID relevantes. [Aprenda qué debe incluir en los vales de soporte](user-interface.md#support-ticket-guidelines).

## Canal de correo electrónico {#ajo-troubleshooting-email}

+++ ¿Cómo evitar problemas de formato de correo electrónico en Adobe Journey Optimizer al utilizar temáticas?

En Adobe Journey Optimizer (AJO), modificar los bloques CSS predeterminados en el encabezado del correo electrónico puede provocar problemas de formato inesperados, especialmente después de eliminar fragmentos de contenido. Estos problemas son más evidentes en los dispositivos móviles y pueden provocar cambios de diseño o incoherencias en el estilo. Para evitarlo, utilice la función Temáticas para aplicar CSS personalizado de forma segura sin alterar los estilos CSS generados por el sistema.

Obtenga más información acerca del formato de correo electrónico [en esta página](../email/get-started-email-design.md).

+++


+++ ¿Por qué los fragmentos con campos editables no funcionan?

En Adobe Journey Optimizer, es posible que los fragmentos con campos editables no se carguen correctamente o se dupliquen inesperadamente cuando se añaden a las plantillas. El problema suele afectar a fragmentos específicos entre entornos. Para resolver esto, compruebe la configuración del fragmento, compruebe si hay definiciones de campo editables en conflicto y realice pruebas en una zona protegida de desarrollo antes de volver a publicar.

Obtenga más información acerca de los fragmentos personalizables [en esta página](../content-management/customizable-fragments.md).

+++

+++ ¿Por qué los fragmentos de HTML no se muestran correctamente en los correos electrónicos?

Es posible que los fragmentos de HTML no se representen correctamente en los correos electrónicos, y que a menudo aparezcan como **ID de fragmento** en lugar de contenido real. A diferencia de los fragmentos visuales, los fragmentos de HTML requieren una configuración cuidadosa. Para resolver esto, siga las prácticas recomendadas para usar **fragmentos de expresiones visuales y HTML** en sus campañas de correo electrónico.

Obtenga más información acerca de los fragmentos de HTML [en esta página](../content-management/fragments.md).

+++

+++ ¿Por qué las plantillas de correo electrónico y el contenido desaparecen de los recorridos no publicados?

Al editar plantillas de correo electrónico en un recorrido sin publicar, el contenido y las plantillas de determinados correos electrónicos pueden desaparecer inesperadamente. Esto puede causar reprocesamiento y retrasos. Para reducir el riesgo de este problema, evite las ediciones simultáneas, limite el número de pestañas abiertas y guarde los cambios con frecuencia.

Obtenga más información acerca de las plantillas [en esta página](../email/use-email-templates.md).

+++

+++ ¿Por qué el campo Encabezado previo de correo electrónico no se muestra en el modo &quot;Codifique usted mismo&quot;? 

En el modo **&#39;Codifique su propio&#39;**&#39; en la función **Editar cuerpo del correo electrónico**, el campo de entrada Preencabezado no aparece. Para incluir texto de preencabezado, los usuarios deben **codificar manualmente el preencabezado** en su contenido personalizado de HTML.

Obtenga más información acerca de la configuración del encabezado previo de correo electrónico [en esta página](../email/header-parameters.md).

+++

+++ ¿Por qué hay una discrepancia en el comportamiento del vínculo al utilizar un componente de HTML en las plantillas de correo electrónico?  

Al agregar un **componente de HTML** a una plantilla de correo electrónico, los vínculos pueden comportarse de manera diferente según el **cliente de correo electrónico**, el **modo de visualización** o el **dispositivo o explorador**. Por ejemplo, los vínculos de anclaje pueden funcionar de forma distinta en la vista simultánea de **Outlook** en comparación con la vista de pantalla completa. Tenga en cuenta estas variaciones al diseñar plantillas de correo electrónico y realizar pruebas en varios clientes y dispositivos.

Consulte también las prácticas recomendadas de diseño de correo electrónico [en esta página](../email/get-started-email-design.md).

+++


+++ ¿Cómo se evita que falten vínculos de seguimiento de correo electrónico en los informes?

El seguimiento de vínculos que faltan en Adobe Journey Optimizer se produce cuando las direcciones URL de correo electrónico utilizan variables dinámicas y no comienzan con http, o cuando las instrucciones lógicas se colocan en el campo URL. Para resolver esto, asegúrese de que todas las direcciones URL comienzan por http, evite utilizar la lógica en el campo URL y mueva la lógica de personalización compleja al contenido de HTML o a los atributos preprocesados.

Obtenga más información acerca del seguimiento de correo electrónico [en esta página](../email/message-tracking.md).

+++

+++ ¿Cómo resuelvo un error de Mail Exchanger al configurar campañas de correo electrónico transaccionales activadas por API? 

Si encuentra un error de Mail Exchanger (MX) al crear una configuración de canal para una campaña de correo electrónico transaccional activada por API en Adobe Journey Optimizer, puede deberse a **configuraciones incorrectas de DNS** o a **limitaciones de directivas de DMARC**. Para resolver esto, asegúrese de que su DNS esté configurado correctamente y verifique que su dominio cumpla con los requisitos de **Autenticación de mensajes, creación de informes y conformidad basados en el dominio (DMARC)**.

Obtenga más información acerca de las directivas de DMARC de correo electrónico [en esta página](../configuration/dmarc-record-update.md).

Consulte también [documentación de campañas activadas por API](../campaigns/api-triggered-campaigns.md).
+++

## Canal push {#ajo-troubleshooting-push}

+++ ¿Puede un perfil tener varios tokens push en Adobe Journey Optimizer?

Al implementar notificaciones push en Journey Optimizer, un solo perfil puede tener varios tokens push asociados a diferentes dispositivos. Durante una campaña de notificaciones push, Journey Optimizer está diseñado para administrar estos tokens y garantizar que el perfil de destino se pueda alcanzar en todos los dispositivos asociados.

Obtenga más información acerca de la configuración de inserción [en esta página](../push/push-configuration.md).

Consulte también [flujo de datos de notificaciones push](../push/push-gs.md) para comprender cómo se registran y administran los tokens de extremo a extremo.

+++

+++ ¿Por qué hacer clic en un mensaje push no me redirige a la URL web configurada?  

Si los mensajes push no redirigen a la URL web deseada, puede deberse a una configuración de acción de clic incorrecta o a que se deshabilitó la configuración de notificaciones push. Asegúrese de que la **acción de clic** para el mensaje push esté configurada correctamente y que la **visualización y el seguimiento automáticos** de las notificaciones push estén habilitados para resolver este problema.

Obtenga más información acerca de la configuración de inserción [en esta página](../push/push-configuration.md).

+++

+++ ¿Por qué las notificaciones push fallan después de actualizar las credenciales de la aplicación?

Las credenciales push caducadas o mal configuradas, como un certificado APNS para iOS o una clave FCM para Android, causan errores de entrega en modo silencioso. Journey Optimizer no puede enviar notificaciones si las credenciales almacenadas en la configuración del canal push ya no coinciden con las registradas en la plataforma del dispositivo. Actualice las credenciales en la configuración del canal push y verifique que la superficie de la aplicación móvil asociada se vuelva a publicar.

Obtenga información sobre cómo configurar las credenciales de inserción [en esta página](../push/push-gs.md).

Consulte también la [documentación de configuración del canal push](../push/push-configuration.md).

+++


## Canal de SMS {#ajo-troubleshooting-sms}

+++ ¿Por qué no se entregan mis SMS transaccionales aunque el consentimiento esté establecido en `marketing.sms.value=y`?

Si un destinatario responde **STOP** a un SMS, todos los mensajes futuros de ese número corto se bloquearán, incluidos los mensajes transaccionales. Para garantizar el envío ininterrumpido de SMS transaccionales, configúrelos y envíelos a través de un **número corto independiente** del que los destinatarios no se hayan excluido anteriormente.

Obtenga más información acerca de la configuración de exclusión de SMS [en esta página](../sms/sms-opt-out.md).

+++

+++ ¿Por qué falla la entrega de SMS aunque el canal esté configurado?

Los errores de entrega de SMS después de la configuración del canal suelen deberse a credenciales de API de proveedor incorrectas, una discrepancia entre el ID del remitente y lo que el proveedor ha registrado o restricciones de enrutamiento a nivel de proveedor. Compruebe que la clave de API, la contraseña y los detalles del remitente introducidos en Journey Optimizer coinciden exactamente con lo que ha proporcionado su proveedor de SMS. A continuación, envíe un mensaje de prueba para confirmar la conectividad antes de iniciar una campaña.

Aprenda a configurar su proveedor de SMS [en esta página](../sms/sms-configuration.md).

+++

+++ ¿Cómo puedo verificar que un perfil se haya excluido de las comunicaciones SMS?

Cuando un perfil envía SMS a STOP, Journey Optimizer actualiza el atributo de consentimiento de SMS del perfil. Para comprobar el estado de exclusión actual, abra el perfil en la interfaz de usuario de Experience Platform e inspeccione los campos de consentimiento en **Privacidad** > **Consentimientos**. Para solucionar problemas de la campaña, compruebe también los motivos de exclusión en el informe de campaña: los perfiles excluidos aparecen en el recuento **Excluido** con el motivo &quot;Excluido&quot;.

Obtenga más información acerca de la exclusión de SMS [en esta página](../sms/sms-opt-out.md).

+++

## Canal en la aplicación {#ajo-troubleshooting-inapp}

+++ ¿Por qué no puedo crear informes sobre el canal en la aplicación en Customer Journey Analytics?

Las dificultades para informar sobre el **canal en la aplicación** en Adobe Customer Journey Analytics suelen deberse a **vistas de datos**, **conjuntos de datos** o **actualizaciones de esquema** mal configurados. Asegúrese de que estas configuraciones se aplican correctamente para resolver el problema.

Consulte también la [documentación de informes permanentes de Journey Optimizer](../reports/report-gs-cja.md).

+++

+++ ¿Por qué no se muestra mi mensaje en la aplicación a los usuarios?

Los mensajes en la aplicación requieren que Adobe Experience Platform Mobile SDK esté correctamente instalado y que la extensión de mensajería esté registrada en la aplicación. Si el mensaje no aparece, compruebe que SDK se haya inicializado antes de que la aplicación intente recuperar mensajes en la aplicación, que la superficie de aplicación correcta (ID de paquete) esté configurada en Journey Optimizer y que la campaña esté en estado **Activo**. Confirme también que el perfil cumple los criterios de audiencia y que aún no se ha limitado con una regla de frecuencia.

Obtenga información sobre cómo configurar el canal en la aplicación [en esta página](../in-app/inapp-configuration.md).

+++

+++ ¿Por qué mi campaña en la aplicación no se activa en el evento esperado?

El déclencheur de las campañas en la aplicación se basa en nombres de eventos que deben coincidir exactamente entre la implementación de SDK de la aplicación y la condición de déclencheur definida en Journey Optimizer. Si no coinciden las mayúsculas y minúsculas, la ortografía o la estructura de carga útil de evento, se evitará que se active el déclencheur. Utilice la herramienta Adobe Experience Platform Assurance para inspeccionar eventos de SDK en directo y compararlos con la configuración de déclencheur de la campaña.

Aprenda a crear y configurar un mensaje en la aplicación [en esta página](../in-app/create-in-app.md).

+++


## Tarjetas de contenido {#ajo-troubleshooting-content-cards}

+++ ¿Por qué las tarjetas de contenido no se muestran en la aplicación?

Las tarjetas de contenido requieren que Adobe Experience Platform Mobile SDK y **Messaging SDK** se instalen, registren y configuren en la aplicación. A diferencia de los mensajes push o en la aplicación, las tarjetas de contenido no se representan automáticamente: la aplicación debe llamar explícitamente a las API de SDK de mensajería para recuperar las tarjetas disponibles y luego procesarlas en la interfaz de usuario. Si las tarjetas no aparecen, usa **Adobe Experience Platform Assurance** para comprobar que las solicitudes de decisión se emiten cuando se activa el evento de destino y que las respuestas regresan de Edge Network.

Obtenga información sobre cómo configurar la compatibilidad con tarjetas de contenido en Mobile SDK [en esta página](../content-card/content-card-configuration-sdk.md).

+++

+++ ¿Las tarjetas de contenido requieren que el usuario conceda permisos de notificaciones push?

No. Las tarjetas de contenido son silenciosas y persistentes: no dependen de los permisos push del nivel del sistema operativo y no se ven afectadas por el estado de inclusión de notificaciones de un usuario. Esto los convierte en un canal de reserva útil para llegar a los usuarios que han deshabilitado las notificaciones push. Las tarjetas se recuperan de Edge Network mientras el usuario está en la sesión y se muestran en la interfaz de usuario de la aplicación.

Obtenga más información acerca del canal de la tarjeta de contenido [en esta página](../content-card/get-started-content-card.md).

+++

+++ ¿Por qué las impresiones de tarjeta de contenido no aparecen en los informes de campaña?

Las impresiones e interacciones de la tarjeta de contenido (clics, rechazos) no se rastrean automáticamente. La aplicación debe enviar explícitamente eventos de seguimiento a Adobe a través de Messaging SDK después de procesar una tarjeta y después de cualquier interacción del usuario con ella. Si estas llamadas de seguimiento no se encuentran en la implementación, los informes no mostrarán impresiones aunque las tarjetas se estén usando correctamente. Compruebe que las llamadas de seguimiento se estén activando en **Assurance** antes de investigar la configuración de la campaña.

Obtenga información sobre cómo acceder a los informes de tarjetas de contenido [en esta página](../content-card/content-card-report.md).

Consulte también la [configuración de SDK de la tarjeta de contenido](../content-card/content-card-configuration-sdk.md) para las llamadas de seguimiento requeridas.

+++

## WhatsApp {#ajo-troubleshooting-whatsapp}

+++ ¿Por qué no se envían mis mensajes de WhatsApp?

La entrega de mensajes de WhatsApp requiere que se cumplan dos condiciones: el destinatario debe haberse suscrito explícitamente para recibir comunicaciones de WhatsApp de su marca y el mensaje debe utilizar una **plantilla de mensaje preaprobada** registrada con la API de WhatsApp Business. Si no se cumple cualquiera de las condiciones, la plataforma WhatsApp bloqueará el mensaje de forma silenciosa antes de la entrega. Compruebe el estado de inclusión en los atributos de consentimiento de perfil del destinatario y confirme que la plantilla está en estado **Aprobado** en su cuenta de WhatsApp Business.

Aprenda a configurar el canal de WhatsApp [en esta página](../whatsapp/whatsapp-configuration.md).

+++

+++ ¿Por qué se rechaza mi mensaje de WhatsApp con un error de plantilla?

La API comercial de WhatsApp solo permite plantillas de mensaje preaprobadas para mensajes salientes iniciados por empresas. Los mensajes en formato libre sólo se permiten dentro de un período de servicio de atención al cliente de **24 horas**, es decir, dentro de las 24 horas siguientes a la primera vez que el cliente envíe un mensaje a su marca. Si el mensaje se rechaza, compruebe que la plantilla se ha enviado a Meta y que la ha aprobado, que las variables de plantilla (marcadores de posición) del mensaje de Journey Optimizer coinciden exactamente con la estructura de plantilla aprobada y que la plantilla correcta está seleccionada en la campaña o en la acción de recorrido.

Aprenda a crear mensajes de WhatsApp [en esta página](../whatsapp/create-whatsapp.md).

+++

+++ ¿Cómo puedo recopilar y verificar la inclusión de WhatsApp de los usuarios?

WhatsApp requiere la inclusión explícita para poder enviar mensajes de marketing. La inclusión se puede recopilar a través de cualquier canal que controle su marca, como un formulario web, SMS de doble inclusión o una pantalla de consentimiento en la aplicación, siempre y cuando el proceso sea claro y esté documentado. Una vez recopilado, actualice el atributo de consentimiento de WhatsApp del perfil en Adobe Experience Platform. Para comprobar el estado de consentimiento actual de un perfil, ábralo en la interfaz de usuario de Experience Platform e inspeccione la sección **Consentimientos**. El envío a perfiles sin un consentimiento válido infringe las políticas de WhatsApp Business y puede provocar la suspensión de su cuenta.

Aprenda a empezar con el canal de WhatsApp [en esta página](../whatsapp/get-started-whatsapp.md).

+++

## Administración de datos {#ajo-troubleshooting-data-management}

+++ ¿Cómo se aplica la configuración del tiempo de vida (TTL) a los conjuntos de datos del perfil y del lago de datos al crear una nueva zona protegida?

Las organizaciones que aprovisionan nuevos entornos limitados en Adobe Journey Optimizer han planteado preguntas sobre cómo se aplica la configuración del tiempo de vida (TTL) a los conjuntos de datos de perfiles y lagos de datos. La configuración de TTL no afecta a los entornos limitados existentes y se aplica automáticamente solo a los recién aprovisionados.

Obtenga más información acerca del tiempo de vida del conjunto de datos [en esta página](../data/datasets-ttl.md).

+++

+++ ¿Por qué no se está habilitando un conjunto de datos para el Perfil del cliente en tiempo real?

Para que un conjunto de datos pueda personalizar según un perfil y cumplir las condiciones de recorrido en Journey Optimizer, se deben cumplir dos requisitos: el esquema XDM subyacente debe tener **Perfil** habilitado y el propio conjunto de datos debe estar activado para **Perfil del cliente en tiempo real** en la interfaz de usuario de Experience Platform. Si falta alguna de las dos, los datos se incorporarán al lago de datos, pero no se combinarán en perfiles unificados. Asegúrese también de que el conjunto de datos contenga al menos un campo de identidad asignado a un área de nombres reconocida.

Obtenga información sobre cómo configurar conjuntos de datos [en esta página](../data/get-started-datasets.md).

Consulte también la [descripción general de administración de datos](../data/gs-data.md) para ver la lista de comprobación de configuración completa.

+++

+++ ¿Cómo superviso y resuelvo los errores de ingesta de datos?

Los errores de ingesta aparecen en el panel **Supervisión** de Adobe Experience Platform en **Fuentes** > **Flujos de datos**. Las causas comunes incluyen errores de validación de esquema (un campo en los datos de origen no coincide con el esquema XDM), campos de identidad requeridos que faltan o cargas JSON mal formadas. Abra el registro por lotes con errores para ver el código de error específico y las filas afectadas. Corrija los datos de origen y vuelva a realizar la ingesta, o ajuste la asignación de esquema si el formato de origen ha cambiado.

Obtenga más información acerca de esquemas y configuración de datos [en esta página](../data/gs-data.md).

+++


## Administración de perfiles y audiencias {#ajo-troubleshooting-audiences}

+++ ¿Cómo se resuelven las discrepancias de recuento de público?

El número de entradas procesadas en la característica **Leer audiencia** de Adobe Journey Optimizer puede ser inferior al recuento de público esperado. Este problema suele deberse a configuraciones de área de nombres incorrectas, lo que provoca que los perfiles se excluyan de los recorridos. La resolución implica comprobar y corregir las configuraciones del área de nombres, revisar la documentación relevante y ajustar las prioridades para garantizar operaciones más fluidas en Adobe Journey Optimizer.

Obtenga más información acerca de la actividad **Leer audiencia** en los recorridos [de esta página](../building-journeys/read-audience.md).

+++

+++ ¿Por qué fallan las actualizaciones de perfil?

En Adobe Journey Optimizer, es posible que algunos valores de campo no se actualicen correctamente después de ejecutar una actividad **Actualizar perfil** en un recorrido. En algunos casos, los campos actualizados pueden desaparecer o volver a su estado anterior. Para solucionarlo, compruebe si hay reglas o condiciones en conflicto, revise la configuración de permisos, utilice un conjunto de datos único para la actividad **Actualizar perfil** y asegúrese de que ningún otro proceso de ingesta esté escribiendo en el mismo perfil al mismo tiempo.

Obtenga más información acerca de la actividad **Actualizar perfil** en los recorridos [de esta página](../building-journeys/update-profiles.md).

+++

+++ ¿Por qué hay una discrepancia en el recuento de perfiles al introducir un recorrido frente a en la audiencia asociada?

La discrepancia puede producirse cuando el recorrido utiliza una instantánea de perfil del día anterior si la instantánea del día actual no está disponible en el momento de ejecutar el recorrido. Para investigar, compruebe cuándo se ejecutó por última vez el trabajo de segmentación diaria y si el recorrido se activó antes de que la instantánea estuviera lista.

Obtenga más información acerca de la actividad **Leer audiencia** y el comportamiento de programación [en esta página](../building-journeys/read-audience.md).

+++

+++ ¿Por qué el selector de audiencias muestra diferentes recuentos de perfiles en Campañas en comparación con los Recorridos?

Es posible que observe que la misma audiencia muestra diferentes recuentos de perfiles cuando se visualizan en Campañas en comparación con los Recorridos. Esto sucede porque cada función utiliza diferentes API para recuperar datos de audiencia, que pueden devolver valores diferentes.

Este es el comportamiento esperado y no afecta a la ejecución de la campaña: los perfiles correctos seguirán siendo el objetivo. Para comprobar el tamaño real de la audiencia, ve a **[!UICONTROL Cliente]** > **[!UICONTROL Audiencias]** y selecciona tu audiencia.

+++


+++ ¿Cómo se resuelven los problemas de población de audiencia?

Pueden producirse problemas de población de audiencias cuando faltan componentes o recursos, a menudo debido a errores de configuración de derechos, aprovisionamiento o permisos. Para solucionar estos problemas, comience por verificar las autorizaciones, garantizar el aprovisionamiento correcto y revisar los permisos. Si el problema persiste, escale el caso y coordine con los equipos de asistencia para una solución completa.

Obtenga más información acerca de la administración de audiencias [en esta página](../audience/about-audiences.md).

+++

+++ ¿Por qué el recuento de Perfiles atractivos ha aumentado significativamente en un corto periodo? 

La métrica **Perfiles atractivos** refleja la cantidad de perfiles únicos involucrados por recorridos o campañas en los últimos 12 meses. Un aumento repentino puede deberse a recorridos o campañas dirigidas a grandes audiencias que no se han involucrado recientemente o a cambios en conjuntos de datos habilitados para el servicio de perfil.

Para investigar y resolver este problema, debe comprender la lógica de recuento de perfiles, investigar los recorridos y campañas dirigidos a audiencias grandes, filtrar audiencias apropiadamente, monitorizar los cambios en los conjuntos de datos y reducir potencialmente el tamaño de la audiencia a la que se puede dirigir.

Aprenda a solucionar problemas y resolver los incrementos de perfiles atractivos, y a monitorizar el uso de licencias de su organización en la [documentación del tablero de uso de licencias](../audience/license-usage.md#troubleshooting-engageable-profiles).

+++

+++ ¿Por qué se envían correos electrónicos a personas fuera de la audiencia objetivo en función de las funciones de fecha?

Es posible que se envíen correos electrónicos a los destinatarios que **no cumplan los criterios de audiencia especificados**. Por ejemplo, los miembros con fechas de canje **anteriores al 4 de julio de 2025** pueden recibir correos electrónicos destinados únicamente a los que venzan después de esa fecha. Este comportamiento puede deberse a **segmentación de audiencia mal configurada** o a **cambios inesperados en la lógica de calificación de perfiles**. Revise la definición de la audiencia y pruébela con perfiles de muestra para comprobar que la lógica de fecha se aplica correctamente.

Obtenga más información acerca de las funciones de fecha [en esta página](../building-journeys/functions/date-functions.md).

+++

+++ ¿Por qué las entregas y las exclusiones superan el tamaño de mi audiencia objetivo en los informes de campaña?

En los informes de campaña, es posible que observe que la suma de **Delivered** y **Exclusions** supera el tamaño de audiencia de destino original. Esto ocurre porque la métrica **Exclusiones** cuenta todos los eventos de exclusión, incluidos los eventos de exclusión duplicados para el mismo perfil. Si un perfil se excluye varias veces durante una campaña, cada evento se cuenta por separado.

**Ejemplo**: una campaña dirigida a 94 000 perfiles muestra 69 000 destinatarios entregados y 37 000 exclusiones, lo que hace un total de 106 000, lo que supera los 94 000 perfiles de destino originales. Este es el comportamiento esperado.

Para comprender la diferencia entre el total de eventos de exclusión y las exclusiones de perfil único, consulte la [explicación de recuento de exclusiones](../reports/exclusion-list.md#exclusion-list).

Obtenga más información sobre [informes de Campaign](../reports/campaign-global-report-cja.md) y [métricas de informes](../reports/global-report-components-cja.md).

+++

+++ ¿Cómo resuelvo los problemas de selección de audiencias y los errores de Chrome al guardar recorridos?

Añadir audiencias a condiciones de recorrido a veces puede provocar **bloqueos de la aplicación** o mostrar un **error de ajuste de Aw** en Chrome, incluidos errores al guardar recorridos. Estos problemas suelen estar relacionados con **Servicios de Chromium**. Para resolverlos, aplique una **actualización del explorador**, borre la caché del explorador o intente una sesión diferente del explorador.

Más información sobre [cómo navegar por la interfaz de Journey Optimizer](user-interface.md).

+++

## Recorridos {#ajo-troubleshooting-journeys}

Para obtener Recorridos, consulte las siguientes secciones de solución de problemas:

* [Solucionar errores antes de probar el recorrido](../building-journeys/troubleshooting.md)
* [Solución de problemas de acciones entrantes en recorridos](../building-journeys/troubleshooting-inbound.md)
* [Solucionar problemas de ejecución de recorrido activo](../building-journeys/troubleshooting-execution.md)
* [Solución de problemas de acciones personalizadas](../action/troubleshoot-custom-action.md)


+++ ¿Por qué se pierden las expresiones al crear una nueva versión del recorrido?  

Al crear una nueva versión de un recorrido, se pueden perder **expresiones en pasos específicos**, causando errores y requiriendo la reentrada manual. Para resolver esto, **duplique el recorrido**, pruebe la reproducibilidad, **evite las recargas del explorador** y use el **lienzo actualizado** para recorridos más antiguos.

Aprenda a duplicar un recorrido [en esta página](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ ¿Por qué los perfiles abandonan los recorridos prematuramente? 

Los perfiles pueden salir de un recorrido inesperadamente sin pasar por un nodo designado cuando la **comprobación de condición del estado de los comentarios** de los mensajes enviados está mal configurada. Para resolver esto, revise la **lógica de condición**, implemente la **lógica alternativa** o consulte con su **equipo de implementación**.

Consulte también [Directrices de diseño de Recorrido](../building-journeys/using-the-journey-designer.md).

+++


+++ ¿Por qué los perfiles salen de los recorridos inesperadamente?

Los perfiles pueden salir de un recorrido de forma inesperada cuando se produce **límite de eventos**, lo que provoca que algunos perfiles se descarten si el número de eventos procesados supera la capacidad del sistema. Para reducir las salidas de perfiles, comprenda los **límites del sistema**, supervise los **picos de eventos** y optimice el **flujo de datos** para evitar que se excedan los umbrales.

Consulte también [protecciones de Recorrido](../start/guardrails.md#decisioning-guardrails).

+++


+++ ¿Por qué mi evento no activa el recorrido deseado?  

Es posible que los eventos no almacenen en déclencheur un recorrido aunque se cumplan todos los criterios cuando se **crean mediante los servicios de consulta** en lugar de transmitirse al **Servicio principal de recopilación de datos (DCCS)**. Para resolver esto, revise la configuración del evento, asegúrese de que los eventos se **transmiten directamente a DCCS** y compruebe la funcionalidad mediante **modo de prueba**.

Más información sobre los eventos [en esta página](../event/about-events.md).

Consulte también [protecciones de eventos de Recorrido](../start/guardrails.md#events-g).

+++


+++ ¿Cómo puedo resolver los problemas de déclencheur de recorrido después de los cambios de audiencia en Adobe Journey Optimizer? 

Si un recorrido deja de activarse después de realizar modificaciones en su audiencia asociada (como cambios en la política de combinación), puede experimentar flujos interrumpidos. Para resolver esto, **duplique y vuelva a publicar el recorrido** con la configuración de audiencia actualizada para garantizar que los déclencheur funcionen correctamente.

Aprenda a duplicar un recorrido [en esta página](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ ¿Por qué se agota el tiempo de espera de una acción personalizada que llama a un extremo de terceros externo?

Pueden producirse errores de tiempo de espera cuando una **acción personalizada** llama a un extremo externo de terceros. Para resolver esto, compruebe que el extremo **es accesible**, compruebe **registros del servidor**, asegúrese de que no haya **ningún bloqueo de Adobe**, actualice las configuraciones de extremo según sea necesario y **pruebe después de las actualizaciones**. Además, tenga en cuenta **las especificaciones de tiempo de espera de llamada API**.

Obtenga más información acerca de la API de restricción de Recorrido [en esta página](../configuration/throttling.md).

Consulte también la [documentación sobre la integración con sistemas externos](../configuration/external-systems.md).

+++

+++ ¿Qué pasos debe seguir si se produce un error 403 con el mensaje **invalid_access** o **No se concede acceso a este dataId=XX** al publicar una audiencia desde un recorrido?

Para resolver este error, pídale al administrador que compruebe que su perfil de usuario tiene acceso a las vistas de datos necesarias para la publicación de audiencias e intente publicar la audiencia de nuevo.

Consulte [la documentación de permisos](../administration/permissions.md) para conocer los pasos que debe seguir para resolver este problema.

+++

## Reglas {#ajo-troubleshooting-rules}

+++ ¿Por qué no funciona el menú desplegable Reglas de límite?

Los problemas con el **menú desplegable de reglas de límite** suelen producirse cuando los conjuntos de reglas están **mal configurados** o **inaccesibles**. Asegúrese de que todos los conjuntos de reglas estén correctamente configurados y disponibles para resolver el problema.

Aprenda a aplicar reglas de límite [en esta sección](../conflict-prioritization/rule-sets.md).

+++

+++ ¿Por qué no se aplica una regla de límite de frecuencia a mi campaña o recorrido?

Las reglas de restricción de frecuencia solo surten efecto cuando el conjunto de reglas se adjunta explícitamente a la campaña o al recorrido. Si el límite no funciona, compruebe que esté seleccionado el conjunto de reglas correcto en la configuración de campaña o recorrido, que el tipo de canal de la regla coincida con el canal que se está utilizando y que la regla tenga el estado **Activo**. Compruebe también si el perfil ya ha alcanzado el límite en una ejecución anterior, lo que impediría recibir más mensajes aunque la regla aparezca correctamente configurada.

Obtenga información sobre cómo configurar las reglas de límite de canal [en esta página](../conflict-prioritization/channel-capping.md).

+++

+++ ¿Cómo configuro las horas de silencio para evitar que los mensajes se envíen por la noche?

Las horas silenciosas son reglas de exclusión basadas en el tiempo configuradas dentro de un **conjunto de reglas de canal**. Defina la ventana de interrupción (por ejemplo, de 22:00 a 08:00) y aplique el conjunto de reglas a las campañas o recorridos relevantes. Cuando se programa el envío de un mensaje durante las horas de inactividad, Journey Optimizer lo retiene hasta la siguiente ventana permitida o lo descarta, según la configuración de la regla.

Aprenda a configurar las horas de inactividad [en esta página](../conflict-prioritization/quiet-hours.md).

+++

## Toma de decisiones {#ajo-troubleshooting-decisioning}

+++ ¿Cómo puedo resolver los problemas al crear colecciones de ofertas?

Las dificultades para crear colecciones de ofertas suelen ocurrir cuando no se han aprovisionado **catálogos** para su organización. Para resolver esto, compruebe que todos los catálogos requeridos estén aprovisionados correctamente antes de intentar crear colecciones de ofertas.

Obtenga más información acerca de las colecciones de ofertas [en esta página](../offers/offer-library/creating-collections.md).

+++

+++ ¿Por qué no puedo acceder a Offer Decisioning?  

Al integrar Adobe Target en una aplicación mediante Adobe Journey Optimizer, es posible que no se pueda acceder a la opción **Offer Decisioning** desde la configuración de la secuencia de datos. Esto suele deberse a **configuración de permisos** o a **restricciones de aprovisionamiento**. Para resolver el problema, compruebe los permisos de usuario y asegúrese de que se dispone del aprovisionamiento necesario.

Obtenga más información acerca de los permisos necesarios para Offer Decisioning [en esta página](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++

+++ ¿Por qué no se devuelve una oferta aunque cumpla los criterios de idoneidad?

Si una oferta que cumple los requisitos no aparece en una respuesta de toma de decisiones, compruebe lo siguiente en orden: compruebe que la oferta está en estado **Aprobado** (no Borrador); confirme que el ID de ubicación de la solicitud coincide con la superficie de representación de la oferta; compruebe si se ha alcanzado algún límite (total o por perfil) para esa oferta; y asegúrese de que la recopilación y el ámbito de decisión estén correctamente configurados. Utilice la herramienta **Simulation** de Experience Decisioning para probar las respuestas de oferta con un perfil específico sin enviar tráfico en directo.

Obtenga información sobre cómo empezar a usar Experience Decisioning [en esta página](../experience-decisioning/gs-experience-decisioning.md).

+++


## Multilingüe {#ajo-troubleshooting-multilingual}

+++ ¿Cómo resolver este problema `Message validation error (CJMMAS - 1069-500)`?

En Adobe Journey Optimizer, un error de validación de mensaje (CJMMAS - 1069-500) vinculado a la función multilingüe evita que las recorridos se establezcan en el modo de prueba o publiquen. Compruebe que todo el contenido de la configuración regional esté completo, que el idioma principal esté configurado correctamente y que no haya campos de traducción obligatorios vacíos antes de intentar publicar.

Obtenga más información acerca del contenido multilingüe [en esta página](../content-management/multilingual-gs.md).

+++

+++ ¿Por qué el proveedor de traducción no se conecta en Journey Optimizer?

Los errores de conexión del proveedor de traducción suelen deberse a credenciales de API incorrectas o a una configuración de proveedor que falta en la configuración multilingüe. Compruebe que la clave de API, la dirección URL del extremo y cualquier token de autenticación requerido introducido en Journey Optimizer coinciden exactamente con lo que ha proporcionado su proveedor de traducción. Si las credenciales son correctas, compruebe si la cuenta de proveedor tiene cuota suficiente o estado de suscripción activo y, a continuación, guarde y vuelva a probar la conexión.

Aprenda a configurar un proveedor de traducción [en esta página](../content-management/multilingual-provider.md).

+++

+++ ¿Qué sucede cuando falta una traducción para una configuración regional?

Si no se ha proporcionado una traducción para una configuración regional específica, Journey Optimizer vuelve al contenido definido en el **idioma principal** (configuración regional de reserva) configurado en la configuración de idioma. Si no se configura ninguna reserva, el mensaje puede procesarse como vacío o dar error a la validación antes de enviarlo. Para evitarlo, defina siempre una configuración regional de reserva en la configuración del proyecto multilingüe y compruebe que todas las configuraciones regionales tengan traducciones aprobadas antes de activar la campaña o el recorrido.

Obtenga más información acerca de la configuración de contenido multilingüe [en esta página](../content-management/multilingual-gs.md).

+++


## Configuración {#ajo-troubleshooting-config}

+++ ¿Cómo habilito TLS v1.3 para acciones personalizadas?  

Para mantener la **integridad y seguridad de los datos** al conectarse a sistemas de terceros, asegúrese de que Transport Layer Security (**TLS**) v1.3 esté habilitado para sus acciones personalizadas. Esto ayuda a proteger las comunicaciones y evita posibles vulnerabilidades de seguridad.

Obtenga más información acerca de la configuración de acciones personalizadas [en esta página](../action/about-custom-action-configuration.md).

+++

+++ ¿Por qué no puedo crear un tablero directamente a partir de una consulta en Adobe Journey Optimizer? 

En Adobe Journey Optimizer, los paneles no se pueden crear directamente a partir de consultas. Para crear paneles, use las **funcionalidades de creación de paneles** disponibles en Adobe Experience Platform, que le permiten visualizar y analizar los datos de las consultas de forma eficaz.

Obtenga más información acerca de las consultas en Journey Optimizer [en esta página](../data/get-started-queries.md).

+++

+++ ¿Por qué la lista de supresión bloquea mis mensajes?

Las direcciones se añaden automáticamente a la lista de supresión después de rechazos graves, quejas por correo no deseado o adiciones manuales realizadas por un administrador. Una vez suprimido, un perfil no recibirá ningún mensaje de ese canal, independientemente de la campaña o el objetivo del recorrido. Para investigar, abra **Administración** > **Canales** > **Lista de supresión** y busque la dirección. Si la supresión se añadió por error, se puede eliminar directamente de la interfaz. Para las supresiones de devoluciones graves, revise también el problema de capacidad de entrega subyacente antes de eliminar la dirección.

Obtenga información sobre cómo administrar la lista de supresión [en esta página](../configuration/manage-suppression-list.md).

+++

## API {#ajo-troubleshooting-apis}

+++ ¿Cómo puedo resolver los problemas de acceso con la API del servicio de consultas?  

Los errores de acceso al usar la **API del servicio de consultas** a través de Postman o herramientas similares suelen deberse a **permisos insuficientes**. Para resolver esto, compruebe los permisos de usuario, compruebe las credenciales de la API con las funciones configuradas en su organización y proporcione información detallada para la asistencia si es necesario.

Obtenga más información acerca de los permisos en Journey Optimizer [en esta página](../administration/permissions.md).

+++

+++ ¿Cómo resuelvo 429 Errores de demasiadas solicitudes al llamar a las API de Journey Optimizer?

Una respuesta 429 significa que la integración ha superado el límite de tasa de API para el punto de conexión. Cada API de Journey Optimizer tiene umbrales de rendimiento definidos. Para resolver esto, implemente la lógica **retroceso exponencial** en su integración: espere durante el tiempo especificado en el encabezado de respuesta `Retry-After` antes de volver a intentarlo. Para casos de uso de gran volumen sostenido, revise la configuración de restricción y límite para sus acciones personalizadas y fuentes de datos para alinear las tasas de llamadas de API con los límites del sistema.

Obtenga más información acerca de la restricción de Journey Optimizer [en esta página](../configuration/throttling.md).

Consulte también la [documentación de integración de sistemas externos](../configuration/external-systems.md).

+++

+++ ¿Por qué mi campaña activada por API no se ejecuta después de la llamada de API?

Si no se está ejecutando una campaña desencadenada por API, compruebe lo siguiente: la campaña está en estado **Activo** (no borrador ni detenido); la llamada de API incluye el ID de campaña correcto en la ruta de acceso del extremo; la carga útil de la solicitud coincide con el esquema del identificador de perfil esperado por la campaña; y las credenciales de API utilizadas tienen el permiso **Administrar campañas**. Compruebe los registros de ejecución de la campaña en el panel de informes para identificar si el perfil se recibió pero se excluyó, o si la llamada no llegó a la campaña en absoluto.

Obtenga más información acerca de las campañas activadas por API [en esta página](../campaigns/api-triggered-campaigns.md).

+++
