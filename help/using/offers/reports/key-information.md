---
title: Información clave sobre eventos de Administración de decisiones
description: Obtenga más información sobre la información clave enviada con cada evento de Administración de decisiones.
feature: Ofertas
topic: Integraciones
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 91%

---

# Información clave sobre eventos de Administración de decisiones {#events-key-information}

Cada evento que se envía cuando se toma una decisión contiene cuatro puntos de datos clave que puede aprovechar para realizar análisis e informes.

![](../../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: Nombre e ID de la oferta de reserva si no se ha seleccionado ninguna oferta personalizada,
* **[!UICONTROL Placement]**: Nombre, ID y canal de la ubicación utilizada para entregar la oferta,
* **[!UICONTROL Selections]**: Nombre e ID de la oferta seleccionada para el perfil,
* **[!UICONTROL Activity]**: Nombre e ID de la decisión (anteriormente conocida como actividad de oferta).

Además, también puede aprovechar los campos **[!UICONTROL identityMap]** y **[!UICONTROL Timestamp]** para recuperar información sobre el perfil y la hora a la que se entregó la oferta.

Para obtener más información sobre todos los campos XDM que se envían con cada decisión, consulte [esta sección](xdm-fields.md).
