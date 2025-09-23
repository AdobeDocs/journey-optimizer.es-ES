---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los esquemas
description: Información sobre cómo utilizar los esquemas de Adobe Experience Platform en Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: esquemas, plataforma, datos, estructura
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
source-git-commit: c584ce48029bd298b503a342a1e663eeeedbba42
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 81%

---

# Introducción a los esquemas {#schemas-gs}

[!DNL Adobe Journey Optimizer] se basa en los **esquemas de Adobe Experience Platform** para describir la estructura de los datos de una manera uniforme y reutilizable. Un esquema proporciona una definición abstracta de un objeto del mundo real (como una persona) y describe qué datos deben incluirse en cada instancia de ese objeto (como nombre, cumpleaños, etc.). Cuando los datos se incorporan en Experience Platform, siempre se estructuran según un **esquema XDM**.

## Esquemas basados en modelos y estándares

Existen dos tipos de esquemas en Adobe Experience Platform:

* **Esquemas estándar** son esquemas que utilizan clases y grupos de campos para capturar datos de registros o de series temporales.

  Un esquema estándar consta de:

   * Una **clase** (que define el comportamiento de los datos: registro o serie temporal).
   * Uno o más **grupos de campos** (que añaden campos específicos al esquema).

  En Journey Optimizer, los esquemas estándar generalmente se utilizan para representar a **personas individuales y sus atributos**, capturar **interacciones de series de tiempo** como clics, compras o inicios de sesión, y potenciar el **Perfil del cliente en tiempo real** para la segmentación y personalización.

  ➡️ [Descubra cómo crear y configurar un esquema estándar en este vídeo](#video-schema) (vídeo)

* **Los esquemas basados en modelos** son esquemas planos no jerárquicos que no utilizan clases ni grupos de campos. Se usan para capturar datos de registros para entidades relacionales y se usan principalmente en [!DNL Journey Optimizer] **campañas orquestadas**.

  Algunos ejemplos de entidades relacionales son:
   * Reservas, contratos o suscripciones
   * Productos o catálogos
   * Tiendas, ubicaciones o socios

  Con los esquemas basados en modelos, puede enviar un mensaje por entidad (por ejemplo, por reserva o por suscripción), crear segmentos basados en atributos de entidad (por ejemplo, categoría de producto, ubicación de tienda) y mejorar la capacidad de direccionamiento llegando a todos los contactos vinculados a una entidad.

  Cómo funcionan los esquemas basados en modelos:

   1. **Crear esquemas manualmente o importar mediante DDL**
   1. **Vincular esquemas** para definir las relaciones entre entidades y personas (por ejemplo, transacciones de fidelidad vinculadas a miembros, recompensas vinculadas a marcas).
   1. **Introducir datos** en su conjunto de datos desde fuentes compatibles.

  ➡️ [Aprenda a administrar esquemas y conjuntos de datos basados en modelos](../orchestrated/gs-schemas.md)
➡️ [Introducción a campañas orquestadas](../orchestrated/gs-schemas.md)

## Vídeo práctico{#video-schema}

Obtenga información sobre cómo crear un esquema estándar, añadir grupos de campos, crear y configurar grupos de campos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/3416869?quality=12&captions=spa)

>[!MORELIKETHIS]
>
>* [Creación de un esquema y un conjunto de datos, e introducción de datos para añadir perfiles de prueba en Journey Optimizer](../audience/creating-test-profiles.md)
>* [Información general sobre el sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}
>* [Prácticas recomendadas para el modelado de datos](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=es){target="_blank"}
>* [Creación de un esquema con la API del registro de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=es){target="_blank"}
>* [Definición de una relación entre dos esquemas con el editor de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=es){target="_blank"}
