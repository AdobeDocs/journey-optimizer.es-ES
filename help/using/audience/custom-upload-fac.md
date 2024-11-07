---
solution: Journey Optimizer
product: journey optimizer
title: Carga personalizada (CSV) y composición de audiencia federada
description: Conozca la información clave y las prácticas recomendadas al trabajar con las audiencias de carga personalizada (CSV) y Composición de audiencia federada.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
source-git-commit: 26d311802236a1f9e8f6273c1291bcb54138aad2
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 6%

---

# Carga personalizada (CSV) y composición de audiencia federada {#csv-fac}

## Acerca de la carga personalizada y la composición de audiencia federada {#about}

Además de las definiciones de segmentos y la composición de audiencias, [!DNL Journey Optimizer] le permite generar y segmentar audiencias importándolas desde un archivo CSV o aprovechando los datos del almacén de datos.

* **Carga personalizada**: importe una audiencia con un archivo CSV. Obtenga información sobre cómo importar audiencias en [Documentación del servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}.

* **Composición de audiencias federada**: federe conjuntos de datos directamente desde el almacén de datos existente para crear y enriquecer audiencias y atributos de Adobe Experience Platform en un solo sistema. Lea la guía de [Composición federada de audiencias](https://experienceleague.adobe.com/es/docs/federated-audience-composition/using/home).

  >[!AVAILABILITY]
  >
  >Ahora mismo, la composición de público federado solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

Puede segmentar estas audiencias en Journey Optimizer o activarlas en cualquier destino admitido por Adobe Experience Platform

➡️ [Descubra estas características en vídeo](#video)

## Lectura obligatoria {#must-read}

Esta sección proporciona información clave que se debe tener en cuenta al trabajar con cargas personalizadas (archivos CSV) y audiencias de composición de audiencias federadas.

* **Compatibilidad con vista previa y prueba:** En la actualidad, la vista previa y la prueba no son compatibles con las audiencias creadas mediante la carga de CSV o la composición de audiencias federada. Tenga esto en cuenta al planificar las campañas.

* **Retraso de activación:** las audiencias están listas para usarse en Journey Optimizer justo después de completarse la ingesta. Aunque esto suele ocurrir en menos de una hora, está sujeto a cierta variabilidad.

* **Registros activados y vinculación de identidad:** Todos los registros de la audiencia están activados, incluidos los duplicados. Durante la próxima exportación de perfiles de UPS, estos registros se vincularán con la identidad. Como resultado, el número de registros activados puede diferir del número de perfiles después de la vinculación de identidad.

* **Segmentación de nuevos perfiles:** Cuando no se encuentra una coincidencia entre un registro y un perfil de UPS, se crea un nuevo perfil vacío. Este perfil está vinculado a los atributos de enriquecimiento que se almacenan en el lago de datos. Dado que este nuevo perfil está vacío, los campos de segmentación que se suelen utilizar en Journey Optimizer (por ejemplo, personalEmail.address, mobilePhone.number) están vacíos y, por lo tanto, no se pueden utilizar para la segmentación.

  Para resolver esto, puede especificar el &quot;campo de ejecución&quot; (o la &quot;dirección de ejecución&quot; según el canal) en la configuración del canal como &quot;identityMap&quot;. Esto garantizará que el atributo elegido como identidad en el momento de la creación de la audiencia sea el que se use para la segmentación en Journey Optimizer.

## Vídeotutoriales {#video}

Obtenga información sobre cómo cargar audiencias en formato CSV en Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)

Más información sobre la Composición de audiencias federada.

>[!VIDEO](https://video.tv.adobe.com/v/3432261?quality=12)
