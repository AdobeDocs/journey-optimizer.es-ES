---
solution: Journey Optimizer
product: journey optimizer
title: Creación de su primer recorrido
description: Pasos clave para crear su primer recorrido con Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, primero, inicio, inicio rápido, audiencia, evento, acción
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 23%

---

# Creación de su primer recorrido{#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Creación de recorridos"
>abstract="Utilice **Adobe Journey Optimizer** para crear casos de uso de orquestación en tiempo real aprovechando los datos contextuales almacenados en eventos o fuentes de datos."


## Requisitos previos{#start-prerequisites}

Para enviar mensajes con recorridos, se requieren las siguientes configuraciones:

1. **Configuración de un evento**: si desea almacenar en déclencheur las recorridos de forma unitaria cuando se recibe un evento, debe configurar un evento. Usted define la información esperada y cómo procesarla. Este paso lo realiza un **usuario técnico**. [Más información](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Crear una audiencia**: el recorrido también puede escuchar a las audiencias de Adobe Experience Platform para enviar mensajes en lote a un conjunto especificado de perfiles. Para ello, debe crear audiencias. [Más información](../audience/about-audiences.md).

   ![](assets/segment2.png)

1. **Configuración de la fuente de datos**: puede definir una conexión a un sistema para recuperar información adicional que se utilizará en los recorridos, por ejemplo, en las condiciones. También se configura una fuente de datos integrada de Adobe Experience Platform en el momento del aprovisionamiento. Este paso no es necesario si solo se aprovechan los datos de los eventos durante el recorrido. Este paso lo realiza un **usuario técnico**. [Más información](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configuración de una acción**: Si utiliza un sistema de terceros para enviar mensajes, puede crear una acción personalizada. Obtenga más información en esta [sección](../action/action.md). Este paso lo realiza un **usuario técnico**. Si utiliza las funciones de mensajes integradas de Journey Optimizer, solo necesita añadir una acción de canal al recorrido y diseñar el contenido.

   ![](assets/custom2.png)

## Acceso a recorridos {#journey-access}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Recorridos"
>abstract="Diseñar recorridos de clientes para ofrecer experiencias personalizadas y contextuales. Journey Optimizer permite crear casos prácticos de orquestación en tiempo real con información contextual almacenada en eventos o fuentes de datos. La pestaña **Información general** muestra un panel con métricas clave relacionadas con los recorridos. La pestaña **Examinar** muestra la lista de recorridos existentes."

### Métricas clave y lista de recorridos {#access-metrics}

En la sección del menú ADMINISTRACIÓN DE RECORRIDO, haga clic en **[!UICONTROL Recorridos]**. Hay dos pestañas disponibles:

**Información general**: esta pestaña muestra un panel con métricas clave relacionadas con los recorridos:

* **Perfiles procesados**: número total de perfiles procesados en las últimas 24 horas
* **Recorridos en directo**: número total de recorridos en directo con tráfico durante las últimas 24 horas. Los recorridos activos incluyen **Recorridos unitarios** (basado en eventos) y **Recorridos por lotes** (leer audiencia).
* **Tasa de error**: proporción de todos los perfiles con error comparada con el número total de perfiles introducidos durante las últimas 24 horas.
* **Tasa de descarte**: proporción de todos los perfiles descartados en comparación con el número total de perfiles introducidos durante las últimas 24 horas. Un perfil descartado representa a alguien que no cumple los requisitos para entrar en el recorrido, por ejemplo, debido a un área de nombres incorrecta o a reglas de reentrada.

>[!NOTE]
>
>Este tablero tiene en cuenta los recorridos con tráfico de las últimas 24 horas. Solo se muestran los recorridos a los que tiene acceso. Las métricas se actualizan cada 30 minutos y solo cuando hay nuevos datos disponibles.

![](assets/journeys-dashboard.png)

**Examinar**: esta pestaña muestra la lista de recorridos existentes. Puede buscar recorridos, utilizarlos y realizar acciones básicas en cada elemento. Por ejemplo, puede duplicar o eliminar un elemento. Para obtener más información, consulte [esta sección](../start/user-interface.md#filter-lists).

![](assets/journeys-browse.png)

### Filtrar recorridos {#filter}

En la lista de recorridos, puede aprovechar varios filtros para restringir la lista de recorridos y mejorar la legibilidad.

![](assets/filter-journeys.png)

Estas son las distintas operaciones de filtrado que puede realizar:

Filtre los recorridos según su estado, tipo, versión y etiquetas asignadas en **[!UICONTROL Filtros de estado y versión]**.

El tipo puede ser: **[!UICONTROL Evento unitario]**, **[!UICONTROL Calificación de audiencia]**, **[!UICONTROL Leer audiencia]** o **[!UICONTROL Evento empresarial]**.

El estado puede ser el siguiente:

* **Cerrado**: el recorrido se ha cerrado utilizando el **Cerca de nuevas entradas** botón. El recorrido deja de permitir que nuevas personas entren en el recorrido. Las personas que ya están en el recorrido pueden terminar el recorrido normalmente.
* **Borrador**: el recorrido se encuentra en su primera fase. Aún no se ha publicado.
* **Borrador (Pruebas)**: el modo de prueba se ha activado utilizando la variable **Modo de prueba** botón.
* **Finalizado**: el recorrido cambia automáticamente a este estado después del día 91 [tiempo de espera global](journey-properties.md#global_timeout). Los perfiles que ya están en el recorrido finalizan el recorrido normalmente. Los nuevos perfiles ya no pueden entrar en el recorrido.
* **Activo**: el recorrido se ha publicado utilizando la variable **Publish** botón.
* **Detenido**: el recorrido se ha apagado usando el **Detener** botón. Todos los individuos abandonan el recorrido al instante.

>[!NOTE]
>
>El ciclo de vida de creación de Recorridos también incluye un conjunto de estados intermedios que no están disponibles para el filtrado: &quot;Publicación&quot; (entre &quot;Borrador&quot; y &quot;Activo&quot;), &quot;Activación del modo de prueba&quot; o &quot;Desactivación del modo de prueba&quot; (entre &quot;Borrador&quot; y &quot;Borrador (prueba)&quot;) y &quot;Detención&quot; (entre &quot;Activo&quot; y &quot;Detenido&quot;). Cuando un recorrido está en un estado intermedio, es de solo lectura.

Utilice el **[!UICONTROL Filtros de creación]** para filtrar los recorridos según su fecha de creación o el usuario que los ha creado.

Mostrar recorridos que utilizan un evento, un grupo de campos o una acción específicos del **[!UICONTROL Filtros de actividad]** y **[!UICONTROL Filtros de datos]**.

Utilice el **[!UICONTROL Filtros de publicación]** para seleccionar una fecha de publicación o un usuario. Puede elegir, por ejemplo, mostrar las versiones más recientes de recorridos en directo que se publicaron ayer.

Para filtrar recorridos basados en un intervalo de fechas específico, seleccione **[!UICONTROL Personalizado]** desde el **[!UICONTROL Publicado]** lista desplegable.

Además, en los paneles Evento, Fuente de datos y Configuración de acciones, la variable **[!UICONTROL Utilizado en]** El campo muestra el número de recorridos que utilizan ese evento, grupo de campos o acción en particular. Puede hacer clic en el botón **[!UICONTROL Ver recorridos]** para mostrar la lista de los recorridos correspondientes.

![](assets/journey3bis.png)

## Cree su recorrido {#jo-build}

Diseñe recorridos para ofrecer experiencias personalizadas y contextuales. [!DNL Journey Optimizer] permiten crear casos prácticos de orquestación en tiempo real con información contextual almacenada en eventos o fuentes de datos. Diseñe escenarios avanzados de varios pasos con las siguientes capacidades:

* Envíe en tiempo real un **envío unitario** que se activa cuando se recibe un evento, o **en lote** con los públicos de Adobe Experience Platform.

* Aprovechar **datos contextuales** desde eventos, información de Adobe Experience Platform o datos de servicios API de terceros.

* Utilice el **acciones de canal integradas** (Correo electrónico, SMS, push, aplicación) para enviar mensajes diseñados en [!DNL Journey Optimizer] o crear **acciones personalizadas** si utiliza un sistema de terceros para enviar sus mensajes.

* Con el **diseñador de recorridos**, genere sus casos de uso de varios pasos: arrastre y suelte fácilmente un evento de entrada o una actividad de lectura de público, agregue condiciones y envíe mensajes personalizados.

➡️ [Descubra esta función en vídeo](journey.md#video)

A continuación se enumeran los pasos para enviar mensajes mediante recorridos.

1. Desde el **Examinar** pestaña, haga clic en **[!UICONTROL Crear Recorrido]** para crear un nuevo recorrido.

1. Edite las propiedades del recorrido en el panel de configuración que se muestra en el lado derecho. Aprenda a configurar las propiedades de su recorrido en esta [esta página](journey-properties.md).

   ![](assets/jo-properties.png)

1. Comience arrastrando y soltando un evento o una **Leer audiencia** actividad desde la paleta al lienzo. Para obtener más información sobre el diseño de recorridos, consulte [esta sección](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Arrastre y suelte los siguientes pasos que seguirá el individuo. Por ejemplo, puede agregar una condición seguida de una acción del canal. Para obtener más información sobre las actividades, consulte [esta sección](using-the-journey-designer.md).

1. Pruebe el recorrido con perfiles de prueba. Obtenga más información en esta [sección](testing-the-journey.md)

1. Publique el recorrido para activarlo. Obtenga más información en esta [sección](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Monitorice su recorrido con las herramientas de sistema de informes específicas para medir la efectividad de su recorrido. Obtenga más información en esta [sección](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)


## Duplicación de un recorrido {#duplicate-a-journey}

Puede duplicar un recorrido existente desde el **Examinar** pestaña. Todos los objetos y configuraciones se duplican en la copia de recorrido.

Para ello, siga los pasos a continuación:

1. Vaya al recorrido que desee copiar y haga clic en **Más acciones** (los tres puntos junto al nombre del recorrido).
1. Seleccione **Duplicar**.

   ![Duplicación de un recorrido](assets/duplicate-jo.png)

1. Introduzca el nombre del recorrido y confírmelo. También puede cambiar el nombre en la pantalla de propiedades del recorrido. De forma predeterminada, el nombre se establece de la siguiente manera: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. El nuevo recorrido se crea y está disponible en la lista de recorridos.
