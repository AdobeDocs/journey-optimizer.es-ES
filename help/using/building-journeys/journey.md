---
solution: Journey Optimizer
product: journey optimizer
title: Principio general
description: Principio general
feature: Journeys
topic: Content Management
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: ca423c25d39162838368b2242c1aff99388df768
workflow-type: tm+mt
source-wordcount: '1253'
ht-degree: 9%

---

# Principio general{#jo-general-principle}

[!DNL Journey Optimizer] permiten crear casos de uso de orquestación en tiempo real aprovechando los datos contextuales almacenados en eventos o fuentes de datos.

Diseñe escenarios avanzados de varios pasos con las siguientes capacidades:

* Enviar en tiempo real **envío unitario** se activa cuando se recibe un evento, o **en lote** uso de segmentos de Adobe Experience Platform.

* Aprovechar **datos contextuales** desde eventos, información de Adobe Experience Platform o datos de servicios API de terceros.

* Utilice la variable **acciones integradas** para enviar mensajes diseñados en [!DNL Journey Optimizer] o crear **acciones personalizadas** si utiliza un sistema de terceros para enviar mensajes.

* Con la variable **diseñador de recorridos**, cree sus casos de uso de varios pasos: arrastre y suelte fácilmente un evento de entrada o una actividad de segmento de lectura, agregue condiciones y envíe mensajes personalizados.

## Ciclo de vida del recorrido{#journey-lifecyle}

### Perfiles en recorridos{#profile-journey}

En un recorrido unitario:

* Si la reentrada está activada, un perfil puede introducir un recorrido varias veces, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido.

* Si la reentrada está desactivada, un perfil no puede introducir varias veces el mismo recorrido

