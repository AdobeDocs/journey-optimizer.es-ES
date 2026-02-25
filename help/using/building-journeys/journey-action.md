---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad recorrido de acción
description: Aprenda a añadir una actividad de acción genérica para configurar acciones únicas y grupos de acciones entrantes de varias acciones dentro del lienzo de recorrido.
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, mensaje, push, sms, correo electrónico, en la aplicación, web, tarjeta de contenido, experiencia basada en código
exl-id: 0ed97ffa-8efc-45a2-99ae-7bcb872148d5
version: Journey Orchestration
source-git-commit: 1455489645b208340085a9ea4d4e6e759dbcde9b
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 12%

---

# Uso de la actividad Acción {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_action_activity"
>title="Actividad de acción"
>abstract="La actividad genérica **Acción** le permite configurar una sola acción de canal nativo y varias actividades entrantes con la capacidad de añadir la optimización a cualquier acción de canal integrada."

[!DNL Journey Optimizer] viene con una nueva actividad **Action** genérica que permite configurar una sola acción de canal integrada y también varias actividades entrantes.

Permite lo siguiente:

* Una configuración de acción nativa simplificada dentro del lienzo de recorrido.
* La capacidad para crear grupos de acciones entrantes de varias acciones.
* Capacidad de añadir optimización a cualquier acción de canal integrada.

>[!NOTE]
>
>Ahora se puede acceder a todos los canales nativos a través de la actividad recorrido de acción. Las actividades heredadas del canal nativo quedarán obsoletas con la versión de marzo. Los recorridos existentes que incluyen acciones heredadas seguirán funcionando tal cual; no se requiere ninguna migración.

