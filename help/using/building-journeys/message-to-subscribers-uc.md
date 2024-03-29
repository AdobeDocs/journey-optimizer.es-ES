---
solution: Journey Optimizer
product: journey optimizer
title: Envío de un mensaje a los suscriptores
description: Obtenga información sobre cómo crear un recorrido para enviar un mensaje a los suscriptores de una lista
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: recorrido, caso de uso, mensaje, suscriptores, lista, lectura
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 17%

---

# Caso de uso: Envío de un mensaje a los suscriptores de una lista{#send-a-message-to-the-subscribers-of-a-list}

El propósito de este caso de uso es crear un recorrido para enviar un mensaje a los suscriptores de una lista.

En este ejemplo, la variable **[!UICONTROL Detalles de consentimiento y preferencia]** grupo de campos de [!DNL Adobe Experience Platform] se utiliza. Para buscar este grupo de campos, en **[!UICONTROL Administración de datos]** menú, elija **[!UICONTROL Esquemas]**. En el **[!UICONTROL Grupos de campos]** pestaña, introduzca el nombre del grupo de campos en el campo de búsqueda.

![Este grupo de campos incluye el elemento subscriptions](assets/consent-and-preference-details-field-group.png)

Para configurar este recorrido, siga estos pasos:

1. Cree un recorrido que comience con una **[!UICONTROL Leer]** actividad. [Más información](journey-gs.md).
1. Añadir un **[!UICONTROL Correo electrónico]** actividad de acción al recorrido. [Más información](journeys-message.md).
1. En el **[!UICONTROL Parámetros de correo electrónico]** de la sección **[!UICONTROL Correo electrónico]** configuración de actividad, sustituya la dirección de correo electrónico predeterminada (`PersonalEmail.adress`) con la dirección de correo electrónico de los suscriptores de la lista:

   1. Haga clic en **[!UICONTROL Habilitar anulación de parámetros]** en la parte derecha del icono **[!UICONTROL Dirección]** y haga clic en el campo **[!UICONTROL Editar]** icono.

      ![](assets/message-to-subscribers-uc-1.png)

   1. En el editor de expresiones, introduzca la expresión para recuperar las direcciones de correo electrónico de los suscriptores. [Más información](expression/expressionadvanced.md).

      Este ejemplo muestra una expresión que incluye referencias a campos de asignación:

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      En este ejemplo, se utilizan estas funciones:

      | Función | Descripción | Ejemplo |
      | --- | --- | --- |
      | `entry` | Hacer referencia a un elemento de mapa según el área de nombres seleccionada | Consulte una lista de suscripción específica |
      | `firstEntryKey` | Recuperación de la primera clave de entrada de un mapa | Recuperación de la primera dirección de correo electrónico de los suscriptores |

      En este ejemplo, la lista de suscripción se denomina `daily-email`. Las direcciones de correo electrónico se definen como claves en la variable `subscribers` map, que está vinculado al mapa de la lista de suscripción.

      Más información sobre [referencias a campos](expression/field-references.md) en expresiones.

      ![](assets/message-to-subscribers-uc-2.png)

   1. En el **[!UICONTROL Añadir una expresión]** , haga clic en **[!UICONTROL Ok]**.

>[!CAUTION]
>
>La anulación de direcciones de correo electrónico solo debe utilizarse para casos de uso específicos. La mayoría de las veces, no es necesario cambiar la dirección de correo electrónico porque el valor definido como la dirección principal en los **[!UICONTROL Campos de ejecución]** es el que debe usarse. [Más información](../configuration/primary-email-addresses.md)
