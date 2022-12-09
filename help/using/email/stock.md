---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con imágenes de Adobe Stock
description: Introducción a Adobe Stock
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 0715f65f-04bd-4dc2-a152-98111f4c42e6
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---

# Trabajar con [!DNL Adobe Stock] imágenes {#stock}

## Introducción a [!DNL Adobe Stock] {#get-started-stock}

La variable [!DNL Adobe Stock] y [!DNL Adobe Journey Optimizer] El complemento de integración del Diseñador de correo electrónico proporciona a los clientes una forma sencilla de navegar, obtener licencias y guardar imágenes para utilizarlas en la creación de mensajes.

[Adobe Stock](https://helpx.adobe.com/stock/get-started.html){target=&quot;_blank&quot;} proporciona acceso a millones de fotos, vídeos, ilustraciones y gráficos vectoriales de alta calidad, depurados y sin derechos de autor. Puede elegir adquirir un paquete de crédito para obtener la licencia de los activos o comprar una licencia Standard o Extended para el activo necesario. Adobe Stock también ofrece una recopilación gratuita de recursos.

con [!DNL Adobe Journey Optimizer], puede cargar imágenes en los correos electrónicos directamente desde [!DNL Adobe Stock] y agréguelo a su **[!UICONTROL Assets]** usando la variable **[!UICONTROL Find Adobe Stock photos]** . Además, la variable **[!UICONTROL Find Similar Stock photos]** ayuda a encontrar imágenes que coincidan con el contenido, el color y la composición del recurso utilizado en la entrega.

## Permisos{#stock-permissions}

La variable **[!UICONTROL Find Adobe Stock photos]** y **[!UICONTROL Find Similar Image]** están disponibles para los usuarios con acceso a un perfil de producto de AEM Assets Essentials.

Para obtener más información, consulte [Documentación esencial de Assets](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html#add-users-to-essentials){target=&quot;_blank&quot;}.

## Insertar una imagen desde [!DNL Adobe Stock] {#add-stock-image}

Para agregar imágenes desde [!DNL Adobe Stock] para ver el contenido, siga los pasos a continuación:

1. En el **[!UICONTROL Content components]** del Diseñador de correo electrónico, arrastre y suelte una **Imagen**.

1. Haga clic en el **[!UICONTROL Find Adobe Stock photos]** a la izquierda del Diseñador de correo electrónico.

   ![](assets/stock-find-photos.png)

1. Busque en la biblioteca o escriba un término en el campo de búsqueda.

   ![](assets/stock-select-from-lib.png)

1. Seleccione la imagen elegida y haga clic en **[!UICONTROL Save]**.

   Si la imagen seleccionada no tiene licencia, debe [obtener la licencia](#license-stock-image).


## Buscar fotos similares {#similar-stock-image}

Puede reemplazar cualquier imagen existente en el contenido del correo electrónico con una foto de [!DNL Adobe Stock]. Tenga en cuenta que esta opción está disponible para todas las imágenes: las imágenes y las imágenes con licencia/sin licencia de Stock de su carpeta Assets.

Para examinar fotos similares, siga los pasos a continuación:

1. Seleccione la imagen que desea reemplazar.
1. Haga clic en el **[!UICONTROL Find similar Stock photos]** para mostrar los recursos en [!DNL Adobe Stock] que coinciden con el contenido, el color y la composición de la imagen.

   ![](assets/stock-similar.png)

1. Seleccione la imagen elegida y haga clic en **[!UICONTROL Save]**.

   ![](assets/stock-similar-results.png)

   Si la imagen seleccionada no tiene licencia, debe [obtener la licencia](#license-stock-image).

1. Personalice la imagen, si es necesario, con la variable **[!UICONTROL Components settings]** para abrir el Navegador. [Obtenga más información sobre la configuración de componentes](content-components.md).

## Obtenga la licencia de [!DNL Adobe Stock] {#license-stock-image}

Si la imagen ya tiene licencia, se representa mediante la variable ![](assets/stock_10.png) icono. Si no es así, debe obtener una licencia.

Para obtener una licencia y descargar la imagen, siga los pasos a continuación:

1. Selecciónelo y haga clic en el botón **[!UICONTROL License Adobe Stock image]** icono.

   ![](assets/stock-license-icon.png)

   A continuación, se le redirige a la función [!DNL Adobe Stock] sitio web a pero la licencia.

   ![](assets/stock-license-photo.png)

1. En el [!DNL Adobe Stock] sitio web, debe adquirir el recurso para poder descargar la imagen y eliminar la marca de agua.

   Esta compra depende del plan o la suscripción de Adobe Stock. Tenga en cuenta que si tiene varias cuentas de Adobe Stock, se le redirigirá al último ID de stock utilizado. En este caso, asegúrese de haber iniciado sesión en la cuenta correcta antes de conceder licencias a su recurso.

   Para obtener más información sobre los planes y precios de Adobe Stock en [Documentación de Adobe Stock](https://stock.adobe.com/plans){target=&quot;_blank&quot;}.

   >[!WARNING]
   > Si se envía un correo electrónico que incluye una imagen sin licencia, la imagen conserva su formulario sin licencia con la marca de agua.

1. Una vez finalizada la compra, ahora puede volver al correo electrónico en [!DNL Adobe Journey Optimizer] y seleccione **[!UICONTROL Import stock image]** para importar la imagen con licencia a los recursos.

   ![](assets/stock_6.png)

1. Seleccione en qué carpeta almacenar el recurso. Para obtener más información, consulte [!DNL Assets Essentials], consulte esta [página](assets-essentials.md#get-started-assets-essentials).

## Temas relacionados{#stock-related-topics}

* [Diseño de correo electrónico en Journey Optimizer](get-started-email-design.md)
* [Configuración de componentes para diseño de correo electrónico](content-components.md)
* [Introducción a Adobe Stock](https://helpx.adobe.com/stock/get-started.html){target=&quot;_blank&quot;}.

