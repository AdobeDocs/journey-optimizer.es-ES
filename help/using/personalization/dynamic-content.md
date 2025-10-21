---
solution: Journey Optimizer
product: journey optimizer
title: Crear contenido dinámico
description: Aprenda a añadir contenido dinámico a los mensajes.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: expresión, editor, dinámico, contenido
exl-id: 639ad7df-0d0f-4c9b-95d1-f3101267aae2
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 14%

---

# Crear contenido dinámico {#dynamic-content}

Adobe Journey Optimizer le permite aprovechar las reglas condicionales creadas en la biblioteca para añadir contenido dinámico a los mensajes.

Se puede crear contenido dinámico en cualquier campo donde se pueda añadir personalización mediante el editor de personalización. Esto incluye la línea de asunto, los vínculos, el contenido de notificaciones push o las representaciones de ofertas de tipo texto. [Más información sobre personalización](personalize.md)

Además, puede utilizar reglas condicionales en el Designer de correo electrónico para crear varias variantes de un componente de contenido.

## Añadir contenido dinámico en expresiones {#perso-expressions}

Los pasos para agregar contenido dinámico en expresiones son los siguientes:

1. Vaya al campo donde desea añadir contenido dinámico y, a continuación, abra el editor de personalización.

1. Seleccione el menú **[!UICONTROL Condiciones]** para mostrar la lista de reglas condicionales disponibles. Haga clic en el botón + situado junto a una regla para añadirla a la expresión actual.

   También puede crear una regla nueva seleccionando **[!UICONTROL Crear nuevo]**. [Aprenda a crear condiciones](create-conditions.md)

   ![](assets/conditions-expression.png)

1. Agregue entre las etiquetas `{%if}` y `{%/if}` el contenido que desea mostrar si se cumple la regla de condición. Puede agregar tantas reglas como sea necesario para crear varias variantes de una expresión.

   En el ejemplo siguiente, se han creado dos variantes para un contenido SMS, según el idioma preferido del destinatario.

   ![](assets/conditions-language-sample.png)

1. Una vez que el contenido esté listo, puede obtener una vista previa de las diferentes variantes mediante el botón **[!UICONTROL Simular contenido]**. [Obtenga información sobre cómo probar y obtener una vista previa de los mensajes](../content-management/preview-test.md)

   ![](assets/conditions-preview.png)

>[!CAUTION]
>
>Si el Designer de correo electrónico no se representa correctamente después de agregar bloques condicionales, compruebe que la sintaxis de cada nueva condición sea correcta y que no existan instrucciones duplicadas o en conflicto. Si los problemas persisten, considere la posibilidad de volver a crear secciones problemáticas en una plantilla nueva y pruebe cada bloque condicional gradualmente.


## Añadir contenido dinámico a correos electrónicos {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="Contenido condicional"
>abstract="Utilice reglas condicionales para crear varias variantes de un componente de contenido. Si no se cumple ninguna de las condiciones al enviar el mensaje, se muestra el contenido de la variante predeterminada."

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="Contenido condicional"
>abstract="Utilice una regla condicional guardada en la biblioteca o cree una nueva."

Los pasos para crear variantes de un componente de contenido en el Designer de correo electrónico son los siguientes:

1. En [Email Designer](../email/content-from-scratch.md), seleccione un componente de contenido y haga clic en **[!UICONTROL Habilitar contenido condicional]**.

   ![](assets/conditions-enable-conditional.png)

1. El panel **[!UICONTROL Contenido condicional]** se muestra a la izquierda. En este panel, puede crear varias variantes del componente de contenido seleccionado mediante condiciones.

   Configure su primera variante seleccionando el botón **[!UICONTROL Seleccionar condición]**.

   ![](assets/conditions-apply.png)

1. Se muestra la biblioteca de condiciones. Seleccione la regla condicional que se asociará a la variante y luego haga clic en **[!UICONTROL Seleccionar]**. En este ejemplo, se desea adaptar el texto del componente en función del idioma preferido del destinatario.

   ![](assets/conditions-select.png)

   También puede crear una regla nueva si hace clic en **[!UICONTROL Crear nuevo]**. [Aprenda a crear condiciones](create-conditions.md)

1. La regla condicional está asociada a la variante. Para mejorar la legibilidad, cambie el nombre de la variante seleccionando la acción **[!UICONTROL Cambiar nombre]** del icono Más acciones.

   ![](assets/conditions-rename.png)

1. Configure cómo debe mostrarse el componente si se cumple la regla al enviar el mensaje. En este ejemplo, deseamos mostrar el texto en francés si es el idioma preferido del destinatario.

   ![](assets/conditions-design.png)

1. Añada tantas variantes como sea necesario para el componente de contenido. Puede cambiar en cualquier momento entre las distintas variantes para comprobar cómo se mostrará el componente de contenido en función de las reglas condicionales.

   >[!NOTE]
   >
   >* Si ninguna de las reglas definidas en las variantes se cumple al enviar el mensaje, el componente de contenido mostrará el contenido definido en la **[!UICONTROL variante predeterminada]**.
   >
   >* El contenido condicional se evaluará según las reglas asociadas en el orden en que se muestran las variantes. La variante predeterminada siempre se muestra si no se cumplen otras condiciones.
   >
   >* Al simular o procesar pruebas de correos electrónicos que contienen varias variantes condicionales, Journey Optimizer puede precisar de más tiempo de procesamiento. Si experimenta tiempos de espera o mensajes de error, considere la posibilidad de reducir la cantidad total de variantes o simplificar las reglas condicionales. Más información sobre cómo probar el contenido en [esta página](../content-management/preview-test.md).


1. Para eliminar una variante, haga clic en el icono Más acciones que está junto a la variante deseada y seleccione **[!UICONTROL Eliminar]**.

   ![](assets/conditions-delete.png)
