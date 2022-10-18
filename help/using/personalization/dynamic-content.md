---
solution: Journey Optimizer
product: journey optimizer
title: Crear contenido dinámico
description: Aprenda a añadir dinámicas a los mensajes.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---


# Crear contenido dinámico {#dynamic-content}

Adobe Journey Optimizer le permite aprovechar las reglas condicionales creadas en la biblioteca para añadir contenido dinámico a los mensajes.

Se puede crear contenido dinámico en cualquier campo en el que se pueda añadir personalización mediante el Editor de expresiones. Esto incluye la línea de asunto, los vínculos, el contenido de las notificaciones push o las representaciones de ofertas de tipo texto. [Más información sobre los contextos de personalización](personalization-contexts.md)

Además, puede utilizar reglas condicionales en el Diseñador de correo electrónico para crear varias variantes de un componente de contenido.

## Añadir contenido dinámico en expresiones {#perso-expressions}

Los pasos para agregar contenido dinámico en expresiones son los siguientes:

1. Vaya al campo en el que desea agregar contenido dinámico y, a continuación, abra el Editor de expresiones.

1. Seleccione el **[!UICONTROL Condiciones]** para mostrar la lista de reglas condicionales disponibles. Haga clic en el botón + situado junto a una regla para agregarla a la expresión actual.

   También puede crear una regla nueva seleccionando **[!UICONTROL Crear nuevo]**. [Aprenda a crear condiciones](create-conditions.md)

   ![](assets/conditions-expression.png)

1. Agregue entre las variables `{%if}` y `{%/if}` etiqueta el contenido que desea mostrar si se cumple la regla condicional. Puede agregar tantas reglas como sea necesario para crear varias variantes de una expresión.

   En el siguiente ejemplo, se han creado dos variantes para un contenido SMS, según el idioma preferido del destinatario.

   ![](assets/conditions-language-sample.png)

1. Una vez que el contenido esté listo, puede obtener una vista previa de las diferentes variantes utilizando la variable **[!UICONTROL Simular contenido]** botón. [Obtenga información sobre cómo probar y previsualizar mensajes](../design/preview.md)

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

1. En el Diseñador de correo electrónico, seleccione un componente de contenido y haga clic en **[!UICONTROL Habilitar contenido condicional]**.

   ![](assets/conditions-enable-conditional.png)

1. La variable **[!UICONTROL Contenido condicional]** en la parte izquierda. En este panel, puede crear varias variantes del componente de contenido seleccionado mediante condiciones.

   Configure la primera variante seleccionando la **[!UICONTROL Condición de aplicación]** botón.

   ![](assets/conditions-apply.png)

1. Se muestra la biblioteca de condiciones. Seleccione la regla condicional para asociarla a la variante y haga clic en **[!UICONTROL Select]**. En este ejemplo, se desea adaptar el texto del componente en función del idioma preferido del destinatario.

   ![](assets/conditions-select.png)

   También puede crear una regla nueva haciendo clic en **[!UICONTROL Crear nuevo]**. [Aprenda a crear condiciones](create-conditions.md)

1. La regla condicional está asociada a la variante . Para mejorar la legibilidad, se recomienda cambiar el nombre de la variante haciendo clic en el menú elipse .

   A continuación, configure cómo se debe mostrar el componente si se cumple la regla al enviar el mensaje. En este ejemplo, deseamos mostrar el texto en francés si es el idioma preferido del destinatario.

   ![](assets/conditions-design.png)

1. Añada tantas variantes como sea necesario para el componente de contenido. Puede cambiar en cualquier momento entre las diferentes variantes para comprobar cómo se mostrará el componente de contenido en función de las reglas condicionales.

   >[!NOTE]
   >Si no se cumple ninguna de las reglas definidas en las variantes al enviar el mensaje, el componente de contenido mostrará el contenido definido en la variable **[!UICONTROL Variante predeterminada]**.
   >
   >El contenido condicional se evaluará con respecto a las reglas asociadas en el orden en que se muestran las variantes. La variante predeterminada siempre se muestra si no se cumplen otras condiciones.
