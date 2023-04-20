---
solution: Journey Optimizer
product: journey optimizer
title: Administrar la lista de supresión
description: Obtenga información sobre cómo acceder y administrar la lista de supresión de Journey Optimizer
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: supresión, lista, rechazo, correo electrónico, optimizador, cuarentena
exl-id: 430a2cd4-781d-4d37-a75d-405f5ed82377
source-git-commit: 2a3bb638ff3485b6c74d92d64126b3b5fd2925e6
workflow-type: tm+mt
source-wordcount: '1488'
ht-degree: 21%

---

# Administrar la lista de supresión {#manage-suppression-list}

con [!DNL Journey Optimizer], puede supervisar todas las direcciones de correo electrónico que se excluyen automáticamente del envío en un recorrido o una campaña, como devoluciones graves, devoluciones leves y quejas por correo no deseado.

Estas direcciones de correo electrónico se recopilan automáticamente en Journey Optimizer **lista de supresión**. Una lista de supresión consta de direcciones y dominios que se excluirán de las audiencias. Recopila direcciones de correo electrónico y dominios que se suprimen en todos los correos en un único entorno de cliente, lo que significa que son específicos de un ID de organización asociado a un ID de simulador de pruebas.

Obtenga más información sobre el concepto de la lista de supresión y su uso en [esta sección](../reports/suppression-list.md).



## Acceso a la lista de supresión  {#access-suppression-list}

Para acceder a la lista detallada de direcciones de correo electrónico y dominios excluidos, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** y seleccione **[!UICONTROL Lista de supresión]**.


![](assets/suppression-list-access.png)

