---
solution: Journey Optimizer
product: journey optimizer
title: Información general sobre el uso compartido de los pasos del recorrido
description: Información general sobre el uso compartido de los pasos del recorrido
feature: Journeys, Reporting
topic: Content Management
role: Engineer, Admin
level: Experienced
exl-id: 29d6b881-35a3-4c62-9e7d-d0aeb206ea77
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 3%

---

# Creación de informes de recorrido {#design-jo-reports}

Además de los [informes en tiempo real](live-report.md) y las [capacidades de generación de informes](report-gs-cja.md) integradas, [!DNL Journey Optimizer] puede enviar automáticamente datos de rendimiento de recorrido a Adobe Experience Platform para que se puedan combinar con otros datos con fines de análisis.

>[!NOTE]
>
>Esta función se activa de forma predeterminada en todas las instancias para eventos de pasos de recorrido. No se pueden modificar ni actualizar los esquemas y conjuntos de datos que se han creado durante el aprovisionamiento para eventos de paso. De forma predeterminada, estos esquemas y conjuntos de datos están en modo de solo lectura.

Por ejemplo, ha configurado un recorrido que envía varios correos electrónicos. Esta capacidad le permite combinar datos de [!DNL Journey Optimizer] con datos de eventos descendentes, como cuántas conversiones se produjeron, cuánta participación se produjo en el sitio web o cuántas transacciones se produjeron en el almacén. La información de recorrido se puede combinar con los datos de Adobe Experience Platform, ya sea desde otras propiedades digitales o desde propiedades sin conexión para proporcionar una vista más completa del rendimiento.

[!DNL Journey Optimizer] crea automáticamente los esquemas y flujos necesarios en conjuntos de datos a Adobe Experience Platform para cada paso que realice un individuo en un recorrido. Un evento de paso corresponde a un individuo que se mueve de un nodo a otro en un recorrido. Por ejemplo, en un recorrido que tiene un evento, una condición y una acción, se envían tres eventos de paso a Adobe Experience Platform.

>[!NOTE]
>
>Además de los eventos de paso a nivel de perfil, el sistema también genera eventos internos para las actividades **Leer audiencia**. Estos eventos, denominados `segmentExportJob` eventos, registran el ciclo de vida del nodo Leer audiencia (como la creación de trabajos de exportación, la puesta en cola, la finalización y los errores) y se generan por actividad Leer audiencia, no por perfil individual. Como resultado, es posible que estos eventos no tengan un identificador de perfil asociado (UPMID). Estos eventos internos son útiles para supervisar y solucionar problemas del rendimiento de la audiencia de lectura y se pueden consultar utilizando los campos documentados en la [sección serviceEvents](../reports/sharing-field-list.md#servicevents-field). Para obtener ejemplos de consultas sobre cómo trabajar con eventos segmentExportJob, consulte [Consultas relacionadas con la audiencia de lectura](../reports/query-examples.md#read-segment-queries).

Hay casos en los que se pueden crear varios eventos para el mismo nodo. Por ejemplo, en el caso de la actividad Wait:

* Se genera un evento cuando el perfil introduce la espera (el atributo journeyNodeProcessed es igual a false)
* Se genera un evento cuando el perfil lo abandona (el atributo journeyNodeProcessed es igual a true)

La lista de campos XDM que se pasan es completa. Algunos contienen códigos generados por el sistema y otros tienen nombres descriptivos en lenguaje natural. Algunos ejemplos son la etiqueta de la actividad de recorrido o el estado del paso: cuántas veces se ha superado el tiempo de espera de una acción o ha finalizado en error.

>[!CAUTION]
>
>Los conjuntos de datos no se pueden activar para el servicio de perfil en tiempo real. Asegúrese de que la opción **[!UICONTROL Perfil]** esté desactivada.

[!DNL Journey Optimizer] envía datos a medida que se producen, en flujo continuo. Puede consultar estos datos mediante el servicio de consultas. Puede conectarse a Customer Journey Analytics u otras herramientas de BI para ver los datos relacionados con estos pasos.

Se crean los siguientes esquemas:

* Esquema de evento de paso de recorrido para [!DNL Journey Orchestration]: evento de paso de Recorrido vinculado a metadatos de Recorrido.
* Esquema de recorrido con campos de Recorrido para [!DNL Journey Orchestration]: metadatos de Recorrido para describir Recorridos.

![](assets/sharing1.png)

![](assets/sharing2.png)

Se pasan los siguientes conjuntos de datos:

* Eventos de paso de recorrido
* Recorridos

![](assets/sharing3.png)

Las listas de campos XDM pasados a Adobe Experience Platform se detallan aquí:

* [Lista de campos de eventos de paso](../reports/sharing-field-list.md)
* [Campos de eventos de paso heredados](../reports/sharing-legacy-fields.md)

## Integración con Customer Journey Analytics {#integration-cja}

[!DNL Journey Optimizer] eventos de paso se pueden vincular a otros conjuntos de datos en [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=es){target="_blank"}.

El flujo de trabajo general es:

* [!DNL Customer Journey Analytics] ingiere el conjunto de datos &quot;Evento de paso de Recorrido&quot;.
* El campo **profileID** del &quot;esquema de evento de paso de Recorrido para Journey Orchestration&quot; asociado se define como un campo de identidad. En [!DNL Customer Journey Analytics], puede vincular este conjunto de datos a cualquier otro conjunto de datos que tenga el mismo valor que el identificador basado en personas.
* Para usar este conjunto de datos en [!DNL Customer Journey Analytics], para el análisis de recorrido entre canales, consulte [Documentación de Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html?lang=es){target="_blank"}.

➡️ [Trabajar con Customer Journey Analytics](cja-ajo.md){target="_blank"}
