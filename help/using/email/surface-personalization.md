---
solution: Journey Optimizer
product: journey optimizer
title: Personalización de la configuración de superficie del correo electrónico
description: Aprenda a definir valores personalizados para su configuración en el nivel de superficie de canal de correo electrónico
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: configuración, correo electrónico, configuración, subdominio
badge: label="Disponibilidad limitada"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: 2cd62c97bef156d0c1e7dda8a962be789f8131de
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 17%

---

# Personalización de la configuración de superficie del correo electrónico {#surface-personalization}

Para obtener una mayor flexibilidad y control sobre la configuración del correo electrónico, [!DNL Journey Optimizer] le permite definir valores personalizados para subdominios y encabezados<!--and URL tracking parameters--> al crear superficies de correo electrónico.

>[!AVAILABILITY]
>
>Actualmente, la personalización de la superficie del correo electrónico solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

## Añadir subdominios dinámicos {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalización no disponible"
>abstract="Esta superficie se ha creado sin ningún atributo de personalización. Consulte la documentación para ver los pasos que debe seguir en caso de que sea necesaria la personalización."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Habilitación de subdominios dinámicos"
>abstract="Al crear una superficie de correo electrónico, puede configurar subdominios dinámicos basados en condiciones que defina con el editor de personalización. Se pueden añadir hasta 50 subdominios dinámicos."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Algunos subdominios podrían no estar disponibles"
>abstract="Algunos subdominios no están disponibles actualmente para su selección debido a que está pendiente el registro del bucle de comentarios. Este proceso puede tardar hasta 10 días hábiles. Una vez finalizado, puede elegir entre todos los subdominios disponibles."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation" text="Introducción a la delegación de subdominios"

Al crear una superficie de correo electrónico, puede configurar subdominios dinámicos basados en condiciones específicas.

Por ejemplo, si tiene restricciones legales para enviar mensajes desde una dirección de correo electrónico dedicada por país, puede utilizar subdominios dinámicos. Esto le permite crear una sola superficie con varios subdominios de envío correspondientes a diferentes países, en lugar de crear varias superficies para cada país. A continuación, puede dirigirse a clientes basados en varios países consolidados en una campaña.

Para definir subdominios dinámicos en una superficie de canal de correo electrónico, siga los pasos a continuación.

1. Antes de crear una superficie, configure los subdominios que desee utilizar para enviar correos electrónicos según el caso de uso. [Descubra cómo](../configuration/about-subdomain-delegation.md)

   Por ejemplo, supongamos que desea utilizar diferentes subdominios para diferentes países: configure un subdominio específico de EE. UU., uno específico de Reino Unido, etc.

1. Cree una superficie de canal. [Descubra cómo](../configuration/channel-surfaces.md)

1. Seleccione el canal **[!UICONTROL Correo electrónico]**.

1. En la sección **Subdominio**, habilite la opción **[!UICONTROL Subdominio dinámico]**.

   ![](assets/surface-email-dynamic-subdomain.png)

1. Seleccione el icono Editar junto al primer campo **[!UICONTROL Condición]**.

1. Se abre [editor de personalización](../personalization/personalization-build-expressions.md). En este ejemplo, establezca una condición como `Country` igual a `US`.

   ![](assets/surface-email-edit-condition.png)

