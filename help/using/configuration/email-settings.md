---
title: Configuración de correo electrónico
description: Obtenga información sobre cómo configurar la configuración de correo electrónico en el nivel de superficie del canal
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '1173'
ht-degree: 2%

---

# Configuración de correo electrónico {#email-settings}

Defina la configuración del correo electrónico en la sección dedicada de la configuración de la superficie del canal (es decir, la configuración preestablecida de mensajes). Aprenda a crear superficies en [esta sección](channel-surfaces.md).

![](assets/preset-email-settings.png)

## Tipo de correo electrónico {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Definir la categoría de correo electrónico"
>abstract="Seleccione el tipo de mensajes que se enviarán al utilizar esta superficie: Marketing para mensajes promocionales, que requieren el consentimiento del usuario, o Transactional para mensajes no comerciales, que también se puede enviar a perfiles cancelados de suscripción en contextos específicos."

En el **TIPO DE CORREO ELECTRÓNICO** seleccione el tipo de mensaje que se enviará con la superficie: **Marketing** o **Transaccional**.

* Choose **Marketing** para correo electrónico promocional: estos mensajes requieren el consentimiento del usuario.

* Choose **Transaccional** para correo electrónico no comercial, como confirmación de pedido, notificaciones de restablecimiento de contraseña o información de entrega, por ejemplo.

>[!CAUTION]
>
>**Transaccional** los correos electrónicos se pueden enviar a perfiles que cancelan la suscripción a las comunicaciones de marketing. Estos mensajes solo se pueden enviar en contextos específicos.

