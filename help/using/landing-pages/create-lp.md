---
title: Creación de una página de aterrizaje
description: Obtenga información sobre cómo configurar y publicar una página de aterrizaje en Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 4%

---

# Creación y publicación de páginas de aterrizaje {#create-lp}

>[!CAUTION]
>
>Actualmente, el uso de páginas de aterrizaje está disponible en acceso anticipado solo para usuarios seleccionados. Si desea aprovechar esta función, póngase en contacto con el administrador de cuentas de Adobe.

## Acceso a las páginas de aterrizaje

Para acceder a la lista de páginas de aterrizaje, seleccione **[!UICONTROL Journey Management]** > **[!UICONTROL Landing pages]** en el menú de la izquierda.

![](../assets/lp_access-list.png)

La variable **[!UICONTROL Landing Pages]** muestra todos los elementos creados. Puede filtrarlos en función de su estado o fecha de modificación.

![](../assets/lp_access-list-filter.png)

## Creación de una página de aterrizaje

Los pasos para crear una página de aterrizaje son los siguientes:

1. En la lista de páginas de aterrizaje, haga clic en **[!UICONTROL Create landing page]**.

   ![](../assets/lp_create-lp.png)

1. Añada un título. Puede agregar una descripción si es necesario.

   ![](../assets/lp_create-lp-details.png)

1. Haga clic en **[!UICONTROL Create]**.

