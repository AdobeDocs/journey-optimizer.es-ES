---
solution: Journey Optimizer
product: journey optimizer
title: Directrices de CNIL sobre los píxeles de seguimiento de correo electrónico
description: Obtenga información acerca de las directrices actualizadas de CNIL sobre los píxeles de seguimiento de correo electrónico y los controles de Adobe Journey Optimizer que pueden apoyar sus esfuerzos de conformidad.
feature: Privacy, Consent Management
topic: Content Management
role: User
level: Intermediate
keywords: CNIL, seguimiento, píxel, correo electrónico, consentimiento, exclusión, privacidad
source-git-commit: 66b0ca498ae2b39575ed57118739234d1f54c887
workflow-type: tm+mt
source-wordcount: '1466'
ht-degree: 1%

---


# Explicación de las directrices actualizadas de CNIL sobre los píxeles de seguimiento de correo electrónico {#cnil-pixel-tracking}

>[!BEGINSHADEBOX]

**En esta página:** Obtenga información acerca de la recomendación de abril de 2026 de CNIL sobre los píxeles de seguimiento de correo electrónico y descubra los controles de Adobe Journey Optimizer (alternadores de seguimiento abiertos, seguimiento de nivel de vínculo, administración de consentimiento, mecanismos de exclusión y supresión) que pueden apoyar sus esfuerzos de conformidad.

>[!ENDSHADEBOX]

>[!NOTE]
>
>Esta página es solo con fines informativos. No es asesoramiento legal y no garantiza el cumplimiento de la ley aplicable. Las funcionalidades del producto de Adobe Journey Optimizer que se describen a continuación son componentes básicos que, configurados y operados correctamente, pueden admitir una implementación compatible. Cada cliente es responsable de determinar y cumplir con sus obligaciones según la ley aplicable.

## Información general {#overview}

El 14 de abril de 2026, la *Comisión Nacional de Informática y Libertades* (CNIL), la autoridad de protección de datos de Francia, publicó una [recomendación sobre el uso de píxeles de seguimiento en correos electrónicos](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf). La guía aclara cuándo se requiere el consentimiento y resalta la importancia de las prácticas de consentimiento adecuadas para el seguimiento de píxeles del correo electrónico. Esta política podría afectar a las prácticas de envío de cualquier entidad que envíe correos electrónicos a suscriptores con sede en Francia.

CNIL proporcionó a las empresas un periodo de tres meses a partir de la fecha de la recomendación para informar a sus destinatarios de correo electrónico (&quot;usuarios&quot;) de la presencia de los píxeles de seguimiento, su propósito y el derecho de los usuarios a la exclusión. Durante este período de transición, se espera que los clientes notifiquen a los usuarios el seguimiento de píxeles y proporcionen una exclusión si es necesario. Se espera que **CNIL comience las actividades de aplicación después del 14 de julio de 2026.**

A medida que la CNIL y otros reguladores aclaren las directrices sobre el seguimiento de píxeles y problemas relacionados, Adobe seguirá supervisando las actualizaciones e informando a los clientes de las funciones técnicas de los productos de Adobe que admiten el marketing por correo electrónico, incluido Adobe Journey Optimizer.

Adobe Journey Optimizer proporciona controles que pueden ayudar a los clientes a administrar el seguimiento abierto en el nivel de entrega. Los clientes son responsables de determinar sus propias obligaciones de cumplimiento según las directrices de CNIL aplicables y otras leyes, pero estas capacidades pueden apoyar los esfuerzos de cumplimiento de los clientes.

## Qué es un píxel de seguimiento de correo electrónico {#tracking-pixel}

Un píxel de seguimiento de correo electrónico es una imagen transparente 1x1 incrustada en el HTML de un correo electrónico. Cuando el cliente de correo electrónico del destinatario carga esa imagen, el píxel hace ping a un servidor que registra datos como una marca de tiempo, un tipo de dispositivo, un cliente de correo electrónico y, a veces, una dirección IP para obtener una ubicación aproximada. A continuación, ese registro se vincula al registro de un destinatario, lo que permite a los especialistas en marketing ver si se abre un correo electrónico.

## Atención al cliente {#support}

Los clientes que busquen ayuda para implementar los cambios descritos anteriormente pueden interactuar con el ecosistema de Adobe existente. Para preguntas técnicas sobre las funcionalidades de Adobe a las que se hace referencia, póngase en contacto con el administrador de éxito del cliente o con el administrador técnico de cuentas.

## Funcionalidad de Adobe Journey Optimizer relacionada con el seguimiento de correo electrónico {#ajo-functionality}

Adobe Journey Optimizer proporciona varios controles nativos para ayudar a los clientes a abordar los elementos de la guía CNIL. Las secciones siguientes describen las funciones de producto relevantes.

### Clasificación de tipo de correo electrónico {#email-type}

En Adobe Journey Optimizer, cada configuración de canal de correo electrónico se clasifica como Marketing o Transaccional. Esta clasificación determina si se requiere el consentimiento del suscriptor antes de enviar.

