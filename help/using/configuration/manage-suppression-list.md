---
title: Administrar la lista de supresión
description: 'Obtenga información sobre cómo acceder y administrar la lista de supresión de Journey Optimizer '
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 50c3dfe4f756e7c6e8f210dc9d3f615965c3a053
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 5%

---


# Administrar la lista de supresión {#manage-suppression-list}

Con [!DNL Journey Optimizer], puede supervisar todas las direcciones de correo electrónico que se excluyen automáticamente del envío en un recorrido, como:

* Direcciones que no son válidas (rechazos graves).
* Direcciones que devuelven mensajes de forma uniforme y que podrían afectar negativamente a la reputación del correo electrónico si continúa incluyéndolas en los envíos.
* Destinatarios que emiten una queja de correo no deseado de algún tipo contra uno de sus mensajes de correo electrónico.

Estas direcciones de correo electrónico se recopilan automáticamente en la **lista de supresión** de Journey Optimizer. Obtenga más información en [esta sección](../suppression-list.md).

## Acceso a la lista de supresión {#access-suppression-list}

Para acceder a la lista detallada de direcciones de correo electrónico excluidas, abra el menú **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** y haga clic en el enlace **[!UICONTROL View suppression lists]**.

![](../assets/suppression-list-link.png)

<!--To access the detailed list of excluded email addresses, go to **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]**, and select **[!UICONTROL Suppression list]**.
You can also display the suppression list content using the **[!UICONTROL View suppression list]** link through the **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** menu, but this view does not allow you to edit the list.

![](../assets/suppression-list-access-temp.png)-->

Los filtros están disponibles para ayudarle a navegar por la lista.

![](../assets/suppression-list-filters-temp.png)

<!--![](../assets/suppression-list-filters.png)

You can filter on the **[!UICONTROL Suppression category]**, **[!UICONTROL Address type]**, or **[!UICONTROL Reason]**. Select the option(s) of your choice for each criterion.

![](../assets/suppression-list-filtering-example.png)

Once selected, you can clear each filter or all filters displayed on top of the list.-->

## Categorías y motivos de supresión {#suppression-categories-and-reasons}

Cuando no se puede enviar un mensaje a una dirección de correo electrónico, [!DNL Journey Optimizer] determina por qué ha fallado el envío y lo asocia con **[!UICONTROL Suppression category]**.

Las categorías de supresión son las siguientes:

* **Grave**: La dirección de correo electrónico se envía inmediatamente a la lista de supresión.

   >[!NOTE]
   >
   >Cuando el error es el resultado de una queja por correo no deseado, también cae en la categoría **Hard**. La dirección de correo electrónico del destinatario que emitió la queja se envía inmediatamente a la lista de supresión.

* **Leve**: Los errores leves envían una dirección a la lista de supresión una vez que el contador de errores alcanza el umbral de límite. [Más información sobre los reintentos](retries.md)

   <!--
    **Ignored**:
    * When the error occurred for a valid email address but is known to be temporary, such as a failed connection attempt or a temporary technical issue, the email address is added to the suppression list once the error counter reaches the limit threshold. [Learn more on retries](retries.md).
    * When the error is the result of a spam complaint, the email address of the recipient who issued the complaint is immediately sent to the suppression list.
    -->

