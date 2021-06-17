---
title: Información general sobre el uso compartido de los pasos del recorrido
description: Información general sobre el uso compartido de los pasos del recorrido
feature: Informes
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: 233b97784843adb26cb37a612feeaf2a8e396f27
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 7%

---

# Creación de informes de recorrido{#design-jo-reports}

Además de [informes en tiempo real](live-report.md) y [funciones integradas de informes globales](global-report.md), [!DNL Journey Optimizer] puede enviar automáticamente datos de rendimiento del recorrido a Adobe Experience Platform para que se puedan combinar con otros datos con fines de análisis.

>[!NOTE]
>
>Esta función está activada de forma predeterminada en todas las instancias para eventos de pasos de recorrido. Para los eventos de paso del perfil de recorrido, la activación se realiza previa solicitud. Los esquemas y conjuntos de datos creados durante el aprovisionamiento de esta función no deben cambiarse.

Por ejemplo, ha configurado un recorrido que envía varios correos electrónicos. Esta capacidad le permite combinar datos de [!DNL Journey Optimizer] con datos de evento descendente como cuántas conversiones se produjeron, cuánta participación se produjo en el sitio web o cuántas transacciones se produjeron en la tienda. La información del recorrido se puede combinar con los datos de Adobe Experience Platform, ya sea de otras propiedades digitales o de propiedades sin conexión, para ofrecer una vista más completa del rendimiento.

[!DNL Journey Optimizer] crea automáticamente los esquemas y transmisiones necesarios en conjuntos de datos a Adobe Experience Platform para cada paso que un individuo realiza en un recorrido. Un evento de paso corresponde a un individuo que se mueve de un nodo a otro en un recorrido. Por ejemplo, en un recorrido que tiene un evento, una condición y una acción, se envían tres eventos a Adobe Experience Platform.

La lista de campos XDM que se pasan es completa. Algunos contienen códigos generados por el sistema y otros tienen nombres descriptivos legibles. Algunos ejemplos son la etiqueta de la actividad de recorrido o el estado del paso: cuántas veces se agotó el tiempo de espera de una acción o finalizó con un error.

>[!CAUTION]
>
>Los conjuntos de datos no se pueden activar para el servicio de perfil en tiempo real. Asegúrese de que la opción **[!UICONTROL Profile]** está desactivada.

Recorrido envía los datos a medida que se producen de forma continua. Puede consultar estos datos mediante el servicio de consulta. Puede conectarse a Customer Journey Analytics u otras herramientas de BI para ver los datos relacionados con estos pasos.

Se crean los siguientes esquemas:

* Esquema de evento de perfil de paso de recorrido para [!DNL Journey Orchestration]: eventos de experiencia para los pasos realizados en un Recorrido junto con un mapa de identidad que se utilizará para la asignación a un participante de Recorrido individual.
* Esquema de evento de paso de recorrido para [!DNL Journey Orchestration]: evento de paso de Recorrido vinculado a metadatos de Recorrido.
* Esquema de recorrido con campos de Recorrido para [!DNL Journey Orchestration] - Metadatos de Recorrido para describir Recorridos.

![](../assets/sharing1.png)

![](../assets/sharing2.png)

Se pasan los siguientes conjuntos de datos:

* Esquema de evento de perfil de paso de recorrido para [!DNL Journey Orchestration]
* Eventos de los pasos del recorrido
* Recorridos

![](../assets/sharing3.png)

Las listas de campos XDM pasados a Adobe Experience Platform se detallan aquí:

* [Campos comunes de los eventos de los journeyStep](../reports/sharing-common-fields.md)
* [Campos de ejecución de la acción eventos de los journeyStep](../reports/sharing-execution-fields.md)
* [Campos de captura de datos de eventos del journeyStep](../reports/sharing-fetch-fields.md)
* [Campos de identidad de los eventos de los journeyStep](../reports/sharing-identity-fields.md)
* [campos del recorrido](../reports/sharing-journey-fields.md)

Para obtener más información sobre los informes de eventos de paso a Adobe Experience Platform, vea este [tutorial en vídeo](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/reporting-step-events-to-adobe-experience-platform.html).
