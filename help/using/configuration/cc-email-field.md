---
solution: Journey Optimizer
product: journey optimizer
title: CC (Carbon Copy) en la configuración del canal de correo electrónico
description: Configurar destinatarios de CC visibles en el canal de correo electrónico Journey Optimizer. Obtenga información acerca de cómo establecer el campo CC, cómo difiere de BCC y limitaciones.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
hide: true
hidefromtoc: true
keywords: CC, copia de carbono, correo electrónico, configuración del canal, encabezados de correo electrónico, BCC
badge: label="Disponibilidad limitada" type="Informative"
exl-id: 9649cc07-3183-4510-b5d9-b1e33eff43e9
source-git-commit: 780a9259ee081336d1efb3e38c2a8eee4e97b7e3
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 1%

---

# Añadir un campo CC a los correos electrónicos {#cc-email-field}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_cc"
>title="Definir una dirección de correo electrónico CC"
>abstract="Puede agregar un campo CC (copia de carbono) visible a los correos electrónicos enviados con esta configuración de canal. Introduzca una dirección de correo electrónico fija o utilice la personalización (atributo de perfil o variable de contexto). Tenga en cuenta que el uso de CC se cuenta en el volumen de mensajes con derecho."

>[!AVAILABILITY]
>
>Esta función está disponible para todos los clientes en Disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

Puede agregar un campo CC (copia de carbón) visible a los correos electrónicos enviados por [!DNL Journey Optimizer] a través de sus recorridos y campañas. Esta característica opcional se configura en el nivel de [configuración de canal](channel-surfaces.md), junto con los parámetros de encabezado de correo electrónico y la opción de correo electrónico CCO.

>[!CAUTION]
>
>El uso de las funciones CC se cuenta contra el número de mensajes para los que tiene licencia. Habilítelo solo donde necesite destinatarios CC visibles. Compruebe si hay volúmenes con licencia en el contrato.

