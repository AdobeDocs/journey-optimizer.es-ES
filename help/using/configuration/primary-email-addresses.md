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
source-git-commit: 9cc263d127fdc56f808770d908030b1d14b1f784
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 14%

---

# Cambio de direcciones de ejecución {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definir qué dirección utilizar"
>abstract="Cuando hay varias direcciones de correo electrónico o números de teléfono disponibles en la base de datos (personal, profesional, etc.), puede elegir cuál priorizar para el envío."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="Definir qué dirección utilizar"
>abstract="Edite los campos utilizados para determinar la dirección de correo electrónico o el número de teléfono del perfil que desea priorizar para el envío."

Al segmentar un perfil, pueden estar disponibles en la base de datos varias direcciones de correo electrónico o números de teléfono (dirección de correo electrónico profesional, número de teléfono personal, etc.).

En ese caso, [!DNL Journey Optimizer] utiliza **[!UICONTROL Campos de ejecución]** para determinar qué dirección de correo electrónico o número de teléfono utilizar del servicio de perfil con prioridad.

Para comprobar los campos que se utilizan de forma predeterminada, acceda al **[!UICONTROL Administration]** > **[!UICONTROL Canales]** > **[!UICONTROL General]** > **[!UICONTROL Campos de ejecución]** menú.

![](assets/primary-address-execution-fields.png)

Los valores actuales se utilizan para todas las entregas a nivel de zona protegida. Puede actualizar estos campos si es necesario.

En la mayoría de los casos, se cambia un campo de ejecución globalmente y se define un valor que debe utilizarse para todos los mensajes de correo electrónico o SMS. <!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## Actualizar la configuración de administración {#admin-settings}

Para cambiar los campos de ejecución globalmente en el nivel de entorno limitado, siga los pasos a continuación.

1. Acceda a la  **[!UICONTROL Canales]** > **[!UICONTROL General]** > **[!UICONTROL Campos de ejecución]** menú.

1. Clic **[!UICONTROL Editar]** para cambiar los valores predeterminados.

   ![](assets/primary-address.png)

1. Haga clic en el campo actual de su elección o en el icono de edición para seleccionar un nuevo campo.

   ![](assets/primary-address-edit.png)

1. Se muestra la lista de campos XDM de tipo correo electrónico disponibles. Seleccione el campo que desea utilizar.

   ![](assets/primary-address-select-field.png)

1. Clic **[!UICONTROL Guardar]** para confirmar su elección.

El campo de ejecución se actualiza y ahora se utiliza como dirección principal.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## Anular un valor en los parámetros de recorrido {#journey-parameters}

Solo para casos de uso específicos, puede anular el campo de ejecución establecido globalmente y definir un valor diferente a nivel de recorrido, en particular para el canal de correo electrónico.

Al añadir un **[!UICONTROL Correo electrónico]** acción a [recorrido](../email/create-email.md#create-email-journey-campaign), la dirección de correo electrónico principal se muestra bajo el recorrido de parámetros avanzados.

En algunos contextos específicos, puede anular este valor mediante la variable **[!UICONTROL Habilitar anulación de parámetros]** a la derecha del icono **[!UICONTROL dirección]** field.

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>La anulación de direcciones de correo electrónico solo debe utilizarse para casos de uso específicos. La mayoría de las veces, no es necesario cambiar la dirección de correo electrónico porque el valor definido como la dirección principal en la variable **[!UICONTROL Campos de ejecución]** es el que debe usarse.

Anular este valor puede resultar útil, por ejemplo, para lo siguiente:

* Probar un correo electrónico. Puede añadir su propia dirección de correo electrónico: después de publicar el recorrido, se le envía el correo electrónico.
* Envíe un correo electrónico a los suscriptores de una lista. Obtenga más información en [este caso de uso](../building-journeys/message-to-subscribers-uc.md).
