---
solution: Journey Optimizer
product: journey optimizer
title: Personalizar configuración de correo electrónico
description: Aprenda a definir valores personalizados para su configuración en el nivel de configuración del canal de correo electrónico
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: configuración, correo electrónico, configuración, subdominio
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 6%

---

# Personalizar configuración de correo electrónico {#surface-personalization}

Para obtener más flexibilidad y control sobre la configuración del correo electrónico, [!DNL Journey Optimizer] le permite definir valores personalizados para subdominios, encabezados y parámetros de seguimiento de URL al crear configuraciones de correo electrónico.

## Añadir subdominios dinámicos {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalización no disponible"
>abstract="Esta configuración se ha creado sin ningún atributo de personalización. Consulte la documentación para ver los pasos que debe seguir en caso de que sea necesaria la personalización."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Habilitación de subdominios dinámicos"
>abstract="Al crear una configuración de correo electrónico, puede configurar subdominios dinámicos basados en condiciones que defina con el editor de personalización. Se pueden añadir hasta 50 subdominios dinámicos."

Al crear una configuración de correo electrónico, puede configurar subdominios dinámicos basados en condiciones específicas.

Por ejemplo, si tiene restricciones legales para enviar mensajes desde una dirección de correo electrónico dedicada por país, puede utilizar subdominios dinámicos. Esto le permite crear una sola configuración con varios subdominios de envío correspondientes a diferentes países, en lugar de crear varias configuraciones para cada país. A continuación, puede dirigirse a clientes basados en varios países consolidados en una campaña.

Para definir subdominios dinámicos en una configuración de canal de correo electrónico, siga los pasos a continuación.

1. Antes de crear una configuración de, configure los subdominios que desee utilizar para enviar correos electrónicos según el caso de uso. [Descubra cómo](../configuration/about-subdomain-delegation.md)

   Por ejemplo, supongamos que desea utilizar diferentes subdominios para diferentes países: configure un subdominio específico de EE. UU., uno específico de Reino Unido, etc.

1. Cree una configuración de canal. [Descubra cómo](../configuration/channel-surfaces.md)

1. Seleccione el canal **[!UICONTROL Correo electrónico]**.

1. En la sección **Subdominio**, habilite la opción **[!UICONTROL Subdominio dinámico]**.

   ![](assets/surface-email-dynamic-subdomain.png)

1. Seleccione el icono Editar junto al primer campo **[!UICONTROL Condición]**.

1. Se abre [editor de personalización](../personalization/personalization-build-expressions.md). En este ejemplo, establezca una condición como `Country` igual a `US`.

   ![](assets/surface-email-edit-condition.png)