* **Manual**: También puede añadir manualmente una dirección de correo electrónico o un dominio a la lista de supresión. [Más información](#add-addresses-and-domains)

>[!NOTE]
>
>Obtenga más información sobre los rechazos leves y los rechazos graves en la sección [Tipos de errores de envío](../suppression-list.md#delivery-failures).

Para cada dirección de correo electrónico de la lista, también puede comprobar el **[!UICONTROL Type]** (correo electrónico o dominio), **[!UICONTROL Reason]** para excluirlo, quién lo agregó y la fecha y hora en que se agregó a la lista de supresión.

<!--![](../assets/suppression-list.png)-->

Los posibles motivos de un error de entrega son:

| Motivo | Descripción | Categoría de supresión |
| --- | --- | --- |
| **[!UICONTROL Invalid Recipient]** | El destinatario no es válido o no existe. | Grave |
| **[!UICONTROL Soft Bounce]** | El mensaje rebotó por un motivo distinto a los errores leves enumerados en esta tabla, como al enviar la velocidad permitida recomendada por un ISP. | Leve |
| **[!UICONTROL DNS Failure]** | El mensaje rebotó debido a un error de DNS. | Leve |
| **[!UICONTROL Mailbox Full]** | El mensaje rebotó debido a que el buzón del destinatario estaba lleno y no pudo aceptar más mensajes. | Leve |
| **[!UICONTROL Relaying Denied]** | El receptor bloqueó el mensaje porque no se permite el reenvío. | Leve |
| **[!UICONTROL Challenge-Response]** | El mensaje es una sonda de respuesta a desafíos. | Leve |

>[!NOTE]
>
>Los usuarios cancelados de suscripción no reciben correos electrónicos de [!DNL Journey Optimizer], por lo que sus direcciones de correo electrónico no se pueden enviar a la lista de supresión. Su elección se gestiona a nivel de Experience Platform. Obtenga más información sobre [exclusión](../consent.md).

<!--
Removed from the table provided by SparkPost/Momentum:
| **[!UICONTROL Undetermined]** | The bounce reason received from the recipient domain Message Transfer Agent (MTA) could not be identified. | Ignored |
| **[!UICONTROL Too Large]** | The message bounced because it was too large for the recipient. [Retries](retries.md) will be performed: you can edit the message size and re-inject it for delivery. | Ignored |
| **[!UICONTROL Timeout]** | The message timed out, meaning it soft bounced and reached the message retry limit (3.5 days). | Ignored |
| **[!UICONTROL Admin Failure]** | The message was failed according to the policies configured by the sending system administrator. ///For example, if emails are blackholed at the global, domain or binding level using the "blackhole" directive, this bounce code is used. | Ignored |
| **[!UICONTROL Generic Bounce: No RCPT]** | No recipient could be determined for the message. | Ignored |
| **[!UICONTROL Generic Bounce]** | The message failed for unspecified reasons. | Ignored |
| **[!UICONTROL Mail Block]** | The message was blocked by the receiver (i.e. recipient MTA). | Ignored |
| **[!UICONTROL Spam Block]** | The message was blocked by the receiver as coming from a known spam source. It could be a sending IP block for example. | Ignored |
| **[!UICONTROL Spam Content]** | The message content was blocked by the receiver (recipient MTA) as spam. | Ignored |
| **[!UICONTROL Prohibited Attachment]** | The message was blocked by the receiver because it contained an attachment. | Ignored |
| **[!UICONTROL Auto-Reply]** | The message is an auto-reply/vacation mail. | Ignored |
| **[!UICONTROL Transient Failure]** | Message transmission has been temporarily delayed. | Ignored |
| **[!UICONTROL Subscribe]** | The message is a subscribe request. | Ignored |
| **[!UICONTROL Unsubscribe]** | The message is an unsubscribe request. | Hard |
-->

<!--Note to add eventually: If a user is subscribed and [!DNL Journey Optimizer] fails to send emails to their subscribed email address, they will get added to the suppression list. (not sure it's possible to subscribe through AJO or need to find reference to Experience Platform doc?)-->

<!--## Manually add addresses and domains {#add-addresses-and-domains}

When a message fails to be delivered to an email address, this address is automatically added to the suppression list based on the defined suppression rule or bounce count.

However, you can also manually populate the [!DNL Journey Optimizer] suppression list to exclude specific email addresses and/or domains from your sending.

You may add email addresses or domains [one at a time](#add-one-address-or-domain), or [in bulk mode](#upload-csv-file) through a CSV file upload.

To do this, select the **[!UICONTROL Add email or domain]** button, then follow one of the methods below.

![](../assets/suppression-list-add-email.png)

### Add one address or domain {#add-one-address-or-domain}

1. Select the **[!UICONTROL One by one]** option.

    ![](../assets/suppression-list-add-email-address.png)

1. Choose the address type: **[!UICONTROL Email address]** or **[!UICONTROL Domain address]**.

1. Enter the email address or domain you want to exclude from your sending.

    >[!NOTE]
    >
    >Make sure you enter a valid email address (such as abc@company) or domain (such as abc.company.com).

1. Specify a reason if needed.

1. Click **[!UICONTROL Submit]**.

### Upload a CSV file {#upload-csv-file}

1. Select the **[!UICONTROL Upload CSV]** option.

    ![](../assets/suppression-list-upload-csv.png)

1. Download the CSV template to use, which includes the columns and format below:

    ```
    TYPE,VALUE,COMMENT
    EMAIL,abc@somedomain.com,Comment
    DOMAIN,somedomain.com,Comment
    ```
    You can also download this template from the **[!UICONTROL Suppression list]** main view.

    >[!CAUTION]
    >
    >Do not change the names of the columns in the CSV template.
    >
    >The file size should not exceed 50 MB.

1. Fill in the CSV template with the email addresses and/or domains you want to add to the suppression list.

1. Once completed, drag and drop your CSV file, then click **[!UICONTROL Upload file]**.

    ![](../assets/suppression-list-upload-file-button.png)

1. Click **[!UICONTROL Submit]**.

### Check recent uploads status {#recent-uploads}

You can check the list of the latest CSV files you uploaded.

To do this, from the **[!UICONTROL Suppression list]** view, click the **[!UICONTROL Recent uploads]** button.

![](../assets/suppression-list-recent-uploads-button.png)

The latest uploads you submitted and their corresponding statuses are displayed.

If an error report is associated with a file, you can download it to check the errors encountered.

![](../assets/suppression-list-recent-uploads-error.png)

Below is an example of the type of entries you can find in the error report:

```
type,value,comments,failureReason
Email,examplemail.com,MANUAL,Invalid format for value: examplemail.com
Email,examplemail,MANUAL,Invalid format for value: examplemail
Email,example@mail,MANUAL,Invalid format for value: example@mail
Domain,example,MANUAL,Invalid format for value: example
Domain,example.!com,MANUAL,Invalid format for value: example.!com
Domain,!examplecom,MANUAL,Invalid format for value: !examplecom
```

-->


