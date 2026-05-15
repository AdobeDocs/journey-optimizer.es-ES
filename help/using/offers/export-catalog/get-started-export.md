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
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
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
