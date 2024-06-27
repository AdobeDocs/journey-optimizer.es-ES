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
source-git-commit: c42fc1069e11b8e34b7477fc26ed8a6b4ef95ac7
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 11%

---

# Introducción a los fragmentos {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Defina sus propios fragmentos"
>abstract="Cree y administre fragmentos independientes para que el contenido se pueda reutilizar en varios recorridos y campañas."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="Creación de fragmentos"

Un fragmento es un componente reutilizable al que se puede hacer referencia en uno o varios correos electrónicos [!DNL Journey Optimizer] campañas y recorridos. Esta funcionalidad permite crear previamente varios bloques de contenido personalizados que los usuarios de marketing pueden utilizar para ensamblar rápidamente el contenido del correo electrónico en un proceso de diseño mejorado.

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [Aprenda a administrar, crear y utilizar fragmentos en estos vídeos](#video-fragments)

Para aprovechar al máximo los fragmentos:

* **Crear sus propios fragmentos**: cree fragmentos visuales o de expresión, ya sea desde cero o guardando el contenido como fragmento. [Aprenda a crear un fragmento](#create-fragments). Además, puede aprovechar Journey Optimizer **API de REST de contenido** para administrar fragmentos de contenido. Para obtener más información, consulte [Documentación de API de Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.
* **Reutilizar los fragmentos:** Utilícelos tantas veces como sea necesario en el contenido. Consulte [Añadir fragmentos visuales](../email/use-visual-fragments.md) y [Aprovechamiento de fragmentos de expresiones](../personalization/use-expression-fragments.md)

## Antes de empezar {#fragment-prerequisites}

Para crear, editar, archivar y publicar fragmentos, necesita el **[!DNL Manage library items]** y **[Fragmento de Publish]** permisos incluidos en la **[!DNL Content Library Manager]** perfil del producto. [Más información](../administration/ootb-product-profiles.md#content-library-manager)

En esta versión, se aplican las siguientes limitaciones:

* **Fragmentos visuales** solo están disponibles para el canal de correo electrónico.
* **Fragmentos de expresión** no están disponibles para el canal en la aplicación.

## Fragmentos visuales y de expresión {#visual-expression}

Hay dos tipos de fragmentos disponibles:

* **Fragmentos visuales** son bloques visuales predefinidos que se pueden reutilizar en varios envíos de correo electrónico con la variable [Correo electrónico Designer](../email/get-started-email-design.md), o en [plantillas de contenido](../email/use-email-templates.md).
* **Fragmentos de expresión** son expresiones predefinidas que están disponibles en una entrada dedicada en la [editor de personalización](../personalization/personalization-build-expressions.md).

Todos los fragmentos creados son accesibles desde el **[!UICONTROL Gestión de contenido]** > **[!UICONTROL Fragmentos]**  menú izquierdo. [Obtenga información sobre cómo administrar fragmentos](../content-management/manage-fragments.md)

![](assets/fragment-list.png)

## Vídeo explicativo {#video-fragments}

Obtenga información sobre cómo administrar, crear y utilizar **fragmentos visuales** in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

Obtenga información sobre cómo administrar, crear y utilizar **fragmentos de expresión** in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
