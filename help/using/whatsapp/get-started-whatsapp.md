---
solution: Journey Optimizer
product: journey optimizer
title: Empezar con los mensajes de WhatsApp
description: Obtenga información sobre la creación y el envío mensajes de WhatsApp en Journey Optimizer
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
TQID: https://experienceleague.adobe.com/uHzRC9X6rB9EXH4gIFiRxFaeNcrTD0-40RrxZkN4XFg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b8df23d2-98a2-4406-86cc-2babe8728d36id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 01105f4dc3f6b52598c634373988570cf6916406
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 92%

---

# Empezar con los mensajes de WhatsApp {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**En esta página:** Entiende cómo funciona el canal WhatsApp en Journey Optimizer, junto con sus requisitos previos y limitaciones, para que puedas decidir cómo añadir WhatsApp a tus recorridos y campañas.

>[!ENDSHADEBOX]

Ahora puede enviar mensajes de WhatsApp directamente a través de Journey Optimizer a través de la [API en la nube](https://developers.facebook.com/docs/whatsapp/cloud-api/) de Meta. Esta función permite la integración optimizada de WhatsApp en recorridos y campañas, lo que mejora la comunicación y la participación con los destinatarios.

* En un **recorrido**. Cree un recorrido, añada una actividad de **WhatsApp**, defina la configuración básica y, a continuación, vaya al panel **[!UICONTROL Acciones: WhatsApp]** para crear el contenido del mensaje de WhatsApp. Aprenda a crear un recorrido en [esta página](../building-journeys/journey-gs.md).

* En una **campaña**. Para crear una campaña, seleccione **WhatsApp** como acción, defina la configuración básica y, a continuación, edite el contenido del mensaje de WhatsApp que desea enviar. Aprenda a crear [una campaña de acción](../campaigns/campaign-action.md#action-campaign-action) | [una campaña desencadenada por API](../campaigns/api-triggered-campaigns.md) | [una campaña orquestada](../orchestrated/create-orchestrated-campaign.md#create)

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Requisitos previos {#prereq}

La integración de WhatsApp con Journey Optimizer requiere lo siguiente:

* Una cuenta de Meta Business Manager
* [Cuenta de empresa de WhatsApp con nombre de remitente y número de teléfono verificados](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [Token de autorización de usuario con los permisos apropiados](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Plantillas de Meta aprobadas](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

También debe tener en cuenta lo siguiente antes de continuar con la integración:

* [Reglas de contenido de WhatsApp](https://www.whatsapp.com/legal/messaging-guidelines)
* [Cumplimiento de las políticas de Meta](https://www.whatsapp.com/legal)
* [Límites de las conversaciones de 24 horas](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## Limitaciones {#limitations}

Las siguientes limitaciones se aplican al canal de WhatsApp:

* El canal de WhatsApp en Adobe Journey Optimizer es compatible con HIPAA, pero los proveedores de terceros no están cubiertos por la BAA de Adobe. Los clientes son responsables de su propia conformidad y validación del proveedor.

* Tenga en cuenta que no se admiten mensajes de respuesta automatizados o predefinidos.

* A partir de abril de 2025, se ha suspendido temporalmente el envío de todos los mensajes de plantilla de marketing a los usuarios de WhatsApp que tengan un número de teléfono de los Estados Unidos (un número compuesto por un código de marcado +1 y un código de área de los Estados Unidos). [Obtenga más información en la documentación de Meta](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* La funcionalidad de integración nativa no permite la integración con proveedores de servicios empresariales (BSP) de terceros.

## Vídeo práctico {#video}

El siguiente vídeo muestra cómo integrar WhatsApp como canal nativo en Adobe Journey Optimizer para enviar mensajes seguros, en tiempo real y personalizados a escala.

+++ Vea el vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3470244?learn=on)

+++

## Recursos de aprendizaje adicionales

Explore más tutoriales en vídeo sobre la mensajería y configuración de WhatsApp.

➡️ [Tutoriales de canal de WhatsApp](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/channels/whatsapp/whatsapp-introduction){target="_blank"}

