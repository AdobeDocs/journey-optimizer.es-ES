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
TQID: https://experienceleague.adobe.com/2XVXr3MjYnD-7o0C2ARXQ8j3sJOFfJfvjfCEZdkV50I
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 346
ht-degree: 21%

---

# Introducción a los fragmentos {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Defina sus propios fragmentos"
>abstract="Cree y administre fragmentos independientes para que el contenido se pueda reutilizar en varios recorridos y campañas."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="Creación de fragmentos"

Un fragmento es un componente reutilizable al que se puede hacer referencia en uno o más correos electrónicos de [!DNL Journey Optimizer] campañas y recorridos. Esta funcionalidad le permite generar varios bloques de contenido personalizados que los usuarios de marketing pueden utilizar para combinar rápidamente el contenido del correo electrónico en un proceso de diseño mejorado.

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [Aprenda a administrar, crear y usar fragmentos en estos vídeos](#video-fragments)

Para aprovechar al máximo los fragmentos:

* **Crear sus propios fragmentos**: cree fragmentos visuales o de expresión, ya sea desde cero o guardando el contenido como fragmento. [Aprenda a crear un fragmento](create-fragments.md). Además, puede aprovechar Journey Optimizer **API de REST de contenido** para administrar fragmentos de contenido. Para obtener más información, consulte la [documentación de las API de Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"}.
* **Reutilice sus fragmentos:** Úselos tantas veces como sea necesario en su contenido. Ver [Agregar fragmentos visuales](../email/use-visual-fragments.md) y [Aprovechar fragmentos de expresiones](../personalization/use-expression-fragments.md)

## Antes de empezar {#fragment-prerequisites}

Para crear, editar, archivar y publicar fragmentos, necesita los permisos **[!DNL Manage library items]** y **[Publicar fragmento]** incluidos en el perfil de producto **[!DNL Content Library Manager]**. [Más información](../administration/ootb-product-profiles.md#content-library-manager)

En esta versión, se aplican las siguientes limitaciones:

* **Los fragmentos visuales** solo están disponibles para el canal de correo electrónico.
* **Los fragmentos de expresiones** no están disponibles para el canal en la aplicación.

Hay más protecciones aplicables a los fragmentos disponibles en [esta sección](../start/guardrails.md#fragments-guardrails).

## Fragmentos visuales y de expresión {#visual-expression}

Hay dos tipos de fragmentos disponibles:

* **Los fragmentos visuales** son bloques visuales predefinidos que se pueden reutilizar en varios envíos de correo electrónico con [Email Designer](../email/get-started-email-design.md) o en [plantillas de contenido](../email/use-email-templates.md).
* **Los fragmentos de expresión** son expresiones predefinidas disponibles en una entrada dedicada en el [editor de personalización](../personalization/personalization-build-expressions.md).

Se puede acceder a todos los fragmentos creados desde el menú de la izquierda **[!UICONTROL Administración de contenido]** > **[!UICONTROL Fragmentos]**. [Aprenda a administrar fragmentos](../content-management/manage-fragments.md)

![](assets/fragment-list.png)

## Vídeo práctico {#video-fragments}

Aprenda a administrar, crear y usar **fragmentos visuales** en [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

Obtenga información sobre cómo administrar, crear y usar **fragmentos de expresiones** en [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
