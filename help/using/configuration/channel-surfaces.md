---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de superficies de canal
description: Obtenga información sobre cómo configurar y monitorizar superficies de canal
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: canal, superficie, técnico, parámetros, optimizador
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 99c509a00a3e8a4dbf9ae8a5b16aa799b0af2e13
workflow-type: tm+mt
source-wordcount: '1651'
ht-degree: 8%

---

# Configuración de superficies de canal {#set-up-channel-surfaces}

>[!CONTEXTUALHELP]
>id="ajo_admin_channel_surfaces"
>title="Superficie de canal"
>abstract="Una superficie de canal es una configuración que ha definido un administrador del sistema. Contiene todos los parámetros técnicos para enviar el mensaje, como parámetros de encabezado, subdominio, aplicaciones móviles, etc."

Con [!DNL Journey Optimizer], puede configurar superficies de canal (es decir, ajustes preestablecidos de mensaje) que definan todos los parámetros técnicos necesarios para sus mensajes: tipo de correo electrónico, nombre y correo electrónico del remitente, aplicaciones móviles, configuración de SMS, etc.

>[!CAUTION]
>
> * Para crear, editar y borrar superficies de canal, se debe disponer de [Administrar ajustes preestablecidos de mensajes](../administration/high-low-permissions.md#administration-permissions) permiso.
>
> * Debe realizar las [Configuración de correo electrónico](../email/get-started-email-config.md), [Configuración push](../push/push-configuration.md), [Configuración de SMS](../sms/sms-configuration.md) y [Configuración de correo directo](../direct-mail/direct-mail-configuration.md) pasos antes de crear superficies de canal.

Una vez configuradas las superficies de canal, puede seleccionarlas al crear mensajes desde un recorrido o una campaña.

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## Creación de una superficie de canal {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="Configuración de la superficie de canal"
>abstract="Al configurar una superficie de canal, seleccione el canal al que se aplica y defina todos los parámetros técnicos necesarios para el envío, como el tipo de correo electrónico, el nombre del remitente, las aplicaciones móviles, la configuración de SMS, etc."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Configuración de la superficie de canal"
>abstract="Para poder crear acciones como correos electrónicos desde un recorrido o una campaña, primero debe crear una superficie de canal que defina toda la configuración técnica necesaria para los mensajes. Debe tener el permiso Administrar ajustes preestablecidos de mensajes para crear, editar y eliminar superficies de canal."

>[!CONTEXTUALHELP]
>id="ajo_surface_marketing_action"
>title="Seleccionar una acción de marketing"
>abstract="Elija una acción de marketing en la superficie para asociar una política de consentimiento con el mensaje."

Para crear una superficie de canal, siga estos pasos:

1. Acceda a la **[!UICONTROL Canales]** > **[!UICONTROL Marca]** > **[!UICONTROL Superficies de canal]** y haga clic en **[!UICONTROL Crear superficie de canal]**.

   ![](assets/preset-create.png)

1. Introduzca un nombre y una descripción (opcional) para la superficie y, a continuación, seleccione los canales que desea configurar.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar guiones bajos `_`, punto`.` y guiones `-` caracteres.

1. Si seleccionó la **[!UICONTROL Correo electrónico]** canal, configure los ajustes tal como se describe en [esta sección](../email/email-settings.md).

   ![](assets/preset-email.png)

1. Para el **[!UICONTROL Notificación push]** canal, seleccione al menos una plataforma -  **iOS** y/o **Android** : y las aplicaciones móviles que se utilizarán para cada plataforma.

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >Para obtener más información sobre cómo configurar su entorno para enviar notificaciones push, consulte [esta sección](../push/push-gs.md).

1. Para el **[!UICONTROL SMS]** canal, defina su configuración como se detalla en [esta sección](../sms/sms-configuration.md#message-preset-sms).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >Para obtener más información sobre cómo configurar su entorno para enviar mensajes SMS, consulte [esta sección](../sms/sms-configuration.md).

<!--
1. Select a **[!UICONTROL Marketing action]** to associate consent policies to the messages using this surface. All consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers. [Learn more](../action/consent.md#marketing-actions)

    >[!NOTE]
    >
    >Consent policies are currently only available for organizations that have purchased the **Healthcare Shield** and **Privacy and Security Shield** add-on offerings. [Learn more](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html){target="_blank"}

    ![](assets/surface-marketing-action.png)

    >[!NOTE]
    >
    >You can only select one marketing action.-->

1. Una vez configurados todos los parámetros, haga clic en **[!UICONTROL Enviar]** para confirmar. También se puede guardar la superficie de canal como inclinación y reanudar su configuración más adelante.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >No puede continuar con la creación de la superficie de correo electrónico mientras el grupo de IP seleccionado esté en [edición](ip-pools.md#edit-ip-pool) (**[!UICONTROL Procesando]** estado) y nunca se ha asociado con el subdominio seleccionado. [Más información](#subdomains-and-ip-pools)
   >
   >Guarde la superficie como inclinación y espere hasta que el grupo de IP tenga la **[!UICONTROL Correcto]** estado para reanudar la creación de superficies.

1. Una vez creada la superficie de canal, esta se muestra en la lista con el **[!UICONTROL Procesando]** estado.

   Durante este paso, se realizarán varias comprobaciones para comprobar que se ha configurado correctamente. <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   > Al crear una superficie de correo electrónico para un subdominio, el tiempo de procesamiento varía según se detalla a continuación:
   >
   > * Para **nuevos subdominios**, el proceso para crear la primera superficie de canal puede llevar **De 10 min a 10 días**.
   > * Para **zonas protegidas de no producción** o si el subdominio seleccionado es **ya se usa** en otra superficie de canal aprobada, el proceso solo lleva hasta **3 horas**.


   Estas comprobaciones incluyen pruebas técnicas y de configuración que realiza el equipo de Adobe:

   * Validación de SPF
   * Validación de DKIM
   * Validación de registro MX
   * Comprobar la IPs inclusión en la lista de bloqueados
   * Comprobación del host HELO
   * Verificación del grupo de IP
   * Registro A/PTR, verificación del subdominio t/m/res
   * Registro FBL (esta comprobación se realizará solo la primera vez que se cree una superficie de correo electrónico para un subdominio determinado)

   >[!NOTE]
   >
   >Si las comprobaciones no se realizan correctamente, obtenga más información sobre los posibles motivos de error en [esta sección](#monitor-channel-surfaces).

1. Una vez que las comprobaciones son correctas, la superficie de canal obtiene el **[!UICONTROL Activo]** estado. Está listo para utilizarse para enviar mensajes.

   ![](assets/preset-active.png)

## Superficies de canal de monitor {#monitor-channel-surfaces}

Todas las superficies de canal se muestran en la **[!UICONTROL Canales]** > **[!UICONTROL Superficies de canal]** menú. Los filtros están disponibles para ayudarle a examinar la lista (canal, usuario, estado).

![](assets/preset-filters.png)

Una vez creadas, las superficies de canal pueden tener los siguientes estados:

* **[!UICONTROL Borrador]**: la superficie de canal se ha guardado como borrador y aún no se ha enviado. Ábralo para reanudar la configuración.
* **[!UICONTROL Procesando]**: la superficie de canal se ha enviado y está pasando por varios pasos de verificación.
* **[!UICONTROL Activo]**: la superficie de canal se ha verificado y se puede seleccionar para crear mensajes.
* **[!UICONTROL Error]**: una o varias comprobaciones han fallado durante la verificación de la superficie del canal.
* **[!UICONTROL Desactivado]**: la superficie de canal está desactivada. No se puede usar para crear mensajes nuevos.

En caso de que falle la creación de una superficie de canal, a continuación se describen los detalles de cada posible motivo de error.

Si se produce uno de estos errores, póngase en contacto con [Adobe del Servicio de atención al cliente](https://helpx.adobe.com/es/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} para obtener ayuda.

* **Error de validación de SPF**: SPF (Marco de Política del Remitente) es un protocolo de autenticación de correo electrónico que permite especificar direcciones IP autorizadas que pueden enviar correos electrónicos desde un subdominio determinado. Un error de validación de SPF significa que las direcciones IP del registro SPF no coinciden con las direcciones IP utilizadas para enviar correos electrónicos a los proveedores de buzones de correo.

* **Error de validación de DKIM**: DKIM (DomainKeys Identified Mail) permite al servidor de destinatarios verificar que el mensaje recibido fue enviado por el remitente auténtico del dominio asociado y que el contenido del mensaje original no se alteró en su camino. Un error de validación de DKIM significa que los servidores de correo receptores no pueden verificar la autenticidad del contenido del mensaje y su asociación con el dominio de envío.:

* **Error de validación de registro MX**: Error de validación de registro MX (Mail eXchange) significa que los servidores de correo responsables de aceptar correos electrónicos entrantes en nombre de un subdominio determinado no están correctamente configurados.

* **Error de configuraciones de entrega**: Los errores en las configuraciones de entrega pueden deberse a cualquiera de las siguientes razones:
   * Inclusión en la lista de bloqueados de las direcciones IP asignadas
   * No válido `helo` name
   * Correos electrónicos enviados desde direcciones IP distintas de las especificadas en el grupo de IP de la superficie correspondiente
   * No se pueden enviar correos electrónicos a las bandejas de entrada de los principales ISP

## Edición de una superficie de canal {#edit-channel-surface}

Para editar una superficie de canal, siga los pasos a continuación.

>[!NOTE]
>
>No se puede editar el **[!UICONTROL Configuración de notificaciones push]**. Si una superficie de canal solo está configurada para el canal de notificaciones push, no se puede editar.

1. En la lista, pulse en el nombre de una superficie de canal para abrirla.

   ![](assets/preset-name.png)

1. Edite sus propiedades según desee.

   >[!NOTE]
   >
   >Si una superficie de canal tiene el **[!UICONTROL Activo]** estado, el **[!UICONTROL Nombre]**, **[!UICONTROL Seleccionar canal]** y **[!UICONTROL Subdominio]** los campos aparecen atenuados y no se pueden editar.

1. Clic **[!UICONTROL Enviar]** para confirmar los cambios.

   >[!NOTE]
   >
   >También se puede guardar la superficie de canal como inclinación y reanudar la actualización más adelante.

Una vez enviados los cambios, la superficie de canal pasará a través de un ciclo de validación similar al que se aplicó cuando [creación de una superficie de canal](#create-channel-surface). El tiempo de procesamiento de la edición puede ser de hasta **3 horas**.

>[!NOTE]
>
>Si solo edita la variable **[!UICONTROL Descripción]**, **[!UICONTROL Tipo de correo electrónico]** y/o **[!UICONTROL Parámetros de reintento de correo electrónico]** , la actualización es instantánea.

### Actualizar detalles {#update-details}

Para superficies de canal que tienen el **[!UICONTROL Activo]** estado, puede comprobar los detalles de la actualización. Para ello:

Haga clic en **[!UICONTROL Actualización reciente]** que se muestra junto al nombre de la superficie activa.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

En el **[!UICONTROL Actualización reciente]** , puede ver información como el estado de la actualización y la lista de cambios solicitados.

<!--![](assets/preset-recent-update-screen.png)-->

### Actualizar estados {#update-statuses}

Una actualización de la superficie de canal puede tener los siguientes estados:

* **[!UICONTROL Procesando]**: la actualización de la superficie de canal se ha enviado y está pasando por varios pasos de verificación.
* **[!UICONTROL Correcto]**: la superficie de canal actualizada se ha verificado y se puede seleccionar para crear mensajes.
* **[!UICONTROL Error]**: una o varias comprobaciones han fallado durante la verificación de la actualización de la superficie del canal.

A continuación se detalla cada estado.

#### Procesamiento {#surface-processing}

Se realizarán varias comprobaciones de entrega para verificar que la superficie se ha actualizado correctamente.

>[!NOTE]
>
>Si solo edita la variable **[!UICONTROL Descripción]**, **[!UICONTROL Tipo de correo electrónico]** y/o **[!UICONTROL Parámetros de reintento de correo electrónico]** , la actualización es instantánea.

El tiempo de procesamiento puede ser de hasta **3 horas**. Obtenga más información sobre las comprobaciones realizadas durante el ciclo de validación en [esta sección](#create-channel-surface).

Si edita una superficie que ya estaba activa:

* Su estado sigue siendo **[!UICONTROL Activo]** mientras el proceso de validación está en curso.

* El **[!UICONTROL Actualización reciente]** aparece junto al nombre de la superficie en la lista de superficies de canal.

* Durante el proceso de validación, los mensajes configurados con esta superficie siguen utilizando la versión anterior de la superficie.

>[!NOTE]
>
>No se puede modificar una superficie de canal mientras la actualización está en curso. Puede seguir haciendo clic en su nombre, pero todos los campos aparecen atenuados. Los cambios no se reflejarán hasta que la actualización se realice correctamente.

#### Correcto {#success}

Una vez que el proceso de validación se realiza correctamente, la nueva versión de la superficie se utiliza automáticamente en todos los mensajes que utilizan esta superficie. Sin embargo, es posible que tenga que esperar:
* unos minutos antes de que los mensajes unitarios lo consuman,
* hasta el siguiente lote para que la superficie sea efectiva en los mensajes por lotes.

#### Error {#failed}

Si el proceso de validación falla, se seguirá utilizando la versión anterior de la superficie.

Obtenga más información sobre los posibles motivos de error en [esta sección](#monitor-channel-surfaces).

Si la actualización falla, la superficie se vuelve editable. Puede hacer clic en su nombre y actualizar la configuración que debe corregirse.

## Desactivación de una superficie de canal {#deactivate-a-surface}

Para realizar una **[!UICONTROL Activo]** superficie de canal no disponible para crear mensajes nuevos, puede desactivarla. Sin embargo, los mensajes de los recorridos que actualmente utilizan esta superficie no se verán afectados y seguirán funcionando.

>[!NOTE]
>
>No se puede desactivar una superficie de canal mientras se esté procesando una actualización. Debe esperar hasta que la actualización se haya realizado correctamente o haya fallado. Más información sobre [edición de superficies de canal](#edit-channel-surface) y en el [actualizar estados](#update-statuses).

1. Acceda a la lista de superficies de canal.

1. Para la superficie activa que elija, pulse en **[!UICONTROL Más acciones]** botón.

1. Seleccionar **[!UICONTROL Desactivar]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>Las superficies de canal desactivadas no se pueden eliminar para evitar cualquier problema en los recorridos que utilizan estas superficies para enviar mensajes.

No se puede editar directamente una superficie de canal desactivada. Sin embargo, puede duplicarla y editar la copia para crear una nueva versión que utilizará para crear mensajes nuevos. También puede volver a activarla y esperar hasta que la actualización se haya realizado correctamente para editarla.

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
