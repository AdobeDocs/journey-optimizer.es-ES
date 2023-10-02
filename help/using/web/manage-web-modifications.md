---
title: Administración de modificaciones web
description: Obtenga información sobre cómo administrar modificaciones en el contenido de páginas web de Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 213511b4-7556-4a25-aa23-b50acd11cd34
source-git-commit: f00843c54f18c6d9599d527101496d1d58df09f3
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 6%

---

# Administración de modificaciones web {#manage-web-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Administrar fácilmente todos los cambios"
>abstract="Con este tablero, puede desplazarse por la página web y administrar todos los ajustes y estilos que haya agregado a ella."

Puede administrar fácilmente todos los componentes, ajustes y estilos que agregó a su página web. También puede agregar modificaciones directamente desde el panel dedicado.

## Trabajar con el panel Modificaciones {#use-modifications-pane}

1. Seleccione el **[!UICONTROL Modificaciones]** para mostrar el panel correspondiente a la izquierda.

   ![](assets/web-designer-modifications-pane.png)

1. Puede revisar cada uno de los cambios realizados en la página.

1. Seleccione una modificación no deseada y haga clic en **[!UICONTROL Eliminar modificación]** de la opción **[!UICONTROL Más acciones]** para eliminarlo.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Proceda con cuidado al eliminar una acción, ya que puede afectar a las acciones posteriores.

1. Para eliminar varias modificaciones al mismo tiempo, haga clic en **[!UICONTROL Seleccionar]** en la parte superior del **[!UICONTROL Modificaciones]** , compruebe las modificaciones que desee y haga clic en el **[!UICONTROL Eliminar]** icono.

   ![](assets/web-designer-modifications-select-delete.png)

1. Utilice el **[!UICONTROL Más acciones]** en la parte superior del **[!UICONTROL Modificaciones]** para eliminar todas las modificaciones a la vez.

   ![](assets/web-designer-delete-modifications.png)

1. También puede eliminar solo las modificaciones no válidas, es decir, los cambios que fueron anulados por otros cambios. Por ejemplo, si modifica el color de un texto y lo elimina, la modificación del color deja de ser válida porque el texto ya no existe.

1. Puede cancelar y rehacer las acciones mediante el **[!UICONTROL Deshacer/Rehacer]** en la parte superior derecha de la pantalla.

   ![](assets/web-designer-undo-redo.png)

   Haga clic y mantenga presionado el botón para cambiar entre las **[!UICONTROL Deshacer]** y **[!UICONTROL Rehacer]** opciones. A continuación, haga clic en el botón para aplicar la acción deseada.

## Agregar modificaciones desde el panel dedicado {#add-modifications}

Al editar una página con el diseñador web, puede agregar nuevos cambios al contenido directamente desde el **[!UICONTROL Modificaciones]** panel: sin necesidad de seleccionar un componente y editarlo desde la interfaz del diseñador web. Complete los siguientes pasos.

1. Desde el **[!UICONTROL Modificaciones]** , haga clic en el **[!UICONTROL Más acciones]** botón.

1. Seleccionar **[!UICONTROL Añadir una modificación]**.

   ![](assets/web-designer-add-modification.png)

