---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de subdominios web
description: Obtenga información sobre cómo configurar subdominios web con Journey Optimizer
role: Admin
feature: Web Channel, Subdomains
level: Experienced
keywords: web, subdominios, configuración
exl-id: 6e00466d-4ce5-4d80-89ff-c7331a5ab158
source-git-commit: ce8818e0216d4f633770fecadd4e74c2651a62f3
workflow-type: tm+mt
source-wordcount: '1075'
ht-degree: 20%

---

# Configuración de subdominios web {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Delegación de un subdominio web"
>abstract="Se configurará el subdominio para el uso del canal web. Puede utilizar un subdominio que ya esté delegado en Adobe o configurar otro subdominio."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Delegación de un subdominio web"
>abstract="Si añade contenido procedente de Adobe Experience Manager Assets a sus experiencias web, debe configurar el subdominio que se utilizará para publicar este contenido. Seleccione entre los subdominios ya delegados a Adobe o configure un nuevo subdominio."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Definición de un subdominio web"
>abstract="Seleccione un subdominio de la lista de subdominios delegados en Adobe. Puede establecer este subdominio web como el predeterminado, pero solo se puede utilizar un subdominio predeterminado a la vez."

When authoring web experiences, if you add content coming from the [Adobe Experience Manager Assets](../integrations/assets.md) library, you  must set up the subdomain that will be used to publish this content.

You can use a subdomain that is already delegated to Adobe, or you can configure another subdomain. Learn more about delegating subdomains to Adobe in [this section](../configuration/delegate-subdomain.md).

Web subdomain configuration is **common to all environments**. Por lo tanto:

* Para acceder y editar subdominios web, debe tener el permiso **[!UICONTROL Administrar subdominios web]** en la zona protegida de producción.

* Cualquier modificación en un subdominio web también afectará a los entornos limitados de producción.

Puede crear varios subdominios web, pero solo se utilizará el subdominio **default**. Puede cambiar el subdominio web predeterminado, pero solo se puede utilizar uno a la vez.

## Acceso y administración de subdominios web {#access-web-subdomains}

1. Go to the **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu, then select **[!UICONTROL Web settings]** > **[!UICONTROL Web subdomains]**. All the subdomains set up with the current sandbox are displayed.

   ![](assets/web-access-subdomains.png)

1. Puede filtrar el usuario que delegó cada subdominio o uno el estado de delegación (**[!UICONTROL Borrador]**, **[!UICONTROL Procesamiento]**, **[!UICONTROL Éxito]** o **[!UICONTROL Error]**).

   ![](assets/web-filter-subdomains.png)

1. El distintivo **[!UICONTROL Default]** se muestra junto al subdominio que se usa actualmente como predeterminado. Para cambiar el subdominio predeterminado, seleccione **[!UICONTROL Establecer como predeterminado]** en el botón **[!UICONTROL Más acciones]** situado junto al subdominio deseado.

   ![](assets/web-subdomain-default.png)

   Puede cambiar el subdominio web predeterminado, pero solo se puede utilizar uno a la vez.

## Usar un subdominio existente {#web-use-existing-subdomain}

Para utilizar un subdominio que ya se haya delegado a Adobe, siga los pasos a continuación.

1. Acceda al menú **[!UICONTROL Administración]** > **[!UICONTROL Canales]** y, a continuación, seleccione **[!UICONTROL Configuración web]** > **[!UICONTROL subdominios web]**.

1. Haga clic en **[!UICONTROL Configurar subdominio]**.

1. Seleccione la opción **[!UICONTROL Usar subdominio delegado]** de la sección **[!UICONTROL Tipo de configuración]** y elija un subdominio delegado de la lista.

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >No puede seleccionar un subdominio que ya se esté utilizando como subdominio web.

1. El prefijo que se mostrará en la URL web se añade automáticamente. No puede cambiarlo.

1. To set this subdomain as default, select the corresponding option.

   ![](assets/web-subdomain-details-default.png)

   Only the **default** subdomain will be used.

1. Click **[!UICONTROL Submit]**. The subdomain gets the **[!UICONTROL Success]** status. It is ready to be used for your web experiences.

   In very rare occasions, a subdomain setup could fail. In this case, you can delete the **[!UICONTROL Failed]** subdomain to clean up the list using the **[!UICONTROL Delete]** button from the **[!UICONTROL More actions]** icon.

## Configuración de un nuevo subdominio {#web-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_web_subdomain_dns"
>title="Generar el registro DNS coincidente"
>abstract="Para configurar un nuevo subdominio web, debe copiar la información del servidor de nombres de Adobe que se muestra en la interfaz de Journey Optimizer y pegarla en la solución de alojamiento de dominios para generar el registro DNS coincidente. Una vez realizadas las comprobaciones correctamente, el subdominio está listo para utilizarse para publicar contenido procedente de la biblioteca de Adobe Experience Manager Assets."