* **Correos electrónicos de marketing**: se han enviado comunicaciones promocionales a los suscriptores de inclusión. Se requiere el consentimiento del usuario. Estos correos electrónicos respetan automáticamente las preferencias de supresión y exclusión.
* **Correos electrónicos de transacción**: comunicaciones no comerciales (por ejemplo, confirmaciones de pedidos, restablecimientos de contraseñas). Pueden enviarse a perfiles que hayan cancelado la suscripción a comunicaciones de marketing, según la legislación aplicable.

El tipo de correo electrónico se establece en el nivel [configuración de canal](../email/email-settings.md#email-type). Al crear un correo electrónico en un recorrido o campaña, los autores deben seleccionar una configuración de canal cuyo tipo de correo electrónico coincida con la naturaleza de la comunicación. Esta clasificación indica qué comprobaciones de consentimiento se aplican antes de la entrega.

### Abrir controles de seguimiento {#open-tracking}

Adobe Journey Optimizer permite a los especialistas en marketing controlar el seguimiento abierto (es decir, el píxel 1x1) en el nivel de mensaje individual. Al crear un correo electrónico en un recorrido o campaña, hay dos opciones de seguimiento disponibles en el panel de propiedades del mensaje:

* **[!UICONTROL Aperturas del correo electrónico]**: controla si el píxel de seguimiento abierto se incluye en el correo electrónico. Esta opción está habilitada de manera predeterminada.
* **[!UICONTROL Hacer clic en el correo electrónico]**: controla si se realiza un seguimiento de los clics en los vínculos. Esta opción también está habilitada de forma predeterminada.

Para deshabilitar el seguimiento de aperturas para un correo electrónico específico, anule la selección de la opción **[!UICONTROL Aperturas de correos electrónicos]** al crear el mensaje. Cuando está desactivada, la opción evita que se recopilen los datos de seguimiento abiertos para esa entrega. Para las organizaciones que envían a suscriptores franceses, revise la configuración de seguimiento abierta para todos los recorridos y campañas activos antes de la fecha de aplicación.

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
Clarify whether unchecking "Email opens" fully removes the 1x1 tracking pixel from the delivered HTML, or whether the pixel is still present in the HTML but open data is suppressed at the data processing layer only. The current wording ("prevents open tracking data from being collected") is intentionally neutral. If the pixel is removed: update to state this explicitly. If the pixel remains but data is not processed: reword to make that distinction clear, to avoid misleading customers seeking CNIL compliance.
-->

[Obtenga información sobre cómo rastrear mensajes](../email/message-tracking.md)

### Administración de seguimiento a nivel de vínculo {#link-tracking}

Más allá de la opción de seguimiento de apertura por mensaje, Email Designer de Adobe Journey Optimizer proporciona un control granular sobre las direcciones URL que se rastrean. Con el panel **[!UICONTROL Links]** del Designer de correo electrónico, los autores pueden ver todas las direcciones URL rastreadas en un mensaje y establecer el modo de seguimiento para cada vínculo de forma individual.

Los modos de seguimiento disponibles para cada vínculo incluyen:

* **Habilitado**: activa el seguimiento en esta dirección URL.
* **Exclusión**: Designa esta dirección URL como una dirección URL de exclusión o de baja.
* **Página espejo**: designa esta dirección URL como vínculo de página espejo.
* **Nunca**: el seguimiento nunca se activa para esta dirección URL, independientemente de la configuración de nivel de mensaje.

Establecer vínculos específicos en **Nunca** puede ayudar a garantizar que no se realice el seguimiento de ciertas direcciones URL aunque el seguimiento en el nivel de mensaje esté habilitado.

[Obtenga información sobre cómo administrar el seguimiento en Email Designer](../email/message-tracking.md#manage-tracking)

### Captura y administración del consentimiento {#consent-management}

Adobe Journey Optimizer administra el consentimiento a través del [esquema de preferencias y consentimiento](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=es){target="_blank"} de Adobe Experience Platform (AEP). Las preferencias de consentimiento se almacenan en el nivel de perfil y se aplican automáticamente durante el recorrido y la ejecución de la campaña.

Los atributos de consentimiento clave relevantes para el seguimiento de correo electrónico incluyen:

* **`consents.marketing.email.val`**: campo principal de consentimiento de marketing por correo electrónico. Un valor de `y` indica la inclusión; `n` indica la exclusión. Un valor vacío se trata como consentimiento de forma predeterminada (este valor predeterminado se puede cambiar durante la incorporación).

### Mecanismos de exclusión y retirada {#opt-out}

Adobe Journey Optimizer ofrece varios mecanismos para que los suscriptores se excluyan de las comunicaciones y administren sus preferencias, todos los cuales actualizan los atributos de consentimiento del perfil en Adobe Experience Platform.

**Cancelar la suscripción con un solo clic (encabezado de correo electrónico)**

Cuando la opción **[!UICONTROL Habilitar cancelación de suscripción a una lista]** está activada en la configuración del canal de correo electrónico, se agrega automáticamente al encabezado del correo electrónico una dirección URL de cancelación de suscripción de un solo clic y una dirección mailto. Los destinatarios pueden excluirse directamente de su cliente de correo electrónico sin hacer clic en el cuerpo del correo electrónico. Esta opción está habilitada de forma predeterminada para las nuevas configuraciones de canal.

[Obtenga información sobre cómo configurar la cancelación de suscripción a una lista](../email/list-unsubscribe.md)

**Exclusión con un clic (cuerpo del correo electrónico)**

Los autores pueden insertar un vínculo de no participación de un solo clic directamente en el contenido del correo electrónico mediante el Designer de correo electrónico. Cuando un destinatario hace clic en este vínculo, su preferencia se actualiza inmediatamente. La exclusión se puede definir en cualquiera de las siguientes ubicaciones:

* **Nivel de canal**: Excluye el perfil de todas las comunicaciones por correo electrónico futuras entre canales.
* **Nivel de identidad**: excluye la dirección de correo electrónico específica utilizada solo en el mensaje actual.

[Obtenga información sobre cómo añadir un vínculo de no participación de un clic](../email/email-opt-out.md#one-click-opt-out)

**Centro de preferencias mediante páginas de aterrizaje**

La funcionalidad de página de aterrizaje nativa de Adobe Journey Optimizer permite a las organizaciones crear centros de preferencias en los que los suscriptores pueden administrar sus preferencias de comunicación y seguimiento. Cuando un suscriptor envía un formulario de centro de preferencias, sus opciones se escriben de nuevo en sus atributos de perfil de AEP en el grupo de campos Consentimiento y Preferencias.

En los casos de cumplimiento de la CNIL, se puede vincular una página de aterrizaje del centro de preferencias desde el pie del correo electrónico (distinto del vínculo de cancelación de suscripción) para que los destinatarios puedan administrar sus preferencias de seguimiento independientemente de su estado de suscripción.

[Aprenda a administrar las preferencias de sus clientes](../action/preference-center.md)

### Procesamiento y aplicación del consentimiento {#consent-enforcement}

Cuando un destinatario se excluye a través de cualquiera de los mecanismos anteriores, ocurre lo siguiente:

* El atributo de consentimiento del perfil (`consents.marketing.email.val`) se ha actualizado a `n` en Adobe Experience Platform.
* El perfil se excluye inmediatamente de futuros envíos de correo electrónico de marketing en recorridos y campañas.
* La información de exclusión se almacena en el conjunto de datos del servicio de consentimiento de AEP.
* Journey Optimizer realiza una comprobación de consentimiento en el nivel de canal antes de cada envío, lo que garantiza que los perfiles de exclusión no reciban comunicaciones de marketing.

[Más información acerca de la administración de la exclusión](opt-out.md)

### Políticas de consentimiento {#consent-policies}

Las organizaciones pueden crear y aplicar políticas de consentimiento en Adobe Journey Optimizer para garantizar que solo los perfiles que cumplan criterios de consentimiento específicos reciban comunicaciones. Las políticas de consentimiento se pueden asociar a las configuraciones de canal mediante acciones de marketing.

[Aprenda a trabajar con directivas de consentimiento](../action/consent.md)

### Lista de supresión y nueva solicitud {#suppression}

Adobe Journey Optimizer administra automáticamente una lista de supresión que incluye las direcciones de correo electrónico, lo que provoca rechazos graves, rechazos leves o quejas de correo no deseado. Los perfiles de la lista de supresión se excluyen de futuros envíos de marketing.

La API de REST de supresión de Journey Optimizer proporciona control programático adicional sobre los mensajes salientes, lo que permite a las organizaciones administrar el comportamiento de supresión y lista de permitidos mediante API.

[Obtenga información sobre cómo administrar la lista de supresión](../configuration/manage-suppression-list.md)

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
AJO has no native equivalent of Campaign v8's "lastPixelRefusalDate" field or re-solicitation typology rule. If re-solicitation governance for pixel consent refusal is required, customers would likely need to: (a) create a custom XDM date field to capture the pixel refusal date, and (b) build an AEP audience that filters out profiles where that date falls within the last six months, then use that audience as a suppression filter in campaigns/journeys. Confirm with Engineering: (1) whether this guidance should be included in this article, and (2) whether any native AJO improvements are planned in this area.
-->

### Creación de informes {#reporting}

Los informes de correo electrónico de Adobe Journey Optimizer proporcionan métricas de aperturas y clics a través de [informes en vivo](../reports/live-report.md) y [informes de Customer Journey Analytics](../reports/report-gs-cja.md). Cuando el seguimiento de **[!UICONTROL Aperturas del correo electrónico]** está deshabilitado para un mensaje, los datos abiertos no se recopilan para ese envío; los informes reflejarán únicamente los clics y otras señales de participación.

