---
solution: Journey Optimizer
product: journey optimizer
title: Creación de contenido multilingüe con traducción manual
description: Aprenda a crear contenido multilingüe con traducción manual en Journey Optimizer
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: introducción, inicio, contenido, experimento
exl-id: 6244d717-fbd6-468e-9164-60451d0d62f0
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: dd4173698d7034173b7ae9f44afec397d62a6f78
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 6%

---

# Creación de contenido multilingüe con traducción manual {#multilingual-manual}

>[!AVAILABILITY]
>
>Ahora mismo, el contenido multilingüe solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

Con el flujo manual, puede traducir fácilmente su contenido directamente en su campaña y recorrido de correo electrónico, notificaciones push o SMS, lo que le proporciona un control preciso y opciones de personalización para sus mensajes multilingües. Además, puede importar fácilmente contenido multilingüe preexistente con la opción Importar HTML.

Siga estos pasos para crear contenido multilingüe con traducción manual:

1. [Cree su configuración regional](#create-locale).

1. [Crear configuración de idioma](#create-language-settings).

1. [Crear contenido multilingüe](#create-a-multilingual-campaign).

## Crear configuración regional {#create-locale}

Al configurar los ajustes de idioma, como se describe en la sección [Crear la configuración de idioma](#language-settings), si no hay una configuración regional específica disponible para el contenido multilingüe, tiene la flexibilidad de crear tantas configuraciones regionales nuevas como sea necesario mediante el menú **[!UICONTROL Traducción]**.

1. Desde el menú **[!UICONTROL Administración de contenido]**, accede a **[!UICONTROL Traducción]**.

1. En la ficha **[!UICONTROL Diccionario local]**, haga clic en **[!UICONTROL Agregar configuración regional]**.

   ![](assets/locale_1.png)

1. Seleccione su código de configuración regional de la lista **[!UICONTROL Idioma]** y la **[!UICONTROL Región]** asociada.

1. Haga clic en **[!UICONTROL Guardar]** para crear su configuración regional.

   ![](assets/locale_2.png)

## Crear configuración de idioma {#language-settings}

En esta sección, puede establecer el idioma principal y sus configuraciones regionales asociadas para administrar el contenido multilingüe. También puede elegir el atributo que desee utilizar para buscar información relacionada con el idioma del perfil

1. Desde el menú **[!UICONTROL Administración]**, accede a **[!UICONTROL Canal]** > **[!UICONTROL Configuración general]**.

1. En el menú **[!UICONTROL Configuración de idioma]**, haga clic en **[!UICONTROL Crear configuración de idioma]**.

   ![](assets/language_settings_1.png)

1. Escriba el nombre de su **[!UICONTROL configuración de idioma]**.

1. Seleccione las **[!UICONTROL configuraciones regionales]** asociadas a esta configuración. Puede agregar un máximo de 50 configuraciones regionales.

   Si falta una **[!UICONTROL configuración regional]**, puede crearla manualmente de antemano desde el menú **[!UICONTROL Traducción]** o por API. Consulte [Crear nueva configuración regional](#create-locale).

   ![](assets/multilingual-settings-2.png)

1. En el menú **[!UICONTROL Preferencia de envío]**, seleccione el atributo que desee buscar para encontrar información sobre los idiomas del perfil.

   ![](assets/multilingual-settings-3.png)

1. Haga clic en **[!UICONTROL Editar]** junto a su **[!UICONTROL configuración regional]** para personalizarla más y agregar **[!UICONTROL preferencias de perfil]**.

   ![](assets/multilingual-settings-4.png)

1. Seleccione otras **[!UICONTROL configuraciones regionales]** en la lista desplegable Preferencias de perfil y haga clic en **[!UICONTROL Agregar perfiles]**.

1. Acceda al menú avanzado de su **[!UICONTROL configuración regional]** para definir su **[!UICONTROL configuración regional principal]**, es decir, el idioma predeterminado si no se especifica el atributo del perfil.

   También puede eliminar la configuración regional desde este menú avanzado.

   ![](assets/multilingual-settings-5.png)

1. Haz clic en **[!UICONTROL Enviar]** para crear tu **[!UICONTROL configuración de idioma]**.

<!--
1. Access the **[!UICONTROL channel configurations]** menu and create a new channel configuration or select an existing one.


1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Creación de contenido multilingüe {#create-multilingual-campaign}

Después de configurar el contenido multilingüe, está listo para crear la campaña o el recorrido y personalizar el contenido para cada una de las configuraciones regionales seleccionadas.

1. Comience creando y configurando su notificación por correo electrónico, SMS o push [campaign](../campaigns/create-campaign.md) o [recorrido](../building-journeys/journeys-message.md) según sus necesidades.

   >[!AVAILABILITY]
   >
   >Se recomienda incluir solo un proyecto de traducción por recorrido.

1. Cree o importe el contenido original y personalícelo según sea necesario.

1. Una vez creado el contenido principal, haz clic en **[!UICONTROL Guardar]** y vuelve a la pantalla de configuración de la campaña.

   ![](assets/multilingual-campaign-2.png)

1. Haga clic en **[!UICONTROL Agregar idiomas]** y seleccione la **[!UICONTROL configuración de idioma]** creada anteriormente. [Más información](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. Acceda a la configuración avanzada del menú **[!UICONTROL Configuraciones regionales]** y seleccione **[!UICONTROL Copiar principal a todas las configuraciones regionales]**.

   ![](assets/multilingual-campaign-4.png)

1. Ahora que el contenido principal está duplicado en las **[!UICONTROL configuraciones regionales]** seleccionadas, acceda a cada configuración regional y haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]** para traducir el contenido.

   ![](assets/multilingual-campaign-5.png)

1. Puede optar por deshabilitar o habilitar configuraciones regionales con el menú **[!UICONTROL Más acción]** de la configuración regional seleccionada.

   ![](assets/multilingual-campaign-6.png)

1. Para desactivar la configuración multilingüe, haga clic en **[!UICONTROL Agregar idiomas]** y seleccione el idioma que desee conservar como idioma local.

   ![](assets/multilingual-campaign-7.png)

1. Haga clic en **[!UICONTROL Revisar para activar]** y mostrar un resumen de la campaña.

   El resumen le permite modificar la campaña si es necesario y comprobar si algún parámetro es incorrecto o falta.

1. Examine el contenido multilingüe para ver la renderización en cada idioma.

   ![](assets/multilingual-campaign-8.png)

Ahora puede activar la campaña o el recorrido. Una vez enviada, puede medir el impacto del recorrido o la campaña multilingüe dentro de los informes.

>[!IMPORTANT]
>
>A partir de la versión de septiembre, una nueva experiencia de activación de recorrido y campaña le permite administrar todo el proceso de aprobación, lo que garantiza que las campañas y los recorridos sean revisados y aprobados a fondo por las partes interesadas adecuadas antes de lanzarse. Esta función está disponible con disponibilidad limitada. [Más información](../test-approve/gs-approval.md)

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

-->
