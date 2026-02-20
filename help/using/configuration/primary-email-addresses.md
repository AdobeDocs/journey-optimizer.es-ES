---
solution: Journey Optimizer
product: journey optimizer
title: Cambio de direcciones de ejecución
description: Obtenga información sobre cómo determinar qué dirección de correo electrónico utilizar desde el servicio de perfil.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: principal, ejecución, correo electrónico, destinatario, perfil, optimizador
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 36a9a4afb24f3c7909c57e983992de2bf12acd24
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 18%

---

# Administrar los campos de ejecución predeterminados {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definir qué dirección utilizar"
>abstract="Cuando hay varias direcciones de correo electrónico o números de teléfono disponibles en la base de datos (personal, profesional, etc.), puede elegir cuál priorizar para el envío."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="Definir qué dirección utilizar"
>abstract="Edite los campos utilizados para determinar la dirección de correo electrónico o el número de teléfono de los perfiles que desea priorizar para el envío."

Al segmentar un perfil, pueden estar disponibles en la base de datos varias direcciones de correo electrónico o números de teléfono (dirección de correo electrónico profesional, número de teléfono personal, etc.).

En ese caso, [!DNL Journey Optimizer] usa **[!UICONTROL Campos de ejecución]** para determinar qué dirección de correo electrónico o número de teléfono usar del servicio de perfil con prioridad.

Para comprobar los campos que se utilizan actualmente de forma predeterminada, acceda al menú **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración general]** > **[!UICONTROL Campos de ejecución]**.

![](assets/primary-address-execution-fields.png){width=90%}

>[!NOTE]
>
>Los campos de ejecución están disponibles para los canales Correo electrónico, SMS y WhatsApp.

Los valores actuales se utilizan para todas las entregas a nivel de zona protegida. Puede actualizar estos campos si es necesario.

En la mayoría de los casos, se cambia un campo de ejecución globalmente y se define un valor que debe utilizarse para todos los mensajes de correo electrónico, SMS o WhatsApp.

## Actualizar la configuración de administración {#admin-settings}

Para cambiar los campos de ejecución globalmente en el nivel de entorno limitado, siga los pasos a continuación.

1. Acceda al menú **[!UICONTROL Canales]** > **[!UICONTROL Configuración general]** > **[!UICONTROL Campos de ejecución]**.

1. Haga clic en **[!UICONTROL Editar]** para cambiar los valores predeterminados.

   ![](assets/primary-address-edit.png){width=70%}

1. Haga clic en el campo actual de su elección o en el icono de edición para seleccionar un nuevo campo.

   ![](assets/primary-address-edit-field.png){width=70%}

1. Se muestra la lista de campos XDM de tipo correo electrónico disponibles. Seleccione el campo que desea utilizar.

   ![](assets/primary-address-select-field.png){width=90%}

1. Haz clic en **[!UICONTROL Guardar]** para confirmar tu elección.

El campo de ejecución se actualiza y ahora se utiliza como dirección principal.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## Anular el campo de ejecución predeterminado en los parámetros de recorrido {#override-execution-address-journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_execution_address"
>title="Definir un valor personalizado"
>abstract="En algunos casos específicos, puede anular el valor del campo de ejecución predeterminado. Utilice el icono **Habilitar anulación de parámetros** a la derecha de este campo para definir una dirección de correo electrónico o un número de teléfono personalizados para priorizar el envío."

Para casos de uso específicos, puede anular el campo de ejecución establecido globalmente y definir un valor diferente en el nivel de recorrido.

Anular este valor puede resultar útil, por ejemplo, para lo siguiente:

* Pruebe su envío. Puede añadir su propia dirección de correo electrónico o número de teléfono: después de publicar el recorrido, se le envía el mensaje de correo electrónico, SMS o WhatsApp.
* Envíe un mensaje a los suscriptores de una lista. Obtenga más información en [este caso de uso](../building-journeys/message-to-subscribers-uc.md).

Al agregar una acción **[!UICONTROL Correo electrónico]**, **[!UICONTROL SMS]** o **[!UICONTROL WhatsApp]** a un [recorrido](../email/create-email.md#create-email), la dirección de correo electrónico principal o el número de teléfono se muestran bajo los parámetros avanzados del recorrido.

Anule este valor con el icono **[!UICONTROL Habilitar anulación de parámetros]** a la derecha del campo.

![](assets/journey-enable-parameter-override.png){width=85%}

>[!CAUTION]
>
>La anulación de direcciones de correo electrónico o números de teléfono solo debe utilizarse para casos de uso específicos. La mayoría de las veces, no es necesario cambiarlo, ya que el valor definido como el campo principal en **[!UICONTROL Campos de ejecución]** a nivel de zona protegida es el que debería usarse. [Más información](#change-primary-email)

## Anular el campo de ejecución predeterminado en la configuración del canal {#override-execution-address-channel-config}

>[!CONTEXTUALHELP]
>id="ajo_email_config_execution_address"
>title="Sobrescribir la dirección de ejecución predeterminada a utilizar"
>abstract="Cuando hay varias direcciones de correo electrónico o números de teléfono disponibles en la base de datos (personal, profesional, etc.), puede elegir cuál priorizar para el envío. La dirección principal se define en el nivel de entorno limitado, pero aquí puede anular la configuración predeterminada de esta configuración de canal específica."

Puede cambiar la dirección de ejecución predeterminada de un correo electrónico, SMS o WhatsApp [configuración de canal](channel-surfaces.md) específico.

Para ello, vaya a la sección **[!UICONTROL Execution dimension]** y edite el campo dedicado en **[!UICONTROL Execution Address]**.

>[!NOTE]
>
>Para el [canal WhatsApp](../whatsapp/whatsapp-configuration.md#whatsapp-configuration), el **[!UICONTROL Campo de ejecución de WhatsApp]** está en la sección **[!UICONTROL Configuración de WhatsApp]**.

![](assets/sms-config-execution-address.png){width=85%}

A continuación, seleccione un elemento de la lista de campos XDM de tipo de correo electrónico disponibles.

![](assets/sms-config-execution-field.png)

El campo execution se actualiza y luego se utiliza como la dirección principal de las campañas o recorridos que utilizan esta configuración de canal. Anula la [configuración general](#admin-settings) definida en el nivel de espacio aislado.

<!--[Learn more on the execution address in the email configuration ](../email/email-settings.md#execution-address)-->
