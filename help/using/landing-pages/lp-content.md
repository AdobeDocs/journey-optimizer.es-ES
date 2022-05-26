---
title: Definición del contenido específico de una página de aterrizaje
description: Aprenda a diseñar contenido específico de una página de aterrizaje en Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
source-git-commit: f4b3a9de47e724f7b23df8a02b8106c131cf1b12
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 3%

---

# Definición del contenido específico de una página de aterrizaje {#lp-content}

Para definir contenido específico que permita a los usuarios seleccionar y enviar sus opciones desde la página de aterrizaje, use la variable **[!UICONTROL Form]** componente. Para ello, siga los pasos a continuación.

>[!NOTE]
>
>También puede crear una página de aterrizaje de pulsaciones sin **[!UICONTROL Form]** componente. En ese caso, la página de aterrizaje se mostrará a los usuarios, pero no se les pedirá que envíen ningún formulario. Esto puede resultar útil si solo desea mostrar una página de aterrizaje sin requerir ninguna acción por parte de sus destinatarios, como la inclusión o la exclusión, o si desea proporcionar información que no requiera la entrada del usuario.

## Uso del componente de formulario {#use-form-component}

1. Arrastre y suelte el elemento específico de la página de aterrizaje **[!UICONTROL Form]** de la paleta izquierda al espacio de trabajo principal.

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >La variable **[!UICONTROL Form]** solo se puede utilizar una vez en la misma página.

1. Selecciónelo. La variable **[!UICONTROL Form content]** se muestra en la paleta derecha para permitirle editar los distintos campos del formulario.

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >Cambie a la **[!UICONTROL Form style]** para editar los estilos del contenido del componente del formulario en cualquier momento. [Más información](#define-lp-styles)

1. En el **[!UICONTROL Checkbox 1]** , puede editar la etiqueta correspondiente a esta casilla de verificación.

1. Defina si esta casilla de verificación debe incluir o excluir usuarios: ¿aceptan recibir comunicaciones o piden que no se les contacte más?

   ![](assets/lp_designer-form-update.png)

   Seleccione entre las tres opciones siguientes:

   * **[!UICONTROL Opt in if checked]**: los usuarios deben marcar la casilla de verificación para aceptar (adhesión).
   * **[!UICONTROL Opt out if checked]**: los usuarios deben marcar la casilla para eliminar su consentimiento (exclusión).
   * **[!UICONTROL Opt in if checked, opt out if unchecked]**: esta opción le permite insertar una sola casilla de verificación para la inclusión/exclusión. Los usuarios deben marcar la casilla de verificación para el consentimiento (inclusión) y desmarcar para eliminar su consentimiento (exclusión).

1. Elija lo que se actualizará entre las tres siguientes opciones:

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Subscription list]**: Debe seleccionar la lista de suscripción que se actualizará si el perfil selecciona esta casilla de verificación. Más información sobre [listas de suscripción](subscription-list.md).

      ![](assets/lp_designer-form-subs-list.png)

   * **[!UICONTROL Channel (email)]**: La inclusión o exclusión se aplica a todo el canal. Por ejemplo, si un perfil que decide excluirse tiene dos direcciones de correo electrónico, ambas se excluirán de todas las comunicaciones.

   * **[!UICONTROL Email identity]**: La opción de inclusión o exclusión solo se aplica a la dirección de correo electrónico que se utilizó para acceder a la página de aterrizaje. Por ejemplo, si un perfil tiene dos direcciones de correo electrónico, solo el que se utilizó para la inclusión recibirá comunicaciones de su marca.

1. Haga clic en **[!UICONTROL Add field]** > **[!UICONTROL Checkbox]** para agregar otra casilla de verificación. Repita los pasos anteriores para definir sus propiedades.

   ![](assets/lp_designer-form-checkbox-2.png)

1. Una vez agregadas todas las casillas de verificación deseadas, haga clic en **[!UICONTROL Call to action]** para expandir la sección correspondiente. Permite definir el comportamiento del botón en la variable **[!UICONTROL Form]** componente.

   ![](assets/lp_designer-form-call-to-action.png)

1. Defina lo que sucederá al hacer clic en el botón :

   * **[!UICONTROL Redirect URL]**: Introduzca la dirección URL de la página a la que se redirigirá a los usuarios.
   * **[!UICONTROL Confirmation text]**: Escriba el texto de confirmación que se mostrará.
   * **[!UICONTROL Link to a subpage]**: Configure un [subpágina](create-lp.md#configure-subpages) y selecciónela en la lista desplegable que se muestra.

   ![](assets/lp_designer-form-confirmation-action.png)

1. Defina lo que sucederá al hacer clic en el botón en caso de que se produzca un error:

   * **[!UICONTROL Redirect URL]**: Introduzca la dirección URL de la página a la que se redirigirá a los usuarios.
   * **[!UICONTROL Error text]**: Escriba el texto del error que se mostrará. Puede obtener una vista previa del texto del error al definir la variable [estilos de formulario](#define-lp-styles).

   * **[!UICONTROL Link to a subpage]**: Configure un [subpágina](create-lp.md#configure-subpages) y selecciónela en la lista desplegable que se muestra.

   ![](assets/lp_designer-form-error.png)

1. Si desea realizar más actualizaciones al enviar el formulario, seleccione **[!UICONTROL Opt in]** o **[!UICONTROL Opt out]** y defina si desea actualizar una lista de suscripción, el canal o solo la dirección de correo electrónico utilizada.

   ![](assets/lp_designer-form-additionnal-update.png)

1. Guarde el contenido y haga clic en la flecha situada junto al nombre de la página para volver al [propiedades de página de aterrizaje](create-lp.md#configure-primary-page).

   ![](assets/lp_designer-form-save.png)

<!--Will the name Email Designer be kept if you can also design LP with the same tool? > To modify in Messages section > content designer or Designer-->

## Definir estilos de formulario de una página de aterrizaje {#lp-form-styles}

1. Para modificar los estilos del contenido del componente del formulario, cambie en cualquier momento a la función **[!UICONTROL Form style]** pestaña .

   ![](assets/lp_designer-form-style.png)

1. Expanda el **[!UICONTROL Checkboxes]** para definir el aspecto de las casillas de verificación y el texto correspondiente. Por ejemplo, puede ajustar la familia o el tamaño de la fuente y el color del borde de la casilla de verificación.

   ![](assets/lp_designer-form-style-checkboxes.png)

1. Expanda el **[!UICONTROL Buttons]** para modificar el aspecto del botón en el formulario de componentes. Por ejemplo, puede añadir un borde, editar el color de la etiqueta al pasar el ratón por encima o ajustar la alineación del botón.

   ![](assets/lp_designer-form-style-buttons.png)

   Puede obtener una vista previa de algunos ajustes, como el color de la etiqueta del botón al pasar el ratón por encima del ratón **[!UICONTROL Preview]** botón. Obtenga más información sobre la prueba de páginas de aterrizaje [here](create-lp.md#test-landing-page).

   ![](assets/lp_designer-form-style-buttons-preview.png)

1. Expanda el **[!UICONTROL Form layout]** para editar los ajustes del diseño, como el color de fondo, el relleno o el margen.

   ![](assets/lp_designer-form-style-layout.png)

1. Expanda el **[!UICONTROL Form error]** para ajustar la visualización del mensaje de error que se muestra en caso de que se produzca un problema. Marque la opción correspondiente para previsualizar el texto del error en el formulario.

   ![](assets/lp_designer-form-error-preview.png)

