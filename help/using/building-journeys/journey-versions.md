---
solution: Journey Optimizer
product: journey optimizer
title: Versiones de recorridos
description: Obtenga información sobre las versiones de recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8d5ea4c1-bf23-4b58-8654-c251b90c3458
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 3%

---

# Versiones de recorridos{#journey-versions}

En la lista recorrido, todas las versiones de recorrido se muestran con el número de versión. Consulte [esta página](../building-journeys/using-the-journey-designer.md).

Al buscar un recorrido, las versiones más recientes aparecen en la parte superior de la lista la primera vez que se abre la aplicación. A continuación, puede definir la clasificación que desee y la aplicación la mantendrá como una preferencia de usuario. La versión del recorrido también se muestra en la parte superior de la interfaz de edición de recorrido, encima del lienzo.

![](assets/journeyversions1.png)

>[!NOTE]
>
>En la mayoría de los casos, un perfil no puede estar presente varias veces en el mismo recorrido, al mismo tiempo. Si la reentrada está activada, un perfil puede volver a introducir un recorrido, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido. [Más información](../building-journeys/journey-end.md)

Si necesita modificar a un recorrido activo, debe crear una nueva versión del recorrido.

>[!NOTE]
>
>Para obtener más información sobre las limitaciones y protecciones de las versiones de recorrido, consulte [esta página](../start/guardrails.md#journey-versions-limitations)

1. Abra la última versión de su recorrido en directo y haga clic en **[!UICONTROL Crear una nueva versión]** y confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Solo puede crear una versión nueva a partir de la versión más reciente de un recorrido.

1. Realice las modificaciones necesarias, haga clic en **[!UICONTROL Publicación]** y confirme.

   ![](assets/journeyversions3.png)

Desde el momento en que se publique el recorrido, las personas empezarán a fluir a la última versión del recorrido. Las personas que ya han introducido una versión anterior permanecen en ella hasta que finalizan el recorrido. Si más adelante vuelven a entrar en el mismo recorrido, pasarán a la última versión.

Las versiones de recorrido se pueden detener individualmente. Todas las versiones de recorridos tienen el mismo nombre.

>[!NOTE]
>
>Cuando publica una nueva versión de un recorrido, la versión anterior finaliza automáticamente y cambia a la función **Cerrado** estado. No habrá entrada en el recorrido. Aunque detenga la última versión, la versión anterior permanecerá cerrada.
