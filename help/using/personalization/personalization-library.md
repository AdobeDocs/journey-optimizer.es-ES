---
title: Trabajar con expresiones guardadas
description: Learn how to work with saved expressions from the [!DNL Journey Optimizer] library.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 163211f95436a37dee7deffea9ced1a3fa09dc34
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Trabajar con expresiones guardadas {#expression-library}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Acerca de la biblioteca de expresiones"
>abstract="[!DNL Journey Optimizer] proporciona una biblioteca en la que puede acceder a las expresiones de personalización guardadas que han configurado los usuarios administradores. "

[!DNL Journey Optimizer] proporciona una biblioteca en la que puede acceder a las expresiones de personalización guardadas anteriormente que han agregado los usuarios administradores.

1. Para acceder a las expresiones guardadas, haga clic en el botón **[!UICONTROL Library]** en el panel izquierdo. La lista muestra todas las expresiones que los usuarios administradores han guardado (consulte [Guardar expresiones en la biblioteca](#save-expressions)).

   >[!NOTE]
   >
   >You can use the info button to get more information about the contents of a saved expression. If you have the appropriate permissions to manage library items, the information button will appear in the ellipse menu.

   ![](assets/library-list.png)

1. Click the + to insert the expression into the editor. A continuación, puede personalizar y validar el contenido de personalización como de costumbre. [Más información](../personalization/personalization-build-expressions.md)

   ![](assets/library-add.png)

## Save an expression to the library {#save-expressions}

[!DNL Journey Optimizer] allows Admin users to save personalization expressions to the library. These expressions will then be available to all users to build personalization contents.

Para guardar una expresión en la biblioteca, siga estos pasos:

1. En la interfaz del editor, cree la expresión y haga clic en **[!UICONTROL Add to library]**.

   >[!NOTE]
   >
   >If the button is not visible, check in the Admin Console that you have the required permissions (see [Permissions levels](../administration/high-low-permissions.md)).

   ![](assets/library-save.png)

1. En el panel derecho, introduzca un título y una descripción para la expresión para ayudar a los usuarios a encontrarla más fácilmente y, a continuación, haga clic en **[!UICONTROL Add]**.

   ![](assets/add-expression.png)

1. La expresión se agrega a la biblioteca . Los usuarios ahora pueden usarlo para crear su contenido personalizado.


>[!NOTE]
>
>* Se guardan hasta 40 expresiones en la biblioteca.
>
>* Las expresiones no pueden superar los 200 KB.
>
>* Las expresiones guardadas se ordenan por fecha de creación: la expresión agregada recientemente se mostrará primero en la lista.



Para editar una expresión existente, agréguela al editor y luego modifíquela según sus necesidades. Haga clic en **[!UICONTROL Add to library]** para validar la sintaxis y guardar la expresión.

Para eliminar una expresión, haga clic en el botón elipse y luego en **[!UICONTROL Delete]**.
