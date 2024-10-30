---
title: Creación de experiencias basadas en código
description: Aprenda a crear experiencias basadas en código en Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '1802'
ht-degree: 14%

---

# Creación de experiencias basadas en código {#create-code-based}

En [!DNL Journey Optimizer], puede crear experiencias basadas en código en un recorrido o una campaña.

Las protecciones específicas y las recomendaciones para experiencias basadas en código se detallan en [esta página](code-based-prerequisites.md).

## Añadir una experiencia basada en código mediante un recorrido o una campaña {#create-code-based-experience}

Para empezar a crear una experiencia basada en código a través de un recorrido o una campaña, siga los pasos a continuación.

>[!BEGINTABS]

>[!TAB Agregar una experiencia basada en código a un recorrido]

Para agregar una actividad de **experiencia basada en código** a un recorrido, siga estos pasos:

1. [Crear un recorrido](../building-journeys/journey-gs.md).

1. Inicie el recorrido con una actividad [Event](../building-journeys/general-events.md) o [Read Audience](../building-journeys/read-audience.md).

1. Arrastre y suelte una actividad de **[!UICONTROL experiencia basada en código]** desde la sección **[!UICONTROL Acciones]** de la paleta.

   ![](assets/code-based-activity-journey.png)

   >[!NOTE]
   >
   >Como **experiencia basada en código** es una actividad de mensaje entrante, viene con una actividad de **espera** de 3 días. [Más información](../building-journeys/wait-activity.md#auto-wait-node)

1. Escriba una **[!UICONTROL Etiqueta]** y **[!UICONTROL Descripción]** para su mensaje.

1. Seleccione o cree la [configuración de experiencia basada en código](code-based-configuration.md) que quiera usar.

   ![](assets/code-based-activity-config.png)

1. Seleccione el botón **[!UICONTROL Editar contenido]** y edite el contenido como desee con el editor de personalización. [Más información](#edit-code)

   También puede utilizar una plantilla de contenido existente como base para el contenido de código. Tenga en cuenta que las plantillas disponibles para elegir tienen ámbitos de HTML o JSON en función de la configuración de canal que se haya elegido previamente. [Aprenda a utilizar las plantillas de contenido](../content-management/use-content-templates.md)

1. Si es necesario, complete el flujo de recorrido arrastrando y soltando acciones o eventos adicionales. [Más información](../building-journeys/about-journey-activities.md)

1. Una vez que la experiencia basada en código esté lista, finalice la configuración y publique el recorrido para activarlo. [Más información](../building-journeys/publishing-the-journey.md)

Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md).

>[!TAB Creación de una campaña de experiencias basadas en código]

Para empezar a crear tu **experiencia basada en código** a través de una campaña, sigue los pasos a continuación.

1. Cree una campaña. [Más información](../campaigns/create-campaign.md)

1. Seleccione el tipo de campaña que desea ejecutar

   * **[!UICONTROL Programado - Marketing]**: ejecute la campaña inmediatamente o en una fecha especificada. Las campañas programadas están destinadas a enviar **marketing** mensajes. Se configuran y ejecutan desde la interfaz de usuario de.

   * **[!UICONTROL Activado por API - Marketing/Transaccional]**: ejecute la campaña mediante una llamada de API. Las campañas activadas por API están destinadas a enviar **marketing** o **mensajes transaccionales**, es decir, mensajes enviados después de una acción realizada por un individuo: restablecimiento de contraseña, compra en el carro de compras, etc. [Aprenda a almacenar en déclencheur una campaña mediante API](../campaigns/api-triggered-campaigns.md)

1. Complete los pasos para crear una campaña, como las propiedades de la campaña, [audiencia](../audience/about-audiences.md) y [programación](../campaigns/create-campaign.md#schedule). Para obtener más información sobre cómo configurar una campaña, consulte [esta página](../campaigns/get-started-with-campaigns.md).

1. Seleccione la acción **[!UICONTROL Experiencia basada en código]**.

1. Seleccione o cree la configuración de experiencia basada en código. [Más información](code-based-configuration.md)

   ![](assets/code-based-campaign-surface.png)

1. Edite el contenido como desee mediante el editor de personalización. [Más información](#edit-code)

   También puede utilizar una plantilla de contenido existente como base para el contenido de código. Tenga en cuenta que las plantillas disponibles para elegir tienen ámbitos de HTML o JSON en función de la configuración de canal que se haya elegido previamente. [Aprenda a utilizar las plantillas de contenido](../content-management/use-content-templates.md)

   <!--![](assets/code-based-campaign-edit-content.png)-->

Para obtener más información sobre cómo configurar una campaña, consulte [esta página](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Edición del contenido del código {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="Utilice el editor de personalización"
>abstract="Inserte y edite el código que desea enviar como parte de esta acción de experiencia basada en código."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html?lang=es" text="Introducción al editor de personalización"

1. En la actividad de recorrido o en la pantalla de edición de la campaña, seleccione **[!UICONTROL Editar código]**.

   ![](assets/code-based-campaign-edit-code.png)

1. Se abre [editor de personalización](../personalization/personalization-build-expressions.md). Es una interfaz de creación de experiencias no visual que le permite crear su código.

1. Puede cambiar el modo de creación de HTML a JSON y viceversa.

   ![](assets/code-based-campaign-code-editor.png)

   >[!CAUTION]
   >
   >Cambiar el modo de creación resultará en la pérdida de todo el código actual, por lo que asegúrese de cambiar de modo antes de comenzar la creación.

1. Introduzca el código según sea necesario. Puede aprovechar el editor de personalización [!DNL Journey Optimizer] con todas sus capacidades de personalización y creación. [Más información](../personalization/personalization-build-expressions.md)

1. Puede agregar fragmentos de expresiones JSON o HTML si es necesario. [Descubra cómo](../personalization/use-expression-fragments.md)

   También puede guardar parte del contenido del código como fragmento. [Descubra cómo](../content-management/fragments.md#save-as-expression-fragment)

1. Con las experiencias basadas en código, puede utilizar la función Decisioning. Seleccione el icono **[!UICONTROL Directiva de decisión]** en la barra izquierda y haga clic en **[!UICONTROL Agregar directiva de decisión]**. [Más información](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >Actualmente, la toma de decisiones solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.


1. Haga clic en **[!UICONTROL Guardar y cerrar]** para confirmar los cambios.

Ahora, tan pronto como el desarrollador realice una llamada de API o SDK para recuperar contenido para la superficie definida en la configuración de canal, los cambios se aplicarán a su página web o aplicación.

## Prueba de la experiencia basada en código {#test-code-based-experience}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Previsualización de la experiencia basada en código"
>abstract="Obtenga una simulación del aspecto que tendrá su experiencia basada en código."

Para mostrar una previsualización de la experiencia basada en código modificada, siga los pasos a continuación.

>[!CAUTION]
>
>Debe tener perfiles de prueba disponibles para simular qué ofertas se les enviarán. Aprenda a [crear perfiles de prueba](../audience/creating-test-profiles.md).

1. En el recorrido o la campaña, desde el editor de personalización o la pantalla de edición de contenido, seleccione **[!UICONTROL Simular contenido]**.

   ![](assets/code-based-campaign-simulate.png)

1. Haga clic en **[!UICONTROL Administrar perfiles de prueba]** para seleccionar uno o más perfiles de prueba.

1. Se muestra una previsualización de la experiencia modificada basada en código.

Encontrará información detallada sobre cómo seleccionar perfiles de prueba y obtener una vista previa del contenido en [esta sección](../content-management/preview.md).

### Previsualización en el dispositivo {#preview-on-device}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device"
>title="Previsualización de la experiencia basada en código en un dispositivo real"
>abstract="Obtenga una previsualización de sus experiencias personalizadas directamente en el explorador o en sus dispositivos móviles, para ver cómo se ven en dispositivos reales."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_web"
>title="Previsualización de la experiencia web basada en código en un dispositivo"
>abstract="Escanee el código QR o copie el vínculo para previsualizarlo en el dispositivo."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_mobile"
>title="Previsualización de la experiencia móvil basada en código en un dispositivo"
>abstract="Escanee el código QR o copie el vínculo para previsualizarlo en el dispositivo. Una vez conectado, introduzca el pin en el dispositivo. Es posible que tenga que reiniciar la aplicación para ver los cambios cada vez que actualice los vínculos de previsualización."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_refresh"
>title="Actualice el vínculo de previsualización para que se refleje la vista actual"
>abstract="La previsualización en el dispositivo mostrará el contenido a partir del momento en que creó o actualizó el vínculo de previsualización. Si ha modificado el contenido o ha seleccionado un perfil de prueba o tratamiento diferente, actualice la previsualización para que se refleje la vista actual."

Al crear experiencias basadas en código para páginas web o aplicaciones móviles, puede obtener una vista previa de sus experiencias personalizadas directamente en el explorador o en sus dispositivos móviles, para ver cómo se ven estas experiencias en dispositivos reales.

>[!WARNING]
>
>La vista previa en el dispositivo no está disponible al usar los atributos contextuales [directivas de decisión](../experience-decisioning/create-decision.md) o [personalización](../personalization/personalization-build-expressions.md).

1. En la pantalla **[!UICONTROL Simular]**, haga clic en el botón **[!UICONTROL Abrir opciones de vista previa]**. Las opciones de vista previa dependen de la plataforma seleccionada en la [configuración basada en código](code-based-configuration.md#create-code-based-configuration).

1. Si usa una [plataforma web](code-based-configuration.md#web) en su configuración basada en código, el campo de solo lectura de **[!UICONTROL URL de vista previa del dispositivo]** está rellenado previamente con la URL ingresada para la configuración de canal actual.

   ![](assets/preview-on-device-web.png)

   Puede:

   * Seleccione el botón **[!UICONTROL Copiar vínculo]** y pegue el vínculo en una pestaña del explorador. También puede compartir el vínculo con su equipo y las partes interesadas, que pueden obtener una vista previa de la nueva experiencia en cualquier explorador antes de que los cambios se activen.

   * Haz clic en **[!UICONTROL Abrir en ficha nueva]** para abrir el vínculo en el explorador actual.

   * Escanee el código QR con su dispositivo móvil para abrir el vínculo de vista previa en un navegador móvil.

1. Si usa [plataformas móviles](code-based-configuration.md#mobile) (iOS/Android) en su configuración basada en código, el campo de solo lectura **[!UICONTROL Vínculo profundo]** está rellenado previamente con el valor de **[!UICONTROL Vista previa de URL]** introducido en la configuración de canal de la plataforma seleccionada.

   Alterne entre las pestañas **[!UICONTROL iOS]** y **[!DNL Android]** para obtener una vista previa de su experiencia en la plataforma que elija.

   ![](assets/preview-on-device-mobile.png)

   Puede:

   * Seleccione el botón **[!UICONTROL Copiar vínculo]** y comparta el vínculo con su equipo y las partes interesadas, que pueden obtener una vista previa de la nueva experiencia en cualquier explorador móvil antes de que los cambios se activen.

   * Escanee el código QR con su dispositivo móvil para abrir el vínculo de vista previa directamente en la aplicación móvil. Debes introducir el PIN en tu dispositivo para establecer la sesión de [Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/implement-assurance){target="_blank"}.

     >[!NOTE]
     >
     >**Adobe Experience Platform Assurance** es un producto de Adobe Experience Cloud que te ayudará a inspeccionar, probar, simular y validar la forma en que recopilas datos o sirves experiencias en tu aplicación móvil. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/assurance/home){target="_blank"}

1. Se generan vínculos de vista previa para el perfil de prueba seleccionado y, si usa [Experimento de contenido](../content-management/content-experiment.md) en su recorrido o campaña, para el tratamiento seleccionado.

   <!--If you have modified the content or selected a different treatment or test profile, scroll down to the bottom of the **[!UICONTROL Preview on device]** pop-up and click **[!UICONTROL Refresh preview link]** to reflect the current state.

   ![](assets/preview-on-device-refresh.png)-->

   <!--When creating a content experiment, you need to select a given treatment and click the **[!UICONTROL Simulate content]** button to obtain the link corresponding to that treatment, then select another treatment, click the **[!UICONTROL Simulate content]** button to obtain a new preview link, and so on.-->

   Al actualizar el contenido o seleccionar un perfil de prueba o un tratamiento diferentes, el vínculo de vista previa se actualiza automáticamente. Puede copiar el vínculo en diferentes pestañas del explorador y comparar las experiencias.

## Publique su experiencia basada en código {#code-based-experience-live}

>[!IMPORTANT]
>
> Si la campaña está sujeta a una directiva de aprobación, deberá solicitar la aprobación para poder activar las experiencias basadas en código. [Más información](../test-approve/gs-approval.md)

Una vez que haya definido la experiencia basada en código y editado el contenido como desee con el [editor basado en código](#edit-code), puede activar el recorrido o la campaña para que los cambios sean visibles a la audiencia.

También puede obtener una vista previa del contenido de la experiencia basado en código antes de publicarlo. [Más información](#test-code-based-experience)

>[!NOTE]
>
>Si activa un recorrido o una campaña basada en código que afecte a las mismas páginas que otro recorrido o campaña que ya está activo, todos los cambios se aplicarán al contenido.
>
>Si varios recorridos o campañas basados en código actualizan los mismos elementos del contenido, la campaña o el recorrido de mayor prioridad tiene prioridad.

Una vez que el recorrido o la campaña basados en código estén activos, el equipo de implementación de la aplicación será responsable de realizar llamadas explícitas de API o SDK para recuperar contenido para las superficies definidas en la [configuración de experiencia basada en código](code-based-configuration.md) seleccionada. Obtenga más información sobre las diferentes implementaciones de clientes en [esta sección](code-based-implementation-samples.md).

### Publish es un recorrido basado en código {#publish-code-based-journey}

Para que la experiencia basada en código esté activa desde un recorrido, siga los pasos a continuación.

1. Compruebe que el recorrido sea válido y que no haya ningún error. [Más información](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)

1. En el recorrido, seleccione la opción **[!UICONTROL Publish]**, que se encuentra en el menú desplegable superior derecho.

   ![](assets/code-based-journey-publish.png)

   >[!NOTE]
   >
   >Obtenga más información sobre cómo publicar recorridos en [esta sección](../building-journeys/publishing-the-journey.md).

El recorrido basado en código toma el estado **[!UICONTROL Activo]** y ahora es visible para la audiencia seleccionada. Cada destinatario del recorrido puede ver las modificaciones.

>[!NOTE]
>
>Después de hacer clic en **[!UICONTROL Publish]**, los cambios pueden tardar hasta 15 minutos en estar disponibles.

### Activación de una campaña basada en código {#activate-code-based-campaign}

1. En su campaña basada en código, seleccione **[!UICONTROL Revisar para activar]**.

   ![](assets/code-based-campaign-review.png)

1. Compruebe y edite si es necesario el contenido, las propiedades, la configuración, la audiencia y la programación.

1. Seleccione **[!UICONTROL Activar]**.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >Más información sobre cómo activar campañas en [esta sección](../campaigns/review-activate-campaign.md).

Su campaña basada en código obtiene el estado **[!UICONTROL Live]** y ahora es visible para la audiencia seleccionada. Cada destinatario de la campaña puede ver las modificaciones agregadas al contenido.

>[!NOTE]
>
>Después de hacer clic en **[!UICONTROL Activar]**, los cambios pueden tardar hasta 15 minutos en estar disponibles.
>
>Si ha definido una programación para su campaña basada en código, tiene el estado **[!UICONTROL Programado]** hasta que se alcance la fecha y la hora de inicio.

## Detener un recorrido o una campaña basados en código {#stop-code-based-experience}

Cuando una experiencia basada en código está activa, puede detenerla para evitar que la audiencia vea las modificaciones. Siga los pasos a continuación.

1. Seleccione un recorrido o una campaña en directo en la lista correspondiente.

1. Realice la acción correspondiente según su caso:

   * En el menú superior de la campaña, seleccione **[!UICONTROL Detener campaña]**.

     ![](assets/code-based-campaign-stop.png)

   * En el menú superior del recorrido, haga clic en el botón **[!UICONTROL Más]** y seleccione **[!UICONTROL Detener]**.

     ![](assets/code-based-journey-stop.png)

1. Las modificaciones que ha añadido ya no serán visibles para la audiencia que ha definido.

>[!NOTE]
>
>Una vez que se detiene un recorrido o una campaña basados en código, no se puede editar ni activar de nuevo. Solo puede duplicarlo y activar la campaña o el recorrido duplicados.

<!--Reporting TBC

## Check the code-based experience reports {#check-code-based-reports}

Once your code-based experience is live, you can check the **[!UICONTROL Code-based]** tab of the  [Journey report](../reports/journey-global-report-cja.md#web-cja) and [Campaign report](../reports/campaign-global-report-cja.md#web) to compare elements such as the number of experiences delivered to your audience, and the number of engagements with your content.-->

<!--## Code-based reports

You can access code-based journey or campaign reports from the summary screen.

Global reports display events that occurred at least two hours ago and cover events over a selected time period. In comparison, Live reports focus on events that took place within the past 24 hours, with a minimum time interval of two minutes from the event occurrence.

### Code-based live report {#live-report-code-based}

From your campaign **[!UICONTROL Live report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages. [Learn more on live report](../reports/campaign-live-report.md)

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your code-based experiences, such as:

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**:  total number of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (impressions, unique impressions and interactions) for the last 24 hours.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.
+++

### Code-based global report {#global-report-code-based}

Code-based campaign global report can be accessed directly from your journey or campaign with the **[!UICONTROL View report]** button. [Learn more on global report](../reports/campaign-global-report-cja.md)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages.

![](assets/code-based-campaign-global-report.png)

Add image TBC

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your experiences, such as:

* **[!UICONTROL Unique impressions]**: number of unique users to whom the experience was delivered.

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**: percentage of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (unique impressions, impressions and interactions) for the concerned period.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.
+++

TBC video if existing

## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