Al igual que [CCO](archiving-support.md#bcc-email), el campo CC está diseñado para enviar una copia del correo electrónico a una dirección adicional. Sin embargo, difiere de CCO en los siguientes aspectos:

* La dirección de correo electrónico de CC es visible para el destinatario principal, por lo que le permite ver quién se copia y saber con quién ponerse en contacto para realizar el seguimiento.
* A diferencia de CCO, el campo de correo electrónico CC admite la personalización, lo que le permite utilizar una configuración de canal para muchos casos y enviar la copia a la persona adecuada por destinatario (por ejemplo, su administrador de relaciones). En el caso de campañas activadas por API, esto le permite registrar la dirección correspondiente a un evento o transacción específicos.

>[!NOTE]
>
>Si necesita conservar copias donde la dirección no debe ser visible para el destinatario con fines de archivo o cumplimiento normativo, use [CCO](archiving-support.md#bcc-email) en lugar de CC.

## Habilitar correo electrónico CC {#enable-cc}

Para habilitar la opción **[!UICONTROL CC email]**, configure el campo CC en la [configuración del canal de correo electrónico](../email/email-settings.md).

![](assets/email-config-cc.png)

Puede especificar cualquier dirección externa en el formato correcto, excepto una dirección de correo electrónico definida en un subdominio delegado a Adobe. Por ejemplo, si delegó el subdominio *marketing.luma.com* en Adobe, queda prohibida cualquier dirección como *abc@marketing.luma.com*.

>[!CAUTION]
>
>Sólo puede definir una dirección de correo electrónico. Asegúrese de que la dirección CC tiene la capacidad de recepción suficiente para almacenar todos los correos electrónicos enviados mediante la configuración del canal actual.
>
>En [esta sección](#cc-recommendations-limitations) se enumeran más recomendaciones.

El campo **[!UICONTROL CC email]** acepta tres tipos de valores:

* Un **valor codificado**, que puede ser una dirección de correo electrónico fija.

* Un **atributo profile**, como la dirección de correo electrónico del administrador de relaciones disponible en el perfil.

* Un **atributo contextual** - este valor sólo se puede usar en campañas activadas por API **.** Se recupera de la carga útil de API que debe incluir la variable de contexto `context.channel.email.ccvalues` con el valor de dirección CC.

  >[!WARNING]
  >
  >Cuando CC se establece utilizando una **variable de contexto**, sólo se admite en **campañas activadas por API**. Si utiliza esa configuración de canal en un viaje o una campaña de acción, el correo electrónico se envía únicamente al destinatario principal; no se envía ninguna copia a la dirección CC.

Cualquier [adjunto](../email/pdf-attachments.md) incluido en el mensaje se envía al destinatario principal y a la dirección CC.

Si el valor CC no es válido o falta en el momento de envío (por ejemplo, una variable de contexto vacía), se omite la copia CC; el destinatario principal sigue recibiendo el correo electrónico.

Si hay varios valores para el campo CC (por ejemplo, cuando se utiliza un atributo o expresión de perfil que se resuelve en varias direcciones), solo se utiliza el primer valor para enviar el correo electrónico.

## Editar correo electrónico CC en configuraciones de canal existentes {#cc-edit}

Si [edita una configuración de correo electrónico](channel-surfaces.md#edit-channel-surface) y agrega o cambia el campo CC, solo puede usar:

* Una dirección de correo electrónico **codificada** CC, o
* Una **variable de contexto** (para uso activado por API).

>[!CAUTION]
>
>Al editar una configuración de canal de correo electrónico existente, no puede agregar nuevos [atributos de perfil](../personalization/personalization-build-expressions.md#sources) al campo **[!UICONTROL Correo electrónico CC]**. Debe crear [una nueva configuración de canal](channel-surfaces.md#create-channel-surface).

## Recomendaciones y limitaciones {#cc-recommendations-limitations}

* **Derecho:** el uso de CC se cuenta para el volumen de mensajes permitido. Utilice CC solo donde necesite destinatarios CC visibles. Compruebe si hay volúmenes con licencia en el contrato.

* **Privacidad y cumplimiento:** Para garantizar su cumplimiento de la privacidad, los correos electrónicos CC deben ser procesados por un sistema capaz de almacenar información de identificación personal (PII) de forma segura cuando corresponda. Dado que los mensajes pueden contener datos confidenciales o privados, como PII, asegúrese de que la dirección CC sea correcta y de que el acceso a los mensajes sea seguro.

* **Administración de la bandeja de entrada:** La bandeja de entrada usada para CC debe ser administrada correctamente para espacio y entrega. Si la bandeja de entrada devuelve rebotes, es posible que algunos correos electrónicos no se reciban.

* **Momento de entrega:** Los mensajes se pueden enviar a la dirección de correo electrónico CC antes de los destinatarios de destino. Los mensajes CC también se pueden enviar aunque los mensajes originales tengan [rebotado](../reports/suppression-list.md#delivery-failures).

* **Informes:** Las aperturas, los clics y otras participaciones de los destinatarios de CC se incluyen en las métricas de informes de correo electrónico. Por lo tanto, cualquier apertura o clic de los destinatarios de CC provocará errores de cálculo en [informes](../reports/report-gs-cja.md).

* **Correo no deseado:** No marque los mensajes como correo no deseado en la bandeja de entrada CC, ya que afectará a todos los demás correos electrónicos enviados a esta dirección.

* **Capacidad de entrega:** Use CC de acuerdo con sus prácticas de envío y las expectativas de los destinatarios. El uso excesivo de CC puede afectar la capacidad de entrega; siga las [prácticas recomendadas de entrega](../reports/deliverability.md) y los términos del contrato.

>[!CAUTION]
>
>No haga clic en el vínculo &quot;Cancelar la suscripción&quot; en los correos electrónicos enviados a la dirección de CC, ya que cancelará inmediatamente la suscripción del destinatario del correo electrónico **To**.
