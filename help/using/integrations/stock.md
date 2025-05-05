---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con imágenes de Adobe Stock
description: Introducción a Adobe Stock
feature: Assets, Integrations
topic: Content Management
role: User
level: Beginner
keywords: stock, imágenes, integración, fotos
exl-id: 0715f65f-04bd-4dc2-a152-98111f4c42e6
source-git-commit: ccfc0870a8d59d16c7f5b6b02856785aa28dd307
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 13%

---

# Trabajar con [!DNL Adobe Stock] imágenes {#stock}

## Introducción a [!DNL Adobe Stock] {#get-started-stock}

El plugin de integración de [!DNL Adobe Stock] y [!DNL Adobe Journey Optimizer] Diseñador de correos electrónicos proporciona a los clientes una forma sencilla de navegar, obtener licencias y guardar imágenes para utilizarlas en la creación de mensajes.

[Adobe Stock](https://helpx.adobe.com/es/stock/get-started.html){target="_blank"} proporciona acceso a millones de fotos, vídeos, ilustraciones y gráficos vectoriales de alta calidad, seleccionados y libres de derechos de autor. Puede optar por adquirir un paquete de crédito para obtener la licencia de los recursos o adquirir solo una licencia estándar o ampliada para el recurso necesario. Adobe Stock también proporciona una colección gratuita de recursos.

Con [!DNL Adobe Journey Optimizer], puede cargar imágenes en sus correos electrónicos directamente desde [!DNL Adobe Stock] y agregarlos a su carpeta **[!UICONTROL Recursos]** usando la opción **[!UICONTROL Buscar fotos de Adobe Stock]**. Además, la variable **[!UICONTROL Buscar fotos de Stock similares]** le ayuda a encontrar imágenes que coincidan con el contenido, el color y la composición del recurso utilizado en el envío.

## Permisos{#stock-permissions}

Las opciones **[!UICONTROL Buscar fotos de Adobe Stock]** y **[!UICONTROL Buscar imagen similar]** están disponibles para los usuarios con acceso a un perfil de producto de AEM Assets Essentials.

Para obtener más información, consulte [Documentación de Experience Manager Assets](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html?lang=es#add-users-to-essentials){target="_blank"}.

## Insertar una imagen de [!DNL Adobe Stock] {#add-stock-image}

Para agregar imágenes de [!DNL Adobe Stock] al contenido, siga los pasos a continuación:

1. En la sección **[!UICONTROL Componentes de contenido]** de Email Designer, arrastre y suelte una **imagen**.

1. Haz clic en el botón **[!UICONTROL Buscar fotos de Adobe Stock]** que se encuentra en la parte izquierda del Designer de correo electrónico.

   ![](assets/stock-find-photos.png)

1. Navegue por la biblioteca o introduzca un término en el campo de búsqueda.

   ![](assets/stock-select-from-lib.png)

1. Seleccione la imagen elegida y haga clic en **[!UICONTROL Guardar]**.

   Si la imagen seleccionada no tiene licencia, debe [obtener la licencia](#license-stock-image).

## Buscar fotos similares {#similar-stock-image}

Puede reemplazar cualquier imagen existente en el contenido de su correo electrónico por una foto de [!DNL Adobe Stock]. Tenga en cuenta que esta opción está disponible para todas las imágenes: imágenes de Stock con licencia o sin licencia e imágenes de la carpeta Assets.

Para examinar fotos similares, siga los pasos a continuación:

1. Seleccione la imagen que desea reemplazar.
1. Haga clic en el botón **[!UICONTROL Buscar fotografías similares de Stock]** para mostrar los recursos de [!DNL Adobe Stock] que coincidan con el contenido, el color y la composición de la imagen.

   ![](assets/stock-similar.png)

1. Seleccione la imagen elegida y haga clic en **[!UICONTROL Guardar]**.

   ![](assets/stock-similar-results.png)

   Si la imagen seleccionada no tiene licencia, debe [obtener la licencia](#license-stock-image).

1. Personaliza tu imagen, si es necesario, con las fichas **[!UICONTROL Configuración]** y **[!UICONTROL Estilos]**. [Más información acerca de la configuración de componentes](../email/content-components.md).

## Obtener la licencia de [!DNL Adobe Stock] {#license-stock-image}

Si la imagen ya tiene licencia, se representa mediante el icono ![](assets/stock_10.png). Si no, debe obtener una licencia.

Para obtener una licencia y descargar la imagen, siga los pasos a continuación:

1. Selecciónelo y haga clic en el icono **[!UICONTROL Imagen de Adobe Stock de licencia]**.

   ![](assets/stock-license-icon.png)

   A continuación, se le redirigirá al sitio web de [!DNL Adobe Stock] para adquirir la licencia.

   ![](assets/stock-license-photo.png)

1. En el sitio web de [!DNL Adobe Stock], debe adquirir el recurso para poder descargar la imagen y quitar la marca de agua.

   Esta compra depende de su plan o suscripción de Adobe Stock. Tenga en cuenta que si tiene varias cuentas de Adobe Stock, se le redirigirá al último ID de Stock utilizado. En este caso, asegúrese de haber iniciado sesión en la cuenta correcta antes de autorizar el recurso.

   Para obtener más información sobre los planes y precios de Adobe Stock en [Documentación de Adobe Stock](https://stock.adobe.com/plans){target="_blank"}.

   >[!WARNING]
   > Si se envía un correo electrónico que incluye una imagen sin licencia, la imagen mantiene su formulario sin licencia con la marca de agua.

1. Una vez que haya completado su compra, ahora puede volver a su correo electrónico en [!DNL Adobe Journey Optimizer] y seleccionar **[!UICONTROL Importar imagen de stock]** para importar su imagen con licencia a sus recursos.

   ![](assets/stock_6.png)

1. Seleccione en qué carpeta almacenar el recurso. Para obtener más información sobre [!DNL Experience Manager Assets], consulte esta [página](assets.md#get-started-assets).

## Temas relacionados{#stock-related-topics}

* [Diseño de correo electrónico en Journey Optimizer](../email/get-started-email-design.md)
* [Configuración de componentes para el diseño de correo electrónico](../email/content-components.md)
* [Introducción a Adobe Stock](https://helpx.adobe.com/es/stock/get-started.html){target="_blank"}.

