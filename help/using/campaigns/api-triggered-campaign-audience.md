---
solution: Journey Optimizer
product: journey optimizer
title: Defina la audiencia de campaña activada por API
description: Obtenga información sobre cómo definir la audiencia de campaña activada por API.
topic: Content Management
role: Developer
level: Experienced
keywords: campañas, activadas por API, REST, optimizador, mensajes
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 1%

---


# Defina la audiencia de campaña activada por API {#api-audience}

Utilice la ficha **[!UICONTROL Audiencia]** para definir la audiencia de la campaña.

![](assets/campaign-audience.png)

1. **Selección de la audiencia**

   * Para las campañas activadas por la API de marketing, haga clic en el botón **[!UICONTROL Seleccionar audiencia]** para mostrar la lista de audiencias de Adobe Experience Platform disponibles. [Más información sobre las audiencias](../audience/about-audiences.md).

     >[!IMPORTANT]
     >
     >El uso de audiencias y atributos de [composición de audiencias](../audience/get-started-audience-orchestration.md) no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield.

   * Para las campañas transaccionales activadas por API, los perfiles objetivo deben definirse en la llamada de API. Una sola llamada de API admite hasta 20 destinatarios únicos. Cada destinatario debe tener un ID de usuario único, no se permiten ID de usuario duplicados. Obtenga más información en la [documentación interactiva de la API de ejecución de mensajes](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution/operation/postIMUnitaryMessageExecution){target="_blank"}

1. **Seleccionar el tipo de identidad**

   En el campo **[!UICONTROL Tipo de identidad]**, elija el tipo de clave que desea usar para identificar a los individuos de la audiencia seleccionada. Puede utilizar un tipo de identidad existente o crear uno nuevo mediante el servicio de identidad de Adobe Experience Platform. Las áreas de nombres de identidad estándar se enumeran en [esta página](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

   Solo se permite un tipo de identidad por campaña. La campaña no puede dirigirse a las personas que pertenezcan a un segmento que no tenga el tipo de identidad seleccionado entre sus diferentes identidades. Obtenga más información acerca de tipos de identidad y áreas de nombres en la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=es){target="_blank"}.

1. **Activar creación de perfiles en la ejecución de la campaña**

   En algunos casos, es posible que deba enviar mensajes transaccionales a perfiles que no existen en el sistema. Por ejemplo, si un usuario desconocido intenta restablecer la contraseña en su sitio web. Cuando un perfil no existe en la base de datos, Journey Optimizer le permite crearlo automáticamente al ejecutar la campaña para permitir el envío del mensaje a este perfil.

   Para activar la creación de perfiles en la ejecución de la campaña, active la opción **[!UICONTROL Crear nuevos perfiles]**. Si esta opción está deshabilitada, los perfiles desconocidos se rechazarán para cualquier envío y la llamada de API fallará.

   ![](assets/api-triggered-create-profile.png)

   >[!IMPORTANT]
   >
   >Esta opción se proporciona para la **creación de perfiles de volumen muy pequeño** en un caso de uso de envío transaccional de gran volumen, con una gran cantidad de perfiles ya existentes en la plataforma.
   >
   >Se crean perfiles desconocidos en el conjunto de datos **AJO Interactive Messaging Profile Dataset**, en tres áreas de nombres predeterminadas (correo electrónico, teléfono y ECID) respectivamente para cada canal saliente (correo electrónico, SMS y push). Sin embargo, si utiliza un área de nombres personalizada, la identidad se crea con el mismo área de nombres personalizada.

## Pasos siguientes {#next}

Una vez que la configuración y el contenido de la campaña estén listos, puede programar su ejecución. [Más información](api-triggered-campaign-schedule.md)
