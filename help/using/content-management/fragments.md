---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los fragmentos
description: Aprenda a trabajar con fragmentos de contenido para reutilizar contenido en campañas y recorridos de Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: e7ff784d51da48c1970841e416c655c02cfafb7c
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 2%

---

# Introducción a los fragmentos {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Definir sus propios fragmentos"
>abstract="Cree y administre fragmentos independientes para que el contenido se pueda reutilizar en varios recorridos y campañas."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="Creación de fragmentos"

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Campañas de actualización de fragmentos"
>abstract="Campañas de actualización de fragmentos"

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Recorridos de actualización de fragmentos"
>abstract="Recorridos de actualización de fragmentos"

Un fragmento es un componente reutilizable al que se puede hacer referencia en uno o varios correos electrónicos [!DNL Journey Optimizer] campañas y recorridos. Esta funcionalidad permite crear previamente varios bloques de contenido personalizados que los usuarios de marketing pueden utilizar para ensamblar rápidamente el contenido del correo electrónico en un proceso de diseño mejorado.

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [Aprenda a administrar, crear y utilizar fragmentos en estos vídeos](#video-fragments)

Para aprovechar al máximo los fragmentos:

* **Crear sus propios fragmentos**: cree fragmentos visuales o de expresión, ya sea desde cero o guardando el contenido como fragmento. [Aprenda a crear un fragmento](#create-fragments). Además, puede aprovechar Journey Optimizer **API de REST de contenido** para administrar fragmentos de contenido. Para obtener más información, consulte [Documentación de API de Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.
* **Reutilizar los fragmentos:** Utilícelos tantas veces como sea necesario en el contenido. Consulte [Añadir fragmentos visuales](../email/use-visual-fragments.md) y [Aprovechamiento de fragmentos de expresiones](../personalization/use-expression-fragments.md)

## Antes de empezar {#fragment-prerequisites}

>[!NOTE]
>
>Para crear, editar y archivar fragmentos, debe tener el **[!DNL Manage library items]** permiso incluido en el **[!DNL Content Library Manager]** perfil del producto. [Más información](../administration/ootb-product-profiles.md#content-library-manager)

En esta versión, se aplican las siguientes limitaciones:

* **Fragmentos visuales** solo están disponibles para el canal de correo electrónico.
* **Fragmentos de expresión** no están disponibles para el canal en la aplicación.

## Fragmentos visuales y de expresión {#visual-expression}

Hay dos tipos de fragmentos disponibles:

* **Fragmentos visuales** son bloques visuales predefinidos que se pueden reutilizar en varios envíos de correo electrónico con la variable [Diseñador de correo electrónico](../email/get-started-email-design.md), o en [plantillas de contenido](../email/use-email-templates.md).
* **Fragmentos de expresión** son expresiones predefinidas que están disponibles en una entrada dedicada en la [editor de personalización](../personalization/personalization-build-expressions.md).


Se puede acceder a todos los fragmentos desde **[!UICONTROL Gestión de contenido]** > **[!UICONTROL Fragmentos]**  menú izquierdo.

![](assets/fragment-list.png)

## Vídeo explicativo {#video-fragments}

Aprenda a administrar, crear y utilizar fragmentos visuales en [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

Obtenga información sobre cómo administrar, crear y utilizar fragmentos de expresiones en [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
