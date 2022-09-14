---
title: Configuración de superficies de canal
description: Aprenda a configurar y monitorizar superficies de canal
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---

# Configuración de superficies de canal {#set-up-channel-surfaces}

con [!DNL Journey Optimizer], puede configurar superficies de canal (es decir, ajustes preestablecidos de mensaje) que definan todos los parámetros técnicos necesarios para los mensajes: tipo de correo electrónico, correo electrónico y nombre del remitente, aplicaciones móviles, configuración de SMS, etc.

>[!CAUTION]
>
> * Para crear, editar y eliminar superficies de canal, debe tener la variable [Administrar superficie de canal](../administration/high-low-permissions.md#manage-channel-surface) permiso.
>
> * Debe realizar la [Configuración de correo electrónico](#configure-email-settings), [Configuración push](../configuration/push-configuration.md) y [Configuración de SMS](../configuration/sms-configuration.md) pasos antes de crear superficies de canal.


Una vez configuradas las superficies del canal, se pueden seleccionar al crear mensajes desde un recorrido.

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## Creación de una superficie de canal {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="Configuración de la superficie del canal"
>abstract="Al configurar una superficie de canal, seleccione el canal al que se aplica y defina todos los parámetros técnicos necesarios para los mensajes, como el tipo de correo electrónico, el subdominio, el nombre del remitente, las aplicaciones móviles, la configuración de SMS, etc."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Configuración de la superficie del canal"
>abstract="Al configurar una superficie de canal, seleccione el canal al que se aplica y defina todos los parámetros técnicos necesarios para los mensajes, como el tipo de correo electrónico, el nombre del remitente, las aplicaciones móviles, la configuración de SMS, etc."

<!--New contextual help content for September release: A channel surface defines all the technical parameters required for your messages (email type, sender name, mobile apps, SMS configuration, etc.): once configured, you will be able to select it when creating actions from a journey or a campaign. Note that you must have the Manage channel surface permission to create, edit and delete channel surfaces.

To create a channel surface, follow these steps:

1. Access the **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** menu, then click **[!UICONTROL Create channel surface]**.

    ![](assets/preset-create.png)

1. Enter a name and a description (optional) for the surface, then select the channel(s) to configure.

    ![](assets/preset-general.png)

    >[!NOTE]
    >
    > Names must begin with a letter (A-Z). It can only contain alpha-numeric characters. You can also use underscore `_`, dot`.` and hyphen `-` characters. 

1. If you selected the **[!UICONTROL Email]** channel, configure your settings as described in [this section](email-settings.md).

    ![](assets/preset-email.png)

1. For the **[!UICONTROL Push Notification]** channel, select at least one platform  -  **iOS** and/or **Android** -, and the mobile applications to use for each platform.

    ![](assets/preset-push.png)
        
    >[!NOTE]
    >
    >For more on how to configure your environment to send push notifications, refer to [this section](push-gs.md).

1. For the **[!UICONTROL SMS]** channel, define your settings as detailed in [this section](sms-configuration.md#message-preset-sms).

    ![](assets/preset-sms.png)

    >[!NOTE]
    >
    >For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

1. Once all the parameters have been configured, click **[!UICONTROL Submit]** to confirm. You can also save the channel surface as draft and resume its configuration later on.

    ![](assets/preset-submit.png)

    >[!NOTE]
    >
    >You cannot proceed with surface creation while the selected IP pool is under [edition](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** status), and has never been associated with the selected subdomain. [Learn more](#subdomains-and-ip-pools)
    >
    >Save the surface as draft and wait until the IP pool has the **[!UICONTROL Success]** status to resume surface creation.
    
1. Once the channel surface has been created, it displays in the list with the **[!UICONTROL Processing]** status.

    During this step, several checks will be performed to verify that it has been configured properly. The processing time is around **48h-72h**, and can take up to **7-10 business days**.

    These checks include configuration and technical tests that are performed by the Adobe team:

    * SPF validation
    * DKIM validation
    * MX record validation
    * Check IPs denylisting
    * Helo host check
    * IP pool verification
    * A/PTR record, t/m/res subdomain verification

    >[!NOTE]
    >
    >If the checks are not successful, learn more on the possible failure reasons in [this section](#monitor-channel-surfaces).  

1. Once the checks are successful, the channel surface gets the **[!UICONTROL Active]** status. It is ready to be used to deliver messages.

    ![](assets/preset-active.png)

## Monitor channel surfaces {#monitor-channel-surfaces}

All your channel surfaces display in the **[!UICONTROL Channels]** > **[!UICONTROL Channel surfaces]** menu. Filters are available to help you browse through the list (channel, user, status).

![](assets/preset-filters.png)

Once created, channel surfaces can have the following statuses:

* **[!UICONTROL Draft]**: The channel surface has been saved as a draft and has not been submitted yet. Open it to resume the configuration.
* **[!UICONTROL Processing]**: The channel surface has been submitted and is going through several verifications steps.
* **[!UICONTROL Active]**: The channel surface has been verified and can be selected to create messages.
* **[!UICONTROL Failed]**: One or several checks have failed during the channel surface verification.
* **[!UICONTROL Deactivated]**: The channel surface is deactivated. It cannot be used to create new messages.

In case a channel surface creation fails, the details on each possible failure reason are described below.

If one of these errors occurs, contact [Adobe Customer Care](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} to get assistance.

* **SPF validation failed**: SPF (Sender Policy Framework) is an email authentication protocol that allows to specify authorized IPs that can send emails from a given subdomain. SPF validation failure means that the IP addresses in the SPF record do not match the IP addresses used for sending emails to the mailbox providers. 

* **DKIM validation failed**: DKIM (DomainKeys Identified Mail) allows the recipient server to verify that the received message was sent by the genuine sender of the associated domain and that the content of the original message was not altered on its way. DKIM validation failure means that the receiving mail servers are unable to verify the authenticity of the message content and its association with the sending domain.:

* **MX record validation failed**: MX (Mail eXchange) record validation failure means that the mail servers responsible for accepting inbound emails on behalf of a given subdomain are not correctly configured.

* **Deliverability configurations failed**: Deliverability configurations failure can happen due to any of the following reasons:
    * Blocklisting of the allocated IPs
    * Invalid `helo` name
    * Emails being sent from IPs other than the ones specified in the IP pool of the corresponding surface
    * Unable to deliver emails to inboxes of major ISPs like Gmail and Yahoo

## Edit a channel surface {#edit-channel-surface}

To edit a channel surface, follow the steps below.

>[!NOTE]
>
>You cannot edit the **[!UICONTROL Push notification settings]**. If a channel surface is only configured for the Push notification channel, it is not editable.

1. From the list, click a channel surface name to open it.

    ![](assets/preset-name.png)

1. Edit its properties as desired.

    >[!NOTE]
    >
    >If a channel surface has the **[!UICONTROL Active]** status, the **[!UICONTROL Name]**, **[!UICONTROL Select channel]** and **[!UICONTROL Subdomain]** fields are greyed out and cannot be edited.

1. Click **[!UICONTROL Submit]** to confirm your changes.

    >[!NOTE]
    >
    >You can also save the channel surface as draft and resume update later on.

Once the changes are submitted, the channel surface will go through a validation cycle similar to the one in place when [creating a channel surface](#create-channel-surface). The edition processing time can take up to **3 hours**.

>[!NOTE]
>
>If you only edit the **[!UICONTROL Description]**, **[!UICONTROL Email type]** and/or **[!UICONTROL Email retry parameters]** fields, the update is instantaneous.

### Update details {#update-details}

For channel surfaces that have the **[!UICONTROL Active]** status, you can check the details of the update. To do so:

Click the **[!UICONTROL Recent update]** icon that is displayed next to the active surface name.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

En el **[!UICONTROL Actualización reciente]** , puede ver información como el estado de actualización y la lista de cambios solicitados.

<!--![](assets/preset-recent-update-screen.png)-->

### Actualizar estados {#update-statuses}

Una actualización de la superficie del canal puede tener los siguientes estados:

* **[!UICONTROL Procesamiento]**: La actualización de la superficie del canal se ha enviado y está pasando por varios pasos de verificación.
* **[!UICONTROL Correcto]**: La superficie de canal actualizada se ha verificado y se puede seleccionar para crear mensajes.
* **[!UICONTROL Error]**: Error de una o varias comprobaciones durante la verificación de actualización de la superficie del canal.

Cada estado se detalla a continuación.

#### Procesamiento {#surface-processing}

Se realizarán varias comprobaciones de la capacidad de envío para verificar que la superficie se haya actualizado correctamente.

>[!NOTE]
>
>Si solo edita la variable **[!UICONTROL Descripción]**, **[!UICONTROL Tipo de correo electrónico]** y/o **[!UICONTROL Parámetros de reintentos de correo electrónico]** , la actualización es instantánea.

El tiempo de procesamiento puede tardar hasta **3 horas**. Obtenga más información sobre las comprobaciones realizadas durante el ciclo de validación en [esta sección](#create-channel-surface).

Si edita una superficie que ya estaba activa:

* Su estatus sigue siendo **[!UICONTROL Activo]** mientras el proceso de validación esté en curso.

* La variable **[!UICONTROL Actualización reciente]** aparece junto al nombre de la superficie en la lista de superficies del canal.

* Durante el proceso de validación, los mensajes configurados con esta superficie siguen utilizando la versión anterior de la superficie.

>[!NOTE]
>
>No se puede modificar una superficie de canal mientras la actualización está en curso. Puede seguir haciendo clic en su nombre, pero todos los campos están atenuados. Los cambios no se reflejarán hasta que la actualización se realice correctamente.

#### Correcto {#success}

Una vez que el proceso de validación se ha realizado correctamente, la nueva versión de la superficie se utiliza automáticamente en todos los mensajes que utilizan esta superficie. Sin embargo, es posible que tenga que esperar:
* unos minutos antes de que los mensajes unitarios lo consuman,
* hasta el siguiente lote para que la superficie sea efectiva en los mensajes por lotes.

#### Fallido {#failed}

Si el proceso de validación falla, se utilizará la versión anterior de la superficie.

Obtenga más información sobre los posibles motivos de error en [esta sección](#monitor-channel-surfaces).

Cuando falla la actualización, la superficie vuelve a ser editable. Puede hacer clic en su nombre y actualizar la configuración que debe corregirse.

## Desactivación de una superficie de canal {#deactivate-a-surface}

Para hacer un **[!UICONTROL Activo]** superficie de canal no disponible para crear nuevos mensajes, puede desactivarlo. Sin embargo, los mensajes de los recorridos que utilicen esta superficie no se verán afectados y seguirán funcionando.

>[!NOTE]
>
>No se puede desactivar una superficie de canal mientras se está procesando una actualización. Debe esperar hasta que la actualización se realice correctamente o haya fallado. Más información sobre [editar superficies de canal](#edit-channel-surface) y [estados de actualización](#update-statuses).

1. Acceda a la lista de superficies del canal.

1. Para la superficie activa de su elección, haga clic en el botón **[!UICONTROL Más acciones]** botón.

1. Select **[!UICONTROL Desactivar]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>Las superficies de canal desactivadas no se pueden eliminar para evitar problemas en los recorridos que utilizan estas superficies para enviar mensajes.

No se puede editar directamente una superficie de canal desactivada. Sin embargo, puede duplicarla y editarla para crear una nueva versión que utilizará para crear nuevos mensajes. También puede volver a activarla y esperar a que la actualización se realice correctamente para editarla.

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
