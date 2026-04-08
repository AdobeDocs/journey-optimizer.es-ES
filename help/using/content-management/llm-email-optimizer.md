---
title: Optimizar el texto del correo electrónico para bandejas de entrada AI
description: Refine la capa de texto sin formato del correo electrónico en Journey Optimizer para que los clientes de la bandeja de entrada asistida por IA puedan utilizar sus ofertas y CTA cuando resuman el correo electrónico o extraigan la intención, en el Designer de correo electrónico con Optimizar con IA.
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: 0c2f95ce-28a0-480c-9829-b7e4975b6340
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 1%

---

# Optimizar el texto del correo electrónico para bandejas de entrada AI {#email-text-optimizer}

[!DNL Adobe Journey Optimizer] incluye una función de canal de correo electrónico que le ayuda a estructurar la [versión de texto](../email/text-version-email.md) de sus mensajes para mejorar las experiencias de la bandeja de entrada asistida por IA, como [!DNL Apple Intelligence] y [!DNL Google Gemini] en [!DNL Gmail], de modo que puedan responder preguntas y resumir el correo electrónico en función de su contenido con mayor precisión y con mejores resultados.

>[!NOTE]
>
>Esta capacidad solo cambia el texto sin formato, no la versión de HTML del contenido del correo electrónico.

Con este optimizador de texto de correo electrónico, puede asegurarse de que la versión de texto sin formato del contenido del correo electrónico se mejore para las experiencias de bandeja de entrada asistida por IA, de modo que la información que proporcione a las funciones de IA de estos proveedores de bandeja de entrada de correo electrónico sea exactamente la que desee proporcionar.

## Funcionamiento {#how-it-works}

Las preguntas típicas que los destinatarios pueden hacer en las experiencias de bandeja de entrada asistida por IA son *¿De qué se trata este correo electrónico?* o *¿Qué son estas ofertas?*.

* Las respuestas proporcionadas por estos asistentes de IA pueden ser un breve resumen (por ejemplo, que el mensaje es promocional, menciona el acceso anticipado de VIP y una venta, e incluye vínculos a categorías de productos), pero aun así omiten los objetivos que preocupaban al experto en marketing, porque los asistentes deducen del texto que ven de forma eficaz, no necesariamente de la historia completa que pretendía.

* Además, los asistentes pueden buscar de forma proactiva descuentos o cupones relacionados con la marca y doblarlos en la respuesta, de modo que el usuario ya no esté mirando únicamente lo que su mensaje realmente prometió. Este comportamiento es útil para los usuarios finales, pero diluye el control para los especialistas en marketing que necesitan respuestas para realizar un seguimiento de los términos reales del envío.

Para evitar estos problemas, [!DNL Journey Optimizer] reescribe el texto sin formato para que los cupones, los intervalos de descuento, las llamadas a la acción y otras prioridades aparezcan de antemano en una copia lineal sin cifrar. El objetivo es que la IA de la bandeja de entrada base resúmenes y preguntas y respuestas en las ofertas y acciones definidas, en lugar de apoyarse en una parte de texto predeterminado delgada o en resultados web no relacionados.

