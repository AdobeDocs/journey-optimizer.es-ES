---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de los protecciones de tiempo de vida (TTL) de los conjuntos de datos
description: Protecciones de tiempo de vida de conjuntos de datos en  [!DNL Adobe Journey Optimizer]
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: plataforma, lago de datos, crear, lago, conjuntos de datos, perfil
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: d4729294a007a348e0233aa8a75bbe3b2999742a
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 15%

---

# Protecciones de tiempo de vida (TTL) de conjuntos de datos {#ttl-guardrail}

A partir de febrero de 2025, se implementará gradualmente un mecanismo de protección de tiempo de vida (TTL) en los conjuntos de datos generados por el sistema de Journey Optimizer en las **nuevas zonas protegidas y organizaciones** de la siguiente manera:

* 90 días para los datos en el almacén de perfiles,
* 13 meses para los datos en el lago de datos.

Este cambio se está implementando en **zonas protegidas de clientes existentes** en una fase posterior.

## Conjuntos de datos afectados {#datasets}

La siguiente tabla enumera todos los conjuntos de datos afectados y su respectivo tiempo de vida en el lago de datos y el almacén de perfiles.

| Conjunto de datos | TTL de lago de datos | TTL de almacenamiento de perfiles |
|------|-----|-----|
| Conjunto de datos de evento de comentarios de mensajes AJO | 13 meses | 90 días |
| Conjunto de datos de evento de experiencia de seguimiento de correo electrónico AJO | 13 meses | 90 días |
| Conjunto de datos de evento de experiencia de seguimiento push de AJO | 13 meses | 90 días |
| Conjunto de datos de entidad AJO | 13 meses | 90 días |
| Conjunto de datos de AJO Surfaces | 13 meses | n/a |
| Conjunto de datos de evento de actividad entrante de AJO | 13 meses | 90 días |
| Conjunto de datos de clasificación AJO | 13 meses | n/a |
| Conjunto de datos de evento de comentarios CCO de correo electrónico de AJO | 13 meses | n/a |
| Conjunto de datos de evento de entidad | 13 meses | n/a |
| Recorridos | 13 meses | n/a |
| Eventos de paso de recorrido | 13 meses | n/a |
| Repositorio de objetos de decisión: ofertas personalizadas | 13 meses | n/a |
| Repositorio de objetos de decisión: ofertas de reserva | 13 meses | n/a |
| Repositorio de objetos de decisión: ubicaciones | 13 meses | n/a |
| Repositorio de objetos de decisión: actividades | 13 meses | n/a |
| Repositorio de objetos de Experience Decisioning: elementos de oferta personalizados | 13 meses | n/a |
| ODE DecisionEvents: toma de decisiones de producción | 13 meses | n/a |

## Preguntas frecuentes {#faq}

A continuación, encontrará las preguntas más frecuentes sobre los conjuntos de datos y el tiempo de vida (TTL).

¿Necesita más detalles? Usa las opciones de comentarios de la parte inferior de esta página para plantear tu pregunta o conectar con la [comunidad de Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=es){target="_blank"}.

+++¿Este cambio se aplicará solo a las zonas protegidas de producción o también a las de desarrollo?

Este cambio se aplicará a todos los tipos de zonas protegidas.

+++

+++Para el TTL de 90 días en el almacén de perfiles, ¿se ven afectados los propios perfiles?

Los datos del conjunto de datos generados por el sistema en el perfil se pierden pasados 90 días, no los propios perfiles.

+++

+++Si se insertan datos de un conjunto de datos generado por el sistema en [!DNL Customer Journey Analytics] (CJA), ¿los datos de CJA también se verán afectados por el TTL?

Los datos de [!DNL Customer Journey Analytics] se mantienen sincronizados con Experience Platform. Por lo tanto, la eliminación de datos debido a un TTL en los datos del conjunto de datos generados por el sistema también afectará a los datos de [!DNL Customer Journey Analytics].

+++

