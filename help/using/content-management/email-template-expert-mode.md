---
solution: Journey Optimizer
product: journey optimizer
title: Edición de plantillas de correo electrónico con el editor avanzado de HTML
description: Utilice el modo experto para ver y editar el origen de HTML del contenido del correo electrónico en el editor de WYSIWYG, con control de indicadores de funciones, protecciones y validación de guardado.
feature: Templates
topic: Content Management
role: User
hidefromtoc: true
hide: true
level: Experienced
exl-id: 0c586565-0c65-435f-986d-cd08b59de159
source-git-commit: 1ab21ba3a656f59de748ee90f360b99c0dc2f7a5
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 5%

---

# Edición de plantillas de correo electrónico con el editor avanzado de HTML {#email-template-expert-mode}

>[!AVAILABILITY]
>
>Esta funcionalidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

El **editor de HTML avanzado** es un modo experto que te permite ver y editar el código fuente sin procesar de las plantillas de contenido de correo electrónico directamente desde la interfaz de Designer de correo electrónico de [!DNL Journey Optimizer].

Esta capacidad permite insertar expresiones avanzadas, como condiciones, directamente en el origen. Cuando vuelva a la vista visual (Escritorio), el contenido se vuelve a procesar para que pueda comprobar su aspecto y seguir editando en cualquier vista.

>[!NOTE]
>
>Esta función solo está disponible en plantillas de contenido y para el canal de correo electrónico.

## Mecanismos de protección {#guardrails}

Cuando se utiliza el editor avanzado de HTML, se aplican las siguientes protecciones para proteger la compatibilidad del contenido y establecer expectativas.

* Actualmente, no hay **ningún proceso de validación** en el editor de HTML avanzado. Los errores de sintaxis y los diseños rotos no están marcados. Asegúrese de revisar el contenido cuidadosamente antes de guardarlo.

* Las futuras actualizaciones del sistema pueden revertir los cambios realizados en el marcado predeterminado. Tenga en cuenta que **es posible que sus cambios se sobrescriban**.

* Los problemas causados por cambios manuales y código personalizado **no se pueden solucionar con problemas** ni resolver por el equipo de soporte técnico de [!DNL Adobe]. Asegúrese de tener una copia de seguridad del contenido en caso de que necesite volver a una versión anterior.

* Para garantizar la compatibilidad del contenido, **guardar no está disponible** en la vista avanzada de HTML. Cuando esté listo para guardar los cambios, debe volver a la vista Escritorio.

>[!WARNING]
>
>El editor de HTML avanzado de la plantilla de contenido no es lo mismo que el modo **[!UICONTROL Codifique su propio]** en el Designer de correo electrónico. En el modo [!UICONTROL Codifique su propio], no puede volver al editor visual; una vez que elija esa ruta, permanecerá en la edición de solo código. Por el contrario, el editor avanzado de HTML le permite alternar entre la vista de HTML y la vista de escritorio (visual) en cualquier momento. [Obtenga más información sobre el editor de código](../email/code-content.md)

## Cambiar a la vista avanzada de HTML {#switch-to-desktop-view}

1. Abra o cree una [plantilla de correo electrónico](../content-management/create-content-templates.md) y abra el [Designer de correo electrónico](../email/get-started-email-design.md) para editar el contenido.

1. Haga clic en el botón **[!UICONTROL HTML]** en la esquina superior derecha de la pantalla.

   ![](assets/email-template-expert-mode-button.png)

1. La primera vez que se abre el editor avanzado de HTML, se muestra un mensaje de advertencia. Revíselo cuidadosamente y haga clic en **[!UICONTROL Aceptar]** para continuar. [Más información](#guardrails)

   >[!NOTE]
   >
   >Esta advertencia aparece solo la primera vez que abre el editor avanzado de HTML y se restablece cada mes.

   ![](assets/email-template-expert-mode-warning.png){zoomable="yes"}

1. Se muestra el editor avanzado de HTML.

   ![](assets/email-template-expert-mode.png)

1. Añada los cambios que desee al contenido del correo electrónico.

   >[!WARNING]
   >
   >Asegúrese de escribir el código CSS y HTML correcto, ya que no hay ningún proceso de validación de sintaxis y [!DNL Adobe] no proporciona compatibilidad. [Más información](#guardrails)

1. Guardar no está disponible en la vista avanzada de HTML. Vuelva a la vista Escritorio para guardar los cambios.

   ![](assets/email-template-expert-mode-save.png){zoomable="yes"}

   >[!NOTE]
   >
   >El contenido solo se puede guardar en la vista de escritorio por motivos de compatibilidad con el contenido. Las ediciones se conservan al cambiar de vista.