1. Seleccione el subdominio que desea asociar con esta condición. [Más información sobre los subdominios](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Algunos subdominios no están disponibles actualmente para su selección debido al registro pendiente de [feedback loop](../reports/deliverability.md#feedback-loops). Este proceso puede tardar hasta 10 días hábiles. Una vez finalizado, puede elegir entre todos los subdominios disponibles. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Todos los destinatarios basados en EE. UU. recibirán mensajes utilizando el subdominio seleccionado para ese país, lo que significa que todas las URL involucradas (como la página espejo, la URL de seguimiento o el vínculo de cancelación de suscripción) se rellenarán en función de ese subdominio.

1. Establezca otros subdominios dinámicos como desee. Puede añadir hasta 50 elementos.

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the surface. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. Defina el resto de la [configuración de correo electrónico](email-settings.md) y [envíe](../configuration/channel-surfaces.md#create-channel-surface) su superficie.

Una vez que haya agregado uno o más subdominios dinámicos a una superficie, se rellenarán los siguientes elementos en función del subdominio dinámico resuelto para esta superficie:

* Todas las direcciones URL (URL de recurso, URL de página espejo y URL de seguimiento)

* La [URL para cancelar la suscripción](email-settings.md#list-unsubscribe)

* Los sufijos **De correo electrónico** y **Correo electrónico de error**

>[!NOTE]
>
>Si configura subdominios dinámicos y luego deshabilita la opción **[!UICONTROL Subdominio dinámico]**, se eliminarán todos los valores dinámicos. Seleccione un subdominio y envíe la superficie para que los cambios surtan efecto.

## Personalice el encabezado {#personalize-header}

También se puede utilizar la personalización para todos los parámetros de cabecera definidos en una superficie.

Por ejemplo, si tiene varias marcas, puede crear una sola superficie y utilizar valores personalizados para los encabezados de correo electrónico. Esto le permite asegurarse de que todos los correos electrónicos enviados desde sus diferentes marcas se dirijan a cada uno de sus clientes con los nombres y correos electrónicos correctos de **From**. Del mismo modo, cuando los destinatarios presionen el botón **Responder** en el software de cliente de correo electrónico, querrá que los nombres y correos electrónicos de **Responder a** correspondan a la marca correcta para el usuario correcto.

Para utilizar variables personalizadas para los parámetros de encabezado de superficie, siga los pasos a continuación.

>[!NOTE]
>
>Puede personalizar todos los campos **[!UICONTROL Parámetros de encabezado]**, excepto el campo **[!UICONTROL Prefijo de correo electrónico de error]**.


1. Defina los parámetros de encabezado como lo haría normalmente. [Descubra cómo](email-settings.md#email-header)

1. Para cada campo, seleccione el icono Editar.

   ![](assets/surface-email-personalize-header.png)

1. Se abre [editor de personalización](../personalization/personalization-build-expressions.md). Defina la condición como desee y guarde los cambios.

   Por ejemplo, configure una condición como que cada destinatario reciba un correo electrónico de su propio representante de marca.

   >[!NOTE]
   >
   >Solo puede seleccionar **[!UICONTROL atributos de perfil]** y **[!UICONTROL funciones de ayuda]**.

1. Repita los pasos anteriores para cada parámetro al que desee agregar personalización.

>[!NOTE]
>
>Si agregó uno o más subdominios dinámicos a su superficie, los sufijos **De correo electrónico** y **Error de correo electrónico** se rellenarán en función del [subdominio dinámico](#dynamic-subdomains) resuelto.

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the personalization editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## Ver detalles de superficie {#view-surface-details}

Al utilizar una superficie con configuración personalizada en una campaña o superficie, puede mostrar los detalles de la superficie directamente dentro de la campaña o superficie. Siga los pasos a continuación.

1. Crear un correo electrónico [campaña](../campaigns/create-campaign.md) o [recorrido](../building-journeys/journey-gs.md).

1. Seleccione el botón **[!UICONTROL Editar contenido]**.

1. Haga clic en el botón **[!UICONTROL Ver detalles de superficie]**.

   ![](assets/campaign-view-surface-details.png)

1. Se muestra la ventana **[!UICONTROL Configuración de envío]**. Se pueden ver todos los ajustes de superficie, incluidos los subdominios dinámicos y los parámetros de cabecera personalizados.

   >[!NOTE]
   >
   >Toda la información de esta pantalla es de solo lectura.

1. Seleccione **[!UICONTROL Expand]** para mostrar los detalles de los subdominios dinámicos.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
