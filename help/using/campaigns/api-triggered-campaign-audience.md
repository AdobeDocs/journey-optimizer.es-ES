---
solution: Journey Optimizer
product: journey optimizer
title: Defina la audiencia de campaña activada por API
description: Obtenga información sobre cómo definir la audiencia de campaña activada por API.
topic: Content Management
role: Developer
level: Experienced
keywords: campañas, activadas por API, REST, optimizador, mensajes
exl-id: 6dda5687-3742-4e88-be7c-c4969b183161
TQID: https://experienceleague.adobe.com/JHnyTJxE0TwHX-izzEQ0VG60L2P2j63anyPQbbdBZ6k
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2: id: f7479fa1-474b-479d-8c98-f6cee5865a38id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: a5c0537a45acbc708ce62bd05a569630230201ac
workflow-type: tm+mt
source-wordcount: 571
ht-degree: 3%

---

# Defina la audiencia de campaña activada por API {#api-audience}

>[!BEGINSHADEBOX]

**En esta página:** Defina la audiencia, el tipo de identidad, la creación automática de perfiles y los enlaces web para que la campaña activada por la API llegue a las personas adecuadas y devuelva el estado de envío en tiempo real.

>[!ENDSHADEBOX]

Utilice la ficha **[!UICONTROL Audiencia]** para definir la audiencia de la campaña.

![](assets/campaign-audience.png)

## Selección del público

**Para las campañas activadas por la API de marketing**, haga clic en el botón **[!UICONTROL Seleccionar audiencia]** para mostrar la lista de audiencias de Adobe Experience Platform disponibles. [Más información sobre las audiencias](../audience/about-audiences.md).

>[!IMPORTANT]
>
>El uso de audiencias y atributos de [composición de audiencias](../audience/get-started-audience-orchestration.md) no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield.

**Para las campañas transaccionales activadas por API**, los perfiles de destino deben definirse en la llamada de API. Una sola llamada de API admite hasta 20 destinatarios únicos. Cada destinatario debe tener un ID de usuario único, no se permiten ID de usuario duplicados. Obtenga más información en la [documentación interactiva de la API de ejecución de mensajes](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMUnitaryMessageExecution){target="_blank"}

## Selección del tipo de identidad

En el campo **[!UICONTROL Tipo de identidad]**, elija el tipo de clave que desea usar para identificar a los individuos de la audiencia seleccionada. Puede utilizar un tipo de identidad existente o crear uno nuevo mediante el servicio de identidad de Adobe Experience Platform. Las áreas de nombres de identidad estándar se enumeran en [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

Solo se permite un tipo de identidad por campaña. La campaña no puede dirigirse a las personas que pertenezcan a un segmento que no tenga el tipo de identidad seleccionado entre sus diferentes identidades. Obtenga más información acerca de tipos de identidad y áreas de nombres en la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=es){target="_blank"}.

## Activar creación de perfiles en ejecución de campaña

En algunos casos, es posible que deba enviar mensajes transaccionales a perfiles que no existen en el sistema. Por ejemplo, si un usuario desconocido intenta restablecer la contraseña en su sitio web. Cuando un perfil no existe en la base de datos, Journey Optimizer le permite crearlo automáticamente al ejecutar la campaña para permitir el envío del mensaje a este perfil.

Para activar la creación de perfiles en la ejecución de la campaña, active la opción **[!UICONTROL Crear nuevos perfiles]**. Si esta opción está deshabilitada, los perfiles desconocidos se rechazarán para cualquier envío y la llamada de API fallará.

![](assets/api-triggered-create-profile.png)

>[!IMPORTANT]
>
>Esta opción se proporciona para la **creación de perfiles de volumen muy pequeño** en un caso de uso de envío transaccional de gran volumen, con una gran cantidad de perfiles ya existentes en la plataforma.
>
>Se crean perfiles desconocidos en el conjunto de datos **AJO Interactive Messaging Profile Dataset**, en tres áreas de nombres predeterminadas (correo electrónico, teléfono y ECID) respectivamente para cada canal saliente (correo electrónico, SMS y push). Sin embargo, si utiliza un área de nombres personalizada, la identidad se crea con el mismo área de nombres personalizada.
>
>La creación de perfiles en la ejecución no está disponible para [campañas de alto rendimiento](../campaigns/api-triggered-high-throughput.md), ya que este modo no depende de perfiles de Adobe. El sistema no comprobará si los perfiles existen o no.

## Habilitar webhooks {#webhook}

Para las campañas activadas por API transaccionales, puede habilitar los webhooks para recibir comentarios en tiempo real sobre el estado de ejecución de sus mensajes. Para ello, cambie la opción **[!UICONTROL Enable webhooks]** para enviar eventos de estado de entrega a un webhook configurado.

![](assets/api-triggered-webhook.png)

Las configuraciones de webhook se administran centralmente en el menú **[!UICONTROL Administración]** / **[!UICONTROL Canales]** / **[!UICONTROL Comentarios de webhook]**. Desde allí, los administradores pueden crear y editar puntos finales de ganchos web. [Aprenda a crear Webhooks de comentarios](../configuration/feedback-webhooks.md)

## Próximos pasos {#next}

Una vez que la configuración y el contenido de la campaña estén listos, puede programar su ejecución. [Más información](api-triggered-campaign-schedule.md)
