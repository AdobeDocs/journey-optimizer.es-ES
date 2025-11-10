---
title: Decisiones por lotes
description: Obtenga información sobre cómo enviar decisiones de oferta a todos los perfiles de una audiencia de Adobe Experience Platform determinada.
badge: label="Heredado" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: 810c05b3-2bae-4368-bf12-3ea8c2f31c01
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 5%

---

# Decisiones por lotes {#deliver}

## Introducción a la toma de decisiones por lotes {#start}

Journey Optimizer le permite enviar decisiones de oferta a todos los perfiles de una audiencia determinada de Adobe Experience Platform.

Para ello, debe crear una solicitud de trabajo en Journey Optimizer que contenga información sobre la audiencia de destino y la decisión de oferta que debe utilizar. El contenido de la oferta para cada perfil de la audiencia se coloca entonces en un conjunto de datos de Adobe Experience Platform, donde está disponible para flujos de trabajo por lotes personalizados.

La entrega por lotes también se puede realizar mediante API. Para obtener más información, consulte la [documentación de la API de decisiones por lotes](api-reference/offer-delivery-api/batch-decisioning-api.md).

## Requisitos previos {#prerequisites}

Antes de configurar una solicitud de trabajo, asegúrese de haber creado:

* **Un conjunto de datos** en Adobe Experience Platform. Este conjunto de datos se utilizará para almacenar el resultado de la decisión mediante el esquema &quot;ODE DecisionEvents&quot;. Obtenga más información en la [documentación de conjuntos de datos](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=es).

* **Una audiencia** en Adobe Experience Platform. La audiencia debe evaluarse y luego actualizarse. Aprenda a actualizar la evaluación de pertenencia a audiencias en la [documentación del servicio de segmentación](https://www.adobe.com/go/segmentation-overview-en_es)

  >[!NOTE]
  >
  >Un trabajo por lotes se ejecuta fuera de la instantánea de perfil que se produce una vez al día. La toma de decisiones por lotes limita la frecuencia y siempre carga perfiles de la instantánea más reciente. Espere hasta 24 horas después de crear una audiencia antes de probar la API de decisiones por lotes.

* **Una decisión** en Adobe Journey Optimizer. [Aprenda a crear una decisión](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## Creación de una solicitud de trabajo

Para crear una nueva solicitud de trabajo, siga los pasos a continuación.

1. En el menú **[!UICONTROL Ofertas]**, abra la pestaña **[!UICONTROL Toma de decisiones por lotes]** y haga clic en **[!UICONTROL Crear solicitud]**.

   ![](assets/batch-create.png)

1. Asigne un nombre a la solicitud de trabajo y seleccione el conjunto de datos al que deben enviarse los datos de trabajo.

1. Seleccione la audiencia de Adobe Experience Platform a la que desee dirigirse.

1. Seleccione uno o varios ámbitos de decisión de ofertas que desee utilizar para entregar ofertas a la audiencia:
   1. Seleccione una ubicación de la lista.
   1. Se muestran las decisiones disponibles para la ubicación seleccionada. Seleccione la decisión que desee y haga clic en **[!UICONTROL Agregar]**.
   1. Repita la operación para agregar tantos ámbitos de decisión como desee.

   ![](assets/batch-decision.png)

1. De forma predeterminada, se devuelve una oferta del ámbito de decisión para cada perfil. Puede ajustar el número de ofertas devueltas usando la opción **[!UICONTROL Solicitar oferta por perfil]**. Por ejemplo, si selecciona 2, se mostrarán las dos mejores ofertas para el ámbito de decisión seleccionado.

   >[!NOTE]
   >
   >Puede solicitar hasta 30 ofertas por ámbito de decisión.

1. Si desea incluir el contenido de la oferta en el conjunto de datos, active la opción **[!UICONTROL Incluir contenido]**. Esta opción está deshabilitada de forma predeterminada.

1. Haga clic en **[!UICONTROL Crear]** para ejecutar la solicitud de trabajo.

## Monitorización de trabajos por lotes

Se puede acceder a todos los trabajos por lotes solicitados desde la ficha **[!UICONTROL Toma de decisiones por lotes]**. Además, hay herramientas de búsqueda y filtrado disponibles para ayudarle a refinar la lista.

![](assets/batch-list.png)

### Estados de solicitudes de trabajo

Una vez creada una solicitud de trabajo, el trabajo por lotes pasa por varios estados:

>[!NOTE]
>
>Para asegurarse de que obtiene la información más reciente sobre el estado de una solicitud de trabajo, utilice el botón de puntos suspensivos situado junto al trabajo para actualizarlo.

1. **[!UICONTROL En cola]**: la solicitud de trabajo se ha creado y ha entrado en la cola de procesamiento. Se pueden ejecutar hasta 5 trabajos por lotes a la vez por conjunto de datos. Cualquier otra solicitud por lotes con el mismo conjunto de datos de salida se agrega a la cola. Se selecciona un trabajo en cola para procesarlo una vez que el trabajo anterior ha terminado de ejecutarse.
1. **[!UICONTROL Procesando]**: la solicitud de trabajo se está procesando
1. **[!UICONTROL Ingesta]**: se ha ejecutado la solicitud de trabajo, los datos de resultado se están introduciendo en el conjunto de datos seleccionado,
1. **[!UICONTROL Completada]**: la solicitud de trabajo se ha ejecutado y los datos resultantes ahora se almacenan en el conjunto de datos seleccionado.

   >[!NOTE]
   >
   >Puede acceder al conjunto de datos donde se almacenan los resultados de un trabajo haciendo clic en su nombre en la lista de trabajos.

Si se produce un error mientras se ejecuta la solicitud de trabajo, se obtiene el estado **[!UICONTROL Error]**. Intente duplicar el trabajo por lotes para crear una nueva solicitud. [Aprenda a duplicar un trabajo por lotes](#duplicate)

### Tiempo de procesamiento del trabajo por lotes

El tiempo de extremo a extremo para cada trabajo por lotes es la duración desde el momento en que se crea la carga de trabajo hasta el momento en que el resultado de la decisión está disponible en el conjunto de datos de salida.

El tamaño de la audiencia es el factor principal que afecta al tiempo de decisión por lotes de un extremo a otro. Si la oferta elegible tiene habilitado un límite de frecuencia global, la toma de decisiones por lotes tarda más tiempo en completarse. A continuación se muestran algunas aproximaciones del tiempo de procesamiento de extremo a extremo para sus respectivos tamaños de audiencia, tanto con límite de frecuencia como sin él para las ofertas aptas:

Con el límite de frecuencia habilitado para las ofertas aptas:

| Tamaño de público | Tiempo de procesamiento de extremo a extremo |
|--------------|----------------------------|
| 10 000 perfiles o menos | 7 minutos |
| 1 millón de perfiles o menos | 30 minutos |
| 15 millones de perfiles o menos | 50 minutos |

Sin límite de frecuencia para ofertas aptas:

| Tamaño de público | Tiempo de procesamiento de extremo a extremo |
|--------------|----------------------------|
| 10 000 perfiles o menos | 6 minutos |
| 1 millón de perfiles o menos | 8 minutos |
| 15 millones de perfiles o menos | 16 minutos |

## Duplicación de una solicitud de trabajo {#duplicate}

Puede reutilizar la información de un trabajo existente para crear una nueva solicitud.

Para ello, haga clic en el icono de duplicado, edite la información del trabajo si es necesario y, a continuación, haga clic en **[!UICONTROL Crear]** para crear la nueva solicitud.

![](assets/batch-duplicate.png)
