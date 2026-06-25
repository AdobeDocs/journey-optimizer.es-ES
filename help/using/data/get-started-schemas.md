---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los esquemas
description: Información sobre cómo utilizar los esquemas de Adobe Experience Platform en Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: esquemas, plataforma, datos, estructura
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
TQID: https://experienceleague.adobe.com/fWsW9Rvyd8L4nphczzc7GF1rbO7HuYsjqDBBpy3uoGU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371id: d6e5c7fd-c1d6-4137-98cd-138ccde6752fid: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12bid: e0eb8757-182f-49f3-94a4-1587d16f5094id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 79b0c44fffb4297a9a5675200f086c5de544ec88
workflow-type: tm+mt
source-wordcount: 609
ht-degree: 78%

---

# Introducción a los esquemas {#schemas-gs}

>[!BEGINSHADEBOX]

**En esta página:** comprenda cómo los esquemas relacionales y estándar de Adobe Experience Platform definen la estructura de los datos para que pueda modelar perfiles, eventos de comportamiento y entidades relacionales para campañas de personalización y orquestadas en Adobe Journey Optimizer.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] se basa en los **esquemas de Adobe Experience Platform** para describir la estructura de los datos de una manera uniforme y reutilizable. Un esquema proporciona una definición abstracta de un objeto del mundo real (como una persona) y describe qué datos deben incluirse en cada instancia de ese objeto (como nombre, cumpleaños, etc.). Cuando los datos se incorporan en Experience Platform, siempre se estructuran según un **esquema XDM**.

## Esquemas estándar y relacionales

Existen dos tipos de esquemas en Adobe Experience Platform:

* **Esquemas estándar** son esquemas que utilizan clases y grupos de campos para capturar datos de registros o de series temporales.

  Un esquema estándar consta de:

   * Una **clase** (que define el comportamiento de los datos: registro o serie temporal).
   * Uno o más **grupos de campos** (que añaden campos específicos al esquema).

  En Journey Optimizer, los esquemas estándar generalmente se utilizan para representar a **personas individuales y sus atributos**, capturar **interacciones de series de tiempo** como clics, compras o inicios de sesión, y potenciar el **Perfil del cliente en tiempo real** para la segmentación y personalización.

  ➡️ [Descubra cómo crear y configurar un esquema estándar en este vídeo](#video-schema) (vídeo)

* Los **esquemas relacionales** son esquemas planos no jerárquicos que no utilizan clases ni grupos de campos. Se usan para capturar datos de registros para entidades relacionales y se usan principalmente en [!DNL Journey Optimizer] **campañas orquestadas**.

  Algunos ejemplos de entidades relacionales son:
   * Reservas, contratos o suscripciones
   * Productos o catálogos
   * Tiendas, ubicaciones o socios

  Con los esquemas relacionales, puede enviar un mensaje por entidad (por ejemplo, por reserva o por suscripción), crear segmentos basados en atributos de entidad (por ejemplo, categoría de producto, ubicación de tienda) y mejorar la capacidad de direccionamiento llegando a todos los contactos vinculados a una entidad.

  Cómo funcionan los esquemas relacionales:

   1. **Crear esquemas manualmente o importar mediante DDL**
   1. **Vincular esquemas** para definir las relaciones entre entidades y personas (por ejemplo, transacciones de fidelidad vinculadas a miembros, recompensas vinculadas a marcas).
   1. **Introducir datos** en su conjunto de datos desde fuentes compatibles.

  ➡️ [Aprenda a administrar los esquemas y conjuntos de datos relacionales](../orchestrated/gs-schemas.md)
➡️ [Introducción a las campañas orquestadas](../orchestrated/gs-schemas.md)

>[!IMPORTANT]
>
>La activación de un esquema para el Perfil del cliente en tiempo real es una decisión permanente: una vez activado, el esquema no se puede desactivar ni eliminar. Los conjuntos de datos creados en ese esquema se pueden deshabilitar o eliminar por separado, pero al hacerlo se eliminan los registros de perfil asociados y pueden afectar a los flujos de trabajo de segmentación y activación. Antes de habilitar, finalice la configuración de identidad y la selección de grupos de campos. Para obtener instrucciones detalladas, consulte [Planificación de habilitación de perfiles](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"} y [Administración de esquemas habilitados para perfiles](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"} en la documentación de Adobe Experience Platform.

## Vídeo tutorial{#video-schema}

Obtenga información sobre cómo crear un esquema estándar, añadir grupos de campos, crear y configurar grupos de campos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/334461?quality=12)

>[!MORELIKETHIS]
>
>* [Introducción a la gestión de datos en Journey Optimizer](gs-data.md)
>* [Creación de un esquema y un conjunto de datos, e introducción de datos para añadir perfiles de prueba en Journey Optimizer](../audience/creating-test-profiles.md)
>* [Información general sobre el sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}
>* [Prácticas recomendadas para el modelado de datos](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=es){target="_blank"}
>* [Planificación de habilitación de perfil](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"}
>* [Administrar esquemas habilitados para perfiles](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"}
>* [Creación de un esquema con la API del registro de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=es){target="_blank"}
>* [Definición de una relación entre dos esquemas con el editor de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=es){target="_blank"}