+++ ¿Pueden los clientes aumentar el TTL para [!DNL Journey Optimizer] datos del conjunto de datos del sistema en el almacén de perfiles? 

Actualmente no se admiten extensiones TTL. Sin embargo, se ha planificado trabajar para optimizar el proceso de TTL a fin de permitir estas solicitudes de extensión en algún momento a partir del segundo semestre de 2025.

>[!NOTE]
>
>Los datos almacenados en el perfil están sujetos al derecho Volumen total de datos. Por lo tanto, cualquier aumento del almacenamiento de datos en el perfil como resultado de una extensión TTL se contaría con el derecho Volumen de datos total. [Más información](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html?lang=es){target=_blank}

+++

+++¿Pueden los clientes aumentar el TTL para los datos del conjunto de datos del sistema [!DNL Journey Optimizer] en el lago de datos? 

Actualmente no se admiten extensiones TTL. Los clientes pueden exportar datos a través de Destinos para conservar los datos durante más tiempo. [Más información](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=es){target=_blank}. Además, los clientes con un derecho de **[!DNL Data Distiller]** pueden crear conjuntos de datos derivados para almacenar los datos en el lago de datos sin un TTL. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=_blank}

+++

+++¿Se verán afectadas las siguientes capacidades por los TTL? 

* **Almacén de búsquedas**: No
* **Límite de Recorrido**: No
* **Límite de oferta**: No
* **Optimización del tiempo de envío (STO)**: No
* **Límite de frecuencia de mensaje** (es decir, Reglas de negocio): No
* **Informes**: No

  >[!NOTE]
  >
  >Ya se ha implementado un TTL en la conexión [!DNL Customer Journey Analytics] (CJA), lo que reduce el período máximo efectivo de retrospectiva de datos del conjunto de datos afectado a 13 meses.

* **Fuente de datos de Experience Platform**: no aplicable: la recuperación de eventos de experiencia no se admite mediante fuentes de datos.
* **Atributos calculados**: Sí - El cálculo de relleno inicial se limitará a los últimos 90 días de datos; el atributo calculado se actualizará en función de los eventos incrementales para las actualizaciones posteriores. Tan pronto como las actualizaciones posteriores llegan al período retrospectivo (máximo de 6 meses), el TTL ya no afecta al atributo calculado. Más información.
* **Segmentación y retargeting**: sí: la segmentación depende de los datos del almacén de perfiles; por lo tanto, la retrospectiva está limitada a 90 días en los datos del conjunto de datos afectado.
* **Seguimiento**: sí: reduce el período máximo efectivo de retrospectiva de datos del conjunto de datos afectado a 90 días. Los datos de los conjuntos de datos afectados residen durante 13 meses en el lago de datos.

+++

+++¿Qué marca de tiempo se utiliza para la aplicación de TTL (por ejemplo, para casos de uso de relleno)? 

Se utiliza la marca de tiempo del evento (es decir, no la fecha de ingesta).

+++

+++¿Puedo eliminar conjuntos de datos generados por el sistema de Journey Optimizer?

Los conjuntos de datos generados por el sistema de Journey Optimizer están protegidos y no se pueden eliminar a través de la IU estándar de Adobe Experience Platform. Estos conjuntos de datos son esenciales para la funcionalidad de Journey Optimizer y los administra el sistema.

Si necesita quitar permanentemente un conjunto de datos del sistema de Journey Optimizer (por ejemplo, para entornos de control de calidad, limpieza de zonas protegidas o requisitos específicos de higiene de los datos), póngase en contacto con el departamento de ingeniería de Adobe o con el Servicio de atención al cliente de Adobe. Estos conjuntos de datos requieren procedimientos backend especializados para garantizar una eliminación completa y segura.

>[!NOTE]
>
>Para la limpieza rutinaria de datos dentro de estos conjuntos de datos del sistema, use las operaciones de **[!UICONTROL Ciclo de vida de datos]** disponibles a través de Privacy Service para eliminar registros o identidades específicos. [Más información](../privacy/data-hygiene.md)

+++
