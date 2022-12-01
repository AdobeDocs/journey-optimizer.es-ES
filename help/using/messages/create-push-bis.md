---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de una notificación push
description: Obtenga información sobre cómo crear una notificación push en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 5e5b078fa61e2c615a2242f50439c2f20ea5216a
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 2%

---

# Crear una notificación push {#create-push-notification-bis}

## Creación de la notificación push en un recorrido o campaña

Para crear una notificación push, siga los pasos a continuación:

>[!BEGINTABS]

>[!TAB Añadir una inserción a un Recorrido]

1. Abra el recorrido y arrastre y suelte una actividad Push desde la sección Actions de la paleta.

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la superficie del mensaje que desea utilizar.

   Para obtener más información sobre cómo configurar un recorrido, consulte

1. En la pantalla de configuración del recorrido, haga clic en el **[!UICONTROL Editar contenido]** para configurar el contenido push.

1. Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo y probarlo.

1. Cuando la notificación push esté lista, complete la configuración de su para enviarla.

   Para realizar un seguimiento del comportamiento de los destinatarios a través de las aperturas de push o las interacciones, asegúrese de que las opciones dedicadas en la sección de seguimiento están habilitadas en .

>[!TAB Adición de una push a una campaña]

1. Cree una nueva campaña programada o activada por la API, seleccione **[!UICONTROL Notificaciones push]** como su acción y elija el **[!UICONTROL Superficie de la aplicación]** para usar.

1. Haga clic en **[!UICONTROL Crear]**.

1. En el **[!UICONTROL Propiedades]** , edite la **[!UICONTROL Título]** y **[!UICONTROL Descripción]**.

1. Haga clic en el **[!UICONTROL Seleccionar la audiencia]** para definir la audiencia a la que se dirigirá desde la lista de segmentos de Adobe Experience Platform disponibles.

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado.

1. Las campañas están diseñadas para ejecutarse en una fecha específica o con una frecuencia recurrente. Obtenga información sobre cómo configurar la variable **[!UICONTROL Programación]** de su campaña en.

1. En el **[!UICONTROL Déclencheur de acción]** , seleccione **[!UICONTROL Frecuencia]** de la notificación push:

   * Una vez
   * Diario
   * Semanal
   * Mensual

1. En la pantalla de configuración de la campaña, haga clic en el botón **[!UICONTROL Editar contenido]** para configurar el contenido push.

1. Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo y probarlo.

1. Cuando la notificación push esté lista, complete la configuración de su para enviarla.

   Para realizar un seguimiento del comportamiento de los destinatarios a través de las aperturas push o las interacciones, asegúrese de que las opciones dedicadas en la sección de seguimiento están habilitadas en ).

>[!ENDTABS]

## Modo de entrega rápido

El modo de entrega rápida, anteriormente conocido como modo de ráfaga en recorridos, es un [!DNL Journey Optimizer] complemento que permite enviar mensajes push muy rápidamente a grandes volúmenes mediante campañas.

La entrega rápida se utiliza cuando el retraso en la entrega de mensajes es crítico para el negocio, cuando desea enviar una alerta push urgente en teléfonos móviles, por ejemplo una noticia de último minuto para los usuarios que han instalado la aplicación de canal de noticias.

Para obtener más información sobre el rendimiento al utilizar el modo de entrega rápida, consulte.

### Requisitos previos

La mensajería de envío rápido incluye los siguientes requisitos:

* La entrega rápida está disponible para **[!UICONTROL Programado]** solo campañas y no está disponible para campañas activadas por API,
* No se permite ninguna personalización en el mensaje push,
* La audiencia de destino debe contener menos de 30 millones de perfiles,
* Puede ejecutar hasta 5 campañas simultáneamente mediante el modo de envío rápido.

### Activar el modo de entrega rápido

1. Cree una campaña de notificaciones push y active la opción **[!UICONTROL Entrega rápida]** .

1. Configure el contenido del mensaje y seleccione la audiencia a la que desea dirigirse.

   >[!IMPORTANT]
   >
   >Asegúrese de que el contenido del mensaje no incluya ninguna personalización y de que la audiencia contenga menos de 30 millones de perfiles.

1. Revise y active la campaña como de costumbre. Tenga en cuenta que, en el modo de prueba, los mensajes no se envían mediante el modo de envío rápido.