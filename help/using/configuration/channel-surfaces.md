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
source-git-commit: 9af49f0a47ad5bc1d2cea3e822ec20e2930140d3
workflow-type: tm+mt
source-wordcount: '1758'
ht-degree: 10%

---

# Configuración de superficies de canal {#set-up-channel-surfaces}

>[!CONTEXTUALHELP]
>id="ajo_admin_channel_surfaces"
>title="Superficie de canal"
>abstract="Una superficie de canal es una configuración que ha definido un administrador del sistema. Contiene todos los parámetros técnicos para enviar el mensaje, como parámetros de encabezado, subdominio, aplicaciones móviles, etc."

>[!CONTEXTUALHELP]
>id="ajo_admin_marketing_action"
>title="Acción de marketing"
>abstract="Por confirmar"

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="ID de la aplicación"
>abstract="Por confirmar"

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="Ubicación en la página"
>abstract="Por confirmar"

>[!CONTEXTUALHELP]
>id="ajo_admin_page_rule"
>title="Regla de coincidencia de páginas"
>abstract="Por confirmar"

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="URL predeterminada"
>abstract="Por confirmar"

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="URI de superficie"
>abstract="Por confirmar"

Con [!DNL Journey Optimizer], puede configurar superficies de canal (es decir, ajustes preestablecidos de mensaje) que definan todos los parámetros técnicos necesarios para sus mensajes: tipo de correo electrónico, nombre y correo electrónico del remitente, aplicaciones móviles, configuración de SMS, etc.

