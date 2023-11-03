---
solution: Journey Optimizer
product: journey optimizer
title: Crear contenido dinámico
description: Aprenda a añadir contenido dinámico a los mensajes.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor, dinámico, contenido
exl-id: 639ad7df-0d0f-4c9b-95d1-f3101267aae2
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 10%

---

# Crear contenido dinámico {#dynamic-content}

Adobe Journey Optimizer le permite aprovechar las reglas condicionales creadas en la biblioteca para añadir contenido dinámico a los mensajes.

Se puede crear contenido dinámico en cualquier campo donde se pueda añadir personalización mediante el Editor de expresiones. Esto incluye la línea de asunto, los vínculos, el contenido de notificaciones push o las representaciones de ofertas de tipo texto. [Más información sobre los contextos de personalización](personalization-contexts.md)

Además, puede utilizar reglas condicionales en el Diseñador de correo electrónico para crear varias variantes de un componente de contenido.

## Añadir contenido dinámico en expresiones {#perso-expressions}

Los pasos para agregar contenido dinámico en expresiones son los siguientes:

1. Desplácese hasta el campo en el que desee añadir contenido dinámico y, a continuación, abra el Editor de expresiones.

1. Seleccione el **[!UICONTROL Condiciones]** para mostrar la lista de reglas condicionales disponibles. Haga clic en el botón + situado junto a una regla para añadirla a la expresión actual.

   También puede crear una regla nueva seleccionando **[!UICONTROL Crear nuevo]**. [Aprenda a crear condiciones](create-conditions.md)

   ![](assets/conditions-expression.png)

1. Agregar entre `{%if}` y `{%/if}` etiqueta el contenido que desea mostrar si se cumple la regla de condición. Puede agregar tantas reglas como sea necesario para crear varias variantes de una expresión.

   En el ejemplo siguiente, se han creado dos variantes para un contenido SMS, según el idioma preferido del destinatario.

   ![](assets/conditions-language-sample.png)

1. Una vez que el contenido esté listo, puede obtener una vista previa de las diferentes variantes mediante las **[!UICONTROL Simular contenido]** botón. [Obtenga información sobre cómo probar y previsualizar mensajes](../content-management/preview-test.md)

   ![](assets/conditions-preview.png)

## Añadir contenido dinámico a correos electrónicos {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="Contenido condicional"
>abstract="Utilice reglas condicionales para crear varias variantes de un componente de contenido. Si no se cumple ninguna de las condiciones al enviar el mensaje, se muestra el contenido de la variante predeterminada."

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="Contenido condicional"
>abstract="Utilice una regla condicional guardada en la biblioteca o cree una nueva."

Los pasos para crear variantes de un componente de contenido en el Diseñador de correo electrónico son los siguientes:

1. En el [Diseñador de correo electrónico](../email/content-from-scratch.md), seleccione un componente de contenido y haga clic en **[!UICONTROL Habilitar contenido condicional]**.

   ![](assets/conditions-enable-conditional.png)

1. El **[!UICONTROL Contenido condicional]** El panel se muestra a la izquierda. En este panel, puede crear varias variantes del componente de contenido seleccionado mediante condiciones.

   Configure la primera variante seleccionando la **[!UICONTROL Seleccionar condición]** botón.

   ![](assets/conditions-apply.png)

1. Se muestra la biblioteca de condiciones. Seleccione la regla condicional que desea asociar a la variante y haga clic en **[!UICONTROL Seleccionar]**. En este ejemplo, se desea adaptar el texto del componente en función del idioma preferido del destinatario.

   ![](assets/conditions-select.png)

   También puede crear una regla nueva haciendo clic en **[!UICONTROL Crear nuevo]**. [Aprenda a crear condiciones](create-conditions.md)

1. La regla condicional está asociada a la variante. Para mejorar la legibilidad, cambie el nombre de la variante seleccionando la **[!UICONTROL Cambiar nombre]** acción del icono Más acciones.

   ![](assets/conditions-rename.png)

1. Configure cómo debe mostrarse el componente si se cumple la regla al enviar el mensaje. En este ejemplo, deseamos mostrar el texto en francés si es el idioma preferido del destinatario.

   ![](assets/conditions-design.png)

1. Añada tantas variantes como sea necesario para el componente de contenido. Puede cambiar en cualquier momento entre las distintas variantes para comprobar cómo se mostrará el componente de contenido en función de las reglas condicionales.

   >[!NOTE]
   >Si ninguna de las reglas definidas en las variantes se cumple al enviar el mensaje, el componente de contenido mostrará el contenido definido en la variable **[!UICONTROL Variante predeterminada]**.
   >
   >El contenido condicional se evaluará según las reglas asociadas en el orden en que se muestran las variantes. La variante predeterminada siempre se muestra si no se cumplen otras condiciones.

1. Para eliminar una variante, haga clic en el icono Más acciones junto a la variante deseada y seleccione **[!UICONTROL Eliminar]**.

   ![](assets/conditions-delete.png)