Para obtener más información sobre la reentrada de perfiles, consulte esta [sección](../building-journeys/journey-gs.md#change-properties).

En un recorrido de segmento de lectura:

* Para recorridos no recurrentes: el perfil se introduce una vez y solo una vez en el recorrido.
* para recorridos recurrentes: el perfil introduce el recorrido en cada recurrencia, si se encuentra en el estado esperado o del segmento. Si todavía estaba en el recorrido por una recurrencia anterior, lo reiniciará desde el principio.

En los recorridos de evento empresarial que comienzan con un segmento de lectura :

Sabiendo que este recorrido se basa en la recepción de un evento empresarial, si el perfil está cualificado en el segmento esperado, introducirá el recorrido para cada evento comercial recibido, lo que significa que este perfil puede estar varias veces en el mismo recorrido, al mismo tiempo, pero en el contexto de diferentes eventos comerciales.

Los recorridos unitarios (comenzando por un evento o una calificación de segmento) incluyen una protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante 5 minutos. Por ejemplo, si un evento déclencheur un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.


### final de recorrido{#journey-ending}

Un recorrido puede finalizar para un individuo en dos contextos específicos:

* La persona llega a la última actividad de una ruta.
* La persona llega a un **Condición** actividad (o **Espera** actividad con una condición) y no coincide con ninguna de las condiciones.

La persona puede volver a entrar en el recorrido si se permite la reentrada. Consulte [esta página](../building-journeys/journey-gs.md#change-properties)

Para finalizar un recorrido activo, le recomendamos que lo cierre. La llegada de nuevos clientes al recorrido será bloqueada. Los clientes que ya han entrado en el recorrido pueden experimentarlo hasta el final. Consulte [esta sección](../building-journeys/.md#close-journey)

Puede detener un recorrido solo si se ha producido una emergencia y todo el procesamiento debe finalizar inmediatamente en un recorrido. A las personas que ya entraron en un recorrido se les detiene el progreso. Consulte [esta sección](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Tenga en cuenta que no puede reanudar un recorrido cerrado o detenido.

#### Recorrido final{#end-tag}

Durante la creación de un recorrido, se muestra una &quot;etiqueta final&quot; al final de cada ruta. Un usuario no puede agregar este nodo, no se puede eliminar y solo se puede cambiar su etiqueta. Marca el final de cada ruta del recorrido. Si el recorrido tiene varias rutas, le recomendamos que agregue una etiqueta a cada extremo para facilitar la lectura de los informes. Consulte [esta página](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

#### Cierre de un recorrido{#close-journey}

Un recorrido puede cerrarse por los siguientes motivos:

* El recorrido se cierra manualmente mediante la variable **[!UICONTROL Cerca de nuevas entradas]** botón.
* Un recorrido basado en segmentos de una toma que ha terminado de ejecutarse.
* Después de la última aparición de un recorrido basado en segmentos recurrentes.

Al cerrar un recorrido manualmente, se garantiza que los clientes que ya hayan entrado en el recorrido puedan finalizar su ruta, pero que los nuevos usuarios no puedan entrar en el recorrido. Cuando se cierra un recorrido (por cualquiera de los motivos anteriores), aparece el estado **[!UICONTROL Cerrado]**. El recorrido deja de permitir que entren nuevos individuos en el recorrido. Las personas que ya están en el recorrido pueden terminar el recorrido normalmente. Después del tiempo de espera global predeterminado de 30 días, el recorrido cambiará a la variable **Finalizado** estado. Consulte esta [sección](../building-journeys/journey-gs.md#global_timeout).

No se puede reiniciar ni eliminar una versión de recorrido cerrada. Puede crear una nueva versión o duplicarla. Solo se pueden eliminar los recorridos finalizados.

Para cerrar un recorrido de la lista de recorridos, haga clic en el botón **[!UICONTROL Elipsis]** botón situado a la derecha del nombre del recorrido y seleccione **[!UICONTROL Cerca de nuevas entradas]**.

![](assets/journey-finish-quick-action.png)

También puede:

1. En el **[!UICONTROL Recorridos]** , haga clic en el recorrido que desee cerrar.
1. En la parte superior derecha, haga clic en la flecha hacia abajo.

   ![](assets/finish_drop_down_list.png)

1. Haga clic en **[!UICONTROL Cerca de nuevas entradas]** y confirme en el cuadro de diálogo.

#### Detener un recorrido{#stop-journey}

En caso de que necesite detener el progreso de todas las personas en el recorrido, puede detenerlo. Al detener el recorrido, se agotará el tiempo de espera de todas las personas del recorrido. Sin embargo, detener un recorrido implica que a las personas que ya entraron en un recorrido se les detiene en su progreso. Básicamente el recorrido está apagado. Si desea poner fin a un recorrido, le recomendamos que lo cierre.

No se puede reiniciar una versión de recorrido detenida.

Cuando se detiene, el estado del recorrido se establece en **[!UICONTROL Detenido]**.

Puede detener un recorrido, por ejemplo, si un especialista en marketing se da cuenta de que el recorrido está dirigido a una audiencia incorrecta o si una acción personalizada que supuestamente debe enviar mensajes no funciona correctamente. Para detener un recorrido de la lista de recorridos, haga clic en el botón **[!UICONTROL Elipsis]** botón situado a la derecha del nombre del recorrido y seleccione **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

También puede:

1. En el **[!UICONTROL Recorridos]** , haga clic en el recorrido que desee detener.
1. En la parte superior derecha, haga clic en la flecha abajo.
   ![](assets/finish_drop_down_list.png)
1. Haga clic en **[!UICONTROL Stop]** y confirme en el cuadro de diálogo.



## Versiones de recorridos{#journey-versions}

En la lista recorrido, todas las versiones de recorrido se muestran con el número de versión. Consulte [esta página](../building-journeys/using-the-journey-designer.md).

Al buscar un recorrido, las versiones más recientes aparecen en la parte superior de la lista la primera vez que se abre la aplicación. A continuación, puede definir la clasificación que desee y la aplicación la mantendrá como una preferencia de usuario. La versión del recorrido también se muestra en la parte superior de la interfaz de edición de recorrido, encima del lienzo.

![](assets/journeyversions1.png)

>[!NOTE]
>
>En la mayoría de los casos, un perfil no puede estar presente varias veces en el mismo recorrido, al mismo tiempo. Si la reentrada está activada, un perfil puede volver a introducir un recorrido, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido. [Más información](#journey-ending)

Si necesita modificar a un recorrido activo, cree una nueva versión de su recorrido.

1. Abra la última versión de su recorrido en directo y haga clic en **[!UICONTROL Crear una nueva versión]** y confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Solo puede crear una versión nueva a partir de la versión más reciente de un recorrido.

1. Realice las modificaciones necesarias, haga clic en **[!UICONTROL Publicación]** y confirme.

   ![](assets/journeyversions3.png)

Desde el momento en que se publique el recorrido, las personas empezarán a fluir a la última versión del recorrido. Las personas que ya han introducido una versión anterior permanecen en ella hasta que finalizan el recorrido. Si más adelante vuelven a entrar en el mismo recorrido, pasarán a la última versión.

Las versiones de recorrido se pueden detener individualmente. Todas las versiones de recorridos tienen el mismo nombre.

Cuando publica una nueva versión de un recorrido, la versión anterior finaliza automáticamente y cambia a la función **Cerrado** estado. No puede pasar ninguna entrada en el recorrido. Aunque detenga la última versión, la versión anterior permanecerá cerrada.

>[!NOTE]
>
>Obtenga más información sobre las versiones de recorrido, barreras y limitaciones, en [esta página](../start/guardrails.md#journey-versions-limitations)