>[!IMPORTANT]
>
>Los comportamientos exactos del asistente de IA dependen del proveedor de la bandeja de entrada y de la versión del modelo. Una vez enviado el correo electrónico, las respuestas y los resúmenes proporcionados por clientes de IA externos pueden ser incorrectos, incompletos o mezclados con los resultados de la web.
>
>La funcionalidad Optimizar el texto del correo electrónico para las bandejas de entrada de IA solo mejora el texto sin formato que crea en Journey Optimizer; no garantiza cómo un asistente de terceros interpretará o mostrará el mensaje. Obtenga más información sobre las [limitaciones y riesgos de la IA de la bandeja de entrada de terceros](#inbox-ai-risks).

## Casos de uso recomendados {#use-cases}

<!--
* **Critical details only in images** — Offers, promo codes, or deadlines shown in banners or graphics are invisible in plain text. Use the optimizer (and manual edits) so the same facts appear as text, improving extraction by AI summaries and text-only clients.
-->

* **Texto denso o fragmentado generado automáticamente**: cuando el texto sin formato predeterminado es difícil de analizar, la optimización puede producir una narrativa lineal más clara con ofertas y vínculos explícitos.

* **Control de las preguntas y respuestas de la bandeja de entrada**: cuando espera que los destinatarios pregunten a los asistentes *de qué se trata el correo electrónico* o *cuáles son las ofertas*, una versión de texto sin formato sólida reduce los resúmenes parciales y la dependencia de las respuestas completadas por la web que no están vinculadas a la copia aprobada.

## Optimizar para experiencias de bandeja de entrada de IA {#optimize-with-ai}

>[!IMPORTANT]
>
>Antes de empezar a usar esta capacidad, lea [Riesgos y limitaciones](#inbox-ai-risks) relacionados.
>
>Para tener acceso a esta característica, debe aceptar un acuerdo de usuario que se muestre la primera vez que utilice IA generativa en [!DNL Journey Optimizer]. Para obtener más información, lea las [Directrices de usuario de IA generativa de Adobe Experience Cloud](https://www.adobe.com/es/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

Para optimizar la versión de texto sin formato del correo electrónico para las bandejas de entrada de IA con [!DNL Journey Optimizer], siga los pasos a continuación.

1. Abra su correo electrónico en [Email Designer](../email/content-from-scratch.md) (de una campaña, recorrido o plantilla, según el flujo de trabajo).

1. Seleccione el icono **[!UICONTROL Texto sin formato]** para abrir la versión de texto del correo electrónico. [Más información](../email/text-version-email.md)

   ![Seleccione el icono Texto sin formato para abrir la versión de texto del correo electrónico](assets/text-optimizer-text-icon.png){zoomable="yes"}

1. Se muestra la versión de texto del correo electrónico. Haga clic en el botón **[!UICONTROL Optimizar para la bandeja de entrada de IA]** para generar una versión mejorada de texto sin formato que resalte la información clave para la lectura y el resumen asistidos por IA.

   ![Optimizar para el botón Bandeja de entrada de IA en la vista de versión de texto](assets/text-optimizer-for-ai-button.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >Al hacer clic en el botón **[!UICONTROL Optimizar para la bandeja de entrada de IA]**, la opción **[!UICONTROL Sincronizar con HTML]** se deshabilita automáticamente. [Más información](../email/text-version-email.md#plain-text-custom)

1. Si es la primera vez que usa IA generativa en [!DNL Journey Optimizer], se le pedirá que acepte el contrato de usuario. Para obtener más información, consulte las [Directrices de usuario de IA generativa de Adobe](https://www.adobe.com/es/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

   ![Cuadro de diálogo de acuerdo de usuario de inteligencia artificial generativa en Journey Optimizer](assets/text-optimizer-agreement.png){width=50%}

   Haga clic en **[!UICONTROL Aceptar]** para continuar.

1. Se muestra el texto generado. Revise los cambios, edítelos si es necesario y guarde el correo electrónico como de costumbre.

   ![Texto generado en la vista de versión de texto](assets/text-optimizer-output.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >El optimizador de texto de correo electrónico actualiza solo el cuerpo del texto sin formato. No cambia el diseño, el diseño ni las imágenes de HTML.

1. Puede volver a la versión de HTML de su correo electrónico en cualquier momento haciendo clic en el icono **[!UICONTROL Cambiar a la vista de escritorio]**. Se conservarán los cambios realizados en la versión de texto.

   >[!CAUTION]
   >
   >Si vuelve a habilitar la opción **[!UICONTROL Sincronizar con HTML]**, los cambios se perderán y se reemplazarán con el contenido de texto generado a partir de la versión de HTML.

## Riesgos y limitaciones de la IA de la bandeja de entrada de terceros {#inbox-ai-risks}

La funcionalidad Optimizar el texto del correo electrónico para las bandejas de entrada de IA le ayuda a preparar texto sin formato para el modo en que los proveedores de buzones de correo pueden procesar sus envíos de [!DNL Journey Optimizer]. No controla los productos de esos proveedores. Una vez enviado el mensaje, las características de IA de [!DNL Gmail], [!DNL Apple] Mail, [!DNL Outlook] u otros clientes funcionarán bajo sus términos, modelos y directivas, no de Adobe.

* **Presentación impredecible**: los resúmenes, las notificaciones, los comentarios y las respuestas conversacionales pueden omitir ofertas, indicar precios o fechas incorrectos, combinar contenido con resultados web no relacionados o parafrasear de formas que ya no coincidan con la copia aprobada. El comportamiento cambia cuando los proveedores actualizan los modelos o la interfaz de usuario sin previo aviso.

* **No hay garantía de paridad con HTML**: Es posible que los destinatarios que dependen de las vistas previas o las respuestas del asistente nunca vean el diseño, las imágenes o los pies de página legales completos de HTML. Lo que creen que el mensaje &quot;dice&quot; puede provenir solamente de un breve resumen generado por IA.

* **Privacidad, cumplimiento y uso de datos**: la inteligencia artificial aplicada a la bandeja de entrada puede procesar el contenido de los mensajes en la infraestructura del proveedor sujeto a la política de privacidad, la retención y las reglas regionales de dicho proveedor. Las organizaciones de los sectores regulados deben evaluar si el uso de estas características por parte de los destinatarios afecta a sus obligaciones, independientemente de cómo se haya creado el correo electrónico en [!DNL Journey Optimizer].

* **Exposición legal o de marca**: los resúmenes de IA incorrectos o incompletos pueden crear confusión o disputas con los clientes acerca de promociones, términos o lenguaje de exclusión. El optimizador mejora la capa de texto que proporciona; no garantiza que el modelo de un tercero lo reproduzca fielmente.

* **[!UICONTROL Optimizar para la bandeja de entrada de IA]** en [!DNL Journey Optimizer]: la acción en tiempo de creación en el Designer de correo electrónico es un sistema independiente de los asistentes de la bandeja de entrada del usuario final. Revise siempre el texto sin formato generado antes de enviarlo.

## Temas relacionados {#related-topics}

* [Administrar la versión de texto de un correo electrónico](../email/text-version-email.md)
* [Introducción al diseño de correo electrónico](../email/get-started-email-design.md)
* Para ver las características generativas de Adobe en un sentido más amplio, consulte [Introducción al asistente de IA para crear contenido](gs-generative.md).
