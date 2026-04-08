---
solution: Journey Optimizer
product: journey optimizer
title: Edición de plantillas de correo electrónico con el editor avanzado de HTML
description: Utilice el modo experto para ver y editar el origen de HTML del contenido del correo electrónico en el editor de WYSIWYG, con control de indicadores de funciones, protecciones y validación de guardado.
feature: Templates
topic: Content Management
role: User
level: Experienced
exl-id: 0c586565-0c65-435f-986d-cd08b59de159
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 7%

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

Al utilizar el editor avanzado de HTML, las siguientes protecciones protegen la compatibilidad del contenido y establecen expectativas.

* El editor de HTML avanzado **no valida** su código. No comprueba errores de sintaxis ni diseños rotos. Revise el contenido cuidadosamente antes de guardarlo.

* Las futuras actualizaciones del sistema pueden sobrescribir los cambios realizados en el marcado predeterminado. **Es posible que los cambios no se mantengan**.

* El equipo de soporte [!DNL Adobe]de **no puede solucionar ni resolver** problemas causados por cambios manuales y código personalizado. Mantenga una copia de seguridad del contenido en caso de que necesite revertirlo.

* No se puede simular contenido en la vista avanzada de HTML. Cambie a la vista de escritorio para previsualizar el contenido.

* Para garantizar la compatibilidad del contenido, **no puede guardar** en la vista avanzada de HTML. Cambie a la vista Escritorio cuando esté listo para guardar los cambios.

>[!WARNING]
>
>El editor de HTML avanzado de la plantilla de contenido no es lo mismo que el modo **[!UICONTROL Codifique su propio]** en el Designer de correo electrónico. En el modo [!UICONTROL Codifique su propio], no puede volver al editor visual; una vez que elija esa ruta, permanecerá en la edición de solo código. Por el contrario, el editor avanzado de HTML le permite alternar entre la vista de HTML y la vista de escritorio (visual) en cualquier momento. [Obtenga más información sobre el editor de código](../email/code-content.md)

## Cambiar a la vista avanzada de HTML {#switch-to-html-view}

Para abrir el editor de HTML avanzado y editar el origen de la plantilla, siga estos pasos.

1. Abra o cree una [plantilla de correo electrónico](../content-management/create-content-templates.md) y abra el [Designer de correo electrónico](../email/get-started-email-design.md) para editar el contenido.

1. Haga clic en el botón **[!UICONTROL HTML]** en la esquina superior derecha de la pantalla.

   ![Ubicación del botón HTML en la barra de herramientas de Designer de correo electrónico](assets/email-template-expert-mode-button.png)

1. La primera vez que se abre el editor avanzado de HTML, se muestra un mensaje de advertencia. Revíselo cuidadosamente y haga clic en **[!UICONTROL Aceptar]** para continuar. [Más información](#guardrails)

   ![Cuadro de diálogo de advertencia al abrir el editor de HTML avanzado por primera vez](assets/email-template-expert-mode-warning.png){zoomable="yes"}

   >[!NOTE]
   >
   >Esta advertencia aparece solo la primera vez que abre el editor avanzado de HTML y se restablece cada mes.

1. Se muestra el editor avanzado de HTML.

   ![Interfaz de editor de HTML avanzada que muestra el código fuente de la plantilla de correo electrónico](assets/email-template-expert-mode.png)

1. Añada los cambios que desee al contenido del correo electrónico.

   >[!WARNING]
   >
   >Asegúrese de escribir el código CSS y HTML correcto, ya que no hay ningún proceso de validación de sintaxis y [!DNL Adobe] no proporciona compatibilidad. [Más información](#guardrails)

1. La simulación y el guardado de contenido no están disponibles en la vista avanzada de HTML por motivos de compatibilidad. Vuelva a la vista Escritorio para obtener una vista previa del contenido y guardar los cambios.

   ![Vuelva a la vista Escritorio para guardar los cambios](assets/email-template-expert-mode-save.png){zoomable="yes"}

   >[!NOTE]
   >
   >Las ediciones se conservan al cambiar de vista.

<!--
    ![](assets/email-template-expert-mode-simulate.png){zoomable="yes"}
-->

## Temas relacionados

* [Codifique su propio contenido de correo electrónico](../email/code-content.md)
* [Creación de plantillas de contenido](create-content-templates.md)
* [Introducción al Diseñador de correo electrónico](../email/get-started-email-design.md)

