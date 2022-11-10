---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de superficies de canal
description: Aprenda a configurar y monitorizar superficies de canal
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 6014088011c41fd5f673eb3d36fb0609c4a01270
workflow-type: tm+mt
source-wordcount: '1572'
ht-degree: 1%

---

# Configuración de superficies de canal {#set-up-channel-surfaces}

con [!DNL Journey Optimizer], puede configurar superficies de canal (es decir, ajustes preestablecidos de mensaje) que definan todos los parámetros técnicos necesarios para los mensajes: tipo de correo electrónico, correo electrónico y nombre del remitente, aplicaciones móviles, configuración de SMS, etc.

>[!CAUTION]
>
> * Para crear, editar y eliminar superficies de canal, debe tener la variable [Administrar superficie de canal](../administration/high-low-permissions.md#manage-channel-surface) permiso.
>
> * Debe realizar la [Configuración de correo electrónico](email-settings.md), [Configuración push](../configuration/push-configuration.md) y [Configuración de SMS](../configuration/sms-configuration.md) pasos antes de crear superficies de canal.


Una vez configuradas las superficies del canal, se pueden seleccionar al crear mensajes desde un recorrido o una campaña.

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## Creación de una superficie de canal {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="Configuración de la superficie del canal"
>abstract="Al configurar una superficie de canal, seleccione el canal al que se aplica y defina todos los parámetros técnicos necesarios para el envío, como el tipo de correo electrónico, el nombre del remitente, las aplicaciones móviles, la configuración de SMS, etc."

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="Configuración de la superficie del canal"
>abstract="Para poder crear acciones como correos electrónicos desde un recorrido o una campaña, primero debe crear una superficie de canal que defina toda la configuración técnica necesaria para los mensajes. Debe tener el permiso Administrar superficie de canal para crear, editar y eliminar superficies de canal."

Para crear una superficie de canal, siga estos pasos:

1. Acceda a la **[!UICONTROL Canales]** > **[!UICONTROL Marcas]** > **[!UICONTROL Superficies de canal]** a continuación, haga clic en **[!UICONTROL Crear superficie de canal]**.

   ![](assets/preset-create.png)

1. Introduzca un nombre y una descripción (opcional) para la superficie y, a continuación, seleccione los canales que desea configurar.

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar guiones bajos `_`, punto`.` Guión `-` caracteres.

1. Si seleccionó la variable **[!UICONTROL Correo electrónico]** canal, configure los ajustes tal como se describe en [esta sección](email-settings.md).

   ![](assets/preset-email.png)

1. Para la variable **[!UICONTROL Notificaciones push]** canal, seleccione al menos una plataforma:  **iOS** y/o **Android** - y las aplicaciones móviles que se utilizarán para cada plataforma.

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >Para obtener más información sobre cómo configurar el entorno para enviar notificaciones push, consulte [esta sección](push-gs.md).

1. Para la variable **[!UICONTROL SMS]** defina la configuración como se detalla en [esta sección](sms-configuration.md#message-preset-sms).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >Para obtener más información sobre cómo configurar su entorno para enviar mensajes SMS, consulte [esta sección](sms-configuration.md).

1. Una vez configurados todos los parámetros, haga clic en **[!UICONTROL Submit]** para confirmar. También puede guardar la superficie del canal como borrador y reanudar su configuración más adelante.

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >No puede continuar con la creación de superficie mientras el grupo IP seleccionado está bajo [edición](ip-pools.md#edit-ip-pool) (**[!UICONTROL Procesamiento]** ) y nunca se ha asociado con el subdominio seleccionado. [Más información](#subdomains-and-ip-pools)
   >
   >Guarde la superficie como borrador y espere hasta que el grupo de IP tenga la variable **[!UICONTROL Correcto]** para reanudar la creación de superficie.

1. Una vez creada la superficie del canal, se muestra en la lista con la variable **[!UICONTROL Procesamiento]** estado.

   Durante este paso, se realizarán varias comprobaciones para verificar que se ha configurado correctamente. <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   >Al crear la primera superficie de correo electrónico para un subdominio determinado, el tiempo de procesamiento puede tardar **de 10 minutos a 10 días**. Si el subdominio seleccionado ya se está utilizando en otra superficie de correo electrónico, solo tardará 3 horas.

   Estas comprobaciones incluyen las pruebas técnicas y de configuración que realiza el equipo de Adobe:

   * Validación de SPF
   * Validación de DKIM
   * Validación de registros MX
   * Comprobación de IP inclusión en la lista de bloqueados
   * Comprobación de host de Helo
   * Verificación del grupo IP
   * Registro A/PTR, verificación del subdominio t/m/res
   * Registro de FBL (esta comprobación solo se realizará la primera vez que se cree una superficie de correo electrónico para un subdominio determinado)

   >[!NOTE]
   >
   >Si las comprobaciones no son correctas, obtenga más información sobre los posibles motivos de error en [esta sección](#monitor-channel-surfaces).

1. Una vez realizadas las comprobaciones, la superficie del canal recibe el **[!UICONTROL Activo]** estado. Está listo para utilizarse para enviar mensajes.

   ![](assets/preset-active.png)

## Superficies del canal de monitorización {#monitor-channel-surfaces}

Todas las superficies de canal se muestran en la sección **[!UICONTROL Canales]** > **[!UICONTROL Superficies de canal]** para abrir el Navegador. Los filtros están disponibles para ayudarle a navegar por la lista (canal, usuario, estado).

![](assets/preset-filters.png)

Una vez creadas, las superficies de canal pueden tener los siguientes estados:

* **[!UICONTROL Borrador]**: La superficie del canal se ha guardado como borrador y aún no se ha enviado. Ábrala para reanudar la configuración.
* **[!UICONTROL Procesamiento]**: La superficie del canal se ha enviado y está pasando por varios pasos de verificación.
* **[!UICONTROL Activo]**: La superficie del canal se ha verificado y se puede seleccionar para crear mensajes.
* **[!UICONTROL Error]**: Se han producido errores en una o varias comprobaciones durante la verificación de la superficie del canal.
* **[!UICONTROL Desactivado]**: La superficie del canal está desactivada. No se puede usar para crear nuevos mensajes.

En caso de que falle la creación de la superficie del canal, a continuación se describen los detalles de cada posible motivo de fallo.

Si se produce uno de estos errores, póngase en contacto con [Servicio de atención al cliente de Adobe](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;} para obtener ayuda.

* **Error de validación de SPF**: SPF (Marco de Política del Remitente) es un protocolo de autenticación por correo electrónico que permite especificar direcciones IP autorizadas que pueden enviar correos electrónicos desde un subdominio determinado. El error de validación de SPF significa que las direcciones IP del registro de SPF no coinciden con las direcciones IP utilizadas para enviar correos electrónicos a los proveedores de buzones de correo.

* **Error de validación de DKIM**: DKIM (DomainKeys Identified Mail) permite al servidor destinatario verificar que el mensaje recibido fue enviado por el remitente original del dominio asociado y que el contenido del mensaje original no se alteró en el camino. El error de validación de DKIM significa que los servidores de correo receptores no pueden verificar la autenticidad del contenido del mensaje y su asociación con el dominio de envío.:

* **Error en la validación del registro MX**: El error de validación del registro MX (Mail eXchange) significa que los servidores de correo responsables de aceptar correos electrónicos entrantes en nombre de un subdominio determinado no están correctamente configurados.

* **Error en las configuraciones de entrega**: El error en las configuraciones de capacidad de envío puede deberse a cualquiera de los siguientes motivos:
   * Inclusión en la lista de bloqueados de las IP asignadas
   * No válido `helo` name
   * Correos electrónicos que se envían desde direcciones IP distintas de las especificadas en el grupo IP de la superficie correspondiente
   * No se pueden enviar correos electrónicos a las bandejas de entrada de los principales ISP

## Edición de una superficie de canal {#edit-channel-surface}

Para editar una superficie de canal, siga los pasos a continuación.

>[!NOTE]
>
>No se puede editar la variable **[!UICONTROL Configuración de notificaciones push]**. Si una superficie de canal solo está configurada para el canal de notificaciones push, no es editable.

1. En la lista, haga clic en un nombre de superficie de canal para abrirlo.

   ![](assets/preset-name.png)

1. Edite sus propiedades como desee.

   >[!NOTE]
   >
   >Si una superficie de canal tiene la variable **[!UICONTROL Activo]** estado, la variable **[!UICONTROL Nombre]**, **[!UICONTROL Seleccionar canal]** y **[!UICONTROL Subdominio]** los campos aparecen atenuados y no se pueden editar.

1. Haga clic en **[!UICONTROL Submit]** para confirmar los cambios.

   >[!NOTE]
   >
   >También puede guardar la superficie del canal como borrador y reanudar la actualización más adelante.

Una vez enviados los cambios, la superficie del canal pasa por un ciclo de validación similar al existente cuando [creación de una superficie de canal](#create-channel-surface). El tiempo de procesamiento de la edición puede tardar hasta **3 horas**.

>[!NOTE]
>
>Si solo edita la variable **[!UICONTROL Descripción]**, **[!UICONTROL Tipo de correo electrónico]** y/o **[!UICONTROL Parámetros de reintentos de correo electrónico]** , la actualización es instantánea.

### Detalles de la actualización {#update-details}

Para superficies de canal que tengan la variable **[!UICONTROL Activo]** , puede comprobar los detalles de la actualización. Para ello:

Haga clic en el **[!UICONTROL Actualización reciente]** que se muestra junto al nombre de la superficie activa.

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