1. Seleccione el tipo de modificación:

   * **[!UICONTROL Selector de CSS]** - [Más información](#css-selector)
   * **[!UICONTROL Página`<Head>`]** - [Más información](#page-head)

1. Introduzca su contenido y **[!UICONTROL Guardar]** sus cambios.

1. Haga clic en **[!UICONTROL Más acciones]** junto a la modificación y seleccione **[!UICONTROL Información]** para mostrar sus detalles.

   ![](assets/web-designer-add-modification-info.png)

### Selector de CSS {#css-selector}

Para agregar un **Selector de CSS** Realice una modificación, siga los pasos a continuación.

1. Seleccionar **[!UICONTROL Selector de CSS]** como el tipo de modificación.

1. El **[!UICONTROL Selector de elementos CSS]** Este campo le ayuda a buscar y seleccionar los elementos HTML (o nodos del árbol DOM) en los que desea aplicar los cambios. <!--specify the desired CSS element that you want to modify.-->

   ![](assets/web-designer-add-modification-css.png)

1. Seleccione un tipo de acción (**[!UICONTROL Definir contenido]** o **[!UICONTROL Establecer atributo]**) y rellene la información/contenido necesarios.

   * **[!UICONTROL Definir contenido]**: especifique el contenido que va al elemento identificado por el **[!UICONTROL Selector de elementos CSS]** field.

   * **[!UICONTROL Establecer atributo]**: especifique un atributo que se asociará al selector CSS actual para que este selector se pueda identificar también por este atributo. Para ello, introduzca un nombre en la variable **[!UICONTROL Nombre de atributo]** y un valor en el campo **[!UICONTROL Contenido]** field. Si el atributo ya existe, el valor se actualiza; de lo contrario, se agrega un nuevo atributo con el nombre y valor especificados.

     ![](assets/web-designer-add-modification-css-attribute.png)

### Página `<head>` {#page-head}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_head"
>title="Añadir código personalizado"
>abstract="El elemento HEAD es un contenedor de metadatos que se coloca entre las etiquetas HTML y BODY. Añada solo elementos SCRIPT y STYLE. Si agrega etiquetas DIV y otros elementos, es posible que el resto de elementos del HEAD salten al BODY."

Puede agregar código personalizado mediante la variable **[!UICONTROL Página`<head>`]** tipo de modificación.

El `<head>` es un contenedor de metadatos (datos sobre datos) y se coloca entre las etiquetas `<html>` y la etiqueta `<body>` etiqueta. En este caso, el código no espera eventos body o page-load: se ejecuta al principio de la carga de la página.

El `<head>` se utiliza comúnmente para añadir código JavaScript o CSS a la parte superior de la página. Los selectores para las acciones visuales subsiguientes dependen de los elementos del HTML agregados en esta pestaña.

Para agregar un **Página`<head>`** Realice una modificación, siga los pasos a continuación.

1. Seleccionar **[!UICONTROL Página`<head>`]** como el tipo de modificación.

   ![](assets/web-designer-add-modification-head-type.png)

1. Añada su código personalizado en **[!UICONTROL Contenido]** cuadro.

   >[!CAUTION]
   >
   >Solo puede añadir `<script>` y `<style>` elementos a la `<head>` sección. Si agrega las etiquetas `<div>` y otros elementos, los restantes elementos de `<head>` podrían saltar a la sección `<body>`. 

1. Haga clic en **[!UICONTROL Opciones de edición avanzadas]** botón. Se abre el Editor de expresiones.

   ![](assets/web-designer-add-modification-head-advanced.png)

   Puede aprovechar las [!DNL Journey Optimizer] Editor de expresiones con todas sus capacidades de personalización y creación. [Más información](../personalization/personalization-build-expressions.md)

#### Ejemplos de código personalizado {#custom-code-examples}

Puede usar el complemento **[!UICONTROL Página`<head>`]** tipo de modificación a:

* Utilice JavaScript en línea o vincule a un archivo JavaScript externo.

  Por ejemplo, para cambiar el color de un elemento:

  ```
  <script type="text/javascript">
  document.getElementById("element_id").style.color = "blue";
  </script>
  ```

* Configure un estilo en línea o un vínculo a una hoja de estilos externa.

  Por ejemplo, para definir una clase para un elemento de superposición:

  ```
  <style>
  .overlay
  { position: absolute; top:0; left: 0; right: 0; bottom: 0; background: red; }
  </style>
  ```

#### Prácticas recomendadas de código personalizado {#custom-code-best-practices}

+++ **Siempre ajuste el código personalizado en un elemento.**

Por ejemplo:

```
<script>
// Code goes here
</script>
```

En caso de que sea necesario realizar alguna modificación, realice cambios dentro de este contenedor.

Si ya no necesita el código personalizado, deje este contenedor vacío, pero no lo elimine. Esto garantiza que otras modificaciones de la experiencia no se vean afectadas.

+++

+++ **No realice acciones document.write en scripts de código personalizados.**

Los scripts se ejecutan de forma asincrónica. Esto suele hacer que las acciones de document.write aparezcan en el lugar incorrecto de la página. No se recomienda utilizar document.write en scripts creados con código personalizado.

+++

+++ **Si crea un elemento y después lo modifica, no elimine el elemento original.**

Cada cambio crea un nuevo elemento en la variable **[!UICONTROL Modificaciones]** panel. Debido a que la segunda acción modifica al Elemento 1, si elimina el Elemento 1, esa acción ya no tiene nada para modificar, por lo que el cambio ya no funciona.

+++

+++ **Tenga cuidado al utilizar el**[!UICONTROL  Página `<head>`]**tipo de modificación para dos campañas que afectan a la misma dirección URL.**

Si usa el **[!UICONTROL Página`<head>`]** Tipo de modificación Para dos campañas que afectan a la misma dirección URL, JavaScript se inserta en la página desde ambas campañas. [!DNL Journey Optimizer] determina automáticamente el orden del contenido enviado. Asegúrese de que el código no dependa de la ubicación. Depende de usted asegurarse de que no haya conflictos en el código.

+++
