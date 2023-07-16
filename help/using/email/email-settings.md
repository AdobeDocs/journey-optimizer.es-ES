---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de correo electrónico
description: Obtenga información sobre cómo configurar el correo electrónico en el nivel de superficie de canal
feature: Surface
topic: Administration
role: Admin
level: Intermediate
keywords: configuración, correo electrónico, configuración
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '1783'
ht-degree: 8%

---

# Configuración de correo electrónico {#email-settings}

Para empezar a crear un correo electrónico, debe configurar las superficies de canal de correo electrónico que definan todos los parámetros técnicos necesarios para los mensajes. [Aprenda a crear superficies](../configuration/channel-surfaces.md)

Defina la configuración de correo electrónico en la sección dedicada de la configuración de la superficie de canal.

![](assets/preset-email-settings.png)

La configuración de la superficie de correo electrónico se recoge para enviar comunicaciones siguiendo la lógica siguiente:

* Para los recorridos por lotes, no se aplica a la ejecución por lotes que ya se había iniciado antes de configurar la superficie de correo electrónico. Los cambios se recogerán en la próxima periodicidad o en la nueva ejecución.

* En el caso de los mensajes transaccionales, el cambio se recoge inmediatamente para la siguiente comunicación (con un retraso de hasta cinco minutos).

>[!NOTE]
>
>La configuración actualizada de la superficie de correo electrónico se recoge automáticamente en los recorridos o campañas en los que se utiliza la superficie.

## Tipo de correo electrónico {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Definir la categoría del correo electrónico"
>abstract="Seleccione el tipo de correos electrónicos que se enviarán al utilizar esta superficie: Marketing para correos electrónicos promocionales, que requieren el consentimiento del usuario, o Transaccional para correos electrónicos no comerciales, que también se pueden enviar a perfiles cuya suscripción se haya cancelado en contextos específicos."

En el **TIPO DE CORREO** , seleccione el tipo de mensaje que se enviará con la superficie: **Marketing** o **Transaccional**.

* Elegir **Marketing** para correo electrónico promocional, como promociones semanales de una tienda minorista. Estos mensajes requieren el consentimiento del usuario.

* Elegir **Transaccional** para correos electrónicos no comerciales, como confirmaciones de pedidos, notificaciones de restablecimiento de contraseña o información de entrega, por ejemplo. Estos correos electrónicos se pueden enviar a perfiles que **cancelado** de comunicaciones de marketing. Estos mensajes solo se pueden enviar en contextos específicos.

Al crear un mensaje, debe elegir una superficie de canal válida que coincida con la categoría seleccionada para el correo electrónico.

## Subdominios y grupos de IP {#subdomains-and-ip-pools}

En el **Subdominios y grupos de IP** , debe:

1. Seleccione el subdominio que desea utilizar para enviar los correos electrónicos. [Más información](../configuration/about-subdomain-delegation.md)

