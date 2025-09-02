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
source-git-commit: c39a71da901b888ff440a1488658b577ff72cc32
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 19%

---

# Cambio de direcciones de ejecución {#change-primary-email}

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

![](assets/primary-address-execution-fields.png)

Los valores actuales se utilizan para todas las entregas a nivel de zona protegida. Puede actualizar estos campos si es necesario.

En la mayoría de los casos, se cambia un campo de ejecución globalmente y se define un valor que debe utilizarse para todos los mensajes de correo electrónico o SMS. <!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## Actualizar la configuración de administración {#admin-settings}

Para cambiar los campos de ejecución globalmente en el nivel de entorno limitado, siga los pasos a continuación.

1. Acceda al menú **[!UICONTROL Canales]** > **[!UICONTROL Configuración general]** > **[!UICONTROL Campos de ejecución]**.

1. Haga clic en **[!UICONTROL Editar]** para cambiar los valores predeterminados.

   ![](assets/primary-address.png)

1. Haga clic en el campo actual de su elección o en el icono de edición para seleccionar un nuevo campo.

   ![](assets/primary-address-edit.png)

1. Se muestra la lista de campos XDM de tipo correo electrónico disponibles. Seleccione el campo que desea utilizar.

   ![](assets/primary-address-select-field.png)

1. Haz clic en **[!UICONTROL Guardar]** para confirmar tu elección.

El campo de ejecución se actualiza y ahora se utiliza como dirección principal.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## Anular el campo de ejecución predeterminado {#override-default-execution-address}

>[!CONTEXTUALHELP]
>id="ajo_journey_execution_address"
>title="Definir un valor personalizado"
>abstract="En algunos casos específicos, puede anular la dirección de ejecución predeterminada. Utilice el icono **Habilitar anulación de parámetros** a la derecha del campo para definir una dirección principal personalizada."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/primary-email-addresses#journey-parameters" text="Acerca de la dirección de ejecución"

Para casos de uso específicos, puede anular el campo de ejecución establecido globalmente y definir un valor diferente en el nivel de configuración de correo electrónico o en el nivel de recorrido.

Anular este valor puede resultar útil, por ejemplo, para lo siguiente:

* Probar un correo electrónico. Puede añadir su propia dirección de correo electrónico: después de publicar el recorrido, se le envía el correo electrónico.
* Envíe un correo electrónico a los suscriptores de una lista. Obtenga más información en [este caso de uso](../building-journeys/message-to-subscribers-uc.md).

### En la configuración de correo electrónico

Puede cambiar el campo de ejecución predeterminado establecido en [configuración general](#admin-settings) al definir una configuración de canal de correo electrónico. [Más información](../email/email-settings.md#execution-address)

Cuando se define una dirección de ejecución en la configuración de correo electrónico, se utiliza como dirección principal y anula la configuración general a nivel de zona protegida.

### En los parámetros de recorrido {#journey-parameters}

Al agregar una acción **[!UICONTROL Correo electrónico]** o **[!UICONTROL SMS]** a un [recorrido](../email/create-email.md#create-email-journey-campaign), la dirección de correo electrónico principal se muestra bajo los parámetros avanzados de recorrido.

En algunos contextos específicos, puede anular este valor usando el icono **[!UICONTROL Habilitar anulación de parámetros]** a la derecha del campo.

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>La anulación de direcciones de correo electrónico solo debe utilizarse para casos de uso específicos. La mayoría de las veces, no es necesario cambiar la dirección de correo electrónico porque el valor definido como la dirección principal en **[!UICONTROL Campos de ejecución]** es el que debería usarse.


