---
title: Introducción a las campañas
description: Obtenga más información sobre las campañas en [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 8%

---

# Introducción a las campañas {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campañas"
>abstract="Con Campañas, puede entregar contenido de una sola vez a un segmento específico en varios canales. Antes de crear una nueva campaña, asegúrese de que tiene una superficie de canal (es decir, un mensaje preestablecido) y un segmento de Adobe Experience Platform listos para usar."

## Acerca de las campañas {#about}

Las campañas le permiten entregar contenido único a un segmento específico mediante varios canales. A diferencia de los recorridos, donde las acciones están diseñadas para ejecutarse en secuencia, las campañas ejecutan acciones simultáneamente, ya sea inmediatamente o en una programación especificada.

Puede crear dos tipos de campañas:

* **Campañas programadas** permite comunicaciones por lotes ad-hoc sencillas para casos de uso de marketing, como ofertas promocionales, campañas de participación, anuncios, avisos legales o actualizaciones de políticas.
* **Campañas de API activadas** permiten mensajes transaccionales/operativos simples con las API de REST (restablecimiento de contraseña, abandono de tarjeta, etc.), donde la necesidad puede implicar personalización mediante atributos de perfil y datos contextuales de carga útil.

Aprenda a trabajar con campañas:
* [Creación de una campaña](create-campaign.md)
* [Creación de campañas activadas por API](api-triggered-campaigns.md)
* [Modificación o detención de una campaña](modify-stop-campaign.md)
* [Informe en directo de la campaña](campaign-live-report.md)
* [Informe global de la campaña](campaign-global-report.md)

## Acceso a campañas {#access}

Se puede acceder a las campañas desde la **[!UICONTROL Campaigns]** para abrir el Navegador.

De forma predeterminada, la lista muestra todas las campañas con la variable **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]** y **[!UICONTROL Live]** estados. Para mostrar las campañas detenidas, completadas y archivadas, debe borrar el filtro.

![](assets/create-campaign-list.png)

## Estados de campaña {#statuses}

Las campañas pueden tener varios estados:

* **[!UICONTROL Draft]**: La campaña se está editando y no se ha activado.
* **[!UICONTROL Activating]**: La campaña se está activando.
* **[!UICONTROL Live]**: La campaña se ha activado.
* **[!UICONTROL Scheduled]**: La campaña se ha configurado para activarse en una fecha de inicio específica.
* **[!UICONTROL Stopped]**: La campaña se ha detenido manualmente. Ya no puede activarlo ni reutilizarlo (consulte [Detener una campaña](modify-stop-campaign.md#stop))
* **[!UICONTROL Completed]**: La campaña ha finalizado.
* **[!UICONTROL Archived]**: La campaña se ha archivado.

>[!NOTE]
>
>El icono &quot;Abrir versión de borrador&quot; junto a una **[!UICONTROL Live]** o **[!UICONTROL Scheduled]** El estado indica que se ha creado una nueva versión de la campaña y que aún no se ha activado (consulte [Modificación de una campaña](modify-stop-campaign.md#modify)).
