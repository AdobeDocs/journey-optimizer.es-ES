---
title: Prueba de representación de correo electrónico
description: Obtenga información sobre cómo probar el procesamiento de correo electrónico y comprenda las limitaciones conocidas de procesamiento en los clientes y entornos de correo electrónico.
feature: Preview
role: User
level: Beginner
exl-id: fe077a8b-9788-4723-a1e7-32816a879af9
feature_v2: []
subfeature_v2:
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
source-git-commit: ca053767a216de5f43415c94eb7dd24cffe9dff7
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 1%

---

# Prueba de representación de correo electrónico {#email-rendering}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a conectar su cuenta de Litmus a Adobe Journey Optimizer para probar el procesamiento de correo electrónico en clientes de correo electrónico populares, y comprenda las limitaciones de procesamiento conocidas, incluidos los entornos de explorador web móvil.

>[!ENDSHADEBOX]

Puede aprovechar su cuenta de **Litmus** en [!DNL Journey Optimizer] para obtener una vista previa instantánea de su **procesamiento de correo electrónico** en clientes de correo electrónico populares. A continuación, puede asegurarse de que el contenido del correo electrónico tenga buen aspecto y funcione correctamente en cada bandeja de entrada.

Para comprobar el procesamiento del correo electrónico, siga estos pasos:

1. En la pantalla Editar contenido del mensaje o en el Designer de correo electrónico, haga clic en **[!UICONTROL Simular contenido]** y, a continuación, seleccione **[!UICONTROL Simular contenido (perfiles de AEP)]** en el menú desplegable.

1. Seleccione el botón **[!UICONTROL Procesar correo electrónico]**.

   ![](../email/assets/email-rendering-button.png)

1. Haga clic en **Conectar su cuenta de Litmus** en la sección superior derecha.

   ![](../email/assets/email-rendering-litmus.png)

1. Introduzca sus credenciales de e inicie sesión.

   ![](../email/assets/email-rendering-credentials.png)

1. Haga clic en el botón **Ejecutar prueba** para generar vistas previas de correo electrónico.

1. Compruebe el contenido de su correo electrónico en clientes populares de escritorio, móviles y web.

   ![](../email/assets/email-rendering-previews.png)

>[!CAUTION]
>
>Al conectar su cuenta de **Litmus** con [!DNL Journey Optimizer], acepta que los mensajes de prueba se envíen a Litmus: una vez enviados, Adobe ya no administra estos mensajes de correo electrónico. Como consecuencia, la política de correo electrónico de retención de datos de Litmus se aplica a estos correos electrónicos, incluidos los datos de personalización que pueden incluirse en estos mensajes de prueba.

## Limitaciones del explorador web móvil {#rendering-limitations}

El procesamiento del correo electrónico puede diferir cuando los destinatarios abren Gmail o Outlook **a través de un explorador web móvil** (por ejemplo, Chrome en un teléfono), en lugar de usar una aplicación móvil nativa o un cliente de escritorio. Se trata de una limitación conocida de los entornos de correo web móviles y no es específica de Journey Optimizer.

Esta diferencia de procesamiento se debe al comportamiento de los clientes de webmail dentro de un navegador móvil. El explorador procesa primero la interfaz de usuario completa del correo web de escritorio, colocando el correo electrónico a dos capas de profundidad, fuera del alcance de cualquier CSS o consulta de medios adaptable. Gmail Web también elimina los bloques de CSS `<style>` y ajusta el contenido del correo electrónico en su propio `<div>`, lo que puede anular los estilos y crear conflictos de alineación.

Los síntomas habituales incluyen el desplazamiento de la alineación del texto (el texto alineado a la izquierda aparece centrado), líneas de separación blancas adicionales entre secciones de contenido y un diseño general que difiere del diseño de la plantilla.

Estos problemas solo se producen en Gmail Web y Outlook Web cuando se accede a ellas a través de un explorador móvil. Las aplicaciones móviles nativas de Outlook y Gmail, así como todos los clientes de escritorio, no se ven afectados.

>[!TIP]
>
>Para minimizar el impacto:
>
>* Utilice diseños sencillos basados en tablas con CSS totalmente alineado.
>
>* Evite depender de consultas de medios o bloques de `<style>` para propiedades de diseño críticas, como la alineación del texto.
