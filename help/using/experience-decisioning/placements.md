---
title: Crear ubicaciones de correo electrónico
description: Obtenga información sobre cómo crear ubicaciones para asociarlas a políticas de decisión en correos electrónicos.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
source-git-commit: 29532b5ebd140f9609a29c1375ceedecf55d0dfb
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 5%

---


# Trabajo con ubicaciones {#create-decision}

## Acerca de las ubicaciones {#about}

Una ubicación es un contenedor que se utiliza para mostrar elementos de decisión. Ayuda a garantizar que el contenido de oferta correcto se muestre en la ubicación correcta dentro del mensaje.

Al agregar una política de decisión a un correo electrónico, debe asociar una ubicación al componente que muestre los elementos de decisión devueltos. Esto le permite, por ejemplo, rastrear el rendimiento de los elementos de decisión en diferentes ubicaciones en la creación de informes.

Se puede acceder a la lista de ubicaciones en el menú **[!UICONTROL Configuración de estrategia]**. Los filtros están disponibles para ayudarle a recuperar ubicaciones según una superficie o etiquetas de canal específicas.

![](assets/placements-list.png)

>[!NOTE]
>
>Por ahora, las ubicaciones solo están disponibles para el canal de correo electrónico.

## Crear una ubicación {#create}

Para crear una ubicación, siga estos pasos:

1. Vaya al menú **[!UICONTROL Configuración de estrategia]**, seleccione **[!UICONTROL Correo electrónico]** y haga clic en el botón **[!UICONTROL Crear ubicación]**.

   También puede crear una ubicación directamente desde el diseñador de correo electrónico al añadir una política de decisión. [Aprenda a asociar una ubicación a un componente de correo electrónico](../experience-decisioning/create-decision.md#save)

1. Defina las propiedades de la ubicación:

   ![](assets/placement-create.png)

   * **[!UICONTROL Nombre]**: El nombre de la ubicación. Asegúrese de definir un nombre significativo para recuperarlo más fácilmente.
   * **[!UICONTROL Descripción]**: Una descripción de la ubicación.
   * **[!UICONTROL Etiquetas]**: asigne etiquetas unificadas de Adobe Experience Platform a la ubicación. Esto le permite clasificarlos fácilmente y mejorar la búsqueda. [Descubra cómo trabajar con campañas](../start/search-filter-categorize.md#tags)
   * **[!UICONTROL Canal]**: Canal para el que se usará la ubicación. Por ahora, las ubicaciones solo están disponibles para correos electrónicos.
   * **[!UICONTROL Configuración de canal]**: asocie una configuración de canal a la ubicación. [Aprenda a configurar canales](../configuration/channel-surfaces.md).

1. Haga clic en **[!UICONTROL Crear]**.

Una vez creada la ubicación, se muestra en la lista de ubicaciones al añadir una política de decisión a un correo electrónico. Puede seleccionarlo para mostrar sus propiedades y editarlo. [Aprenda a crear directivas de decisión](../experience-decisioning/create-decision.md)

![](assets/placement-list.png)
