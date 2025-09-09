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
source-git-commit: 1d3638499a9e8261a5f1b09744b82642198a5d5d
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 3%

---


# Ejecución de una campaña activada por API {#execute}

Una vez activada la campaña, debe recuperar la solicitud cURL de muestra generada y utilizarla en la API para crear la carga útil y almacenar la campaña en déclencheur.

## Lectura obligatoria {#must-read}

* **Fechas de inicio y finalización de la campaña**: si ha configurado una fecha específica de inicio o finalización al crear la campaña, esta no se ejecutará fuera de estas fechas y las llamadas a la API fallarán.

* **Tiempo de espera de llamada**: la llamada a la API de REST de ejecución de mensaje interactivo tiene un tiempo de espera de 60 segundos. Sin embargo, hay reintentos internos en caso de tiempos de espera inesperados para garantizar el envío.

## Déclencheur de la campaña {#trigger}

1. Abra la campaña y copie y pegue la solicitud de carga útil de la sección **[!UICONTROL cURL request]**. Esta carga útil incluye todas las variables de personalización (perfil y contexto) utilizadas en el mensaje. Está disponible una vez que la campaña está activa.

   ![](assets/api-triggered-curl.png)

1. Utilice esta solicitud de cURL en las API para crear la carga útil y almacenar en déclencheur la campaña. Para obtener más información, consulte la [documentación interactiva de la API de ejecución de mensajes](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

   También hay ejemplos de llamadas API disponibles en [esta página](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).
