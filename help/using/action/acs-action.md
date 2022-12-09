---
solution: Journey Optimizer
product: journey optimizer
title: Integración con Adobe Campaign Standard
description: Obtenga información sobre cómo integrar con Adobe Campaign Standard
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Integración con Adobe Campaign Standard {#using_adobe_campaign_standard}

Puede enviar correos electrónicos, notificaciones push y SMS utilizando las capacidades de mensajería transaccional de Adobe Campaign Standard.

Si tiene Adobe Campaign Standard, hay una acción integrada disponible para permitir la conexión a Adobe Campaign Standard.

El mensaje transaccional de Campaign Standard y su evento asociado deben publicarse para poder utilizarlo en Journey Optimizer. Si el evento se publica pero el mensaje no lo es, no estará visible en la interfaz de Journey Optimizer. Si el mensaje se publica pero su evento asociado no, será visible en la interfaz de Journey Optimizer , pero no se podrá utilizar.

## Notas importantes {#important-notes}

* Una regla de límite de 4000 llamadas por 5 minutos se define automáticamente para las acciones de Adobe Campaign Standard. Esto corresponde a la escala oficial de la mensajería transaccional de Adobe Campaign Standard. Obtenga más información sobre los SLA de mensajería transaccional en [Descripción del producto de Adobe Campaign Standard](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html).

* La integración de Adobe Campaign Standard se configura mediante una acción integrada dedicada en la lista de acciones. Esto debe configurarse para cada simulador de pruebas.

* No puede utilizar una acción de Campaign Standard con una calificación de segmento o una actividad de segmento Leer.

* Un recorrido no puede utilizar tanto las acciones de Mensajes como las de Campaign Standard.

## Configuración de la acción {#configure-action}

Estos son los pasos para configurarlo:

1. Select **[!UICONTROL Configurations]** en la sección del menú ADMINISTRACIÓN . En el  **[!UICONTROL Actions]** , haga clic en **[!UICONTROL Manage]**. Se muestra la lista de acciones.

1. Seleccione el complemento **[!UICONTROL AdobeCampaignStandard]** acción. El panel de configuración de acciones se abre en el lado derecho de la pantalla.

   ![](assets/actioncampaign.png)

1. Copie la dirección URL de la instancia de Adobe Campaign Standard y péguela en el **[!UICONTROL URL]** campo .

1. Haga clic en el **[!UICONTROL Test the instance URL]** para probar la validez de la instancia.

   >[!NOTE]
   >
   >Esta prueba comprueba que:
   >
   >El host es &quot;.campaign.adobe.com&quot;, &quot;.campaign-sandbox.adobe.com&quot;, &quot;.campaign-demo.adobe.com&quot;, &quot;.ats.adobe.com&quot; o &quot;.adls.adobe.com&quot;.
   >
   >La dirección URL empieza por https,
   >
   >El ORG asociado a la instancia de Adobe Campaign Standard es el mismo que el ORG de Journey Optimizer.

Al diseñar el recorrido, habrá tres acciones disponibles en la variable **[!UICONTROL Action]** categoría: **[!UICONTROL Email]**, **[!UICONTROL Push]**, **[!UICONTROL SMS]** (consulte [Uso de acciones de Adobe Campaign](../building-journeys/using-adobe-campaign-standard.md)).

![](assets/journey58.png)

Puede usar un **Reacciones** para reaccionar ante los datos de seguimiento relacionados con un mensaje de Campaign Standard enviado durante el mismo recorrido. Para las notificaciones push, puede reaccionar a mensajes en los que se ha hecho clic, enviados o en los que se han producido errores. En el caso de los mensajes SMS, puede reaccionar ante los mensajes enviados o fallidos. En el caso de los correos electrónicos, puede reaccionar ante los mensajes en los que se ha hecho clic, se han enviado, se han abierto o no se han podido realizar. Consulte [Eventos de reacción](../building-journeys/reaction-events.md).

Si utiliza un sistema de terceros para enviar mensajes, debe agregar y configurar una acción personalizada. Consulte [Acerca de la configuración de acciones personalizadas](../action/about-custom-action-configuration.md).
