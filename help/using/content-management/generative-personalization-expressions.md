---
solution: Journey Optimizer
product: journey optimizer
title: Asistente de IA para expresiones Personalization
description: Aprenda a utilizar el asistente de IA en Journey Optimizer para generar expresiones de personalización a partir del lenguaje natural, desde el Editor de Personalization o en línea en el Designer de correo electrónico.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Intermediate
mini-toc-levels: 1
source-git-commit: 8a905fd7e51c2dac60f4edccb9e9dd790a0dd424
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 1%

---

# Asistente de IA para expresiones de personalización{#generative-personalization-expressions}

>[!IMPORTANT]
>
>Antes de empezar a usar esta capacidad, lea las [Mecanismos de protecciones y limitaciones](gs-generative.md#generative-guardrails) relacionadas.
></br>
>
>Debe aceptar un [acuerdo de usuario](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) para poder usar el Asistente de IA en Journey Optimizer. Para obtener más información, contacte con su representante de Adobe.

## Información general {#where-available}

[!UICONTROL Ayudante de IA] le ayuda a generar una nueva personalización a partir de un lenguaje sencillo, a explicar lo que hacen las expresiones existentes y a solucionar problemas en el código seleccionado, de modo que dedique menos tiempo a la sintaxis y a la detección manual de campos. También puede iterar en una selección o solicitar otros cambios en la conversación. Está disponible desde dos puntos de entrada:

* **[!UICONTROL Editor de Personalization]**: siempre que el editor esté disponible (línea de asunto, cuerpo y otros campos que lo abran). Para saber dónde y cómo abrir el editor, consulte [Agregar personalización](../personalization/personalization-build-expressions.md#where).
* **Editar texto en línea de Designer de correo electrónico**: directamente desde la ventana emergente de edición en línea al editar un componente de texto. Ver [Generar desde el Designer de correo electrónico](#generate-email-designer).

Para obtener información sobre la configuración y los idiomas del Asistente de IA, consulte [Introducción al Asistente de IA](gs-generative.md). Para ver los conceptos de personalización, consulte [Introducción a la personalización](../personalization/personalize.md). Para obtener ideas rápidas, consulte [Prácticas recomendadas de mensajes de IA](ai-assistant-prompting-guide.md).

Según el contexto de su campaña o recorrido, el asistente puede trabajar con datos y construir el [!UICONTROL Editor de Personalization] que ya expone, por ejemplo atributos de perfil, pertenencia a segmentos, funciones de ayuda y fuentes de personalización relacionadas.

>[!NOTE]
>
>El asistente mantiene el contexto alejado de los mensajes mientras [!UICONTROL AI Assistant] permanece abierto en esa sesión. Al cerrar el asistente o el editor, se borra la conversación; la próxima vez que abra el asistente, iniciará una nueva conversación.

## Generar expresiones de personalización {#generate}

Estos pasos cubren la generación de expresiones de personalización desde cero. Para trabajar con código que ya se encuentra en el editor, consulte [Editar, corregir o explicar el código existente](#edit-existing).

1. En el mensaje o el contenido, abra **[!UICONTROL Personalization Editor]**.

1. Coloque el cursor en el editor donde desee insertar el código de personalización generado y, a continuación, haga clic en el botón **[!UICONTROL Ayudante de IA]**.

   ![](assets/ai-perso-access.png)

1. En el campo de texto, describa la expresión personalizada que desee en lenguaje sin formato; por ejemplo, qué atributos de perfil, segmentos o lógica necesita y, a continuación, haga clic en **[!UICONTROL Generar]**.

   También puede usar indicadores listos para usar de la sección **[!UICONTROL Indicadores rápidos]**, como saludo personalizado, generación de código de promoción y más.

   ![](assets/ai-perso-generate.png)

   >[!NOTE]
   >
   >Cualquier pregunta o petición de datos no relacionada devuelve un error fuera de ámbito. Ajuste el mensaje y haga una pregunta relevante acerca de la personalización que necesita.

1. Puede seguir hablando con el asistente en una conversación de varias vueltas: mantiene el contexto alejado de los mensajes para que pueda refinar la misma expresión paso a paso. Para volver a empezar, haga clic en el botón **[!UICONTROL Nueva sesión]**.

   ![](assets/ai-perso-question.png)

1. Después de generar una expresión, haga clic en **[!UICONTROL Mostrar vistas previas de perfiles de muestra]** para ver cómo se evalúa la expresión con datos de muestra y para ver la carga útil asociada como JSON. Para esta comprobación, el asistente genera un conjunto limitado de perfiles de muestra sintéticos; no se guardan ni almacenan en su organización.

   Si necesita perfiles de muestra personalizados o adicionales, describa lo que necesita en la conversación con el asistente e incluya la palabra clave **preview** en la solicitud para que pueda generar los perfiles de vista previa adecuados para su comprobación.

   ![](assets/ai-perso-preview-button.png)

   +++Previsualizar ejemplo

   ![](assets/ai-perso-preview.png)

   >[!NOTE]
   >
   >Se ofrecen previsualizaciones adicionales para la comprobación puntual. El asistente está configurado para generar aproximadamente uno o cinco perfiles. Si se solicita un número muy grande, la solicitud puede fallar.

   +++

   >[!NOTE]
   >
   >Este control sirve para comprobar rápidamente el código personalizado en el editor, no para obtener una vista previa completa del mensaje del contenido. Para validar completamente la experiencia, utilice el flujo de simulación habitual. [Obtenga información sobre cómo obtener una vista previa y probar el contenido](../content-management/preview-test.md)

1. Para implementar el resultado en su expresión personalizada, haga clic en **[!UICONTROL Aplicar]**. La salida del asistente se inserta en la ubicación del cursor en el editor de personalización. Para reemplazar el código que ya está allí, selecciónelo primero en el editor y, a continuación, usa **[!UICONTROL Editar con el Asistente para IA]** (consulta [Editar, corregir o explicar el código existente](#edit-existing)).

   También puede copiar el resultado y pegarlo donde lo necesite utilizando el icono ![Copiar icono](../orchestrated/assets/do-not-localize/activity-copy.svg).

## Editar, corregir o explicar el código existente {#edit-existing}

Puede seleccionar una expresión de personalización existente y utilizar el Asistente de IA para solucionar problemas de personalización, explicar lo que hace el código o solicitar otros cambios.

1. Seleccione código de personalización existente en el editor.

1. Haga clic con el botón derecho en la selección y elija **[!UICONTROL Editar con el asistente de IA]** para que el asistente use su selección como contexto.

   ![](assets/ai-perso-right-click.png)

1. Se abre **[!UICONTROL Asistente de IA]**. En **[!UICONTROL Comandos rápidos]**, haga clic en **[!UICONTROL Explicar]** o **[!UICONTROL Corregir]**, o use el campo de texto para solicitar otros cambios e iniciar una conversación.

   ![](assets/ai-perso-edit.png)

1. Cuando use **[!UICONTROL Corrección]**, haga clic en **[!UICONTROL Mostrar detalles de la corrección]** en la discusión para mostrar una explicación de la corrección y una línea por línea antes y después de la vista previa.

   ![](assets/ai-perso-fix.png)

1. Al igual que cuando genera una expresión personalizada, haga clic en **[!UICONTROL Aplicar]** para implementar el resultado del asistente. Reemplaza el código seleccionado en el editor de personalización. Por ejemplo, si solicita una explicación del código, al aplicar se agregan comentarios en la expresión que describen lo que hace.

## Generar desde Designer de correo electrónico {#generate-email-designer}

[!UICONTROL El Asistente de IA para expresiones de personalización] también está disponible directamente desde la experiencia de edición en línea en el Designer de correo electrónico, sin abrir el [!UICONTROL Editor de Personalization] completo. La expresión generada se inserta en la posición del cursor en el componente de texto.

1. En Email Designer, seleccione un componente de texto y empiece a editarlo en línea.

1. Abra la ventana emergente de personalización en línea de una de las dos maneras siguientes:

   * Escriba `{{` en la posición en la que desea insertar la expresión (la ventana emergente se abrirá automáticamente).
   * Haga clic en **[!UICONTROL Usar IA para generar]** en la ventana emergente de edición en línea si ya está abierta.

   ![](assets/ai-perso-email-entry.png)

1. En el campo de texto, describa la expresión de personalización que desee en lenguaje sin formato y, a continuación, haga clic en **[!UICONTROL Generar]**.

1. Revise el resultado en la ficha **[!UICONTROL Expresión]** para ver la expresión generada.

   Cambie a la pestaña **[!UICONTROL Preview]** para ver cómo se evalúa la expresión mediante valores de perfil de muestra, de modo que pueda comprobar el resultado antes de insertarlo.

   ![](assets/ai-perso-email-result.png)

1. Haga clic en **[!UICONTROL Insertar]** para aplicar la expresión en la posición del cursor en el componente de texto. Use **[!UICONTROL Regenerar]** para generar una nueva sugerencia o **[!UICONTROL Restablecer]** para empezar de nuevo.

>[!NOTE]
>
>La sesión [!UICONTROL AI Assistant for personalization expression] de la ventana emergente de Designer de correo electrónico en línea es independiente de las sesiones del [!UICONTROL Editor de Personalization]. Al cerrar la ventana emergente, se borra la conversación.