When [creación de un mensaje](../messages/get-started-content.md#create-new-message), debe elegir una superficie de canal válida que coincida con la categoría seleccionada para el correo electrónico.

## Subdominio y grupo de IP {#subdomains-and-ip-pools}

En el **DETALLES DEL GRUPO DE IP Y SUBDOMINIOS** , debe:

1. Seleccione el subdominio que desea utilizar para enviar los correos electrónicos. [Más información](about-subdomain-delegation.md)

1. Seleccione el grupo IP que desea asociar con la superficie. [Más información](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

No puede continuar con la creación de superficie mientras el grupo IP seleccionado está bajo [edición](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** ) y nunca se ha asociado con el subdominio seleccionado. De lo contrario, se seguirá utilizando la versión más antigua de la asociación de agrupación/subdominio de IP. Si este es el caso, guarde la superficie como borrador y vuelva a intentarlo una vez que el grupo de IP tenga la variable **[!UICONTROL Success]** estado.

>[!NOTE]
>
>Para los entornos que no son de producción, Adobe no crea subdominios de prueba predeterminados ni concede acceso a un grupo de IP de envío compartido. Debe [delegar sus propios subdominios](delegate-subdomain.md) y usar las IP del grupo asignado a su organización.

## Cancelación de suscripción a una lista {#list-unsubscribe}

upon [selección de un subdominio](#subdomains-and-ip-pools) de la lista, la variable **[!UICONTROL Enable List-Unsubscribe]** se muestra.

![](assets/preset-list-unsubscribe.png)

Esta opción está habilitada de manera predeterminada.

Si lo deja habilitado, se incluirá automáticamente un vínculo de cancelación de suscripción en el encabezado del correo electrónico, como:

![](assets/preset-list-unsubscribe-header.png)

Si desactiva esta opción, no aparecerá ningún vínculo de cancelación de suscripción en el encabezado del correo electrónico.

El vínculo de cancelación de suscripción consta de dos elementos:

* Un **cancelar la suscripción de la dirección de correo electrónico**, a la que se envían todas las solicitudes de cancelación de suscripción.

   En [!DNL Journey Optimizer], la dirección de correo electrónico de cancelación de suscripción es la predeterminada **[!UICONTROL Mailto (unsubscribe)]** dirección mostrada en la superficie del canal, según la variable [subdominio seleccionado](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* La variable **cancelar la suscripción de la dirección URL**, que es la dirección URL de la página de aterrizaje a la que se redirige al usuario una vez que se da de baja de la suscripción.

   Si agrega un [vínculo de exclusión con un solo clic](../messages/consent.md#one-click-opt-out) en un mensaje creado con esta superficie, la URL de cancelación de suscripción será la URL definida para el vínculo de exclusión de un clic.

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >Si no agrega un vínculo de exclusión de un clic al contenido del mensaje, no se mostrará ninguna página de aterrizaje al usuario.

Obtenga más información sobre cómo añadir un vínculo de cancelación de suscripción a un encabezado a sus mensajes en [esta sección](../messages/consent.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## Parámetros de encabezado{#email-header}

En el **[!UICONTROL HEADER PARAMETERS]** , introduzca los nombres del remitente y las direcciones de correo electrónico asociadas al tipo de correos electrónicos enviados con esa superficie.

>[!CAUTION]
>
>Las direcciones de correo electrónico deben utilizar el seleccionado actual [subdominio delegado](about-subdomain-delegation.md).

* **[!UICONTROL Sender name]**: El nombre del remitente, como el nombre de su marca.

* **[!UICONTROL Sender email]**: La dirección de correo electrónico que desea utilizar para sus comunicaciones. Por ejemplo, si el subdominio delegado es *marketing.luma.com*, puede usar *contact@marketing.luma.com*.

* **[!UICONTROL Reply to (name)]**: El nombre que se utilizará cuando el destinatario haga clic en la variable **Responder** en el software cliente de correo electrónico.

* **[!UICONTROL Reply to (email)]**: La dirección de correo electrónico que se utilizará cuando el destinatario haga clic en el **Responder** en el software cliente de correo electrónico. Debe utilizar una dirección definida en el subdominio delegado (por ejemplo, *reply@marketing.luma.com*), de lo contrario, se enviarán los correos electrónicos.

* **[!UICONTROL Error email]**: Todos los errores generados por los ISP después de unos días de envío del correo (devoluciones asincrónicas) se reciben en esta dirección.

![](assets/preset-header.png)

>[!NOTE]
>
>Las direcciones deben comenzar por una letra (A-Z) y solo pueden contener caracteres alfanuméricos. También puede utilizar guiones bajos `_`, punto`.` Guión `-` caracteres.

### Reenviar correo electrónico {#forward-email}

Si desea reenviar a una dirección de correo electrónico específica, todos los correos electrónicos recibidos por [!DNL Journey Optimizer] para el subdominio delegado, póngase en contacto con el servicio de atención al cliente de Adobe. Deberá proporcionar:

* La dirección de correo electrónico de reenvío que elija. Tenga en cuenta que el dominio de dirección de correo electrónico de reenvío no puede coincidir con ningún subdominio delegado a Adobe.
* El nombre del simulador de pruebas.
* El nombre de superficie para el que se utilizará la dirección de correo electrónico de reenvío.
* El **[!UICONTROL Reply to (email)]** dirección definida en el nivel de superficie del canal.

>[!NOTE]
>
>Solo puede haber una dirección de correo electrónico de reenvío por subdominio. Por lo tanto, si varias superficies utilizan el mismo subdominio, se debe utilizar la misma dirección de correo electrónico de reenvío para todas ellas.

La dirección de correo electrónico de reenvío se configura por Adobe. Esto puede tardar entre 3 y 4 días.

## Correo electrónico CCO {#bcc-email}

Puede enviar una copia idéntica (o una copia ciega de los correos electrónicos enviados por [!DNL Journey Optimizer] a una bandeja de entrada BCC donde se almacenarán para fines de cumplimiento o archivo.

Para ello, habilite la **[!UICONTROL BCC EMAIL]** función opcional en el nivel de superficie del canal. [Más información](bcc-email.md)

![](assets/preset-bcc.png)

## Parámetros de reintentos de correo electrónico {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="Ajustar el período de tiempo de reintento"
>abstract="Los reintentos se realizan durante 3,5 días (84 horas) cuando un envío de correo electrónico falla debido a un error temporal de devolución del mensaje. Puede ajustar este período de tiempo de reintento predeterminado para adaptarlo mejor a sus necesidades."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html" text="Acerca de los reintentos"

Puede configurar la variable **PARÁMETROS DE REINTENTO DE CORREO ELECTRÓNICO**.

![](assets/preset-retry-parameters.png)

De forma predeterminada, la variable [periodo de tiempo de reintento](retries.md#retry-duration) está configurada a 84 horas, pero puede ajustar esta configuración para adaptarla mejor a sus necesidades.

Debe introducir un valor entero (en horas o minutos) dentro del siguiente intervalo:

* En los correos electrónicos de marketing, el periodo de reintento mínimo es de 6 horas.
* Para los correos electrónicos transaccionales, el periodo mínimo de reintentos es de 10 minutos.
* Para ambos tipos de correo electrónico, el periodo de reintento máximo es de 84 horas (o 5040 minutos).

Obtenga más información sobre los reintentos en [esta sección](retries.md).

## Seguimiento de URL {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Definir los parámetros de seguimiento de URL"
>abstract="Utilice esta sección para adjuntar automáticamente parámetros de seguimiento a las direcciones URL presentes en el contenido del correo electrónico. Esta función es opcional."

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="Vista previa de los parámetros de seguimiento de URL"
>abstract="Revise cómo se adjuntarán los parámetros de seguimiento a las direcciones URL presentes en el contenido del correo electrónico."

Puede usar **[!UICONTROL URL TRACKING PARAMETERS]** para medir la eficacia de sus esfuerzos de marketing en todos los canales. Esta función es opcional.

Los parámetros definidos en esta sección se anexarán al final de las direcciones URL incluidas en el contenido del mensaje de correo electrónico. A continuación, puede capturar estos parámetros en herramientas de análisis web, como Adobe Analytics o Google Analytics, y crear varios informes de rendimiento.

![](assets/preset-url-tracking.png)

Se rellenan automáticamente tres parámetros de seguimiento de URL como ejemplo al crear una superficie de canal. Puede editarlas y agregar hasta 10 parámetros de seguimiento mediante la variable **[!UICONTROL Add new parameter]** botón.

Para configurar un parámetro de seguimiento de URL, puede introducir directamente los valores deseados en la variable **[!UICONTROL Name]** y **[!UICONTROL Value]** campos.

<!--You can also choose from a list of predefined values by navigating to the following objects:
* Journey attributes: **Source id**, **Source name**, **Source version id**
* Action attributes: **Action id**, **Action name**
* Offer decisioning attributes: **Offer id**, **Offer name**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>Do not select a folder: make sure to browse to the necessary folder and select a profile attribute to use as a tracking parameter value.-->

También puede editar cada **[!UICONTROL Value]** utilizando la variable [Editor de expresiones](../personalization/personalization-build-expressions.md). Haga clic en el icono de edición para abrir el Editor de expresiones. Desde allí, puede seleccionar los atributos contextuales de su elección o editar directamente el texto.

![](assets/preset-url-tracking-editor.png)

<!--You can drag and drop the parameters to reorder them.-->

A continuación se muestran ejemplos de URL compatibles con Adobe Analytics y Google Analytics.

* URL compatible con Adobe Analytics: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* URL compatible con Google Analytics: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

>[!NOTE]
>
>Puede combinar la escritura de valores de texto y el uso de atributos contextuales desde el Editor de expresiones. Cada **[!UICONTROL Value]** puede contener hasta 255 caracteres en total.

Puede obtener una vista previa dinámica de la URL de seguimiento resultante. Cada vez que se añade, edita o elimina un parámetro, la vista previa se actualiza automáticamente.

![](assets/preset-url-tracking-preview.png)