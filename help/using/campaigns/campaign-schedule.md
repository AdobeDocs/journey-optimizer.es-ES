---
solution: Journey Optimizer
product: journey optimizer
title: Programación de la campaña de acción
description: Obtenga información sobre cómo programar la campaña de acción.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: crear, optimizador, campaña, superficie, mensajes
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Programación de la campaña de acción {#action-campaign-schedule}

Use la ficha **[!UICONTROL Programación]** para definir la programación de la campaña.

De forma predeterminada, las campañas de acción se inician una vez que se activan manualmente y finalizan en cuanto se envía el mensaje una vez. Si no desea ejecutar la campaña justo después de su activación, puede especificar una fecha y una hora a las que se debe enviar el mensaje mediante la opción **[!UICONTROL Inicio de campaña]**.

La opción **[!UICONTROL Fin de campaña]** le permite especificar cuándo debe dejar de ejecutarse una campaña. Fuera de las fechas especificadas, la campaña no se ejecuta.

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>Al programar campañas en [!DNL Adobe Journey Optimizer], asegúrese de que la fecha y la hora de inicio se ajusten a la primera entrega deseada. En el caso de las campañas recurrentes, si ya ha pasado la hora programada inicial, las campañas se transferirán a la siguiente franja horaria disponible según sus reglas de periodicidad.

Hay opciones de programación adicionales disponibles en función del canal de campaña:

* **Frecuencia** (correo electrónico, SMS, acción push)

  Puede definir una frecuencia con la que se debe enviar el mensaje de la campaña. Para ello, usa las opciones **[!UICONTROL déclencheur de acción]** en la pantalla de creación de campañas para especificar si la campaña se debe ejecutar diaria, semanal o mensualmente.

* **Activación del plan de calentamiento de IP** (Correo electrónico)

  Para las campañas de correo electrónico, puede crear campañas de activación de planes de calentamiento de IP específicas. La programación de campaña se basa en el plan de calentamiento de IP con el que está asociado, lo que significa que la programación ya no está definida en la propia campaña. [Aprenda a crear campañas de calentamiento de IP](../configuration/ip-warmup-campaign.md).

## Pasos siguientes {#next}

Una vez que la programación de la campaña esté lista, puede revisarla y activarla. [Más información](review-activate-campaign.md)