1. Seleccione el grupo de IP que se asociará a la superficie. [Más información](../configuration/ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

No se puede continuar con la creación de superficies mientras el grupo de IP seleccionado se encuentra en [edición](../configuration/ip-pools.md#edit-ip-pool) (**[!UICONTROL Procesando]** estado) y nunca se ha asociado con el subdominio seleccionado. De lo contrario, se seguirá utilizando la versión más antigua de la asociación de subdominios/grupos de IP. En este caso, guarde la superficie como borrador y vuelva a intentarlo una vez que el grupo de IP tenga el valor **[!UICONTROL Correcto]** estado.

>[!NOTE]
>
>En los entornos que no son de producción, Adobe no crea subdominios de prueba predeterminados ni concede acceso a un grupo de IP de envío compartido. Tienes que hacerlo [delegar sus propios subdominios](../configuration/delegate-subdomain.md) y utilice las direcciones IP del grupo asignado a su organización.

Una vez seleccionado un grupo de IP, la información de PTR se ve al pasar el ratón por encima de las direcciones IP que se muestran debajo de la lista desplegable Grupo de IP. [Más información sobre los registros PTR](../configuration/ptr-records.md)

![](assets/email-surface-ptr-record.png)

>[!NOTE]
>
>Si no se ha configurado un registro PTR, póngase en contacto con el representante del Adobe.

## Cancelación de suscripción a una lista {#list-unsubscribe}

Tras [selección de un subdominio](#subdomains-and-ip-pools) de la lista, la variable **[!UICONTROL Habilitar cancelación de suscripción a lista]** se muestra la opción.

![](assets/preset-list-unsubscribe.png)

Esta opción está habilitada de manera predeterminada.

Si lo deja habilitado, se incluirá automáticamente un vínculo para cancelar la suscripción en el encabezado del correo electrónico, como:

![](assets/preset-list-unsubscribe-header.png)

Si desactiva esta opción, no se mostrará ningún vínculo para cancelar la suscripción en el encabezado del correo electrónico.

El vínculo de cancelación de suscripción consta de dos elementos:

* Un **cancelar suscripción de dirección de correo electrónico**, a los que se envían todas las solicitudes de cancelación de suscripción.

  Entrada [!DNL Journey Optimizer], la dirección de correo electrónico para cancelar la suscripción es la predeterminada **[!UICONTROL Mailto (cancelar la suscripción)]** dirección mostrada en la superficie de canal, basada en la variable [subdominio seleccionado](#subdomains-and-ip-pools).

  ![](assets/preset-list-unsubscribe-mailto.png)

* El **URL de cancelación de suscripción**, que es la dirección URL de la página de aterrizaje a la que se redirige al usuario una vez cancelada la suscripción.

  Si agrega un [vínculo de no participación de un clic](../privacy/opt-out.md#one-click-opt-out) Para agregar un mensaje creado con esta superficie, la URL de cancelación de suscripción será la URL definida para el vínculo de no participación de un solo clic.

  ![](assets/preset-list-unsubscribe-opt-out-url.png)

  >[!NOTE]
  >
  >Si no agrega un vínculo de no participación de un clic al contenido del mensaje, no se mostrará ninguna página de aterrizaje al usuario.

Obtenga más información sobre cómo añadir un vínculo de cancelación de suscripción de encabezado a los mensajes en [esta sección](../privacy/opt-out.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## Parámetros de encabezado {#email-header}

En el **[!UICONTROL Parámetros de encabezado]** , introduzca los nombres de remitente y direcciones de correo electrónico asociados al tipo de correos electrónicos enviados mediante esa superficie.

* **[!UICONTROL Nombre del remitente]**: Nombre del remitente, como el nombre de la marca.

* **[!UICONTROL Correo electrónico del remitente]**: la dirección de correo electrónico que desea utilizar para sus comunicaciones.

* **[!UICONTROL Responder a (nombre)]**: Nombre que se utilizará cuando el destinatario haga clic en el **Responder** en el software de cliente de correo electrónico.

* **[!UICONTROL Responder a (correo electrónico)]**: La dirección de correo electrónico que se utilizará cuando el destinatario haga clic en el **Responder** en el software de cliente de correo electrónico. [Más información](#reply-to-email)

* **[!UICONTROL Correo electrónico de error]**: Todos los errores generados por los ISP después de unos días de envío del correo (devoluciones asincrónicas) se reciben en esta dirección.

>[!CAUTION]
>
>El **[!UICONTROL Correo electrónico del remitente]** y **[!UICONTROL Correo electrónico de error]** las direcciones deben utilizar el seleccionado actualmente [subdominio delegado](../configuration/about-subdomain-delegation.md). Por ejemplo, si el subdominio delegado es *marketing.luma.com*, puede utilizar *contact@marketing.luma.com* y *error@marketing.luma.com*.

![](assets/preset-header.png)

>[!NOTE]
>
>Las direcciones deben comenzar por una letra (A-Z) y solo pueden contener caracteres alfanuméricos. También puede utilizar guiones bajos `_`, punto`.` y guiones `-` caracteres.

### Responder al correo electrónico {#reply-to-email}

Al definir la variable **[!UICONTROL Responder a (correo electrónico)]** dirección, puede especificar cualquier dirección de correo electrónico siempre que sea una dirección válida, en el formato correcto y sin errores tipográficos.

Para garantizar una administración de respuestas adecuada, siga las recomendaciones a continuación:

* La bandeja de entrada utilizada para las respuestas recibirá todos los correos electrónicos de respuesta, incluidas las notificaciones fuera de la oficina y las respuestas de desafío. Por lo tanto, asegúrese de tener un proceso manual o automatizado para procesar los correos electrónicos que llegan a esta bandeja de entrada.

* Asegúrese de que la bandeja de entrada dedicada tenga suficiente capacidad de recepción para recibir todos los correos electrónicos de respuesta enviados mediante la superficie de correo electrónico. Si la bandeja de entrada devuelve devoluciones, es posible que algunas respuestas de sus clientes no se reciban.

* Las respuestas deben procesarse teniendo en cuenta las obligaciones de privacidad y cumplimiento, ya que pueden contener información de identificación personal (PII).

* No marque los mensajes como correo no deseado en la bandeja de entrada de respuestas, ya que afectará a todas las demás respuestas enviadas a esta dirección.

Además, al definir la variable **[!UICONTROL Responder a (correo electrónico)]** , asegúrese de utilizar un subdominio que tenga una configuración de registro MX válida; de lo contrario, el procesamiento de la superficie de correo electrónico fallará.

Si se produce un error al enviar la superficie de correo electrónico, significa que el registro MX no está configurado para el subdominio de la dirección introducida. Póngase en contacto con el administrador para configurar el registro MX correspondiente o use otra dirección con una configuración de registro MX válida.

>[!NOTE]
>
>Si el subdominio de la dirección que ha introducido es un dominio que [totalmente delegado](../configuration/delegate-subdomain.md#full-subdomain-delegation) para obtener Adobe, póngase en contacto con su administrador de cuentas de Adobe.

### Reenviar correo electrónico {#forward-email}

Si desea reenviar a una dirección de correo electrónico específica todos los correos electrónicos recibidos por [!DNL Journey Optimizer] para el subdominio delegado, póngase en contacto con el Servicio de atención al cliente de Adobe. Deberá proporcionar lo siguiente:

* La dirección de correo electrónico de reenvío que elija. Tenga en cuenta que el dominio de dirección de correo electrónico de reenvío no puede coincidir con ningún subdominio delegado al Adobe.
* Nombre de la zona protegida.
* Nombre de la superficie para la que se utilizará la dirección de correo electrónico de reenvío.
* El actual **[!UICONTROL Responder a (correo electrónico)]** dirección definida en el nivel de superficie de canal.

>[!NOTE]
>
>Solo puede haber una dirección de correo electrónico de reenvío por subdominio. Por lo tanto, si varias superficies utilizan el mismo subdominio, se debe utilizar la misma dirección de correo electrónico de reenvío para todas ellas.

La dirección de correo electrónico de reenvío se configura por Adobe. Esto puede tardar de 3 a 4 días.

## Correo electrónico CCO {#bcc-email}

Puede enviar una copia idéntica (o copia oculta) de los correos electrónicos enviados por [!DNL Journey Optimizer] a una bandeja de entrada CCO donde se almacenarán para fines de cumplimiento o archivo.

Para ello, habilite la variable **[!UICONTROL Correo electrónico CCO]** función opcional en el nivel de superficie de canal. [Más información](../configuration/archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

Además, al definir la variable **[!UICONTROL Correo electrónico CCO]** , asegúrese de utilizar un subdominio que tenga una configuración de registro MX válida; de lo contrario, el procesamiento de la superficie de correo electrónico fallará.

Si se produce un error al enviar la superficie de correo electrónico, significa que el registro MX no está configurado para el subdominio de la dirección introducida. Póngase en contacto con el administrador para configurar el registro MX correspondiente o use otra dirección con una configuración de registro MX válida.

## Parámetros de reintento de correo electrónico {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="Ajustar el período de tiempo de reintento"
>abstract="Los reintentos se realizan durante 3,5 días (84 horas) cuando falla el envío de un correo electrónico debido a un error temporal de mensaje devuelto no entregado. Puede ajustar este período de tiempo de reintento predeterminado para adaptarlo mejor a sus necesidades."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/retries.html?lang=es" text="Acerca de los reintentos"

Puede configurar las variables **Parámetros de reintento de correo electrónico**.

![](assets/preset-retry-parameters.png)

De forma predeterminada, la variable [período de tiempo de reintento](../configuration/retries.md#retry-duration) tiene un valor de 84 horas, pero puede ajustarlo para adaptarlo mejor a sus necesidades.

Debe introducir un valor entero (en horas o minutos) dentro del siguiente intervalo:

* Para los correos electrónicos de marketing, el periodo mínimo de reintento es de 6 horas.
* Para los correos electrónicos transaccionales, el período mínimo de reintento es de 10 minutos.
* Para ambos tipos de correo electrónico, el periodo máximo de reintento es de 84 horas (o 5040 minutos).

Obtenga más información sobre reintentos en [esta sección](../configuration/retries.md).

## Seguimiento de URL {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Definir los parámetros de seguimiento de URL"
>abstract="Utilice esta sección para adjuntar automáticamente parámetros de seguimiento a las direcciones URL presentes en el contenido del correo electrónico. Esta función es opcional."

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="Previsualizar los parámetros de seguimiento de URL"
>abstract="Revise cómo se adjuntarán los parámetros de seguimiento a las direcciones URL presentes en el contenido del correo electrónico."

Puede utilizar **[!UICONTROL Parámetros de seguimiento de URL]** para medir la eficacia de sus esfuerzos de marketing entre canales. Esta función es opcional.

Los parámetros definidos en esta sección se adjuntan al final de las direcciones URL incluidas en el contenido del mensaje de correo electrónico. A continuación, puede capturar estos parámetros en herramientas de análisis web como Adobe Analytics o Google Analytics y crear varios informes de rendimiento.

Puede añadir hasta 10 parámetros de seguimiento con la variable **[!UICONTROL Añadir nuevo parámetro]** botón.

![](assets/preset-url-tracking.png)

Para configurar un parámetro de seguimiento de URL, puede introducir directamente los valores deseados en **[!UICONTROL Nombre]** y **[!UICONTROL Valor]** campos.

También puede editar cada **[!UICONTROL Valor]** mediante el campo [Editor de expresiones](../personalization/personalization-build-expressions.md). Haga clic en el icono de edición para abrir el editor. Desde allí, puede seleccionar los atributos contextuales disponibles o editar directamente el texto.

![](assets/preset-url-tracking-editor.png)

Los siguientes valores predefinidos están disponibles a través del Editor de expresiones:

* **ID de acción de origen**: ID de la acción de correo electrónico agregada al recorrido o la campaña.

* **Nombre de acción de origen**: nombre de la acción de correo electrónico agregada al recorrido o a la campaña.

* **ID de origen**: ID del recorrido o campaña con la que se envió el correo electrónico.

* **Nombre de origen**: nombre del recorrido o campaña con la que se envió el correo electrónico.

* **ID de versión de origen**: ID de la versión de recorrido o campaña con la que se envió el correo electrónico.

* **ID de oferta**: ID de la oferta utilizada en el correo electrónico.

>[!NOTE]
>
>Puede combinar la escritura de valores de texto y el uso de atributos contextuales desde el Editor de expresiones. Cada **[!UICONTROL Valor]** El campo puede contener un número de caracteres hasta el límite de 5 KB.

<!--You can drag and drop the parameters to reorder them.-->

A continuación, se muestran ejemplos de URL compatibles con Adobe Analytics y Google Analytics.

* URL compatible con Adobe Analytics: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* URL compatible con Google Analytics: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

Puede obtener una vista previa dinámica de la URL de seguimiento resultante. Cada vez que se añade, edita o elimina un parámetro, la vista previa se actualiza automáticamente.

![](assets/preset-url-tracking-preview.png)

>[!NOTE]
>
>También puede añadir parámetros de seguimiento personalizados dinámicos a los vínculos presentes en el contenido del correo electrónico, pero esto no es posible en el nivel de superficie. Debe hacerlo al crear el mensaje con el diseñador de correo electrónico. [Más información](message-tracking.md#url-tracking)