>[!CAUTION]
>
> * Para crear, editar y eliminar superficies de canal, debe tener el permiso [Administrar mensajes preestablecidos](../administration/high-low-permissions.md#administration-permissions).
>
> * Debe realizar los pasos de [Configuración de correo electrónico](../email/get-started-email-config.md), [Configuración push](../push/push-configuration.md), [Configuración de SMS](../sms/sms-configuration.md) y [Configuración de correo directo](../direct-mail/direct-mail-configuration.md) antes de crear superficies de canal.

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
>title="Selección de una acción de marketing"
>abstract="Elija una acción de marketing en la superficie para asociar una política de consentimiento con el mensaje."

Para crear una superficie de canal, siga estos pasos:

1. Acceda al menú **[!UICONTROL Canales]** > **[!UICONTROL Marca]** > **[!UICONTROL Superficies de canal]** y haga clic en **[!UICONTROL Crear superficie de canal]**.

   ![](assets/preset-create.png)

1. Introduzca un nombre y una descripción (opcional) para la superficie y, a continuación, seleccione los canales que desea configurar.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar caracteres de guion bajo `_`, punto`.` y guión `-`.

1. Para asignar etiquetas de uso de datos principales o personalizadas a la superficie, puedes seleccionar **[!UICONTROL Administrar acceso]**. [Más información sobre el Control de acceso de nivel de objeto (OLAC)](../administration/object-based-access.md).

1. Si seleccionó el canal **[!UICONTROL Correo electrónico]**, configure las opciones tal como se describe en [esta sección](../email/email-settings.md).

   ![](assets/preset-email.png)

1. Para el canal **[!UICONTROL Notificación push]**, seleccione al menos una plataforma - **iOS** y/o **Android** - y las aplicaciones móviles que se usarán para cada plataforma.

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >Para obtener más información sobre cómo configurar su entorno para enviar notificaciones push, consulte [esta sección](../push/push-gs.md).

1. Para el canal **[!UICONTROL SMS]**, defina la configuración tal como se detalla en [esta sección](../sms/sms-configuration.md).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >Para obtener más información sobre cómo configurar su entorno para enviar mensajes SMS, consulte [esta sección](../sms/sms-configuration.md).

1. Seleccione una **[!UICONTROL acción de marketing]** para asociar directivas de consentimiento a los mensajes que usan esta superficie. Todas las políticas de consentimiento asociadas con esa acción de marketing se aprovechan para respetar las preferencias de los clientes. [Más información](../action/consent.md#surface-marketing-actions)

   >[!NOTE]
   >
   >Actualmente, las directivas de consentimiento solo están disponibles para las organizaciones que han adquirido las ofertas de complementos de **Healthcare Shield** y **Privacy and Security Shield**.

   ![](assets/surface-marketing-action.png)

   >[!NOTE]
   >
   >Solo puede seleccionar una acción de marketing.

1. Una vez configurados todos los parámetros, haga clic en **[!UICONTROL Enviar]** para confirmar. También se puede guardar la superficie de canal como inclinación y reanudar su configuración más adelante.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >No puede continuar con la creación de la superficie de correo electrónico mientras el grupo de IP seleccionado esté en [edición](ip-pools.md#edit-ip-pool) (**[!UICONTROL Procesando]** estado) y nunca se haya asociado con el subdominio seleccionado. [Más información](#subdomains-and-ip-pools)
   >
   >Guarde la superficie como borrador y espere hasta que el grupo de IP tenga el estado **[!UICONTROL Éxito]** para reanudar la creación de la superficie.

1. Una vez creada la superficie de canal, se muestra en la lista con el estado **[!UICONTROL Procesando]**.

   Durante este paso, se realizarán varias comprobaciones para comprobar que se ha configurado correctamente. <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   > Al crear una superficie de correo electrónico para un subdominio, el tiempo de procesamiento varía según se detalla a continuación:
   >
   > * Para **nuevos subdominios**, el proceso de creación de la primera superficie de canal puede tardar de **10 min a 10 días**.
   > * Para **zonas protegidas sin producción**, o si el subdominio seleccionado **ya se ha utilizado** en otra superficie de canal aprobada, el proceso solo tarda **3 horas**.


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

1. Una vez que las comprobaciones son correctas, la superficie de canal obtiene el estado **[!UICONTROL Activo]**. Está listo para utilizarse para enviar mensajes.

   ![](assets/preset-active.png)

## Superficies de canal de monitor {#monitor-channel-surfaces}

Todas las superficies de canal se muestran en el menú **[!UICONTROL Canales]** > **[!UICONTROL Superficies de canal]**. Los filtros están disponibles para ayudarle a examinar la lista (canal, usuario, estado).

![](assets/preset-filters.png)

Una vez creadas, las superficies de canal pueden tener los siguientes estados:

* **[!UICONTROL Borrador]**: la superficie de canal se ha guardado como borrador y aún no se ha enviado. Ábralo para reanudar la configuración.
* **[!UICONTROL Procesando]**: la superficie de canal se ha enviado y está pasando por varios pasos de verificación.
* **[!UICONTROL Activo]**: la superficie de canal se ha verificado y se puede seleccionar para crear mensajes.
* **[!UICONTROL Error]**: una o varias comprobaciones han fallado durante la verificación de la superficie de canal.
* **[!UICONTROL Desactivada]**: la superficie de canal está desactivada. No se puede usar para crear mensajes nuevos.

En caso de que falle la creación de una superficie de canal, a continuación se describen los detalles de cada posible motivo de error.

Si se produce uno de estos errores, póngase en contacto con el servicio de atención al cliente de [Adobe](https://helpx.adobe.com/es/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} para obtener ayuda.

* **Error de validación de SPF**: SPF (Marco de Política del Remitente) es un protocolo de autenticación de correo electrónico que permite especificar direcciones IP autorizadas que pueden enviar correos electrónicos desde un subdominio determinado. Un error de validación de SPF significa que las direcciones IP del registro SPF no coinciden con las direcciones IP utilizadas para enviar correos electrónicos a los proveedores de buzones de correo.

* **Error de validación de DKIM**: DKIM (DomainKeys Identified Mail) permite al servidor de destinatario comprobar que el mensaje recibido fue enviado por el remitente original del dominio asociado y que el contenido del mensaje original no se alteró en su camino. Un error de validación de DKIM significa que los servidores de correo receptores no pueden verificar la autenticidad del contenido del mensaje y su asociación con el dominio de envío.:

* **Error de validación de registro MX**: El error de validación de registro MX (Mail eXchange) significa que los servidores de correo responsables de aceptar correos electrónicos entrantes en nombre de un subdominio determinado no están correctamente configurados.

* **Error en las configuraciones de entrega**: El error en las configuraciones de entrega puede deberse a cualquiera de las siguientes razones:
   * Inclusión en la lista de bloqueados de las direcciones IP asignadas
   * Nombre de `helo` no válido
   * Correos electrónicos enviados desde direcciones IP distintas de las especificadas en el grupo de IP de la superficie correspondiente
   * No se pueden enviar correos electrónicos a las bandejas de entrada de los principales ISP

## Edición de una superficie de canal {#edit-channel-surface}

Para editar una superficie de canal, siga los pasos a continuación.

>[!NOTE]
>
>No puede editar la **[!UICONTROL configuración de notificaciones push]**. Si una superficie de canal solo está configurada para el canal de notificaciones push, no se puede editar.

1. En la lista, pulse en el nombre de una superficie de canal para abrirla.

   ![](assets/preset-name.png)

1. Edite sus propiedades según desee.

   >[!NOTE]
   >
   >Si una superficie de canal tiene el estado **[!UICONTROL Activo]**, los campos **[!UICONTROL Nombre]**, **[!UICONTROL Seleccionar canal]** y **[!UICONTROL Subdominio]** aparecen atenuados y no se pueden editar.

1. Haga clic en **[!UICONTROL Enviar]** para confirmar los cambios.

   >[!NOTE]
   >
   >También se puede guardar la superficie de canal como inclinación y reanudar la actualización más adelante.

Una vez enviados los cambios, la superficie de canal pasará a través de un ciclo de validación similar al existente al [crear una superficie de canal](#create-channel-surface). El tiempo de procesamiento de la edición puede llevar **3 horas**.

>[!NOTE]
>
>Si solo edita los campos **[!UICONTROL Descripción]**, **[!UICONTROL Tipo de correo electrónico]** o **[!UICONTROL Parámetros de reintento de correo electrónico]**, la actualización es instantánea.

### Actualizar detalles {#update-details}

Para las superficies de canal que tienen el estado **[!UICONTROL Activo]**, puede comprobar los detalles de la actualización. Para ello:

Haga clic en el icono **[!UICONTROL Actualización reciente]** que se muestra junto al nombre de la superficie activa.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

En la pantalla **[!UICONTROL Actualización reciente]**, puede ver información como el estado de la actualización y la lista de cambios solicitados.

<!--![](assets/preset-recent-update-screen.png)-->

### Actualizar estados {#update-statuses}

Una actualización de la superficie de canal puede tener los siguientes estados:

* **[!UICONTROL Procesando]**: la actualización de la superficie de canal se ha enviado y está pasando por varios pasos de verificación.
* **[!UICONTROL Éxito]**: la superficie de canal actualizada se ha verificado y se puede seleccionar para crear mensajes.
* **[!UICONTROL Error]**: una o varias comprobaciones han fallado durante la verificación de la actualización de la superficie de canal.

A continuación se detalla cada estado.

#### Procesamiento {#surface-processing}

Se realizarán varias comprobaciones de entrega para verificar que la superficie se ha actualizado correctamente.

>[!NOTE]
>
>Si solo edita los campos **[!UICONTROL Descripción]**, **[!UICONTROL Tipo de correo electrónico]** o **[!UICONTROL Parámetros de reintento de correo electrónico]**, la actualización es instantánea.

El tiempo de procesamiento puede ser de **3 horas**. Obtenga más información sobre las comprobaciones realizadas durante el ciclo de validación en [esta sección](#create-channel-surface).

Si edita una superficie que ya estaba activa:

* Su estado permanece **[!UICONTROL Activo]** mientras el proceso de validación está en curso.

* El icono **[!UICONTROL Actualización reciente]** se muestra junto al nombre de la superficie en la lista de superficies de canal.

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

Para que una superficie de canal **[!UICONTROL Active]** no esté disponible para crear mensajes nuevos, puede desactivarla. Sin embargo, los mensajes de los recorridos que actualmente utilizan esta superficie no se verán afectados y seguirán funcionando.

>[!NOTE]
>
>No se puede desactivar una superficie de canal mientras se esté procesando una actualización. Debe esperar hasta que la actualización se haya realizado correctamente o haya fallado. Obtenga más información sobre [editar superficies de canal](#edit-channel-surface) y sobre los [estados de actualización](#update-statuses).

1. Acceda a la lista de superficies de canal.

1. Para la superficie activa que elija, haga clic en el botón **[!UICONTROL Más acciones]**.

1. Seleccione **[!UICONTROL Desactivar]**.

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
