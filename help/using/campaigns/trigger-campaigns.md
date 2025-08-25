---
solution: Journey Optimizer
product: journey optimizer
title: Revisión y activación de una campaña
description: Obtenga información sobre cómo revisar y activar campañas en Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campaña, revisión, validación, activación, activación, optimizador
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: 45c95d5682b35c8afb161b75c88942c010b36d1c
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---

# Ejecución de una campaña activada por API {#execute}

Una vez activada la campaña, debe recuperar la solicitud cURL de muestra generada y utilizarla en la API para crear la carga útil y almacenar la campaña en déclencheur.

1. Abra la campaña y copie y pegue la solicitud de carga útil de la sección **[!UICONTROL cURL request]**. Esta carga útil incluye todas las variables de personalización (perfil y contexto) utilizadas en el mensaje. Está disponible una vez que la campaña está activa.

   ![](assets/api-triggered-curl.png)

1. Utilice esta solicitud de cURL en las API para crear la carga útil y almacenar en déclencheur la campaña. Para obtener más información, consulte la [documentación interactiva de la API de ejecución de mensajes](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).


   También hay ejemplos de llamadas API disponibles en [esta página](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

   >[!NOTE]
   >
   >Si ha configurado una fecha específica de inicio o finalización al crear la campaña, esta no se ejecuta fuera de estas fechas y las llamadas a la API fallan.
