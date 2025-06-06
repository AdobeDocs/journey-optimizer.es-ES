---
solution: Journey Optimizer
product: journey optimizer
title: Añadir CSS personalizado al contenido del correo electrónico
description: Aprenda a añadir CSS personalizado al contenido del correo electrónico directamente en el Designer de correo electrónico en Journey Optimizer
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: css, editor, resumen, correo electrónico
source-git-commit: feb3576c230f2fb28ab031f87cc5f99263329b57
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# Añadir metadatos al contenido del correo electrónico {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_css"
>title="Añadir CSS personalizado"
>abstract="xxx."

Al diseñar los correos electrónicos, puede agregar su propio CSS personalizado directamente en [!DNL Journey Optimizer] [Email Designer](get-started-email-design.md).

Lo que se espera en el área de texto Agregar CSS personalizado es una cadena CSS válida.

![](assets/email-body-css.png)

Condiciones de disponibilidad

La función Añadir CSS personalizada solo está disponible cuando hay contenido definido en el editor. Para ver la sección Añadir CSS personalizado, el usuario debe añadir contenido en el editor. Si el usuario elimina todo su contenido, la sección desaparece y no se aplica el CSS personalizado. Si el usuario vuelve a agregar contenido, la sección estará disponible y se aplicará el CSS personalizado.

**Ejemplos de entradas de CSS no válidas**

CSS no válido no se puede guardar. Si el CSS no es válido, aparecerá un mensaje rojo que indica que no se pudo guardar el CSS.

`<style>` no se acepta


```
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```


falta llave no válida

```
body {
 background: red; 
```
