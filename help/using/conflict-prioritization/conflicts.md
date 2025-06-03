---
title: Identificar posibles conflictos en recorridos y campañas
description: Aprenda a identificar conflictos potenciales en recorridos y campañas.
role: User
level: Beginner
exl-id: efbb5ac4-4c07-4c62-9460-39eb4fed129a
source-git-commit: 6da1d9a3edb8a30b8f13fd0cb6a138f22459ad00
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 16%

---

# Detección de posibles conflictos en recorridos y campañas {#conflict}

A medida que los especialistas en marketing aumentan el volumen de campañas y Recorridos en Journey Optimizer, se hace cada vez más difícil para un experto en marketing saber si está bombardeando a sus clientes con demasiadas interacciones de marketing. por lo tanto, es esencial identificar fácilmente cuándo hay campañas y recorridos superpuestos para garantizar que logren el equilibrio adecuado en las comunicaciones de marketing y, al mismo tiempo, mitigar el riesgo de fatiga de los clientes.

Las áreas clave para monitorizar la posible superposición son las siguientes:

* **Cronología** (fechas de inicio y finalización): ¿se están ejecutando demasiados recorridos simultáneamente?
* **Audiencia**: ¿Qué porcentaje de mi audiencia de recorrido también es parte de otros recorridos?
* **Canal**: ¿Hay otras comunicaciones programadas para el mismo periodo de tiempo y, si es así, cuántas?
* **Conjunto de reglas de límite**: ¿Qué tipos de recorridos limito y hay superposición dentro de ellos?
* **Configuración del canal**: ¿Hay otros recorridos o campañas que usan alguna configuración de canal que se esté usando en el mismo recorrido o campaña y que podrían impedir que el recorrido o la campaña se muestre al usuario final?

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Cómo detecta Journey Optimizer los conflictos {#detection}

A continuación se muestra un resumen de cómo Journey Optimizer identifica posibles conflictos para recorridos y campañas:

* **Ámbito de identificación de conflictos**: los conflictos solo se muestran para campañas y recorridos en directo o programados.
* **recorridos unitarios**: si el recorrido seleccionado es unitario, se muestran otros recorridos que comienzan con el mismo evento, ya que este evento almacenará en déclencheur todos estos recorridos.
* **recorridos de calificación de audiencias y lectura de audiencias o eventos empresariales**: si el recorrido seleccionado es una calificación de audiencias o un recorrido de lectura de audiencias o eventos empresariales, se mostrarán todos los demás recorridos del mismo tipo con una audiencia válida, ya que puede haber superposiciones entre las audiencias.
* **Campañas**: dado que todas las campañas están dirigidas a audiencias y no hay concepto de eventos, todas las campañas pueden entrar en conflicto con recorridos activados por segmentos (a partir de una actividad Leer audiencia).
* **Campañas en vivo/programadas**: Las campañas en vivo y programadas pueden entrar en conflicto entre sí debido a una posible superposición de audiencias. Para cualquier campaña determinada, todas las campañas en directo o programadas se muestran en el visor de conflictos.

## Ver conflictos identificados para un recorrido o una campaña determinados {#view}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Ver posibles conflictos"
>abstract="Compruebe siempre que haya una posibilidad de superposición con otras campañas. Los conflictos solo se muestran para campañas en directo y programadas. Tenga en cuenta que el botón estará disponible en cuanto asigne cualquiera de las siguientes opciones de configuración: **[!UICONTROL Fecha de inicio/finalización]**, **[!UICONTROL Público]**, **[!UICONTROL Canal]**, **[!UICONTROL Configuración de canal]** y **[!UICONTROL Conjunto de reglas]**."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Ver posibles conflictos"
>abstract="Compruebe siempre que exista la posibilidad de superposición con otros recorridos. Los conflictos solo se muestran para recorridos activos y programados. Tenga en cuenta que el botón estará disponible en cuanto asigne cualquiera de las siguientes opciones de configuración: **[!UICONTROL Fecha de inicio/finalización]**, **[!UICONTROL Público]**, **[!UICONTROL Canal]**, **[!UICONTROL Configuración de canal]** y **[!UICONTROL Conjunto de reglas]**."

Al crear un recorrido o una campaña, Journey Optimizer le permite comprobar si existe la posibilidad de superposición con otros recorridos o campañas. Para ello, siga estos pasos:

1. En el momento de crear un recorrido o una campaña, haga clic en el botón **[!UICONTROL Ver conflictos potenciales]** en las propiedades del recorrido o de la campaña.

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >El botón **[!UICONTROL Ver conflictos potenciales]** está disponible para su selección en cuanto se asigne cualquiera de las siguientes opciones de configuración: **[!UICONTROL Fecha de inicio/finalización]**, **[!UICONTROL Audiencia]**, **[!UICONTROL Canal]**, **[!UICONTROL Configuración de canal]** y **[!UICONTROL Conjunto de reglas]**. Asegúrese de seleccionar **[!UICONTROL Guardar]** después de asignar esta configuración, ya que el botón no se podrá seleccionar hasta que se guarden los cambios.

1. Se abre la ventana **[!UICONTROL Potential conflicts]**, que le permite visualizar todos los elementos que se superponen con el recorrido o la campaña actual.

   Puede abrir un recorrido o una campaña superpuestos directamente desde esta pantalla seleccionando su nombre.

   ![](assets/potential-conflicts.png)

   >[!NOTE]
   >
   >Debido a que el almacenamiento en caché ha implementado, es posible que las campañas y los recorridos publicados recientemente tarden entre tres y siete minutos en mostrarse en el visor de conflictos.

Para restringir aún más la búsqueda de posibles superposiciones, puede filtrar la lista de campañas y recorridos en función de los campos que sean relevantes. Para ello, seleccione el icono de filtro en la vista de inventario. [Aprenda a trabajar con filtros](../start/search-filter-categorize.md#filter-lists)

## Resolver conflictos {#resolve}

A continuación se ofrecen algunas sugerencias para reducir los conflictos potenciales una vez identificados:

* Ajuste las **fechas de inicio y finalización** para evitar campañas o recorridos superpuestos.
* Restrinja **la segmentación de audiencia** para minimizar la superposición entre recorridos.
* Implemente **límites de frecuencia** para evitar que los clientes reciban demasiadas comunicaciones.
* Reduzca la cantidad de **recorridos activos** para administrar la experiencia del cliente de manera más efectiva.
* Establezca **prioridades** en las acciones entrantes para asegurarse de que se muestre la acción más importante a los clientes.

Al aprovechar estas capacidades, puede asegurarse de que los esfuerzos de marketing estén alineados y de que mantiene el equilibrio adecuado en su estrategia de comunicaciones.

## Vídeo práctico {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435528?quality=12)
