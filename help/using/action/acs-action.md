---
solution: Journey Optimizer
product: journey optimizer
title: Integrar con Adobe Campaign Standard
description: Obtenga información sobre cómo integrar Journey Optimizer con Adobe Campaign Standard
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: campaña, estándar, integración, límite, acción
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
TQID: https://experienceleague.adobe.com/1JQFfviWGc3OXYN0YdAh0Koaboro2wJU8HpEf75PoKQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 450
ht-degree: 5%

---

# Integrar con Adobe Campaign Standard {#using_adobe_campaign_standard}

Si tiene Adobe Campaign Standard, hay una acción integrada disponible para permitir la conexión a Adobe Campaign Standard. Puede enviar correos electrónicos, notificaciones push y SMS mediante las funciones de mensajería transaccional de Adobe Campaign Standard.

El mensaje transaccional de Campaign Standard y su evento asociado deben publicarse para poder utilizarse en Journey Optimizer. Si el evento se publica pero el mensaje no, no será visible en la interfaz de Journey Optimizer. Si el mensaje se publica pero su evento asociado no, estará visible en la interfaz de Journey Optimizer, pero no se podrá utilizar.

## Mecanismos de protección y limitaciones {#important-notes}

* Se define automáticamente una regla de límite de 4000 llamadas por cada 5 minutos para las acciones de Adobe Campaign Standard. Obtenga más información sobre los SLA de mensajería transaccional en [Descripción del producto de Adobe Campaign Standard](https://helpx.adobe.com/es/legal/product-descriptions/campaign-standard.html){target="_blank"}.

* La integración de Adobe Campaign Standard se configura mediante una acción integrada específica en la lista de acciones. Esto debe configurarse para cada zona protegida.

* No puede utilizar una acción de Campaign Standard con una actividad de calificación de audiencia o de lectura de audiencia.

* Un recorrido no puede usar [acciones de canal integradas](../building-journeys/journey-action.md) y [acciones de Campaign Standard](../building-journeys/using-adobe-campaign-standard.md).

## Configurar la acción {#configure-action}

En Journey Optimizer, debe configurar una acción por mensaje transaccional.

Para configurar una acción de Campaign Standard, siga estos pasos:

1. Seleccione **[!UICONTROL Configuraciones]** en la sección del menú ADMINISTRACIÓN.

1. En la sección **[!UICONTROL Acciones]**, haga clic en **[!UICONTROL Administrar]**. Se muestra la lista de acciones.

1. Seleccione la acción integrada **[!UICONTROL AdobeCampaignStandard]**. El panel de configuración de acción se abre en el lado derecho de la pantalla.

   ![](assets/actioncampaign.png)

1. Copie la URL de instancia de Adobe Campaign Standard y péguela en el campo **[!UICONTROL URL]**.

1. Haga clic en **[!UICONTROL Probar la URL de instancia]** para probar la validez de la instancia.

   >[!NOTE]
   >
   >Esta prueba comprueba lo siguiente:
   >
   >* El host es &quot;.campaign.adobe.com&quot;, &quot;.campaign-sandbox.adobe.com&quot;, &quot;.campaign-demo.adobe.com&quot;, &quot;.ats.adobe.com&quot; o &quot;.adls.adobe.com&quot;
   >
   >* La dirección URL comienza con https
   >
   >* La organización asociada a esta instancia de Adobe Campaign Standard es la misma que la organización de Journey Optimizer

Una vez completada esta configuración, hay tres acciones disponibles en la categoría **[!UICONTROL Acción]** al diseñar un recorrido: **[!UICONTROL Correo electrónico]**, **[!UICONTROL Push]**, **[!UICONTROL SMS]**. [Aprenda a utilizarlos](../building-journeys/using-adobe-campaign-standard.md).

![](assets/journey58.png)

Use un evento **Reactions** para reaccionar ante los datos de seguimiento relacionados con un mensaje de Campaign Standard enviado dentro del mismo recorrido:

* Para las notificaciones push, los recorridos pueden reaccionar a los mensajes en los que se hace clic, los que se envían o los que generan errores.

* En los mensajes SMS, los recorridos pueden reaccionar a los mensajes enviados o fallidos.

* En el caso de los correos electrónicos, los recorridos pueden reaccionar a los mensajes en los que se hizo clic, enviados, abiertos o fallidos. [Más información sobre las reacciones y eventos](../building-journeys/reaction-events.md).

Cuando utilice un sistema de terceros para enviar mensajes, debe agregar y configurar una acción personalizada. [Más información acerca de la configuración de acciones personalizadas](../action/about-custom-action-configuration.md).