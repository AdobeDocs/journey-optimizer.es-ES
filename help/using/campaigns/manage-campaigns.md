---
solution: Journey Optimizer
product: journey optimizer
title: Acceso y administración de campañas
description: Obtenga información sobre cómo acceder y administrar sus campañas en Journey Optimizer.
feature: Campaigns
topic: Content Management
role: User
mini-toc-levels: 1
level: Beginner
keywords: administrar campañas, estado, programación, acceso, optimizador
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '1707'
ht-degree: 14%

---

# Acceso y administración de campañas {#manage-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Inventario de campañas orquestadas"
>abstract="En esta pantalla, puede acceder a la lista completa de campañas orquestadas, comprobar su estado actual, las fechas de la última/próxima ejecución y crear una nueva campaña orquestada."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Acción"
>abstract="Esta sección enumera todas las acciones utilizadas dentro de la campaña orquestada."

Se puede acceder a las campañas desde el menú **[!UICONTROL Campañas]**. Utilice las fichas para examinar las campañas por tipo: **Campañas de acción**, **campañas activadas por API** y **orquestadas**. Más información sobre los [tipos de campañas](get-started-with-campaigns.md#get-started-with-campaigns). Los tipos disponibles dependen del acuerdo de licencia y de los permisos.

>[!BEGINTABS]

>[!TAB Campañas de acción]

Seleccione la pestaña **[!UICONTROL Action]** para acceder a la lista de campañas de acción.

De manera predeterminada, la lista muestra todas las campañas con los estados **[!UICONTROL Borrador]**, **[!UICONTROL Programado]** y **[!UICONTROL Activo]**. Para mostrar las campañas detenidas, completadas y archivadas, debe borrar el filtro.

![](assets/create-campaign-list.png)

>[!TAB Campañas activadas mediante API]

Seleccione la pestaña **[!UICONTROL API activada]** para acceder a la lista de campañas activadas por API.

De manera predeterminada, la lista muestra todas las campañas con los estados **[!UICONTROL Borrador]**, **[!UICONTROL Programado]** y **[!UICONTROL Activo]**. Para mostrar las campañas detenidas, completadas y archivadas, debe borrar el filtro.

![](assets/api-triggered-list.png)

>[!TAB Campañas orquestadas]

Seleccione la pestaña **[!UICONTROL Orchestration]** para acceder a la lista de campañas orquestadas.

![imagen que muestra el inventario de campañas orquestadas](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

Cada campaña orquestada de la lista muestra información como el [estado](#status) actual de la campaña, el canal asociado y las etiquetas, o la última vez que se modificó. Puede personalizar las columnas mostradas haciendo clic en el botón ![Configurar diseño](assets/do-not-localize/inventory-configure-layout.svg).

>[!ENDTABS]

Además, hay una barra de búsqueda y filtros disponibles para facilitar la búsqueda dentro de la lista. Por ejemplo, puede filtrar las campañas para mostrar solo las asociadas a un canal o etiqueta determinados, o las creadas durante un intervalo de fechas específico.

El botón ![Imagen que muestra el botón Más acciones](assets/do-not-localize/rule-builder-icon-more.svg) en el inventario de campañas le permite realizar varias operaciones detalladas a continuación.

![imagen que muestra el inventario de campañas](assets/inventory-actions.png)

* **[!UICONTROL Ver informe de todos los tiempos]** / **[!UICONTROL Ver informe de las últimas 24 horas]**: acceda a informes para medir y visualizar el impacto y el rendimiento de sus campañas. Más información sobre [informes de campaña](../reports/campaign-global-report-cja.md).
* **[!UICONTROL Editar etiquetas]**: edite las etiquetas asociadas a la campaña. Aprenda a [usar etiquetas en sus campañas](../start/search-filter-categorize.md#add-tags-to-an-object)
* **[!UICONTROL Duplicate]**: utilice esta opción para duplicar una campaña, por ejemplo, para ejecutar una campaña orquestada que se haya detenido. [Más información](#duplicate-a-campaign)
* **[!UICONTROL Eliminar]** - Utilice esta opción para eliminar una campaña. [Más información](#delete-a-campaign)
* **[!UICONTROL Archivar]**: archive la campaña. Todas las campañas archivadas se eliminan según una programación móvil 30 días después de su última fecha de modificación. Esta acción está disponible para todas las campañas excepto para **[!UICONTROL Borrador]**. Más información sobre [archivo de campaña](#archive-a-campaign).

Para las campañas activadas por acciones y API, están disponibles las siguientes acciones adicionales:

* **[!UICONTROL Agregar al paquete]**: agregue la campaña a un paquete para exportarla a otra zona protegida. Obtenga información sobre cómo [exportar objetos a otra zona protegida](../configuration/copy-objects-to-sandbox.md)
* **[!UICONTROL Abrir versión de borrador]**: si se ha creado una nueva versión de la campaña y aún no se ha activado, puede acceder a su versión de borrador mediante esta acción.

## Ciclo de vida de Campaign {#statuses}

En Adobe Journey Optimizer, cada campaña se desplaza por un ciclo de vida que se refleja en su estado en la interfaz. Los estados disponibles varían según el tipo de campaña: Acción, Activado por API u Organizado. Utilice las pestañas siguientes para explorar el ciclo de vida y los estados específicos de cada tipo de campaña.

>[!BEGINTABS]

>[!TAB Campañas de acción]

* **[!UICONTROL Borrador]**: la campaña se está editando y no se ha activado.
* **[!UICONTROL Programada]**: la campaña está configurada para activarse en una fecha de inicio específica.
* **[!UICONTROL Activo]**: la campaña se ha activado.
* **[!UICONTROL En revisión]**: la campaña se ha enviado para su aprobación con el fin de publicarse. [Aprenda a trabajar con aprobaciones](../test-approve/gs-approval.md)
* **[!UICONTROL Detenida]**: la campaña se detuvo manualmente. Ya no puede activarlo ni reutilizarlo. [Aprenda a detener una campaña](manage-campaigns.md#stop)
* **[!UICONTROL Completada]**: la campaña se ha completado. Este estado se asigna automáticamente 3 días después de activar una campaña o en la fecha de finalización de la campaña si tiene una ejecución recurrente.
* **[!UICONTROL Error]**: Error en la ejecución de la campaña. Compruebe los registros para identificar el problema.
* **[!UICONTROL Archivada]**: se archivó la campaña. [Aprenda a archivar campañas](manage-campaigns.md#archive)

>[!NOTE]
>
>El icono &quot;Abrir versión de borrador&quot; junto a un estado **[!UICONTROL Activo]** o **[!UICONTROL Programado]** indica que se ha creado una nueva versión de una campaña activada por una acción o API y que aún no se ha activado.

>[!TAB Campañas activadas mediante API]

* **[!UICONTROL Borrador]**: la campaña se está editando y no se ha activado.
* **[!UICONTROL Programada]**: la campaña está configurada para activarse en una fecha de inicio específica.
* **[!UICONTROL Activo]**: la campaña se ha activado.
* **[!UICONTROL En revisión]**: la campaña se ha enviado para su aprobación con el fin de publicarse. [Aprenda a trabajar con aprobaciones](../test-approve/gs-approval.md)
* **[!UICONTROL Detenida]**: la campaña se detuvo manualmente. Ya no puede activarlo ni reutilizarlo. [Aprenda a detener una campaña](manage-campaigns.md#stop)
* **[!UICONTROL Completada]**: la campaña se ha completado. Este estado se asigna automáticamente 3 días después de activar una campaña o en la fecha de finalización de la campaña si tiene una ejecución recurrente.
* **[!UICONTROL Error]**: Error en la ejecución de la campaña. Compruebe los registros para identificar el problema.
* **[!UICONTROL Archivada]**: se archivó la campaña. [Aprenda a archivar campañas](manage-campaigns.md#archive)

>[!NOTE]
>
>El icono &quot;Abrir versión de borrador&quot; junto a un estado **[!UICONTROL Activo]** o **[!UICONTROL Programado]** indica que se ha creado una nueva versión de una campaña activada por una acción o API y que aún no se ha activado.

>[!TAB Campañas orquestadas]

* **[!UICONTROL Borrador]**: se ha creado la campaña orquestada. Aún no se ha publicado.
* **[!UICONTROL Publicación]**: La campaña orquestada se está publicando.
* **[!UICONTROL Activo]**: la campaña orquestada se ha publicado y se está ejecutando.
* **[!UICONTROL Programado]**: La ejecución de la campaña orquestada se ha programado.
* **[!UICONTROL Completada]**: la ejecución de la campaña orquestada ha finalizado. El estado Completado se asigna automáticamente hasta tres días después de que una campaña haya completado el envío de mensajes sin errores.
* **[!UICONTROL Cerrado]**: este estado se muestra cuando se ha cerrado una campaña recurrente. La campaña continúa su ejecución hasta que se hayan completado todas sus actividades, pero no pueden entrar más perfiles en la campaña.
* **[!UICONTROL Archivada]**: se archivó la campaña orquestada. Todas las campañas archivadas se eliminarán en una reprogramación escalonada 30 días después de la última fecha de modificación. Puede duplicar una campaña archivada si es necesario para seguir trabajando en ella.
* **[!UICONTROL Detenido]**: la ejecución de la campaña orquestada se ha detenido. Para volver a iniciar la campaña, debe duplicarla.

>[!ENDTABS]

Cuando se produce un error en una de las campañas, aparece un icono de advertencia junto al estado de la campaña. Haga clic en ella para mostrar información sobre la alerta. Estas alertas pueden producirse en varias situaciones, como cuando el mensaje de la campaña no se ha publicado o si la configuración elegida es incorrecta.

![](assets/campaign-alerts.png)

## Calendario de campañas {#calendar}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_view"
>title="Vistas de lista y calendario de campañas"
>abstract="Además de la lista de campañas, [!DNL Journey Optimizer] proporciona una vista de calendario de sus campañas, lo que ofrece una representación visual clara de sus programaciones. Puede cambiar entre las vistas de lista y calendario en cualquier momento con estos botones."

Además de la lista de campañas, [!DNL Journey Optimizer] proporciona una vista de calendario de sus campañas, lo que ofrece una representación visual clara de sus programaciones.

Representación de las campañas:

* De forma predeterminada, la cuadrícula del calendario muestra todas las campañas en directo y programadas de la semana seleccionada. Las opciones de filtro adicionales pueden mostrar activaciones o activaciones completadas, detenidas y finalizadas de un tipo o canal determinado.
* No se muestran los borradores de campañas.
* Las campañas que abarcan varios días aparecen en la parte superior de la cuadrícula del calendario.
* Si no se especifica ninguna hora de inicio, se utiliza la hora de activación manual más cercana para colocarla en el calendario.
* Las campañas se muestran como intervalos de tiempo de 1 hora, pero esto no refleja la hora de envío o finalización real.

Para navegar en el calendario de campañas:

1. Haga clic en el icono ![calendario](assets/do-not-localize/Smock_Calendar_18_N.svg) para acceder a su calendario de campañas.

1. Utilice los botones de flecha o el selector de fecha situado encima del calendario para desplazarse entre semanas.

   El calendario muestra todas las campañas programadas para la semana actual.

   ![vista de calendario que muestra campañas en vivo](assets/campaigns-timeline.png)

1. Haga clic en el icono ![engranaje](assets/do-not-localize/Smock_Gears_18_N.png) para alternar la visualización de elementos que abarcan varios días o semanas.

   ![vista de calendario que muestra campañas en vivo](assets/campaign-long-term.png)

1. Haga clic en el icono ![agregar calendario](assets/do-not-localize/Smock_CalendarAdd_18_N.svg) para administrar y agregar hasta tres calendarios externos.

   ![vista de calendario que muestra calendarios externos](assets/campaign-external-calendar.png)

1. Arrastre y suelte los archivos CSV que contienen nombres de evento, fechas de inicio y fechas de finalización.

   Los eventos cargados aparecen para todos los usuarios de la organización y se muestran en los calendarios de Recorrido y de campaña.

   +++El formato CSV debe ser el siguiente:

   | Columna1 | Columna2 | Columna3 |
   |-|-|-|
   | Nombre del evento | Fecha de inicio en formato mm/dd/aa | Fecha de finalización en formato mm/dd/aa |

   +++

1. Si es necesario, puede ocultar, mostrar o quitar los calendarios externos agregados.

   ![vista de calendario que muestra calendarios externos](assets/campaign-manage-calendar.png)

1. Para obtener más información sobre una campaña, haga clic en su bloque visual para abrir los detalles. Se abrirá un panel de información con información diversa sobre la campaña, como su tipo, el acceso a los informes o las etiquetas asignadas.

   ![lista de campañas con el panel de información abierto](assets/campaign-rail.png)

## Modificación y detención de campañas de acción recurrentes {#modify}

### Modificación de una campaña de acción

Para modificar y crear una nueva versión de una campaña de acción recurrente, siga estos pasos:

1. Abra la campaña Acción y haga clic en el botón **[!UICONTROL Modificar campaña]**.

1. Se crea una nueva versión de la campaña. Para comprobar la versión activa, haga clic en **[!UICONTROL Abrir versión activa]**.

   ![](assets/create-campaign-draft.png)

   En la lista de campañas, las campañas activadas con una versión de borrador en curso se mostrarán con un icono específico en la columna **[!UICONTROL Estado]**. Haga clic en este icono para abrir la versión de borrador de la campaña.

   ![](assets/create-campaign-edit-list.png)

1. Una vez que los cambios estén listos, puede activar la nueva versión de la campaña (consulte [Revisar y activar una campaña](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >Al activar el borrador, se reemplazará la versión activa de la campaña.

### Detener una campaña de acción {#stop}

Para detener una campaña recurrente, ábrala y haga clic en el botón **[!UICONTROL Detener campaña]**.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Al detener una campaña, no se detiene un envío en curso, sino que se detiene un envío programado o las siguientes ocurrencias si el envío ya está en curso.

## Archivado de una campaña {#archive}

Con el tiempo, la lista de campañas sigue creciendo y, finalmente, dificulta la exploración de campañas completadas y detenidas.

Para evitarlo, puede archivar las campañas completadas y detenidas que ya no necesite. Para ello, haga clic en el botón de los tres puntos y seleccione **[!UICONTROL Archivo]**.

![](assets/create-campaign-archive.png)

Las campañas archivadas se pueden recuperar utilizando el filtro dedicado de la lista.


## Eliminación de una campaña {#delete}

Para eliminar una campaña, usa los puntos suspensivos ![la imagen que muestra el botón Más acciones](assets/do-not-localize/rule-builder-icon-more.svg) y selecciona **[!UICONTROL Eliminar]**.

![](assets/delete-a-campaign.png){width="70%" align="left"}

>[!IMPORTANT]
>
>Esta opción solo está disponible para **[!UICONTROL Borrador]** campañas.


## Duplicación de una campaña {#duplicate}

Para duplicar una campaña, por ejemplo, si se ha detenido, use los puntos suspensivos ![imagen que muestra el botón Más acciones](assets/do-not-localize/rule-builder-icon-more.svg) y seleccione **[!UICONTROL Duplicar]**.

Introduzca el nombre de la campaña y confirme.

La campaña se crea y se añade a la lista de campañas.
