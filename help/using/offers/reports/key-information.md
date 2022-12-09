---
title: Información clave sobre eventos de gestión de decisiones
description: Obtenga más información sobre la información clave enviada con cada evento de Administración de decisiones.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 07be59e8-e994-4854-8089-25614d005dbe
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Información clave sobre eventos de gestión de decisiones {#events-key-information}

Cada evento que se envía cuando se toma una decisión contiene cuatro puntos de datos clave que puede aprovechar para realizar análisis e informes.

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: Nombre e ID de la oferta de reserva, si no se ha seleccionado ninguna oferta personalizada,
* **[!UICONTROL Placement]**: Nombre, ID y canal de la colocación utilizada para entregar la oferta,
* **[!UICONTROL Selections]**: Nombre e ID de la oferta seleccionada para el perfil,
* **[!UICONTROL Activity]**: Nombre e ID de la decisión.

Además, también puede aprovechar el **[!UICONTROL identityMap]** y **[!UICONTROL Timestamp]** para recuperar información sobre el perfil y la hora a la que se entregó la oferta.

Para obtener más información sobre todos los campos XDM que se envían con cada decisión, consulte [esta sección](xdm-fields.md).
