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
source-git-commit: c082d9329949fd8dc68929e3934daf2d9dfdbd46
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Configuración de subdominios dinámicos de correo electrónico {#surface-personalization}

Para obtener una mayor flexibilidad y control sobre la configuración de correo electrónico, al crear superficies de correo electrónico, [!DNL Journey Optimizer] permite definir valores personalizados para subdominios, encabezados y parámetros de seguimiento de URL.

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

Para definir subdominios dinámicos, siga los pasos a continuación.

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

   Todos los destinatarios basados en Estados Unidos recibirán mensajes utilizando el subdominio seleccionado para ese país, lo que significa que todas las URL involucradas (como la página espejo, la URL de seguimiento o el vínculo de cancelación de suscripción) se rellenarán en función de ese subdominio.

1. Establezca otro subdominio dinámico como desee. Puede añadir hasta 50 elementos.

   ![](assets/surface-email-add-dynamic-subdomain.png)

1. Seleccione el [Grupo de IP](../configuration/ip-pools.md) para asociarlo con la superficie. [Más información](email-settings.md#subdomains-and-ip-pools)

Una vez que haya agregado uno o más subdominios dinámicos a una superficie, se rellenarán los siguientes elementos en función del subdominio dinámico resuelto para esta superficie:

* Todas las direcciones URL (URL de recurso, URL de página espejo y URL de seguimiento)

* El [URL de cancelación de suscripción](email-settings.md#list-unsubscribe)

* El **Desde correo electrónico** y **Correo electrónico de error** sufijos

## Personalice el encabezado (#personalize-header)

También se puede utilizar la personalización para todos los parámetros de cabecera definidos en una superficie.

Por ejemplo, si tiene varias marcas, puede crear una sola superficie y utilizar valores personalizados para los encabezados de correo electrónico. Esto le permite asegurarse de que todos los correos electrónicos enviados desde sus diferentes marcas se dirijan a cada uno de sus clientes con la dirección correcta **Desde** nombres y correos electrónicos. Del mismo modo, cuando los destinatarios pulsen el botón **Responder** en el software de cliente de correo electrónico, desea el **Responder a** los nombres y correos electrónicos corresponden a la marca correcta del usuario correcto.

Para utilizar variables personalizadas para los parámetros de encabezado de superficie, siga los pasos a continuación.

1. Defina los parámetros de encabezado como lo haría normalmente. [Descubra cómo](email-settings.md#email-header)

1. Para cada campo, seleccione el icono Editar.

   ![](assets/surface-email-personalize-header.png)

1. El [Editor de expresiones](../personalization/personalization-build-expressions.md) abre. Defina la condición como desee y guarde los cambios.<!--In this example, set a condition such as -->

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

select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->