También puede configurar acciones personalizadas para enviar los mensajes en [!DNL Journey Optimizer]. [Más información](#recommendation)

## Añadir una acción a un recorrido  {#add-action}

Para añadir una acción de canal integrada a un recorrido, siga los pasos a continuación.

1. Inicie el recorrido con una actividad [Event](general-events.md) o [Read Audience](read-audience.md).

1. En la sección **[!UICONTROL Acciones]** de la paleta, arrastre y suelte una actividad **[!UICONTROL Acción]** en el lienzo.

1. Seleccione la actividad de canal integrada que desee aprovechar en el recorrido.

   ![Menú desplegable de tipo de acción que muestra las opciones de acción del canal y acción personalizada](assets/journey-action-type-cbe.png)

1. Agregue una etiqueta a su acción y seleccione **[!UICONTROL Configurar acción]**.

   ![Panel de configuración de actividades de acción con campos de etiqueta y descripción](assets/journey-action-configure.png){width="80%"}

1. Se le dirigirá a la ficha **[!UICONTROL Acciones]** de la pantalla de configuración de acciones de recorrido.

   Seleccione la configuración que desea utilizar para el canal seleccionado.

   ![Ficha Acciones del menú Administración que muestra las acciones personalizadas y de Adobe](assets/journey-action-actions-tab.png)

1. Si ha seleccionado un canal entrante, puede añadir varias acciones. [Más información](#multi-action)

1. Configure la actividad según el canal seleccionado. Aprenda a configurar acciones de canal integradas en [esta sección](journeys-message.md).

1. Use la sección **[!UICONTROL Optimización]** para ejecutar experimentos de contenido, aprovechar reglas de segmentación o usar combinaciones avanzadas de experimentación y segmentación.

   Estas diferentes opciones y los pasos a seguir se detallan en [esta sección](../content-management/gs-message-optimization.md).

1. Utilice la sección **[!UICONTROL Idiomas]** para crear contenido en varios idiomas dentro de la acción de recorrido. Para ello, haga clic en el botón **[!UICONTROL Agregar idiomas]** y seleccione la **[!UICONTROL configuración de idioma]** que desee.

   Encontrará información detallada sobre cómo configurar y utilizar las capacidades multilingües en [esta sección](../content-management/multilingual-gs.md).

Hay disponibles ajustes adicionales en función del canal de comunicación seleccionado. Expanda las secciones siguientes para obtener más información.

+++**Aplicar reglas de límite** (correo electrónico, push, SMS)

En la lista desplegable **[!UICONTROL Reglas de negocio]**, seleccione un conjunto de reglas para aplicar reglas de límite a la acción de recorrido.

El uso de conjuntos de reglas de canal le permite establecer límites de frecuencia por tipo de comunicación para evitar sobrecargar a los clientes con mensajes similares.

[Aprenda a trabajar con conjuntos de reglas](../conflict-prioritization/rule-sets.md)

+++

+++**Rastrear participación** (correo electrónico, SMS).

Utilice la sección **[!UICONTROL Seguimiento de acciones]** para rastrear cómo reaccionan sus destinatarios a sus envíos de correo electrónico o SMS.

Se puede acceder a los resultados de seguimiento desde el informe de recorrido una vez que se ha ejecutado el recorrido.

[Más información sobre los informes de recorrido](../reports/journey-global-report-cja.md)

+++

+++**Habilitar modo de envío rápido** (push).

El modo de envío rápido es un complemento de [!DNL Journey Optimizer] que permite el envío muy rápido de mensajes push en grandes volúmenes a través de campañas.

La entrega rápida se utiliza cuando el retraso en la entrega de mensajes es crítico para la empresa, cuando desea enviar una alerta push urgente en teléfonos móviles, por ejemplo, una noticia de última hora a los usuarios que han instalado su aplicación de canal de noticias.

Aprenda a habilitar el modo de envío rápido para las notificaciones push [en esta página](../push/create-push.md#rapid-delivery).

Para obtener más información sobre el rendimiento al usar el modo de envío rápido, consulte [[!DNL Adobe Journey Optimizer] descripción del producto](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

+++

+++**Asignar puntuaciones de prioridad** (web, en la aplicación, basado en código)

En la sección **[!UICONTROL Administración de conflictos]**, puede asignar una puntuación de prioridad a la acción de recorrido, lo que le permite priorizar una acción entrante cuando hay varias acciones de recorrido o campañas que utilizan la misma configuración de canal.

De forma predeterminada, la puntuación de prioridad de la acción se hereda de la puntuación de prioridad general del recorrido.

[Aprenda a asignar puntuaciones de prioridad a las acciones del canal](../conflict-prioritization/priority-scores.md#priority-action)

+++

+++**Establecer reglas de envío adicionales** (Tarjetas de contenido)

En el caso de los recorridos de tarjetas de contenido, puede habilitar reglas de entrega adicionales para elegir los eventos y criterios que almacenan el mensaje en déclencheur.

[Aprenda a crear tarjetas de contenido](../content-card/create-content-card.md)

+++

+++**Definir déclencheur** (en la aplicación)

Para los mensajes en la aplicación, puedes usar el botón **[!UICONTROL Editar déclencheur]** para elegir los eventos y los criterios que almacenan el mensaje en déclencheur.

[Obtenga información sobre cómo crear un mensaje en la aplicación](../in-app/create-in-app.md)

+++

## Añadir varias acciones entrantes {#multi-action}

>[!CONTEXTUALHELP]
>id="ajo_multi_action_journey"
>title="Añadir varias acciones entrantes"
>abstract="Puede seleccionar varias acciones entrantes dentro de un solo recorrido. Esta función le permite enviar varias experiencias basadas en código, mensajes en la aplicación, tarjetas de contenido o acciones web a diferentes ubicaciones al mismo tiempo, y cada acción con un contenido específico."

Para simplificar la orquestación de recorrido, puede definir varias acciones entrantes dentro de una sola acción de recorrido.

>[!NOTE]
>
>Esta capacidad solo está disponible para canales entrantes. Actualmente, no se admiten canales salientes como correo electrónico.

Esta capacidad le permite enviar varias experiencias basadas en código, mensajes en la aplicación, tarjetas de contenido o acciones web a diferentes ubicaciones al mismo tiempo, sin necesidad de crear varias acciones de recorrido. Facilita la implementación del recorrido y ofrece una creación de informes más fluida, con todos los datos consolidados en un solo recorrido.

Por ejemplo, puede enviar una experiencia basada en código a varios extremos con contenido ligeramente diferente. Para ello, cree varias acciones basadas en código dentro de la misma acción de recorrido, cada una con una configuración de extremo diferente.

Para definir varias acciones entrantes en un solo nodo de acción de recorrido, siga los pasos a continuación.

1. Inicie el recorrido con una actividad [Event](general-events.md) o [Read Audience](read-audience.md).

1. En la sección **[!UICONTROL Acciones]** de la paleta, arrastre y suelte una actividad **[!UICONTROL Acción]** en el lienzo.

1. Seleccione **[!UICONTROL Acción múltiple]** como tipo de acción.

   ![Actividad de varias acciones en la paleta de recorrido en Orquestación](assets/journey-multi-action.png)

1. Agregue una etiqueta si es necesario y seleccione **[!UICONTROL Configurar acción]**.

   ![Panel de configuración de varias acciones con campos de etiqueta y descripción](assets/journey-multi-action-configure.png){width="60%"}

1. Se le dirigirá a la ficha **[!UICONTROL Acciones]** de la pantalla de configuración de acciones de recorrido.

   ![Configuración de varias acciones que muestra la lista de acciones a ejecutar](assets/journey-multi-action-configuration.png){width="70%"}

1. Seleccione una acción entrante (**Experiencia basada en código**, **Mensaje en la aplicación**, **Tarjeta de contenido** o **Web**) de la sección **[!UICONTROL Acciones]**.

1. Seleccione la configuración de canal y defina un contenido específico para esa acción.

1. Utilice el botón **[!UICONTROL Agregar acción]** para seleccionar otra acción de entrada de la lista desplegable.

   ![Agregar botón de acción para incluir acciones adicionales en la actividad de varias acciones](assets/journey-multi-action-add.png){width="80%"}

1. Continúe de la misma manera para agregar más acciones. Puede añadir hasta 10 acciones entrantes en un grupo de acciones de recorrido.

Una vez que el recorrido esté [activo](publish-journey.md), todas las acciones se activarán simultáneamente.
<!--
## Next steps {#next}

Once your action is configured, you can design its content. [Learn more]-->
