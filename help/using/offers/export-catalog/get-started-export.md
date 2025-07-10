---
title: Introducción a la exportación del catálogo de ofertas
description: Obtenga información sobre cómo exportar el catálogo de ofertas como un conjunto de datos
badge: label="Heredado" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: f30abea1-b204-4470-9836-75fae916bbb1
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: ht
source-wordcount: '115'
ht-degree: 100%

---

# Introducción a la exportación del catálogo de ofertas {#export-catalog}

Journey Optimizer le permite exportar automáticamente el catálogo de ofertas a Adobe Experience Platform.

La exportación crea un conjunto de datos para cada objeto de la Biblioteca de ofertas (consulte [Acceso a conjuntos de datos exportados](../export-catalog/access-dataset.md)). Incluye:

* Ofertas personalizadas
* Ofertas de reserva
* Ubicaciones
* Decisiones

Cada vez que se modifica uno de estos objetos en la Biblioteca de ofertas, se ejecuta automáticamente un nuevo trabajo de exportación para actualizar los conjuntos de datos.

>[!NOTE]
>
>Esta función está habilitada de forma predeterminada. Puede empezar a utilizarla sin ningún paso de activación adicional. Una vez activados, los trabajos de exportación se automatizarán y no requerirán ninguna acción por su parte.

<!--
>[!NOTE]
>
>This feature is not enabled by default. If you want to use it, reach out to your Adobe contact to have it activated for your catalog. Once it is enabled, export jobs will be automated and will require no action from your side.
-->