1. Se muestra la página principal y sus propiedades. Obtenga información sobre cómo configurar los ajustes de la página [here](#configure-primary-page).

   ![](../assets/lp_primary-page.png)

1. Haga clic en el icono + para añadir una subpágina. Obtenga información sobre cómo configurar sus ajustes [here](#configure-subpages).

   ![](../assets/lp_add-subpage.png)

Una vez que haya configurado y diseñado el [página principal](#configure-primary-page) y [subpáginas](#configure-subpages) si hay alguno, puede [prueba](#test) y [publicar](#publish) su página de aterrizaje.

## Configuración de la página principal {#configure-primary-page}

La página principal es la página que se muestra inmediatamente a los usuarios cuando hacen clic en el vínculo de la página de aterrizaje, por ejemplo, desde un correo electrónico o un sitio web.

Para definir la configuración de la página principal, siga los pasos a continuación.

1. Puede cambiar el nombre de la página, que es **[!UICONTROL Primary page]** de forma predeterminada.

1. Edite el contenido de la página con el diseñador de contenido. Aprenda a diseñar contenido de página de aterrizaje [here](design-lp.md).

   ![](../assets/lp_open-designer.png)

1. Defina la dirección URL de la página de aterrizaje.

   >[!CAUTION]
   >
   >La dirección URL de la página de aterrizaje debe ser única.

   ![](../assets/lp_access-url.png)

   La primera parte de la URL está cargada previamente y no se puede editar a través de la interfaz de usuario. Para configurarlo, póngase en contacto con su representante de cuentas de Adobe o con el [Equipo de asistencia al servicio de atención al cliente de Adobe](https://helpx.adobe.com/es/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}.

1. Puede definir una fecha de caducidad para la página. En ese caso, debe seleccionar una acción al expirar la página:

   * **[!UICONTROL Redirect URL]**: Introduzca la dirección URL de la página a la que se redirigirá a los usuarios cuando caduque la página.
   * **[!UICONTROL Custom page]**: [Configurar una subpágina](#configure-subpages) y selecciónela en la lista desplegable que se muestra.
   * **[!UICONTROL Browser error]**: Escriba el texto del error que se mostrará en lugar de la página.

   ![](../assets/lp_expiry-date.png)

   <!--1. In the **[!UICONTROL Additional data]** section, define a **[!UICONTROL Key]** and the corresponding **[!UICONTROL Parameter value]**. // you can define how the data entered in the landing page is managed once it has been submitted by a user??-->

1. Si ha seleccionado una o más listas de suscripción para la página principal, estas se muestran en la **[!UICONTROL Subscription list]** para obtener más información.

   ![](../assets/lp_subscription-list.png)

1. Desde la página de aterrizaje, puede crear directamente un recorrido que enviará un mensaje de confirmación a los usuarios cuando envíen el formulario.

   ![](../assets/lp_create-journey.png)

   Haga clic en **[!UICONTROL Create journey]** para empezar [configuración de este recorrido](../building-journeys/journey-gs.md#jo-build). Se le redirigirá al **[!UICONTROL Journey Management]** > **[!UICONTROL Journeys]** lista.

## Configurar subpáginas {#configure-subpages}

Puede agregar tantas subpáginas como sea necesario. Por ejemplo, puede crear una página de agradecimiento que se mostrará una vez que los usuarios envíen el formulario. También puede definir una página de error a la que se llamará cuando se produzca un error con la página de aterrizaje.

Para definir la configuración de una subpágina, siga los pasos a continuación.

1. Puede cambiar el nombre de la página, que es **[!UICONTROL Subpage 1]** de forma predeterminada.

1. Edite el contenido de la página con el diseñador de contenido. Aprenda a diseñar contenido de página de aterrizaje [here](design-lp.md).

1. Defina la dirección URL de la página de aterrizaje.

   La primera parte de la URL está cargada previamente y no se puede editar a través de la interfaz de usuario. Para configurarlo, póngase en contacto con su representante de cuentas de Adobe o con el [Equipo de asistencia al servicio de atención al cliente de Adobe](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}.

   >[!CAUTION]
   >
   >La dirección URL de la página de aterrizaje debe ser única.

![](../assets/lp_subpage-settings.png)

## Prueba de la página de aterrizaje {#test}

Una vez que se hayan definido la configuración y el contenido de la página de aterrizaje, puede utilizar perfiles de prueba para previsualizarlos. Si ha insertado [contenido personalizado](../personalization/personalize.md), podrá comprobar cómo se muestra este contenido en la página de aterrizaje, aprovechando los datos de perfil de prueba.

>[!CAUTION]
>
>Debe tener perfiles de prueba disponibles para poder previsualizar los mensajes y enviar pruebas. Aprenda a crear perfiles de prueba en [esta página](../building-journeys/creating-test-profiles.md).

1. En la interfaz de página de aterrizaje o en el diseñador de contenido, haga clic en el **[!UICONTROL Preview & test]** para acceder a la selección de perfil de prueba.

   ![](../assets/lp_preview-button.png)

1. Seleccione uno o varios perfiles de prueba.

   ![](../assets/lp_test-profiles.png)

   Los pasos para seleccionar perfiles de prueba son los mismos que al probar un mensaje. Se detallan en [esta sección](../preview.md#select-test-profiles).

1. Haga clic en el **[!UICONTROL Preview]** para probar la página de aterrizaje.

   <!--![](../assets/lp_preview.png)-->

1. Los elementos personalizados se sustituyen por los datos de perfil de prueba seleccionados. Seleccione otros perfiles de prueba para previsualizar la renderización de cada variante de la página de aterrizaje.

## Comprobación de alertas {#alerts}

Mientras crea la página de aterrizaje, las alertas le avisan cuando necesita realizar acciones importantes antes de publicarla.

Las alertas se muestran en la parte superior derecha de la pantalla, como se muestra a continuación:

![](../assets/lp_alerts.png)

>[!NOTE]
>
>Si no ve este botón, no se ha detectado ninguna alerta.

Pueden producirse dos tipos de alertas:

* **Advertencias** consulte recomendaciones y prácticas recomendadas. <!--For example, a message will display if -->

* **Errores** impida la publicación del mensaje mientras no se resuelvan. Por ejemplo, un mensaje le avisará de que falta la dirección URL de la página principal.

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> Debe resolver todo **error** alertas antes de la publicación.

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

* 

>[!CAUTION]
>
> To be able to publish your message, you need to resolve all **error** alerts.
-->

## Publicación de la página de aterrizaje {#publish}

Una vez que la página de aterrizaje esté lista, puede publicarla para que esté disponible para su uso en un mensaje o en un sitio web.

![](../assets/lp_publish.png)

>[!CAUTION]
>
>Antes de publicar, compruebe y resuelva las alertas. [Más información](#alerts)

Una vez publicada la página de aterrizaje, se añade a la lista de páginas de aterrizaje con la variable **[!UICONTROL Published]** estado.

Ahora está activo y el vínculo a él está listo para utilizarse en un [message](../create-message.md) y se envían a través de un [recorrido](../building-journeys/journey.md).