De manera predeterminada, [!DNL Journey Optimizer] le permite delegar **hasta 10 subdominios** en total (que abarcan tanto los canales de correo electrónico como los canales web). Sin embargo, según el contrato de licencia, puede delegar hasta 100 subdominios. Póngase en contacto con la persona de contacto de Adobe para obtener más información sobre el número de subdominios a los que tiene derecho.

Para configurar un nuevo subdominio, siga los pasos a continuación:

1. Acceda al menú **[!UICONTROL Administración]** > **[!UICONTROL Canales]** y, a continuación, seleccione **[!UICONTROL Configuración web]** > **[!UICONTROL subdominios web]**.

1. Haga clic en **[!UICONTROL Configurar subdominio]**.

1. Seleccione **[!UICONTROL Agregar su propio dominio]** de la sección **[!UICONTROL Tipo de configuración]**.

1. Especifique el subdominio que desea delegar.

   >[!CAUTION]
   >
   >* No se puede utilizar un subdominio web existente.
   >
   >* Capital letters are not allowed in subdomains.

   ![](assets/web-add-your-own-domain.png)

   Delegating an invalid subdomain to Adobe is not allowed. Make sure you enter a valid subdomain which is owned by your organization, such as marketing.yourcompany.com.

   Multi-level subdomains (of the same parent domain) are supported. For example, you can use &#39;web.marketing.yourcompany.com&#39;.

1. To set this subdomain as default, select the corresponding option.

   >[!NOTE]
   >
   >Solo se usará el subdominio **default**.

1. Se muestra el registro que se va a colocar en los servidores DNS. Copie este registro o descargue un archivo CSV y, a continuación, vaya a la solución de alojamiento de dominios para generar el registro DNS correspondiente.

1. Asegúrese de que se ha generado un registro DNS en la solución de alojamiento de dominios. Si todo está configurado correctamente, marque la casilla &quot;Confirmo...&quot; y luego haga clic en **[!UICONTROL Enviar]**.

   ![](assets/web-add-your-own-domain-confirm.png)

   Al configurar un nuevo subdominio web, siempre apunta a un registro CNAME.

1. Una vez enviada la delegación del subdominio, este se muestra en la lista con el estado **[!UICONTROL Procesando]**. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   Antes de poder usar ese subdominio para enviar mensajes web, debe esperar hasta que Adobe realice las comprobaciones necesarias, que pueden tardar **hasta 4 horas**.

1. Una vez que las comprobaciones son correctas, el subdominio obtiene el estado **[!UICONTROL Success]**. Está listo para utilizarse para crear configuraciones de canal web.

   Tenga en cuenta que el subdominio se marcará como **[!UICONTROL Error]** si no crea el registro de validación en la solución de alojamiento.

<!--
Only a subdomain with the **[!UICONTROL Success]** status can be set as default.
You cannot delete a subdomain with the **[!UICONTROL Processing]** status.
-->

## Anular la delegación de un subdominio {#undelegate-subdomain}

Si desea desdelegar un subdominio web, póngase en contacto con su representante de Adobe.

Sin embargo, debe realizar varios pasos en la interfaz de usuario antes de ponerse en contacto con Adobe.

>[!NOTE]
>
>Solo puede anular la delegación de subdominios con el estado **[!UICONTROL Correcto]**. Los subdominios con los estados **[!UICONTROL Borrador]** y **[!UICONTROL Error]** simplemente se pueden eliminar de la interfaz de usuario.

Primero, realice los siguientes pasos en [!DNL Journey Optimizer]:

1. Desactive todas las configuraciones de canal asociadas con el subdominio. [Descubra cómo](../configuration/channel-surfaces.md#deactivate-a-surface)

<!--
1. If the web subdomain is using an email subdomain that was [already delegated](#lp-use-existing-subdomain) to Adobe, undelegate the email subdomain. [Learn how](../configuration/delegate-subdomain.md#undelegate-subdomain)-->

1. Stop the active campaigns associated with the subdomains. [Descubra cómo](../campaigns/modify-stop-campaign.md#stop)

1. Stop the active journeys associated with the subdomains. [Descubra cómo](../building-journeys/end-journey.md#stop-journey)

1. If the web subdomain was a [new delegated subdomain](#web-configure-new-subdomain), remove the DNS entries associated with that subdomain.

Once done, reach out to your Adobe representative with the subdomain you want to undelegate.

Una vez que Adobe administra la solicitud, el dominio no delegado ya no se muestra en la página de inventario de subdominios.

>[!CAUTION]
>
>Después de anular la delegación de un subdominio:
>
>   * No puede reactivar las configuraciones de canal que utilizaban ese subdominio.
>
>   * No puede volver a delegar el subdominio exacto a través de la interfaz de usuario. Si desea hacerlo, póngase en contacto con su representante de Adobe.