---
solution: Journey Optimizer
product: journey optimizer
title: Creación de condiciones
description: Aprenda a crear condiciones
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor, condicional, reglas
exl-id: 246a4a55-059e-462c-ac1e-43b90f4abda4
source-git-commit: 59499dec7d15dd4565c7910d7b454d82243ff011
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 8%

---

# Trabajo con reglas condicionales {#conditions}

Las reglas condicionales son conjuntos de reglas que definen qué contenido debe mostrarse en los mensajes, según varios criterios como atributos de perfiles, pertenencia a segmentos o eventos contextuales.

Las reglas condicionales se crean mediante el editor de expresiones y se pueden almacenar si desea reutilizarlas en el contenido. [Obtenga información sobre cómo guardar una regla condicional en la biblioteca](#save)

>[!NOTE]
>
>Las personas necesitarán el [Administrar elementos de biblioteca](../administration/ootb-product-profiles.md) permiso para guardar o eliminar reglas condicionales. Las condiciones guardadas están disponibles para su uso por parte de todos los usuarios de una organización.

## Acceso al generador de reglas condicionales {#access}

Las reglas condicionales se crean a partir de **[!UICONTROL Condiciones]** dentro del editor de expresiones, al que se puede acceder desde:

* Desde el Diseñador de correo electrónico, al habilitar el contenido dinámico para un componente en el cuerpo del correo electrónico. [Aprenda a añadir contenido dinámico a los correos electrónicos](dynamic-content.md#emails)

   ![](assets/conditions-access-email.png)

* En cualquier campo en el que se pueda añadir personalización utilizando la variable [Editor de expresiones](personalization-build-expressions.md).

   ![](assets/conditions-access-editor.png)

## Creación de una regla condicional {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="Crear condición"
>abstract="Combine atributos de perfil, eventos contextuales o audiencias para crear reglas que definan qué contenido debe mostrarse en los mensajes."

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="Crear condición"
>abstract="Combine atributos de perfil, eventos contextuales o audiencias para crear reglas que definan qué contenido debe mostrarse en los mensajes."

Los pasos para crear una regla condicional son los siguientes:

1. Acceda a la **[!UICONTROL Condiciones]** en el Editor de expresiones o el Diseñador de correo electrónico y, a continuación, haga clic en **[!UICONTROL Crear nuevo]**.

1. Genere la regla condicional según sus necesidades. Para ello, arrastre y suelte y organice los atributos deseados del menú de la izquierda al lienzo.

   Los pasos para combinar atributos en el lienzo son similares a la experiencia de creación de segmentos. Para obtener más información sobre cómo trabajar con el lienzo del generador de reglas, consulte [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#rule-builder-canvas).

   ![](assets/conditions-create.png)

   Los atributos se organizan en tres pestañas:

   * **[!UICONTROL Perfil]**:
      * **[!UICONTROL Abono de segmentos]** enumera todos los atributos del segmento (es decir, estado, versión, etc.) para [Servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html),
      * **[!UICONTROL Perfiles individuales de XDM]** enumera todos los atributos de perfil asociados a [Esquema del modelo de datos de experiencia (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es) definido en Adobe Experience Platform.
   * **[!UICONTROL Contextual]**: cuando el mensaje se utiliza en un recorrido, los campos de recorrido contextual están disponibles a través de esta pestaña.
   * **[!UICONTROL Audiencias]**: enumera todas las audiencias generadas a partir de segmentos creados en [Servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

1. Una vez que la regla condicional esté lista, puede agregarla al mensaje para crear contenido dinámico. [Aprenda a añadir contenido dinámico](dynamic-content.md)

   También puede guardar la regla para permitir una mayor reutilización. [Obtenga información sobre cómo guardar una condición](#save)

## Guardar una regla condicional {#save}

Si hay reglas de condición que reutilizará con frecuencia, puede guardarlas en la biblioteca de condiciones. Todas las reglas guardadas se comparten y las personas de su organización pueden acceder y utilizar.

>[!NOTE]
>
>Las reglas condicionales que aprovechan los recorridos y los atributos contextuales no se pueden guardar en la biblioteca.

1. En la pantalla de edición de la condición, haga clic en **[!UICONTROL Guardar condición]** botón.

1. Asigne un nombre y una descripción (opcional) a la regla y haga clic en **[!UICONTROL Añadir]**.

   ![](assets/conditions-name-description.png)

1. La regla condicional se guardará en la biblioteca. Ahora puede utilizarlo para crear contenido dinámico en los mensajes. [Aprenda a añadir contenido dinámico](dynamic-content.md)

## Editar y eliminar reglas condicionales guardadas {#edit-delete}

Puede eliminar una regla condicional en cualquier momento mediante el botón de puntos suspensivos.

![](assets/conditions-open.png)

No se pueden modificar las reglas condicionales guardadas en la biblioteca. Sin embargo, aún puede utilizarlas para crear nuevas reglas. Para ello, abra la regla condicional, realice los cambios deseados y guárdela en la biblioteca. [Obtenga información sobre cómo guardar una condición en la biblioteca](#save)
