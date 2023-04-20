---
solution: Journey Optimizer
product: journey optimizer
title: Fuente de datos de Adobe Experience Platform
description: Obtenga información sobre cómo configurar la fuente de datos de Adobe Experience Platform
feature: Data Sources
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: integrado, fuente, datos, plataforma, integración
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 32%

---

# Fuente de datos de Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Fuente de datos de Adobe Experience Platform"
>abstract="La fuente de datos de Adobe Experience Platform define la conexión con el perfil del cliente en tiempo real de Adobe. Esta fuente de datos está integrada y preconfigurada, y no se puede eliminar. Se ha diseñado para recuperar y utilizar datos del servicio del perfil del cliente en tiempo real; por ejemplo, comprobar si la persona que ha introducido un recorrido es una mujer. Permite utilizar información del perfil y datos de los eventos de experiencia."

La fuente de datos de Adobe Experience Platform define la conexión con el perfil del cliente en tiempo real de Adobe. Esta fuente de datos está integrada y preconfigurada, y no se puede eliminar. Esta fuente de datos está diseñada para recuperar y utilizar datos del servicio Perfil del cliente en tiempo real (por ejemplo, comprobar si la persona que ha introducido un recorrido es una mujer). Permite utilizar información del perfil y datos de los eventos de experiencia. Para obtener más información sobre el perfil del cliente en tiempo real de Adobe, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}.


Para permitir la conexión con el servicio de Perfil del cliente en tiempo real, debemos utilizar una clave para identificar a una persona y un área de nombres que contextualice la clave. Como resultado, solo puede utilizar esta fuente de datos si sus recorridos empiezan por un evento que contenga una clave y un área de nombres. [Más información](../building-journeys/journey.md).

Puede editar el grupo de campos preconfigurado llamado &quot;ProfileFieldGroup&quot;, agregar nuevos y eliminar los que no se usan en borradores o recorridos activos. [Más información](../datasource/configure-data-sources.md#define-field-groups).


>[!NOTE]
>
>Puede recuperar los 1000 últimos eventos de experiencia creados hace menos de un año.

Estos son los pasos principales para agregar grupos de campos al origen de datos integrado.

1. En la lista de fuentes de datos, seleccione la fuente de datos integrada de Adobe Experience Platform.

   Se abre el panel de configuración de la fuente de datos en el lado derecho de la pantalla.

   ![](assets/journey23.png)

1. Haga clic en **[!UICONTROL Agregar un nuevo grupo de campos]** para definir una nueva serie de campos que se recuperarán. [Más información](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Seleccione un esquema del **[!UICONTROL Esquema]** lista desplegable. Este campo enumera los esquemas de perfil y eventos de experiencia disponibles en Adobe Experience Platform. La creación del esquema no se realiza en [!DNL Journey Optimizer]. Se realiza en Adobe Experience Platform.
1. Seleccione los campos que desee utilizar.
1. Haga clic en **[!UICONTROL Guardar]**.

Cuando coloque el cursor en el nombre de un grupo de campos, verá dos iconos a la derecha. Permiten eliminar y duplicar el grupo de campos. Tenga en cuenta que **[!UICONTROL Eliminar]** solo está disponible si el grupo de campos no se utiliza en ningún recorrido activo o borrador (la información se muestra en la **[!UICONTROL Se usa en]** ).
