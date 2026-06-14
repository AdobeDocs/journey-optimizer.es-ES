---
solution: Journey Optimizer
product: journey optimizer
title: Añadir metadatos al contenido del correo electrónico
description: Aprenda a mejorar la legibilidad y accesibilidad del contenido del correo electrónico con los metadatos en Journey Optimizer
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: preencabezado, editor, resumen, correo electrónico
exl-id: 7ed52b2e-eabf-414f-b169-4b004733dea9
TQID: https://experienceleague.adobe.com/apen1-tlKZ3bnGV9X1RacDk1LXt7sJBQNfTQiaFAyYA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 364
ht-degree: 24%

---

# Añadir metadatos al contenido del correo electrónico {#email-metadata}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a establecer metadatos de correo electrónico en el Designer de correo electrónico, incluido el preencabezado, el título y el idioma del documento, para mejorar la legibilidad y accesibilidad del contenido del correo electrónico.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="Definir un preencabezado"
>abstract="Un preencabezado es un breve texto de resumen que sigue a la línea del asunto cuando se visualiza un correo electrónico desde su cliente de correo electrónico. En muchos casos, proporciona un breve resumen del correo electrónico y suele contener una frase."

Al diseñar los correos electrónicos, para mejorar la legibilidad y la accesibilidad, puede definir metaatributos adicionales para el contenido. El [!DNL Journey Optimizer] [Designer de correo electrónico](get-started-email-design.md) le permite especificar los siguientes elementos:

![](assets/email_body_settings_ex.png)

* **[!UICONTROL Encabezado previo]**: Un encabezado previo es un breve texto de resumen que sigue a la línea de asunto cuando ve un correo electrónico de su cliente de correo electrónico. En muchos casos, proporciona un breve resumen del correo electrónico y suele contener una frase.

  >[!NOTE]
  >
  >Los preencabezados no son compatibles con todos los clientes de correo electrónico. Cuando no se admite, el preencabezado no se muestra.

* **[!UICONTROL Título del documento]**: este campo, que corresponde al elemento `<title>`, proporciona información descriptiva sobre el contenido del correo electrónico, que normalmente se muestra como información de objeto al pasar el ratón por encima. Puede ayudar a los usuarios con discapacidades al proporcionar un contexto adicional y puede contribuir a una mejor comprensión del contenido por parte de los motores de búsqueda.

* **[!UICONTROL Idioma del documento]**: para garantizar la accesibilidad, puede especificar el idioma que los lectores de pantalla utilizarán para convertir texto e imágenes en voz o braille, para personas con deficiencias visuales o con discapacidades de aprendizaje. Esta configuración corresponde al atributo `lang` en el elemento `<html>`.

Para establecer esta configuración, siga los pasos a continuación.

1. En [Email Designer](content-from-scratch.md), agrega al menos un **[!UICONTROL componente de estructura]** para comenzar a diseñar tu correo electrónico.

1. Haga clic en **[!UICONTROL Cuerpo]**, ya sea en el **[!UICONTROL árbol de navegación]** a la izquierda o en la parte superior del panel derecho.

   ![](assets/email_body.png)

1. En la ficha **[!UICONTROL Configuración]**, escriba texto dentro de los campos **[!UICONTROL Encabezado previo]**, **[!UICONTROL Título del documento]** o **[!UICONTROL Idioma del documento]**.

1. También puede hacer clic en el icono de personalización junto a cada campo para personalizar el contenido de atributos de perfil, audiencias, atributos contextuales, etc. [Más información sobre personalización](../personalization/personalization-build-expressions.md)

   ![](assets/email_body_settings.png)

1. Haz clic en **[!UICONTROL Guardar]** para confirmar los cambios.