---
title: Fuente de datos de Adobe Experience Platform
description: Obtenga información sobre cómo configurar la fuente de datos de Adobe Experience Platform
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: bd35bf2ec4c1b2898007d670fc20626f06cc3750
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 11%

---

# Fuente de datos de Adobe Experience Platform {#adobe-experience-platform-data-source}

La fuente de datos de Adobe Experience Platform define la conexión con el servicio Perfil del cliente en tiempo real. Esta fuente de datos está integrada y preconfigurada. No se puede eliminar. Esta fuente de datos está diseñada para recuperar y utilizar datos del servicio Perfil del cliente en tiempo real (por ejemplo, comprobar si la persona que ha introducido un recorrido es una mujer). Permite utilizar datos de perfil y datos de eventos de experiencia. Para obtener más información sobre el servicio Perfil del cliente en tiempo real, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target=&quot;_blank&quot;}.

>[!NOTE]
>
>Puede recuperar los 1000 últimos eventos de experiencia creados hace menos de un año.

Para permitir la conexión con el servicio de Perfil del cliente en tiempo real, debemos utilizar una clave para identificar a una persona y un área de nombres que contextualice la clave. Como resultado, solo puede utilizar esta fuente de datos si sus recorridos empiezan por un evento que contenga una clave y un área de nombres. Consulte [esta página](../building-journeys/journey.md).

Puede editar el grupo de campos preconfigurado llamado &quot;ProfileFieldGroup&quot;, agregar nuevos y eliminar los que no se usan en borradores o recorridos activos. Consulte [esta página](../datasource/configure-data-sources.md#define-field-groups).

Estos son los pasos principales para agregar grupos de campos al origen de datos integrado.

1. En la lista de fuentes de datos, seleccione la fuente de datos integrada de Adobe Experience Platform.

   Se abre el panel de configuración de la fuente de datos en el lado derecho de la pantalla.

   ![](assets/journey23.png)

1. Haga clic en **[!UICONTROL Add a New Field Group]** para definir una nueva serie de campos que se recuperarán. Consulte [esta página](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Seleccione un esquema del **[!UICONTROL Schema]** lista desplegable. Este campo enumera los esquemas de perfil y eventos de experiencia disponibles en Adobe Experience Platform. La creación del esquema no se realiza en [!DNL Journey Optimizer]. Se realiza en Adobe Experience Platform.
1. Seleccione los campos que desee utilizar.
1. Haga clic en **[!UICONTROL Save]**.

Cuando coloque el cursor en el nombre de un grupo de campos, verá dos iconos a la derecha. Permiten eliminar y duplicar el grupo de campos. Tenga en cuenta que **[!UICONTROL Delete]** solo está disponible si el grupo de campos no se utiliza en ningún recorrido activo o borrador (la información se muestra en la **[!UICONTROL Used in]** ).
