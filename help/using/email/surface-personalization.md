---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de subdominios dinámicos de correo electrónico
description: Obtenga información sobre cómo configurar subdominios dinámicos en el nivel de superficie de canal de correo electrónico
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: configuración, correo electrónico, configuración, subdominio
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: 94d39089d94b4fe42eb3fb95603426012b104517
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# Personalizar configuración de superficie de correo electrónico {#surface-personalization}

Para obtener una mayor flexibilidad y control sobre la configuración de correo electrónico, [!DNL Journey Optimizer] permite definir valores personalizados para subdominios y encabezados<!--and URL tracking parameters--> al crear superficies de correo electrónico.

>[!AVAILABILITY]
>
>Actualmente, esta funcionalidad está disponible como una versión beta para seleccionar solo usuarios. <!--To join the beta program, contact Adobe Customer Care.-->

## Adición de subdominios dinámicos {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalización no disponible"
>abstract="Esta superficie se creó sin atributos de personalización. Consulte la documentación para ver los pasos que debe seguir si es necesaria la personalización."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Habilitar subdominios dinámicos"
>abstract="Al crear una superficie de correo electrónico, puede configurar subdominios dinámicos basados en condiciones que defina con el Editor de expresiones. Puede añadir hasta 50 subdominios dinámicos."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Algunos subdominios pueden no estar disponibles"
>abstract="Algunos subdominios no están disponibles actualmente para su selección debido a que está pendiente el registro del bucle de comentarios. Este proceso puede tardar hasta 10 días hábiles. Una vez finalizado, puede elegir entre todos los subdominios disponibles."

Al crear una superficie de correo electrónico, puede configurar subdominios dinámicos basados en condiciones específicas.

Por ejemplo, si tiene restricciones legales para enviar mensajes desde una dirección de correo electrónico dedicada por país, puede utilizar subdominios dinámicos. Esto le permite crear una sola superficie con varios subdominios de envío correspondientes a diferentes países, en lugar de crear varias superficies para cada país. A continuación, puede dirigirse a clientes basados en varios países consolidados en una campaña.

Para definir subdominios dinámicos en una superficie de canal de correo electrónico, siga los pasos a continuación.

1. Antes de crear una superficie, configure los subdominios que desee utilizar para enviar correos electrónicos según el caso de uso. [Descubra cómo](../configuration/about-subdomain-delegation.md)

   Por ejemplo, supongamos que desea utilizar diferentes subdominios para diferentes países: configure un subdominio específico de EE. UU., uno específico de Reino Unido, etc.

1. Cree una superficie de canal. [Descubra cómo](../configuration/channel-surfaces.md)

1. Seleccione el **[!UICONTROL Correo electrónico]** canal.

1. En el **Subdominio** , habilite la sección **[!UICONTROL Subdominio dinámico]** opción.

   ![](assets/surface-email-dynamic-subdomain.png)

1. Seleccione el icono Editar junto al primero **[!UICONTROL Condición]** field.

1. El [Editor de expresiones](../personalization/personalization-build-expressions.md) abre. En este ejemplo, defina una condición como `Country` igual a `US`.

   ![](assets/surface-email-edit-condition.png)

1. Seleccione el subdominio que desea asociar con esta condición. [Más información sobre los subdominios](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Algunos subdominios no están disponibles actualmente para su selección debido a que están pendientes [bucle de retroalimentación](../reports/deliverability.md#feedback-loops) registro. Este proceso puede tardar hasta 10 días hábiles. Una vez finalizado, puede elegir entre todos los subdominios disponibles. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Todos los destinatarios basados en EE. UU. recibirán mensajes utilizando el subdominio seleccionado para ese país, lo que significa que todas las URL involucradas (como la página espejo, la URL de seguimiento o el vínculo de cancelación de suscripción) se rellenarán en función de ese subdominio.

1. Establezca otros subdominios dinámicos como desee. Puede añadir hasta 50 elementos.

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the surface. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. Definir todos los demás [configuración de correo electrónico](email-settings.md) y [enviar](../configuration/channel-surfaces.md#create-channel-surface) su superficie.

Una vez que haya agregado uno o más subdominios dinámicos a una superficie, se rellenarán los siguientes elementos en función del subdominio dinámico resuelto para esta superficie:

* Todas las direcciones URL (URL de recurso, URL de página espejo y URL de seguimiento)

* El [URL de cancelación de suscripción](email-settings.md#list-unsubscribe)

* El **Desde correo electrónico** y **Correo electrónico de error** sufijos

>[!NOTE]
>
>Si configura subdominios dinámicos y, a continuación, deshabilita la variable **[!UICONTROL Subdominio dinámico]** opción, se eliminan todos los valores dinámicos. Seleccione un subdominio y envíe la superficie para que los cambios surtan efecto.

## Personalice el encabezado {#personalize-header}

También se puede utilizar la personalización para todos los parámetros de cabecera definidos en una superficie.

Por ejemplo, si tiene varias marcas, puede crear una sola superficie y utilizar valores personalizados para los encabezados de correo electrónico. Esto le permite asegurarse de que todos los correos electrónicos enviados desde sus diferentes marcas se dirijan a cada uno de sus clientes con la dirección correcta **Desde** nombres y correos electrónicos. Del mismo modo, cuando los destinatarios pulsen el botón **Responder** en el software de cliente de correo electrónico, desea el **Responder a** los nombres y correos electrónicos corresponden a la marca correcta del usuario correcto.

Para utilizar variables personalizadas para los parámetros de encabezado de superficie, siga los pasos a continuación.

>[!NOTE]
>
>Puede personalizar todas las **[!UICONTROL Parámetros de encabezado]** campos, excepto el **[!UICONTROL Error de prefijo de correo electrónico]** field.


1. Defina los parámetros de encabezado como lo haría normalmente. [Descubra cómo](email-settings.md#email-header)

1. Para cada campo, seleccione el icono Editar.

   ![](assets/surface-email-personalize-header.png)

1. El [Editor de expresiones](../personalization/personalization-build-expressions.md) abre. Defina la condición como desee y guarde los cambios.

   Por ejemplo, configure una condición como que cada destinatario reciba un correo electrónico de su propio representante de marca.

   >[!NOTE]
   >
   >Solo puede seleccionar **[!UICONTROL Atributos de perfil]** y **[!UICONTROL Funciones de ayuda]**.

1. Repita los pasos anteriores para cada parámetro al que desee agregar personalización.

>[!NOTE]
>
>Si ha añadido uno o más subdominios dinámicos a la superficie, la variable **Desde correo electrónico** y **Correo electrónico de error** los sufijos se rellenarán en función del [subdominio dinámico](#dynamic-subdomains).

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## Ver detalles de superficie {#view-surface-details}

Al utilizar una superficie con configuración personalizada en una campaña o superficie, puede mostrar los detalles de la superficie directamente dentro de la campaña o superficie. Siga los pasos a continuación.

1. Creación de un correo electrónico [campaña](../campaigns/create-campaign.md) o [recorrido](../building-journeys/journey-gs.md).

1. Seleccione el **[!UICONTROL Editar contenido]** botón.

1. Haga clic en **[!UICONTROL Ver detalles de superficie]** botón.

   ![](assets/campaign-view-surface-details.png)

1. El **[!UICONTROL Configuración de envío]** se muestra la ventana. Se pueden ver todos los ajustes de superficie, incluidos los subdominios dinámicos y los parámetros de cabecera personalizados.

   >[!NOTE]
   >
   >Toda la información de esta pantalla es de solo lectura.

1. Seleccionar **[!UICONTROL Expandir]** para mostrar los detalles de los subdominios dinámicos.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
