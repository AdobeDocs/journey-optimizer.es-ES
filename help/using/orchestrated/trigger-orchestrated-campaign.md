---
solution: Journey Optimizer
product: journey optimizer
title: Déclencheur de una campaña orquestada mediante una señal
description: Obtenga información sobre cómo almacenar en déclencheur una campaña orquestada con una señal de la API de REST o de la actividad final de otra campaña, y cómo pasar parámetros a la campaña.
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
exl-id: d1fd072d-b143-4752-822f-23f98684ba80
feature_v2: id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1429
ht-degree: 0%

---

# Activación de campañas orquestadas mediante una señal {#trigger-signal}

Puede iniciar una campaña orquestada con una señal en lugar de una programación fija. Cuando la campaña recibe la señal, se ejecuta y puede pasar parámetros en la carga útil. Están disponibles como variables para el direccionamiento, las condiciones o las expresiones.

La señal puede proceder de cualquiera de las siguientes opciones:

* API de REST: su aplicación o integración llama al extremo de déclencheur (consulte [Publicar y almacenar en déclencheur la campaña](#publish) y la [referencia de API](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"}).
* Otra campaña orquestada: la actividad **[!UICONTROL End]** de una campaña de subida envía el mismo tipo de señal cuando se completa una rama. [Aprenda a configurar la actividad End](#signal-end).

Esta página explica cómo configurar la campaña que recibe la señal (programación, parámetros, prueba, publicación) y cómo activarla desde la API o desde una actividad **[!UICONTROL End]**. Una vez que las variables estén disponibles, para obtener detalles sobre cómo usarlas en reglas y condiciones de **[!UICONTROL Test]**, consulte [Usar variables en campañas orquestadas](variables-orchestrated-campaigns.md).

Para obtener la especificación REST completa del extremo de déclencheur (rutas, encabezados, cuerpo, respuestas y errores), consulte [API de campañas orquestadas con Déclencheur](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} en la documentación de la API de Adobe Journey Optimizer.

Proceso completo para almacenar en déclencheur una campaña orquestada con una señal:

1. [Programe la campaña para que se active por una señal](#configure-signal)
1. [Agregar parámetros para la carga útil de señal](#parameters) (opcional)
1. [Creación y prueba de la campaña](#build-and-test)
1. [Publicación y déclencheur de la campaña](#publish)

>[!NOTE]
>
>Para almacenar en déclencheur una campaña organizada mediante una señal, necesita el permiso **[!DNL Publish orchestrated campaigns]** (`orchestrated-campaign.publish`). Consulte [Permisos integrados](../administration/ootb-permissions.md).

## Programe la campaña para que se active por una señal {#configure-signal}

Para configurar una campaña orquestada para que se inicie en una señal en lugar de en una programación, siga estos pasos:

1. Abra la campaña orquestada en la que desee almacenar el déclencheur mediante una señal.

1. Abra la configuración de programación. [Aprenda a programar una campaña organizada](create-orchestrated-campaign.md#schedule).

1. Seleccione **[!UICONTROL Activado por una señal]** para que la campaña espere una señal en lugar de ejecutarse según una programación.

   ![Menú de horario con la opción Activado por una señal seleccionada](assets/triggered-oc-scheduler.png){zoomable="yes"}

## Añadir parámetros para la carga útil de señal (opcional) {#parameters}

Puede pasar parámetros en la señal de déclencheur y utilizarlos en la campaña en el contexto de ejecución como, por ejemplo, en objetivos, condiciones o expresiones. Defina primero cada parámetro en la configuración de programación y luego pase su valor cuando llame a la API de déclencheur o cuando asigne parámetros desde la actividad **[!UICONTROL End]** de una campaña ascendente ([ver a continuación](#signal-end)).

1. Abra el programador de campañas y seleccione **[!UICONTROL Agregar parámetro]**.

1. Defina el nombre y el tipo de datos de cada parámetro para enviar en la carga útil de señal. También puede proporcionar **Valores de prueba** que se utilizarán cuando almacene en déclencheur la campaña en modo de prueba. [Aprenda a probar una campaña desencadenada](#build-and-test).

   ![Agregar parámetro para definir parámetros de carga útil para la señal](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>En el caso de las campañas orquestadas activadas por la API de REST, si se pasa un parámetro en la llamada de API que no se ha definido en el programador, la llamada de API se realiza correctamente, el parámetro se propaga y se puede utilizar en expresiones. Sin embargo, la interfaz de campaña orquestada no le ayudará a utilizarla; por ejemplo, la actividad Test no muestra ni enumera parámetros que no se hayan definido en el planificador.

## Prueba de la campaña {#build-and-test}

Cree la campaña en el lienzo y, a continuación, pruébela en **[!UICONTROL Borrador]** antes de publicar enviando la señal a través de la API de REST.

* **Campañas orquestadas activadas por la API de REST**: siga los pasos a continuación para ejecutar la campaña en borrador y validar el objetivo, los parámetros y la lógica de envío antes de la publicación.

* **Campañas orquestadas activadas por una actividad End**: no se puede ejecutar la cadena completa de extremo a extremo en borrador: una vez publicada la campaña ascendente, su actividad **[!UICONTROL End]** solo inicia una campaña descendente publicada. Para probar el lado descendente antes de que se publiquen ambas campañas, mantén esa campaña en **[!UICONTROL Borrador]**, establece **[!UICONTROL Valores de prueba]** para los parámetros de señal en el programador ([Agregar parámetros para la carga útil de señal](#parameters)) y luego sigue los pasos de la API a continuación. La llamada a la API de déclencheur usa la misma carga que una actividad **[!UICONTROL End]** en tiempo de ejecución, por lo que puede validar el enrutamiento de parámetros y la lógica del lienzo antes de publicar la campaña de flujo descendente y configurar la actividad **[!UICONTROL End]** de flujo ascendente ([Déclencheur de la actividad End de otra campaña](#signal-end)).

1. Añada y conecte actividades (audiencia, segmentación, envíos) en el lienzo. [Obtenga información sobre cómo organizar actividades de campaña](orchestrate-activities.md)

1. Si ha definido parámetros en la señal, puede conectarlos a la lógica del lienzo (por ejemplo, en condiciones o segmentación). En este ejemplo, el parámetro &quot;channel&quot; se usa como condición en una actividad **[!UICONTROL Test]**.

   ![Parámetro de canal usado como condición en la actividad de prueba](assets/triggered-oc-use-parameters.png)

   Para usar un parámetro de señal en el editor de expresiones (por ejemplo, para generar una consulta en una actividad **[!UICONTROL Generar audiencia]**), escriba `$(vars/@<parameterName>)` en el campo de expresión. Reemplace `<parameterName>` con el nombre del parámetro definido en el programador, por ejemplo, `$(vars/@channel)`. [Aprenda a trabajar con el editor de expresiones](edit-expressions.md).

1. Abra el programador de campañas, seleccione **[!UICONTROL Copiar solicitud de API]** y elija el formato (cURL o petición HTTP).

   La información copiada incluye el ID de campaña orquestada, el nombre de la zona protegida, el ID de organización y los valores de prueba de los parámetros, si ha añadido alguno.

   ![Copiar opción de solicitud de API en la configuración de programación](assets/triggered-oc-copy.png)

   +++Solicitud cURL de ejemplo con un parámetro y un valor de prueba

   ```bash
   POST https://platform.adobe.io/ajo/campaign-orchestration/orchestratedCampaigns/1c7529c7-7a8c-491a-a2c6-3d8131d2e17d/trigger
   
   Headers:
   Authorization: Bearer ## Access token ##
   Content-Type: application/json
   x-api-key: ## Provide API Key here ##
   x-api-version: 1
   x-gw-ims-org-id: 123456ABCDEFG@LumaOrg
   x-sandbox-name: prod
   
   Body:
   {
   "variables": {
      "channel": "sms"
   }
   }
   ```

   +++

1. Haga clic en **[!UICONTROL Iniciar]** para iniciar la campaña.

1. Envíe la llamada de API de déclencheur mediante la solicitud de ejemplo que ha copiado del planificador. Consulte [API de campañas orquestadas por Déclencheur](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} para obtener detalles de solicitud y respuesta.

Cuando esté satisfecho con los resultados de la prueba, [publique la campaña](#publish).

## Publicación y déclencheur de la campaña {#publish}

Después de [probar la campaña](#build-and-test), publíquela para que pueda recibir una señal de su aplicación o de la actividad **[!UICONTROL End]** de otra campaña. [Más información sobre cómo iniciar y supervisar la campaña](start-monitor-campaigns.md#publish).

A continuación, puede almacenarlo en déclencheur desde la API de REST o desde la actividad **[!UICONTROL End]** de otra campaña. Consulte las secciones siguientes.

### Enviar la señal con la API de REST {#publish-api}

Después de la publicación, siga estos pasos cada vez que almacene en déclencheur la campaña desde su propia aplicación:

1. Abra el programador de campañas, seleccione **[!UICONTROL Copiar solicitud de API]** y elija el formato (cURL o petición HTTP).

   La información copiada incluye el ID de campaña orquestada, el nombre de la zona protegida, el ID de organización y parámetros, si ha añadido alguno.

   ![Copiar solicitud de API en la configuración de programación](assets/triggered-oc-copy.png)

1. Llame a la API de déclencheur desde el sistema. Consulte [API de campañas orquestadas por Déclencheur](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} para la especificación de extremo activo.

   >[!IMPORTANT]
   >
   >Para una campaña orquestada en directo, una protección de acelerador aplica un intervalo mínimo de una hora entre dos ejecuciones de déclencheur de API. Si vuelve a llamar a la API antes de que transcurra ese intervalo, la API devuelve el código HTTP 429 (Demasiadas solicitudes). Esta protección no se aplica al almacenar en déclencheur una versión de borrador para probarla.

   Si ha añadido parámetros a la carga útil de señal, los valores que pasa en la llamada de API se exponen como variables de evento de campaña cuando se ejecuta la campaña. Para inspeccionarlos, abra los registros de campaña desde la barra de herramientas del lienzo de la campaña. En la ficha **[!UICONTROL Tareas]**, identifique la tarea correspondiente a la señal y haga clic en el icono de lápiz para acceder a las variables de evento relacionadas. [Obtenga información sobre cómo acceder a los registros y tareas](start-monitor-campaigns.md#logs-tasks).

   ![Pantalla de registros y tareas donde hay variables de eventos de campaña disponibles](assets/trigger-events-variables.png){zoomable="yes"}

### Envíe la señal desde la actividad End de otra campaña {#signal-end}

Utilice esta ruta para encadenar campañas orquestadas: cuando la campaña ascendente finalice una rama, la actividad **[!UICONTROL End]** envía una señal a una campaña descendente que ya está configurada en **[!UICONTROL Activada por una señal]**. Esto le permite reutilizar campañas más pequeñas y pasar una carga útil diferente a cada llamante.

>[!NOTE]
>
>* Puede usar varias actividades **[!UICONTROL End]** en el mismo lienzo y configurar cada una de ellas para almacenar en déclencheur una campaña descendente diferente.
>* Varias campañas pueden almacenar en déclencheur la misma campaña descendente. Cada llamada a puede enviar una carga útil diferente.

Siga estos pasos en la campaña que debe ejecutarse primero:

1. Abra la campaña orquestada que debe enviar la señal y seleccione una actividad **[!UICONTROL End]** al final de la rama que debe completarse antes de que se inicie la campaña descendente.
1. En la sección **[!UICONTROL Señal externa]**, seleccione la campaña de flujo descendente que desea almacenar en déclencheur.

1. De forma opcional, añada parámetros: utilice los mismos nombres que en la programación de la campaña de flujo descendente y establezca cada valor.

   ![](assets/end-signal.png)

1. Para probar la campaña descendente en modo de borrador antes de publicarla, siga los pasos de la sección [probar la campaña](#build-and-test) para almacenarla en déclencheur en modo de borrador con la API de REST.

La campaña descendente debe publicarse antes de que la campaña ascendente se ejecute lo suficientemente lejos como para alcanzar la actividad **[!UICONTROL End]** que la almacena en déclencheur. Si la señal se envía mientras la campaña de Target no se publica, la ejecución falla. Publique la campaña descendente y, a continuación, reanude o reinicie según sea necesario.
