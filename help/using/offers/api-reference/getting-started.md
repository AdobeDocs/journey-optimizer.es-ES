---
title: Introducción
description: Obtenga información sobre cómo empezar a utilizar la API de la biblioteca de ofertas para realizar operaciones clave mediante el motor de decisión.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 4f2bbef98b2e529c2f6a663a3cf7e1ad5493c41a
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 7%

---

# Guía para desarrolladores de API de Administración de decisiones {#decision-management-api-developer-guide}

Esta guía para desarrolladores proporciona pasos para ayudarle a empezar a utilizar [!DNL Offer Library] API. A continuación, la guía proporciona llamadas de API de ejemplo para realizar operaciones clave mediante el motor de toma de decisiones.

➡️ [Obtenga más información sobre los componentes de Administración de decisiones en este vídeo](#video)

## Requisitos previos {#prerequisites}

Esta guía requiere una comprensión práctica de los siguientes componentes de Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}: El marco estandarizado mediante el cual [!DNL Experience Platform] organiza los datos de experiencia del cliente.
   * [Conceptos básicos de composición de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=es){target="_blank"}: Obtenga información acerca de los componentes básicos de los esquemas XDM.
* [Gestión de decisiones](../../../using/offers/get-started/starting-offer-decisioning.md): Explica los conceptos y componentes utilizados para Experience Decisioning en general y para la administración de decisiones en particular. Ilustra las estrategias utilizadas para elegir la mejor opción para presentar durante la experiencia de un cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}: PQL es un lenguaje potente para escribir expresiones en instancias de XDM. El PQL se utiliza para definir reglas de decisión.

## Leer llamadas de API de muestra {#reading-sample-api-calls}

Esta guía proporciona ejemplos de llamadas API para mostrar cómo dar formato a las solicitudes. Estas incluyen rutas, encabezados obligatorios y cargas de solicitud con el formato correcto. También se proporciona el JSON de muestra devuelto en las respuestas de API. Para obtener información sobre las convenciones utilizadas en la documentación de las llamadas de API de ejemplo, consulte la sección sobre [cómo leer llamadas de API de ejemplo](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} en el [!DNL Experience Platform] guía de solución de problemas.

## Recopilar valores para los encabezados obligatorios {#gather-values-for-required-headers}

Para realizar llamadas a [!DNL Adobe Experience Platform] API, primero debe completar el [tutorial de autenticación](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=es){target="_blank"}. Al completar el tutorial de autenticación, se proporcionan los valores para cada uno de los encabezados necesarios en todas las [!DNL Experience Platform] Llamadas de API, como se muestra a continuación:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

Todas las solicitudes que contienen una carga útil (POST, PUT, PATCH) requieren un encabezado adicional:

* `Content-Type: application/json`

## Pasos siguientes {#next-steps}

Este documento abarcaba los conocimientos previos necesarios para realizar llamadas a la [!DNL Offer Library] API. Ahora puede continuar con las llamadas de ejemplo proporcionadas en esta guía para desarrolladores y seguir junto con sus instrucciones.

## Vídeo explicativo {#video}

El siguiente vídeo tiene como objetivo ayudarle a comprender los componentes de Administración de decisiones.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

