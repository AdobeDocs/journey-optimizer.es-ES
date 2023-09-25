---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los planes de calentamiento de IP
description: Obtenga información sobre cómo implementar un plan de calentamiento de IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, capacidad de entrega
hide: true
hidefromtoc: true
source-git-commit: b3e5a825b881736516b3bcd1d368843c3a601100
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 26%

---

# Introducción a los planes de calentamiento de IP {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* **[Introducción al calentamiento de IP](ip-warmup-gs.md)**
* [Creación de campañas de calentamiento de IP](ip-warmup-campaign.md)
* [Crear un plan de calentamiento de IP](ip-warmup-plan.md)
* [Ejecución del plan de calentamiento de IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Actualmente, la función de calentamiento de IP está disponible como una versión beta únicamente para usuarios seleccionados. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.

Con [!DNL Journey Optimizer], puede realizar fácilmente flujos de trabajo de calentamiento de IP directamente desde la interfaz de usuario de una manera estandarizada y eficaz que siga las prácticas recomendadas para una entrega óptima.

>[!CAUTION]
>
>Esta función solo se aplica al canal de correo electrónico.

Cuando se envían correos electrónicos utilizando una plataforma nueva, los proveedores de servicios de Internet (ISP) sospechan de las direcciones IP desconocidas. Si se envían, de repente, grandes volúmenes de correos electrónicos, los ISP suelen marcarlos como correo no deseado.

Para evitar que se lo considere correo no deseado, puede aumentar progresivamente el volumen enviado mediante la función de plan de calentamiento de IP. Esta nueva opción de la **[!UICONTROL Administration]** El menú le permite hacerlo más fácilmente de una manera consolidada en lugar de crear recorridos diarios complejos. Esto debería garantizar un desarrollo uniforme de la fase de inicio y permitir reducir la velocidad total de direcciones no válidas.

>[!NOTE]
>
>Obtenga más información sobre cómo aumentar su reputación de correo electrónico con el calentamiento de IP en [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

Los pasos clave para implementar un plan de calentamiento de IP son los siguientes:

1. Primero debe crear una o más campañas con la opción Calentamiento de IP habilitada. [Más información](ip-warmup-campaign.md)

1. Creación de un plan de calentamiento de IP en [!DNL Journey Optimizer] y cargue la hoja de Excel preparada con la ayuda del consultor del equipo de entrega. [Más información](ip-warmup-plan.md)

1. Seleccione una campaña para cada fase del plan y active las ejecuciones correspondientes. [Más información](ip-warmup-execution.md)
