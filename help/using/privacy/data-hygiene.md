---
solution: Journey Optimizer
product: journey optimizer
title: Realizar operaciones de ciclo de vida de datos
description: Aprenda a realizar operaciones de ciclo de vida de datos
feature: Privacy, Monitoring
role: User
level: Intermediate
exl-id: 8045b559-bf5e-4b5f-9da4-accd44641a68
TQID: https://experienceleague.adobe.com/-zue9aNrWtfL3MGs7OjH-1CF436mzPh50fsru8OSEq8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2: id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56id: f365ec33-2b99-4b7f-b4ee-c743dd7f615fid: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d095671a-1355-40aa-8b5f-06c33c68080bid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 100%

---

# Realizar operaciones de ciclo de vida de datos {#data-hygiene}

>[!AVAILABILITY]
>
>Las funcionalidades de ciclo de vida de los datos solo están disponibles para las organizaciones que han adquirido las ofertas sobre el **programa de protección sanitaria** y el **programa de protección de la seguridad y la privacidad**.

A medida que los datos se incorporan continuamente en Adobe Experience Platform, resulta crucial garantizar que los datos se utilicen según lo previsto, que se actualicen cuando sea necesario y que se eliminen según las políticas organizativas.

Estas tareas se pueden realizar utilizando el menú **[!UICONTROL Ciclo de vida de los datos]**, que le permite configurar y programar operaciones de ciclo de vida de datos, asegurándose de que los registros se mantengan correctamente.

![](assets/data-hygiene.png)


## Recomendaciones {#data-hygiene-recommendations}

Al realizar operaciones de higiene de los datos (como eliminar identidades o conjuntos de datos), tenga en cuenta que los eventos de envío históricos asociados a identidades eliminadas ya no aparecen en los informes estándar ni en las consultas de lago de datos. Esto puede generar discrepancias entre el número de correos electrónicos notificados como **Entregados** y el número de correos electrónicos **Recibidos** en las bandejas de entrada de los destinatarios, especialmente para los recorridos más antiguos.

Antes de ejecutar eliminaciones a gran escala, valide y exporte los datos de envío o de creación de informes necesarios. Si es necesario realizar una reconciliación después de la higiene de los datos, coordínese con el servicio de asistencia de Adobe para acceder a los registros archivados o utilizar consultas del conjunto de datos de evento de comentarios sobre mensajes para los datos recientes.

## Más información {#data-hygiene-learn-more}

Para obtener más información sobre Privacy Service y cómo crear y administrar solicitudes de ciclo de vida de datos, consulte la siguiente documentación de Adobe Experience Platform:

* [Información general de Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=es)
* [Ciclo de vida de datos en Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/home.html?lang=es)
