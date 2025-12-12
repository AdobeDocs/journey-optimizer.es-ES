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
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 43%

---

# Introducción a los planes de calentamiento de IP {#ip-warmup-gs}

Con [!DNL Journey Optimizer], puede realizar fácilmente flujos de trabajo de calentamiento de IP directamente desde la interfaz de usuario de una manera estandarizada y eficaz que siga las prácticas recomendadas para una entrega óptima. Cuando se envían correos electrónicos utilizando una plataforma nueva, los proveedores de servicios de Internet (ISP) sospechan de las direcciones IP desconocidas. Si se envían, de repente, grandes volúmenes de correos electrónicos, los ISP suelen marcarlos como correo no deseado.

Para evitar que se considere correo no deseado, puede aumentar progresivamente el volumen enviado mediante la función de plan de calentamiento de IP. Esta nueva opción del menú **[!UICONTROL Administración]** le permite automatizar la administración del volumen y simplificar el proceso de calentamiento sin requerir configuraciones de recorrido complejas.

>[!NOTE]
>
>Antes de implementar su plan de calentamiento de IP, obtenga información acerca de los aspectos básicos de la capacidad de entrega, la creación de reputación y las prácticas recomendadas en esta [guía de calentamiento de IP](ip-warmup-deliverability-guide.md).

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

>[!VIDEO](https://video.tv.adobe.com/v/3432637/?learn=on)

>[!NOTE]
>
>Obtenga más información sobre cómo aumentar su reputación de correo electrónico con el calentamiento de IP en la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=es).

## Recursos adicionales {#additional-resources}

Explore estas útiles publicaciones de blog para obtener instrucciones más detalladas sobre el calentamiento de la IP:

* [Guía de entrega de Adobe Journey Optimizer: de cero reputación a la bandeja de entrada principal](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950): Guía completa que cubre los aspectos básicos de la reputación, los calendarios de calentamiento, la monitorización y las prácticas recomendadas de solución de problemas.

* [Comprender cómo configurar el calentamiento de IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warmup-understanding-how-to-set-up-the-ip-warmup/ba-p/761949): conozca los aspectos básicos de la configuración de planes de calentamiento de IP y las prácticas recomendadas para una implementación exitosa.

* [Funciones avanzadas en planes de calentamiento de IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/advanced-features-in-ajo-ip-warm-up-plans-granular-controls-for/ba-p/761958): descubra funciones avanzadas y controles granulares para optimizar su estrategia de calentamiento de IP.

* [Solución de problemas de calentamiento de IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warm-up-troubleshooting-audience-delays-and-smart-retry/ba-p/761952): encuentre soluciones a problemas comunes, como retrasos de audiencia, y obtenga información acerca de los mecanismos de reintentos inteligentes.