1. Seleccione el subdominio que desea asociar con esta condición. [Más información sobre los subdominios](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Algunos subdominios no están disponibles actualmente para su selección debido al registro pendiente de [feedback loop](../reports/deliverability.md#feedback-loops). Este proceso puede tardar hasta 10 días hábiles. Una vez finalizado, puede elegir entre todos los subdominios disponibles. <!--where FL registration happens? is it when delegating a subdomain and you are awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Todos los destinatarios basados en EE. UU. recibirán mensajes utilizando el subdominio seleccionado para ese país, lo que significa que todas las URL involucradas (como la página espejo, la URL de seguimiento o el vínculo de cancelación de suscripción) se rellenarán en función de ese subdominio.

1. Establezca otros subdominios dinámicos como desee. Puede añadir hasta 50 elementos.

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the configuration. [Learn more](email-settings.md#ip-pools)-->

1. Defina todas las demás [configuraciones de correo electrónico](email-settings.md) y [envíe](../configuration/channel-surfaces.md#create-channel-surface) su configuración.

Una vez que haya agregado uno o más subdominios dinámicos a una configuración, los siguientes elementos se rellenarán en función del subdominio dinámico resuelto para esta configuración:

* Todas las direcciones URL (URL de recurso, URL de página espejo y URL de seguimiento)

* La [URL para cancelar la suscripción](email-settings.md#list-unsubscribe)

* Los sufijos **De correo electrónico** y **Correo electrónico de error**

>[!NOTE]
>
>Si configura subdominios dinámicos y luego deshabilita la opción **[!UICONTROL Subdominio dinámico]**, se eliminarán todos los valores dinámicos. Seleccione un subdominio y envíe la configuración para que los cambios surtan efecto.

## Personalice el encabezado {#personalize-header}

También puede utilizar la personalización para todos los parámetros de encabezado definidos en una configuración.

Por ejemplo, si tiene varias marcas, puede crear una sola configuración y utilizar valores personalizados para los encabezados de correo electrónico. Esto le permite asegurarse de que todos los correos electrónicos enviados desde sus diferentes marcas se dirijan a cada uno de sus clientes con los nombres y correos electrónicos correctos de **From**. Del mismo modo, cuando los destinatarios presionen el botón **Responder** en el software de cliente de correo electrónico, querrá que los nombres y correos electrónicos de **Responder a** correspondan a la marca correcta para el usuario correcto.

Para utilizar variables personalizadas para los parámetros de encabezado de la configuración, siga los pasos a continuación.

>[!NOTE]
>
>Puede personalizar todos los campos **[!UICONTROL Parámetros de encabezado]**, excepto el campo **[!UICONTROL Prefijo de correo electrónico de error]**.

1. Defina los parámetros de encabezado como lo haría normalmente. [Descubra cómo](email-settings.md#email-header)

1. Para cada campo, seleccione el icono Editar.

   ![](assets/surface-email-personalize-header.png)

1. Se abre [editor de personalización](../personalization/personalization-build-expressions.md). Defina la condición como desee y guarde los cambios.

   <!--For example, set a condition such as each recipient receives an email from their own brand representative.-->

   >[!NOTE]
   >
   >Solo puede seleccionar **[!UICONTROL atributos de perfil]** y **[!UICONTROL funciones de ayuda]**.

   Por ejemplo, desea gestionar dinámicamente los correos electrónicos enviados en nombre de un administrador de relaciones, cuyos detalles se almacenan en el perfil del cliente, de modo que cada cliente esté vinculado a un administrador de relaciones. En un [recorrido](../building-journeys/journey-gs.md), el encabezado del correo electrónico (nombre del remitente, correo electrónico del remitente, dirección de respuesta) se puede personalizar con los parámetros del administrador de relaciones, tomados de los atributos del perfil.

   <!--The examples below use event parameters, which are currently not available.
    
    Let's say you want to handle dynamically emails sent on behalf of a sales assistant, where the sales assistant is retrieved from an event or campaign contextual parameters. For example: In a [journey](../building-journeys/journey-gs.md), when a purchase event is linked to the sales assistant of a specific shop, the email header (sender name, sender email, reply to address) can be personalized with the sales assistant parameters, taken from the event attributes. In an [API-triggered campaign](../campaigns/api-triggered-campaigns.md), initiated externally by a sales assistant, the triggered email can be sent on behalf of the sales assistant and the header personalization values taken from campaign contextual parameters.-->

1. Repita los pasos anteriores para cada parámetro al que desee agregar personalización.

>[!NOTE]
>
>Si agregó uno o más subdominios dinámicos a la configuración, los sufijos **De correo electrónico** y **Error de correo electrónico** se rellenarán en función del [subdominio dinámico](#dynamic-subdomains) resuelto.

## Usar seguimiento de URL personalizado {#personalize-url-tracking}

Para utilizar parámetros de seguimiento de URL personalizados, siga los pasos a continuación.

1. Vaya a la sección **[!UICONTROL parámetros de seguimiento de URL]** de la configuración de su canal de correo electrónico. [Más información](url-tracking.md)

1. Haga clic en el icono Editar junto a cada campo. Además de los atributos contextuales, puede seleccionar atributos de perfil.

1. Seleccione el atributo de perfil que desee en [editor de personalización](../personalization/personalization-build-expressions.md).

1. Repita los pasos anteriores para cada parámetro de seguimiento que desee personalizar.

Ahora, cuando se envía el correo electrónico, el parámetro personalizado se anexa automáticamente al final de la dirección URL. A continuación, puede capturar este parámetro en las herramientas de análisis web o en los informes de rendimiento.

## Ver detalles de configuración {#view-surface-details}

Al utilizar una configuración con configuración personalizada en una campaña o un recorrido, puede mostrar los detalles de configuración directamente en la campaña o el recorrido. Siga los pasos a continuación.

1. Crear un correo electrónico [campaña](../campaigns/create-campaign.md) o [recorrido](../building-journeys/journey-gs.md).

1. Seleccione el botón **[!UICONTROL Editar contenido]**.

1. Haga clic en el botón **[!UICONTROL Ver detalles de configuración]**.

   ![](assets/campaign-view-surface-details.png)

1. Se muestra la ventana **[!UICONTROL Configuración de envío]**. Puede ver todas las opciones de configuración, incluidos los subdominios dinámicos y los parámetros de encabezado personalizados.

   >[!NOTE]
   >
   >Toda la información de esta pantalla es de solo lectura.

1. Seleccione **[!UICONTROL Expand]** para mostrar los detalles de los subdominios dinámicos.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)

## Compruebe la configuración {#check-configuration}

Al utilizar una configuración personalizada en una campaña o un recorrido, puede obtener una vista previa del contenido del correo electrónico mediante perfiles de prueba para comprobar posibles errores con la configuración dinámica definida. Siga los pasos a continuación.

>[!NOTE]
>
>Además de los perfiles de prueba, [!DNL Journey optimizer] también le permite probar distintas variantes del contenido mediante la vista previa y el envío de pruebas utilizando datos de entrada de muestra cargados desde un archivo CSV/JSON, o agregados manualmente. [Aprenda a simular variaciones de contenido](../test-approve/simulate-sample-input.md)

Para obtener una vista previa del contenido mediante perfiles de prueba, siga estos pasos:

1. En la pantalla Editar contenido del mensaje o en el Designer de correo electrónico, haga clic en el botón **[!UICONTROL Simular contenido]**. [Más información](../content-management/preview.md)

1. Seleccione un [perfil de prueba](../content-management/test-profiles.md).

1. Si se muestra un error, haga clic en el botón **[!UICONTROL Ver detalles de configuración]**.

   ![](assets/campaign-simulate-config-error.png)

1. Consulte la pantalla **[!UICONTROL Configuración de envío]** para ver los detalles del error.

   ![](assets/campaign-simulate-config-details.png)

Los posibles errores pueden ser los siguientes:

* El **subdominio** no se resolvió para el perfil de prueba seleccionado. Por ejemplo, la configuración utiliza varios subdominios de envío correspondientes a diferentes países, pero el perfil seleccionado no tiene un valor definido para el atributo `Country` o el atributo está establecido en `France`, pero este valor no está asociado a ningún subdominio de esa configuración.

* El perfil seleccionado no tiene valores asociados para uno o más **parámetros de encabezado**.

Con cualquiera de estos errores, no se envía un correo electrónico al perfil de prueba seleccionado.

Para evitar este tipo de error, asegúrese de que los parámetros de encabezado definidos utilizan atributos personalizados con valores para la mayoría de los perfiles. Los valores que faltan pueden afectar a la entrega de correo electrónico.

>[!NOTE]
>
>Obtenga más información acerca de la capacidad de entrega en [esta sección](../reports/deliverability.md)
