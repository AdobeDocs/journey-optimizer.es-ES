---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de los cambios de segmentación de tiempo de vida (TTL) y de flujo continuo
description: Cambios en la segmentación por streaming y tiempo de vida en Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: plataforma, lago de datos, crear, lago, conjuntos de datos, perfil
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: ccb4cc944271fb197e7aee87f57b51c28cb3565f
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 13%

---

# Cambios en la segmentación por streaming y tiempo de vida {#ttl-guardrail}

## Actualizaciones de segmentación de streaming {#segmentation-update}

A partir del 1 de noviembre de 2024, la segmentación de streaming ya no admitirá el uso de eventos de envío y apertura derivados del seguimiento y los comentarios de los conjuntos de datos de Journey Optimizer. Este cambio se aplicará a todas las zonas protegidas y organizaciones de clientes. Encontrará información sobre por qué se desaconsejó esta práctica en el pasado [aquí](../audience/about-audiences.md#streaming-segmentation-events-guardrails).

**Preguntas más frecuentes**

+++ ¿Afectarán estos cambios al uso de clics u otros eventos de seguimiento?

Este cambio solo afecta al uso de los eventos de envío y apertura; los clics y otros eventos de seguimiento se pueden seguir utilizando en un segmento de flujo continuo.

+++

+++ ¿Se verá afectada la segmentación por lotes por este cambio?

Este cambio solo afecta a la segmentación de flujo continuo; los eventos de envío y apertura se pueden seguir utilizando en un segmento por lotes. Si se utilizan en un segmento de flujo continuo, se evaluarán por lotes.

+++

+++ ¿Afectará este cambio a la recopilación de datos de seguimiento?

Este cambio no afecta a la recopilación de datos de seguimiento. Enviar y abrir eventos se seguirán recopilando.

+++

+++ ¿Se ven afectados los eventos de reacción por este cambio?

Los eventos de reacción en Recorridos no se ven afectados por este cambio.

+++

+++ ¿Este cambio se aplicará solo a las zonas protegidas de producción o también a las de desarrollo?

Este cambio se aplicará a todos los tipos de zonas protegidas.

+++

+++ ¿Los eventos de comentarios resultantes del evento de envío también se ven afectados por el cambio?

Este cambio también se aplica a los eventos de exclusión y a los eventos de devolución/retraso resultantes del envío.

+++

## Actualización del tiempo de vida por fases (TTL) {#ttl}

A partir de febrero de 2025, se implementará una protección de tiempo de vida (TTL) en los conjuntos de datos generados por el sistema de Journey Optimizer en **nuevos entornos limitados y nuevas organizaciones** de la siguiente manera:

* 90 días para los datos en el almacén de perfiles
* 13 meses para los datos en el lago de datos

Este cambio se implementará en **zonas protegidas de clientes existentes** en una fase posterior.

**Preguntas más frecuentes**

+++ ¿Este cambio se aplicará solo a las zonas protegidas de producción o también a las de desarrollo?

Este cambio se aplicará a todos los tipos de zonas protegidas.

+++

+++ Para el TTL de 90 días en el almacén de perfiles, ¿se ven afectados los propios perfiles?

Los datos del conjunto de datos generados por el sistema en el perfil se pierden pasados 90 días, no los propios perfiles.

+++

+++ Si se insertan datos de un conjunto de datos generado por el sistema en Customer Journey Analytics (CJA), ¿los datos de CJA también se verán afectados por el TTL?

Los datos de CJA se mantienen sincronizados con el Experience Platform. Por lo tanto, la eliminación de datos debido a un TTL en los datos del conjunto de datos generados por el sistema también afectará a los datos en CJA.

+++
