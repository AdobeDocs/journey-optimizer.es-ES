---
solution: Journey Optimizer
product: journey optimizer
title: Realizar operaciones del ciclo vital de datos
description: Obtenga información sobre cómo realizar operaciones del ciclo vital de datos
feature: Privacy, Monitoring
role: User
level: Intermediate
exl-id: 8045b559-bf5e-4b5f-9da4-accd44641a68
TQID: https://experienceleague.adobe.com/-zue9aNrWtfL3MGs7OjH-1CF436mzPh50fsru8OSEq8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 0%

---

# Realizar operaciones del ciclo vital de datos {#data-hygiene}

>[!AVAILABILITY]
>
>Actualmente, las funciones del ciclo vital de datos solo están disponibles para las organizaciones que han adquirido las ofertas adicionales de **Healthcare Shield** y **Privacy and Security Shield**.

A medida que los datos se incorporan continuamente en Adobe Experience Platform, es crucial asegurarse de que los datos se utilizan según lo previsto, se actualizan cuando es necesario y se eliminan por directivas de la organización.

Estas tareas se pueden realizar utilizando el menú **[!UICONTROL Ciclo de vida de los datos]**, que le permite configurar y programar operaciones del ciclo de vida de los datos, asegurándose de que los registros se mantengan correctamente.

![](assets/data-hygiene.png)


## Recommendations {#data-hygiene-recommendations}

Al realizar operaciones de higiene de los datos (como eliminar identidades o conjuntos de datos), tenga en cuenta que los eventos de envío históricos asociados con identidades eliminadas ya no aparecerán en los informes estándar ni en las consultas de lago de datos. Esto puede generar discrepancias entre el número de correos electrónicos reportados como **Entregados** y el número de correos electrónicos **Recibidos** en las bandejas de entrada de los destinatarios, especialmente para los recorridos más antiguos.

Antes de ejecutar eliminaciones a gran escala, valide y exporte los datos de envío o de creación de informes necesarios. Si se necesita reconciliación después de la higiene de los datos, debe coordinarse con el soporte de Adobe para acceder a los registros archivados o utilizar las consultas del conjunto de datos de evento de comentarios de mensajes para los datos recientes.

## Más información {#data-hygiene-learn-more}

Para obtener más información sobre Privacy Service y cómo realizar operaciones del ciclo vital de datos, consulte la documentación de Adobe Experience Platform:

* [Información general de Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)
* [Ciclo de vida de datos en Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/home.html)
