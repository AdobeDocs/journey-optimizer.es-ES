---
solution: Journey Optimizer
product: journey optimizer
title: Creación de una página de aterrizaje
description: Obtenga información sobre cómo configurar y publicar una página de aterrizaje en Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: aterrizaje, página de aterrizaje, creación, publicación
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '1785'
ht-degree: 24%

---

# Creación y publicación de páginas de aterrizaje {#create-lp}

>[!CAUTION]
>
>Para poder probar y publicar páginas de aterrizaje, debe tener **[!UICONTROL Publicar mensajes]** permiso.

Para dirigir a los clientes a una página web definida que desee mostrar cuando hagan clic en un vínculo específico, cree una página de aterrizaje en [!DNL Journey Optimizer], configure la página principal y las subpáginas, pruébelas y publíquelas.

>[!CAUTION]
>
>No puede acceder a la página de aterrizaje simplemente copiando y pegando en un explorador web la URL definida cuando [creación de la página](#create-landing-page), incluso si se ha publicado. En su lugar, puede probarlo con la función de previsualización como se describe en [esta sección](#test-landing-page).

## Acceso a páginas de aterrizaje {#access-landing-pages}

Para acceder a la lista de página de aterrizaje, seleccione **[!UICONTROL Administración de recorrido]** > **[!UICONTROL Páginas de aterrizaje]** en el menú de la izquierda.

![](assets/lp_access-list.png)

El **[!UICONTROL Páginas de aterrizaje]** La lista muestra todos los elementos creados. Puede filtrarlos en función de su estado o fecha de modificación.

![](assets/lp_access-list-filter.png)

Desde esta lista, puede acceder a las [Página de aterrizaje Informe en directo](../reports/lp-report-live.md) o [Página de aterrizaje Informe global](../reports/lp-report-global.md) para elementos publicados.

También puede eliminar, duplicar y cancelar la publicación de una página de aterrizaje.

>[!CAUTION]
>
>Si cancela la publicación de una página de aterrizaje a la que se hace referencia en un mensaje, el vínculo a la página de aterrizaje se interrumpirá y se mostrará una página de error.

Haga clic en los tres puntos junto a una página de aterrizaje para seleccionar la acción deseada.

![](assets/lp_access-list-actions.png)

>[!NOTE]
>
>No puede eliminar un [publicado](#publish-landing-page) página de aterrizaje. Para eliminarlo, primero debe cancelar la publicación.

## Creación de una página de aterrizaje {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_create"
>title="Definir y configurar la página de aterrizaje"
>abstract="Para crear una página de aterrizaje, debe seleccionar un ajuste preestablecido, configurar la página principal y las subpáginas y, por último, probar la página antes de publicarla."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html?lang=es#lp-create-preset" text="Crear ajustes preestablecidos de la página de aterrizaje"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/create-lp.html?lang=es#publish-landing-page" text="Publicar la página de aterrizaje"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_management_labels"
>title="Asignar etiquetas a la página de aterrizaje"
>abstract="Para proteger los recursos digitales confidenciales, puede definir autorizaciones para administrar el acceso a los datos en la página de aterrizaje mediante etiquetas."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/access-control/object-based-access.html?lang=es" text="Control de acceso de nivel de objeto"

Los pasos principales para crear páginas de aterrizaje son los siguientes:

![](assets/lp-creation-process.png)

1. En la lista de página de aterrizaje, haga clic en **[!UICONTROL Crear página de aterrizaje]**.

   ![](assets/lp_create-lp.png)

1. Añada un título. Puede agregar una descripción si es necesario.

   ![](assets/lp_create-lp-details.png)

1. Para asignar etiquetas de uso de datos personalizadas o principales a la página de aterrizaje, seleccione **[!UICONTROL Administrar acceso]**. [Obtenga más información sobre el Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md)

1. Seleccione o cree etiquetas de Adobe Experience Platform en **[!UICONTROL Etiquetas]** para categorizar la página de aterrizaje y mejorar la búsqueda. [Más información](../start/search-filter-categorize.md#tags)

1. Seleccione un ajuste preestablecido. Obtenga información sobre cómo crear ajustes preestablecidos de página de aterrizaje en [esta sección](../landing-pages/lp-presets.md#lp-create-preset).

   ![](assets/lp_create-lp-presets.png)

1. Haga clic en **[!UICONTROL Crear]**.

1. Se muestra la página principal y sus propiedades. Obtenga información sobre cómo configurar la página principal [aquí](#configure-primary-page).

   ![](assets/lp_primary-page.png)

1. Haga clic en el icono + para añadir una subpágina. Obtenga información sobre cómo configurar las opciones de subpágina [aquí](#configure-subpages).

   ![](assets/lp_add-subpage.png)

Una vez que haya configurado y diseñado el [página principal](#configure-primary-page), y el [subpáginas](#configure-subpages) si existe, puede hacer lo siguiente [prueba](#test-landing-page) y [publicar](#publish-landing-page) su página de aterrizaje.

>[!CAUTION]
>
>No puede acceder a la página de aterrizaje simplemente copiando y pegando la URL definida en un explorador web, incluso si se ha publicado. En su lugar, puede probarlo con la función de previsualización como se describe en [esta sección](#test-landing-page).

## Configuración de la página principal {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_primary_page"
>title="Definir la configuración de la página principal"
>abstract="La página principal se muestra inmediatamente a los usuarios después de hacer clic en el vínculo a la página de aterrizaje, por ejemplo, desde un correo electrónico o un sitio web."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html?lang=es" text="Diseñar el contenido de la página de aterrizaje"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings"
>title="Definir la dirección URL de la página de aterrizaje"
>abstract="En esta sección, defina una dirección URL de página de aterrizaje única. La primera parte de la dirección URL requiere que haya configurado previamente un subdominio de página de aterrizaje como parte del ajuste preestablecido que ha seleccionado."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-subdomains.html?lang=es" text="Configurar subdominios de página de aterrizaje"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html?lang=es#lp-create-preset" text="Crear ajustes preestablecidos de la página de aterrizaje"

La página principal es la página que se muestra inmediatamente a los usuarios después de hacer clic en el vínculo a la página de aterrizaje, como desde un correo electrónico o un sitio web.

Para definir la configuración de la página principal, siga los pasos a continuación.

1. Puede cambiar el nombre de la página, que es **[!UICONTROL Página principal]** de forma predeterminada.

1. Edite el contenido de la página con el diseñador de contenido. Aprenda a definir el contenido de la página de aterrizaje [aquí](design-lp.md).

   ![](assets/lp_open-designer.png)

1. Definir la dirección URL de la página de aterrizaje. La primera parte de la URL requiere que haya configurado previamente un subdominio de página de aterrizaje como parte de [preajustar](../landing-pages/lp-presets.md#lp-create-preset) ha seleccionado. [Más información](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >La dirección URL de la página de aterrizaje debe ser única.
   >
   >No puede acceder a la página de aterrizaje simplemente copiando y pegando esta URL en un explorador web, aunque esté publicada. En su lugar, puede probarlo con la función de previsualización como se describe en [esta sección](#test-landing-page).

   ![](assets/lp_access-url.png)

1. Si desea que la página de aterrizaje precargue los datos del formulario que ya están disponibles, seleccione la **[!UICONTROL Rellenar previamente campos de formulario con información de perfil]**.

   ![](assets/lp_prefill-form-fields.png)

   Cuando esta opción está habilitada, si un perfil ya se ha incluido o excluido de una lista de suscripción, sus opciones se reflejarán al mostrar la página de aterrizaje.

   Por ejemplo, si un perfil se ha suscrito para recibir comunicaciones sobre eventos futuros, la casilla de verificación correspondiente ya estará seleccionada la próxima vez que se muestre la página de aterrizaje a ese perfil.

   ![](assets/lp_prefill-form-ex.png)

1. Puede definir una fecha de caducidad para la página. En ese caso, debe seleccionar una acción al expirar la página:

   * **[!UICONTROL URL de redireccionamiento]**: introduzca la dirección URL de la página a la que se redirigirá a los usuarios cuando caduque la página.
   * **[!UICONTROL Página personalizada]**: [Configuración de una subpágina](#configure-subpages) y selecciónelo en la lista desplegable que se muestra.
   * **[!UICONTROL Error del explorador]**: escriba el texto de error que se mostrará en lugar de la página.

   ![](assets/lp_expiry-date.png)

1. En el **[!UICONTROL Datos adicionales]** , defina una o varias claves y sus valores de parámetro correspondientes. Podrá aprovechar estas claves en el contenido de su página principal y de sus subpáginas utilizando [Editor de expresiones](../personalization/personalization-build-expressions.md). Obtenga más información en [esta sección](lp-content.md#use-form-component#use-additional-data).

   ![](assets/lp_create-lp-additional-data.png)

1. Si seleccionó una o más listas de suscripción al [diseño de la página principal](design-lp.md), se muestran en la **[!UICONTROL Lista de suscripción]** sección.

   ![](assets/lp_subscription-list.png)

1. Desde la página de aterrizaje, puede [crear un recorrido](../building-journeys/journey-gs.md#jo-build) que enviará un mensaje de confirmación a los usuarios cuando envíen el formulario. Aprenda a crear un recorrido de este tipo al final de esta [caso de uso](lp-use-cases.md#subscription-to-a-service).

   ![](assets/lp_create-journey.png)

   Clic **[!UICONTROL Crear recorrido]** para que se le redirija a **[!UICONTROL Administración de recorrido]** > **[!UICONTROL Recorridos]** lista.

## Configuración de subpáginas {#configure-subpages}

>[!CONTEXTUALHELP]
>id="ajo_lp_subpage"
>title="Definir la configuración de la subpágina"
>abstract="Se pueden añadir hasta dos subpáginas. Por ejemplo, puede crear una página de agradecimiento que se mostrará una vez que los usuarios envíen el formulario, y puede definir una página de error a la que se llamará si se produce un problema con la página de aterrizaje."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html?lang=es" text="Diseñar el contenido de la página de aterrizaje"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings-subpage"
>title="Definir la dirección URL de la página de aterrizaje"
>abstract="En esta sección, defina una dirección URL de página de aterrizaje única. La primera parte de la dirección URL requiere que haya configurado previamente un subdominio de página de aterrizaje como parte del ajuste preestablecido que ha seleccionado."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-subdomains.html?lang=es" text="Configurar subdominios de página de aterrizaje"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html?lang=es#lp-create-preset" text="Crear ajustes preestablecidos de la página de aterrizaje"

Se pueden añadir hasta dos subpáginas. Por ejemplo, puede crear una página de agradecimiento que se mostrará una vez que los usuarios envíen el formulario, y puede definir una página de error a la que se llamará si se produce un problema con la página de aterrizaje.

Para definir la configuración de la subpágina, siga los pasos a continuación.

1. Puede cambiar el nombre de la página, que es **[!UICONTROL Subpágina 1]** de forma predeterminada.

1. Edite el contenido de la página con el diseñador de contenido. Aprenda a definir el contenido de la página de aterrizaje [aquí](design-lp.md).

   >[!NOTE]
   >
   >Puede insertar un vínculo a la página principal desde cualquier subpágina de la misma página de aterrizaje. Por ejemplo, para redirigir a los usuarios que cometieron un error y desean suscribirse de nuevo, puede agregar un vínculo de la subpágina de confirmación a la página principal de suscripción. Obtenga información sobre cómo insertar vínculos en [esta sección](../email/message-tracking.md#insert-links).

1. Definir la dirección URL de la página de aterrizaje. La primera parte de la URL requiere que haya configurado previamente un subdominio de página de aterrizaje. [Más información](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >La dirección URL de la página de aterrizaje debe ser única.
   >
   >No puede acceder a la subpágina simplemente copiando y pegando esta URL en un explorador web, aunque esté publicada. En su lugar, puede probarlo con la función de previsualización como se describe en [esta sección](#test-landing-page).

![](assets/lp_subpage-settings.png)

## Prueba de la página de aterrizaje {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ac_preview_lp_profiles"
>title="Previsualizar y probar la página de aterrizaje"
>abstract="Una vez que haya definido la configuración y el contenido de la página de aterrizaje, puede utilizar perfiles de prueba para previsualizarlos."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/profiles/creating-test-profiles.html?lang=es" text="Seleccionar perfiles de prueba"

Una vez definida la configuración y el contenido de la página de aterrizaje, puede utilizar perfiles de prueba para previsualizarlo. Si ha insertado [contenido personalizado](../personalization/personalize.md), podrá comprobar cómo se muestra este contenido en la página de aterrizaje mediante los datos de perfil de prueba.

>[!CAUTION]
>
>Para poder probar las páginas de aterrizaje, debe tener el **[!UICONTROL Publicar mensajes]** permiso.
>
>Debe tener perfiles de prueba disponibles para poder previsualizar los mensajes y enviar pruebas. Obtenga información sobre cómo [creación de perfiles de prueba](../audience/creating-test-profiles.md).

1. En la interfaz de la página de aterrizaje, haga clic en **[!UICONTROL Simular contenido]** para acceder a la selección del perfil de prueba.

   ![](assets/lp_simulate-button.png)

   >[!NOTE]
   >
   >El **[!UICONTROL Simular contenido]** también se puede acceder a este botón desde el diseñador de contenido.

1. Desde el **[!UICONTROL Simular]** , seleccione uno o más perfiles de prueba.

   ![](assets/lp_test-profiles.png)

   Los pasos para seleccionar perfiles de prueba son los mismos que al probar un mensaje. Se encuentran detalladas en la [Gestión de contenido](../content-management/test-profiles.md) sección.

1. Seleccionar **[!UICONTROL Abrir vista previa]** para probar la página de aterrizaje.

   ![](assets/lp_open-preview.png)

1. La vista previa de la página de aterrizaje se abrirá en una nueva pestaña. Los elementos personalizados se sustituyen por los datos de perfil de prueba seleccionados.

   <!--![](assets/lp_preview.png)-->

1. Seleccione otros perfiles de prueba para previsualizar el procesamiento de cada variante de la página de aterrizaje.

## Comprobación de alertas {#check-alerts}

Mientras crea la página de aterrizaje, las alertas le avisan cuando debe realizar acciones importantes antes de publicar.

Las alertas se muestran en la parte superior derecha de la pantalla, como se muestra a continuación:

![](assets/lp_alerts.png)

>[!NOTE]
>
>Si no ve este botón, no se ha detectado ninguna alerta.

Pueden producirse dos tipos de alertas:

* **Advertencias** consulte recomendaciones y prácticas recomendadas. <!--For example, a message will display if -->

* **Errores** evite publicar la página de aterrizaje siempre y cuando no se resuelvan. Por ejemplo, recibirá una advertencia si falta la dirección URL de la página principal.

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> Debe resolver todos los **error** alertas antes de la publicación.

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

* 

>[!CAUTION]
>
> To be able to publish your message, you must resolve all **error** alerts.
-->

## Publicar la página de aterrizaje {#publish-landing-page}

>[!CAUTION]
>
>Para poder publicar páginas de aterrizaje, debe tener el **[!UICONTROL Publicar mensajes]** permiso.

Una vez que la página de aterrizaje esté lista, puede publicarla para que esté disponible para usarla en un mensaje.

![](assets/lp_publish.png)

>[!CAUTION]
>
>Antes de publicar, compruebe y resuelva las alertas. [Más información](#check-alerts)

Una vez publicada la página de aterrizaje, se añade a la lista de página de aterrizaje con el **[!UICONTROL Publicado]** estado.

Ahora está activo y listo para utilizarse en un [!DNL Journey Optimizer] mensaje que se enviará a través de un [recorrido](../building-journeys/journey.md).

>[!NOTE]
>
>No puede acceder a la página de aterrizaje simplemente copiando y pegando en un explorador web la URL definida cuando [creación de la página](#create-landing-page), incluso si se ha publicado. En su lugar, puede probarlo con la función de previsualización como se describe en [esta sección](#test-landing-page).

Puede monitorizar el impacto de su página de aterrizaje a través de informes específicos. [Más información](../reports/lp-report-live.md)
