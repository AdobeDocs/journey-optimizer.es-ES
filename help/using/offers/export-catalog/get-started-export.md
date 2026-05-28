---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Introducción a la exportación del catálogo de ofertas
description: Obtenga información sobre cómo exportar el catálogo de ofertas como un conjunto de datos
badge: label="Heredado" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: f30abea1-b204-4470-9836-75fae916bbb1
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/71W86v7R-wgsa7JDTE3d6Lddc71MOcTxrY5l0Ts600o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 133
ht-degree: 100%

---

# Introducción a la exportación del catálogo de ofertas {#export-catalog}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../experience-decisioning/gs-experience-decisioning.md)

Journey Optimizer le permite exportar automáticamente el catálogo de ofertas a Adobe Experience Platform.

La exportación crea un conjunto de datos para cada objeto de la Biblioteca de ofertas (consulte [Acceso a conjuntos de datos exportados](../export-catalog/access-dataset.md)). Incluye:

* Ofertas personalizadas
* Ofertas de reserva
* Ubicaciones
* Decisiones

Cada vez que se modifica uno de estos objetos en la Biblioteca de ofertas, se ejecuta automáticamente un nuevo trabajo de exportación para actualizar los conjuntos de datos.

>[!NOTE]
>
>Esta función está habilitada de forma predeterminada. Puede empezar a utilizarla sin ningún paso de activación adicional. Una vez habilitados, los trabajos de exportación se automatizarán y no requerirán ninguna acción por su parte.

<!--
>[!NOTE]
>
>This feature is not enabled by default. If you want to use it, reach out to your Adobe contact to have it activated for your catalog. Once it is enabled, export jobs will be automated and will require no action from your side.
-->
