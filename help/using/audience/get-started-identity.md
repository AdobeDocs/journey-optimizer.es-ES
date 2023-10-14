---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las identidades en Journey Optimizer
description: Obtenga información sobre cómo administrar identidades en Adobe Journey Optimizer
feature: Profiles, Identities
role: User
level: Beginner
exl-id: 90e892e9-33c2-4da5-be1d-496b42572897
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 100%

---

# Introducción a las identidades {#identities-gs}

Una identidad son datos que son exclusivos de una entidad, normalmente de una persona individual. Una identidad como, por ejemplo, un ID de inicio de sesión, un ECID o un ID de lealtad se denomina identidad conocida.

La información de identificación personal (PII), como la dirección de correo electrónico y el número de teléfono, sirve para identificar directamente a un cliente. Como resultado, PII se utiliza para hacer coincidir las múltiples identidades de un cliente en todos los sistemas.

En [!DNL Adobe Journey Optimizer], las **Identidades**[ vinculan los consumidores con dispositivos y canales, y el resultado es un gráfico de identidad](#id-graph). El gráfico de identidad vinculado se utiliza para personalizar las experiencias en función de las interacciones en todos los puntos de contacto empresariales.

![](assets/identities-home.png)

Más información sobre **Servicio de identidad** en [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=es){target="_blank"}.

## Áreas de nombres de identidad {#identity-namespaces}

**** Las áreas de nombres de identidad son un componente del servicio de identidad que sirve de indicadores del contexto al que se relaciona una identidad. Por ejemplo, distinguen un valor de `name@email.com` como dirección de correo electrónico o `443522` como ID de CRM numérico. El trabajo con áreas de nombres de identidad requiere comprender los distintos servicios de Adobe Experience Platform implicados. Antes de empezar a trabajar con áreas de nombres, revise la documentación de los servicios siguientes:

Más información sobre **Áreas de nombres de identidad** en [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=es){target="_blank"}.

## Gráfico de identidad{#id-graph}

El **Gráfico de identidad** es un mapa de las relaciones entre las distintas identidades de un cliente concreto, que proporciona una representación visual de cómo el cliente interactúa con la marca a través de diferentes canales. El servicio de identidad de Adobe Experience Platform administra y actualiza todos los gráficos de identidad de los clientes de forma colectiva casi en tiempo real como respuesta a la actividad de los clientes.

El visor de gráficos de identidad en la interfaz de usuario de [!DNL Adobe Journey Optimizer] le permite visualizar y comprender mejor qué identidades de cliente se vinculan entre sí y de qué manera. El visor le permite arrastrar e interactuar con diferentes partes del gráfico, lo que le permite examinar relaciones de identidad complejas, depurar de forma más eficaz y beneficiarse de una mayor transparencia con la forma en que se utiliza la información.

Más información sobre **Gráfico de identidad** en [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html?lang=es){target="_blank"}.