>[!CAUTION]
>
>Los permisos para ver, exportar y administrar la lista de supresión están restringidos a [Administradores de recorrido](../administration/ootb-product-profiles.md#journey-administrator). Más información sobre la administración [!DNL Journey Optimizer] derechos de acceso de los usuarios en [esta sección](../administration/permissions-overview.md).


Hay filtros a su disposición para ayudarle a navegar por la lista.

![](assets/suppression-list-filters.png)

Puede filtrar por la variable **[!UICONTROL Categoría de supresión]**, **[!UICONTROL Tipo de dirección]** o **[!UICONTROL Razón]**. Seleccione una o más opciones para cada criterio. Una vez seleccionados, puede borrar cada filtro o todos los filtros mostrados en la parte superior de la lista.

![](assets/suppression-list-filtering-example.png)


## Comprender las razones de error {#suppression-categories-and-reasons}

Cuando un mensaje no se puede enviar a una dirección de correo electrónico, [!DNL Journey Optimizer] determina por qué se ha producido un error en la entrega y lo asocia con un **[!UICONTROL Categoría de supresión]**.

Las categorías de supresión son las siguientes:

* **Grave**: Un rechazo grave indica una dirección de correo electrónico no válida (es decir, una dirección de correo electrónico que no existe). Esto implica un mensaje de rechazo del servidor de correo electrónico receptor que indica explícitamente que la dirección no es válida. La dirección de correo electrónico se envía inmediatamente a la lista de supresión.

   Cuando el error es el resultado de una queja por correo no deseado, también cae en el **Grave** categoría. La dirección de correo electrónico del destinatario que emitió la queja se envía inmediatamente a la lista de supresión.

* **Leve**: Un rechazo leve es una devolución temporal por correo electrónico que se produjo para una dirección de correo electrónico válida. La dirección de correo electrónico se agrega a la lista de supresión después de varios reintentos. Los errores leves envían una dirección a la lista de supresión una vez que el contador de errores alcanza el umbral de límite. [Más información sobre los reintentos](retries.md)

* **Manual**: Los errores manuales se han agregado manualmente a la lista de supresión. [Más información](#add-addresses-and-domains)

Para cada dirección de correo electrónico de la lista, también puede comprobar la variable **[!UICONTROL Tipo]** (correo electrónico o dominio), **[!UICONTROL Razón]** para excluirlo, quién lo agregó y la fecha y hora en que se agregó a la lista de supresión.

![](assets/suppression-list.png)

Los posibles motivos de un error de entrega son:

| Motivo | Descripción | Categoría |
| --- | --- | --- |
| **[!UICONTROL Destinatario no válido]** | El destinatario no es válido o no existe. | Grave |
| **[!UICONTROL Mensajes devueltos no entregados]** | El mensaje rebotó por un motivo distinto a los errores leves enumerados en esta tabla, como al enviar la velocidad permitida recomendada por un ISP. | Leve |
| **[!UICONTROL Error de DNS]** | El mensaje rebotó debido a un error de DNS. | Leve |
| **[!UICONTROL Buzón de correo lleno]** | El mensaje rebotó debido a que el buzón del destinatario estaba lleno y no pudo aceptar más mensajes. | Leve |
| **[!UICONTROL Retransmisión denegada]** | El receptor bloqueó el mensaje porque no se permite el reenvío. | Leve |
| **[!UICONTROL Challenge-Response]** | El mensaje es una sonda de respuesta a desafíos. | Leve |
| **[!UICONTROL Reclamación por correo no deseado]** | El mensaje se bloqueó porque el destinatario lo marcó como correo no deseado. | Grave |

>[!NOTE]
>
>Los usuarios cancelados de suscripción no reciben correos electrónicos de [!DNL Journey Optimizer], por lo tanto, sus direcciones de correo electrónico no se pueden enviar a la lista de supresión. Su elección se gestiona a nivel de Experience Platform. [Más información sobre la exclusión](../privacy/opt-out.md)


### Reglas de supresión  {#suppression-rules}

En el **[!UICONTROL Lista de supresión]** , también puede editar el parámetro de reintento asociado a las reglas de supresión desde la **[!UICONTROL Editar reglas de supresión]** botón. Utilice esta opción para actualizar el umbral de reintentos del simulador para pruebas actual. [Más información sobre los reintentos](retries.md).


## Añadir direcciones y dominios a la lista de supresión{#add-addresses-and-domains}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_header"
>title="Añadir correos electrónicos o dominios a la lista de supresión"
>abstract="Puede rellenar manualmente la lista de supresión de Journey Optimizer para excluir de la entrega direcciones de correo electrónico o dominios específicos."

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list"
>title="Añadir correos electrónicos o dominios a la lista de supresión"
>abstract="Para rellenar la lista de supresión, puede añadir manualmente direcciones de correo electrónico o dominios: uno a la vez o en modo masivo a través de una carga de archivo CSV. Estas direcciones de correo electrónico o dominios específicos se excluirán del envío."

Cuando un mensaje no se puede enviar a una dirección de correo electrónico, esta dirección se agrega automáticamente a la lista de supresión en función de la regla de supresión definida o del recuento de devoluciones.

Sin embargo, también puede rellenar manualmente la variable [!DNL Journey Optimizer] lista de supresión para excluir de la entrega direcciones de correo electrónico o dominios específicos.

>[!NOTE]
>
>Puede tardar hasta 60 minutos en [!DNL Journey Optimizer] para tener en cuenta las direcciones suprimidas en los correos electrónicos salientes.

Puede añadir direcciones de correo electrónico o dominios [de una en una](#add-one-address-or-domain) o [en modo masivo](#upload-csv-file) mediante la carga de un archivo CSV.

### Adición de una dirección o un dominio {#add-one-address-or-domain}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_address"
>title="Añadir un elemento a la lista de supresión"
>abstract="Puede rellenar la lista de supresión añadiendo direcciones de correo electrónico o dominios uno a uno."

Para añadir una dirección de correo electrónico o un dominio a la lista de supresión, siga los pasos a continuación:

1. Seleccione el **[!UICONTROL Añadir correo electrónico o dominio]** botón.

   ![](assets/suppression-list-add-email.png)

1. Elija la **[!UICONTROL Uno por uno]** .

   ![](assets/suppression-list-add-email-address.png)

1. Seleccione el tipo de dirección: **[!UICONTROL Correo electrónico]** o **[!UICONTROL Dominio]**.

1. Introduzca la dirección de correo electrónico o el dominio que desea excluir del envío.

   >[!NOTE]
   >
   >Asegúrese de introducir una dirección de correo electrónico válida (como abc@compañía.com) o un dominio (como abc.compañía.com).

1. (opcional) Introduzca un motivo. En este campo se permiten todos los caracteres imprimibles ASCII comprendidos entre 32 y 126.

1. Utilice la variable **[!UICONTROL Submit]** para confirmar.

### Cargar un archivo CSV {#upload-csv-file}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_csv"
>title="Cargar CSV para añadir elementos a la lista de supresión"
>abstract="Puede rellenar la lista de supresión cargando un archivo CSV rellenado con las direcciones de correo electrónico o los dominios que desea excluir."

Para añadir un grupo de direcciones de correo electrónico o un dominio a la lista de supresión, siga los pasos a continuación:

1. Seleccione el **[!UICONTROL Añadir correo electrónico o dominio]** botón.
1. Elija la **[!UICONTROL Cargar CSV]** .

   ![](assets/suppression-list-upload-csv.png)

1. Descargue la plantilla CSV que debe utilizar, que incluye las columnas y el formato que se indican a continuación:

   ```
   TYPE,VALUE,COMMENT
   EMAIL,abc@somedomain.com,Comment
   DOMAIN,somedomain.com,Comment
   ```

1. Rellene la plantilla CSV con las direcciones de correo electrónico o los dominios que desee agregar a la lista de supresión. Se permiten todos los caracteres imprimibles ASCII comprendidos entre 32 y 126 en la variable **COMENTARIO** para abrir el Navegador.

   >[!CAUTION]
   >
   >No cambie el nombre de las columnas en la plantilla CSV.
   >
   >El tamaño del archivo no debe superar 1 MB.

1. Una vez finalizado, arrastre y suelte el archivo CSV y utilice el **[!UICONTROL Submit]** para confirmar.

   ![](assets/suppression-list-upload-csv-submit.png)

Una vez finalizada la carga, puede comprobar su estado desde la página [Cargas recientes](#recent-uploads) como se detalla a continuación.

### Comprobar el estado de las cargas {#recent-uploads}

Utilice la variable **[!UICONTROL Cargas recientes]** para comprobar el estado de los últimos archivos CSV cargados.

![](assets/suppression-list-recent-uploads-button.png)

Los estados posibles son:

* **[!UICONTROL Pendiente]**: se está procesando la carga de archivo.
* **[!UICONTROL Error]**: error en el proceso de carga del archivo debido a un problema técnico o a un error de formato de archivo.
* **[!UICONTROL Completado]**: el proceso de carga de archivos se ha completado correctamente.

Durante la carga, si algunas direcciones no tienen el formato correcto, no se agregan al grupo [!DNL Journey Optimizer] lista de supresión.

En ese caso, cuando se completa la carga, se asocia a un informe. Puede descargarlo para comprobar los errores encontrados<!-- and understand why they were not added to the suppression list-->.

![](assets/suppression-list-recent-uploads-report.png)

A continuación, se muestra un ejemplo del tipo de entradas que puede encontrar en el informe de error:

```
type,value,comments,failureReason
Email,examplemail.com,MANUAL,Invalid format for value: examplemail.com
Email,examplemail,MANUAL,Invalid format for value: examplemail
Email,example@mail,MANUAL,Invalid format for value: example@mail
Domain,example,MANUAL,Invalid format for value: example
Domain,example.!com,MANUAL,Invalid format for value: example.!com
Domain,!examplecom,MANUAL,Invalid format for value: !examplecom
```

## Eliminar una dirección de la lista de supresión{#remove-from-suppression-list}

Puede actualizar manualmente la lista de supresión. La eliminación de una dirección de correo electrónico de la cuarentena es una operación delicada que puede afectar a su reputación de IP y a las tasas de envío. Asegúrese de proceder con precaución.

Al eliminar una dirección de correo electrónico o un dominio de la lista de supresión, Adobe Journey Optimizer puede volver a empezar a enviar a esta dirección o dominio.  Obtenga más información sobre la capacidad de envío en [esta sección](../reports/deliverability.md).

Para eliminar una dirección de la lista de supresión, utilice el **[!UICONTROL Eliminar]** botón.

![](assets/suppression-list-delete.png)


>[!NOTE]
>
>Tenga especial cuidado al considerar la eliminación de cualquier dirección de correo electrónico o dominio. En caso de duda, póngase en contacto con un experto en capacidad de entrega.

Por ejemplo, en el caso de una interrupción del servicio de Internet Provider (ISP), los correos electrónicos se marcan erróneamente como rechazos graves porque no se pueden enviar correctamente a su destinatario. Estas direcciones de correo electrónico deben eliminarse de la lista de supresión.

Para recuperar esas direcciones, ejecute una consulta específica con parámetros personalizados, según el contexto de la interrupción. [Obtenga más información en esta muestra](../data/datasets-query-examples.md#isp-outage-query).

Una vez identificadas las direcciones de correo electrónico afectadas, filtre la lista de supresión para mostrarlas. Por ejemplo, si se produjo un corte en el ISP desde el 11 de noviembre de 2022 hasta el 13 de noviembre de 2022 en la variable **test.com** , filtre las direcciones agregadas a la lista de supresión en ese intervalo de tiempo, como se muestra a continuación:

![](assets/remove-from-supp-list.png)

A continuación, puede eliminar las direcciones de correo electrónico en cuarentena de la lista de supresión mediante la función **[!UICONTROL Eliminar]** botón.

## Descargar la lista de supresión {#download-suppression-list}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_download"
>title="Export the list as a CSV file"
>abstract="To download the suppression list, Qou can either export the current list by generating a new file, or download the file that was previously generated."
-->

Para exportar la lista de supresión como archivo CSV, siga los pasos a continuación:

1. Seleccione el **[!UICONTROL Descargar CSV]** botón.

   ![](assets/suppression-list-download-csv.png)

1. Espere hasta que se genere el archivo.

   ![](assets/suppression-list-download-generate.png)

   >[!NOTE]
   >
   >El tiempo de descarga depende del tamaño del archivo, es decir, el número de direcciones que están en la lista de supresión.
   >
   >Se puede procesar una solicitud de descarga a la vez para un entorno limitado determinado.

1. Una vez generado el archivo, recibe una notificación. Haga clic en el icono de campana en la parte superior derecha de la pantalla para mostrarlo.

1. Haga clic en la propia notificación para descargar el archivo.

   ![](assets/suppression-list-download-notification.png)

   >[!NOTE]
   >
   >El vínculo es válido durante 24 horas.

<!--When downloading the CSV file, you can choose to either:

* Download the file that was previously generated by another user or yourself.

* Generate a new file in order to export the current suppression list.-->