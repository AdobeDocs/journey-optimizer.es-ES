---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los planes de calentamiento de IP
description: Obtenga información sobre cómo implementar un plan de calentamiento de IP
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, entregabilidad
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: 5e0d683bf52df4992773c6147b9e418241777e5d
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 73%

---

# Introducción a los planes de calentamiento de IP {#ip-warmup-gs}

Con [!DNL Journey Optimizer], puede realizar fácilmente flujos de trabajo de calentamiento de IP directamente desde la interfaz de usuario de una manera estandarizada y eficaz que siga las prácticas recomendadas para una entrega óptima. Cuando se envían correos electrónicos utilizando una plataforma nueva, los proveedores de servicios de Internet (ISP) sospechan de las direcciones IP desconocidas. Si se envían, de repente, grandes volúmenes de correos electrónicos, los ISP suelen marcarlos como correo no deseado.

Para evitar que se considere correo no deseado, puede aumentar progresivamente el volumen enviado mediante la función de plan de calentamiento de IP. Esta nueva opción del menú **[!UICONTROL Administración]** le permite hacerlo más fácilmente de una manera consolidada en lugar de crear recorridos diarios complejos.

➡️ [Aprenda a crear y ejecutar un plan de calentamiento de IP en este vídeo](#video)

>[!AVAILABILITY]
>
>Esta capacidad solo se puede habilitar en entornos limitados de tipo de producción.

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

Los pasos clave para implementar un plan de calentamiento de IP son los siguientes:

1. Primero, debe crear una o más campañas con la opción Calentamiento de IP habilitada. [Más información](ip-warmup-campaign.md)

1. Cree un plan de calentamiento de IP en [!DNL Journey Optimizer] y cargue la hoja de Excel preparada con la ayuda del consultor del equipo de entrega. [Más información](ip-warmup-plan.md)

1. Seleccione una campaña para cada fase del plan y active las ejecuciones correspondientes. [Más información](ip-warmup-execution.md)

## Vídeo explicativo {#video}

Obtenga información sobre cómo crear y ejecutar un plan de calentamiento de IP.

>[!VIDEO](https://video.tv.adobe.com/v/3453843/?captions=spa&learn=on)

>[!NOTE]
>
>Obtenga más información sobre cómo aumentar su reputación de correo electrónico con el calentamiento de IP en la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=es).
