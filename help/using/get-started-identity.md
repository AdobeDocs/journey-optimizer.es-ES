---
title: Introducción a las identidades en Journey Optimizer
description: Obtenga información sobre cómo administrar identidades en Adobe Journey Optimizer
feature: Perfiles
role: User
level: Beginner
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 7%

---

# Introducción a las identidades {#identities-gs}

Una identidad es datos que son exclusivos de una entidad, normalmente de una persona individual. Una identidad como, por ejemplo, un ID de inicio de sesión, un ECID o un ID de lealtad se denomina identidad conocida.

La información de identificación personal (PII), como la dirección de correo electrónico y el número de teléfono, sirve para identificar directamente a un cliente. Como resultado, la PII se utiliza para hacer coincidir las múltiples identidades de un cliente en todos los sistemas.

En [!DNL Adobe Journey Optimizer], **Identities** vincula a los consumidores entre dispositivos y canales, el resultado es un [gráfico de identidad](#id-graph). El gráfico de identidad vinculado se utiliza para personalizar las experiencias en función de las interacciones en todos los puntos de contacto empresariales.

![](assets/identities-home.png)

Obtenga más información sobre **Identity Service** en [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html){target=&quot;_blank&quot;}.

## Espacios de nombres de identidad

**** Las áreas de nombres de identidad son un componente de Identity Service de   que sirve de indicadores del contexto al que se relaciona una identidad. Por ejemplo, distinguen un valor de `name@email.com` como dirección de correo electrónico o `443522` como ID de CRM numérico. El trabajo con áreas de nombres de identidad requiere comprender los distintos servicios de Adobe Experience Platform involucrados. Antes de comenzar a trabajar con áreas de nombres, revise la documentación de los siguientes servicios:

Obtenga más información sobre **área de nombres de identidad** en [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html){target=&quot;_blank&quot;}.

## Gráfico de identidad{#id-graph}

El **gráfico de identidad** es un mapa de las relaciones entre las distintas identidades de un cliente concreto, que proporciona una representación visual de cómo el cliente interactúa con la marca a través de diferentes canales. El servicio de identidad de Adobe Experience Platform administra y actualiza todos los gráficos de identidad de los clientes de forma colectiva casi en tiempo real como respuesta a la actividad de los clientes.

El visor de gráficos de identidad en la interfaz de usuario [!DNL Adobe Journey Optimizer] le permite visualizar y comprender mejor qué identidades de cliente se vinculan entre sí y de qué manera. El visor le permite arrastrar e interactuar con diferentes partes del gráfico, lo que le permite examinar relaciones de identidad complejas, depurar de forma más eficaz y beneficiarse de una mayor transparencia con la forma en que se utiliza la información.

Obtenga más información sobre **Identity Graph** en [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html){target=&quot;_blank&quot;}.

