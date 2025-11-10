---
title: Introducción
description: Obtenga información sobre cómo empezar a utilizar la API de la biblioteca de ofertas para realizar operaciones clave con el motor de toma de decisiones.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 100%

---

# Guía para desarrolladores de la API de gestión de decisiones {#decision-management-api-developer-guide}

>[!CONTEXTUALHELP]
>id="od_api_support"
>title="Nuevas API de gestión de decisiones"
>abstract="Ya están disponibles las nuevas API para la creación y administración de objetos de gestión de decisiones. Las API heredadas serán compatibles hasta el 27/03/2024."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_api_support"
>title="Nuevas API de gestión de decisiones"
>abstract="Ya están disponibles las nuevas API para la creación y administración de objetos de gestión de decisiones. Las API heredadas serán compatibles hasta el 27/03/2024."

Esta guía para desarrolladores proporciona pasos para ayudarle a utilizar la API de [!DNL Offer Library]. A continuación, la guía proporciona llamadas de API de muestra para realizar operaciones clave mediante el motor de toma de decisiones.

➡️ [Obtenga más información sobre los componentes de Gestión de decisiones en este vídeo](#video)

## Requisitos previos {#prerequisites}

Esta guía requiere una comprensión práctica de los siguientes componentes de Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}: el marco estandarizado mediante el cual [!DNL Experience Platform] organiza los datos de experiencia del cliente.
   * [Conceptos básicos de composición de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=es){target="_blank"}: obtenga información acerca de los componentes básicos de los esquemas XDM.
* [Gestión de decisiones](../../../using/offers/get-started/starting-offer-decisioning.md): explica los conceptos y componentes que se utilizan en Decisioning en general y para la gestión de decisiones en particular. Ilustra las estrategias que se emplean para elegir la mejor opción de presentación durante la experiencia de un cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=es){target="_blank"}: PQL es un lenguaje potente para escribir expresiones en instancias de XDM. PQL se utiliza para definir reglas de decisión.

## Lectura de llamadas de API de muestra {#reading-sample-api-calls}

Esta guía proporciona ejemplos de llamadas de API para mostrar cómo dar formato a las solicitudes. Estas incluyen rutas, encabezados obligatorios y cargas de solicitud con el formato correcto. También se proporciona el JSON de muestra devuelto en las respuestas de la API. Para obtener información sobre las convenciones utilizadas en la documentación de las llamadas de API de muestra, consulte la sección sobre [cómo leer llamadas de API de ejemplo](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=es#how-do-i-format-an-api-request){target="_blank"} en la guía de solución de problemas de [!DNL Experience Platform].

## Recopilación de valores para los encabezados obligatorios {#gather-values-for-required-headers}

Para realizar llamadas a las API de [!DNL Adobe Experience Platform], primero debe completar el [tutorial de autenticación](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=es){target="_blank"}. Al completar el tutorial de autenticación, se proporcionan los valores para cada uno de los encabezados obligatorios en todas las llamadas de API de [!DNL Experience Platform], como se muestra a continuación:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

Todas las solicitudes que contienen una carga útil (POST, PUT, PATCH) requieren un encabezado adicional:

* `Content-Type: application/json`

>[!NOTE]
>
>Las comprobaciones de permisos se aplican según los perfiles de producto asignados. Solo los permisos otorgados en el perfil de producto asociado determinan a qué recursos se puede acceder o administrar a través de la API.

## Pasos siguientes {#next-steps}

Este documento cubría los conocimientos previos necesarios para realizar llamadas a la API de [!DNL Offer Library]. Ahora puede continuar con las llamadas de muestra que se proporcionan en esta guía para desarrolladores y seguir junto con sus instrucciones.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = "Mobile_Sheliak"`.
-->

<!-- ## How-to video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!VIDEO](https://video.tv.adobe.com/v/342828?captions=spa&quality=12) -->

