---
solution: Journey Optimizer
product: journey optimizer
title: Envío de un mensaje a los suscriptores
description: Obtenga información sobre cómo crear un recorrido para enviar un mensaje a los suscriptores de una lista
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: recorrido, caso de uso, mensaje, suscriptores, lista, lectura
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 17%

---

# Envío de un mensaje a los suscriptores de una lista {#send-a-message-to-the-subscribers-of-a-list}

El propósito de este caso de uso es crear un recorrido para enviar un mensaje a los suscriptores de una lista.

En este ejemplo, se usa el grupo de campos **[!UICONTROL Detalles de consentimiento y preferencia]** de [!DNL Adobe Experience Platform]. Para encontrar este grupo de campos, en el menú **[!UICONTROL Administración de datos]**, elija **[!UICONTROL Esquemas]**. En la ficha **[!UICONTROL Grupos de campos]**, escriba el nombre del grupo de campos en el campo de búsqueda.

![Este grupo de campos incluye el elemento subscriptions](assets/consent-and-preference-details-field-group.png)

Para configurar este recorrido, siga estos pasos:

1. Cree un recorrido que comience con una actividad **[!UICONTROL Read]**. [Más información](journey-gs.md).
1. Agregue una actividad de acción **[!UICONTROL Correo electrónico]** al recorrido. [Más información](journeys-message.md).
1. En la sección **[!UICONTROL Parámetros de correo electrónico]** de la configuración de la actividad **[!UICONTROL Correo electrónico]**, reemplace la dirección de correo electrónico predeterminada (`PersonalEmail.adress`) por la dirección de correo electrónico de los suscriptores de la lista:

   1. Haga clic en el icono **[!UICONTROL Habilitar anulación de parámetros]** a la derecha del campo **[!UICONTROL Dirección]** y, a continuación, haga clic en el icono **[!UICONTROL Editar]**.

      ![Flujo de Recorrido con audiencia de lectura para la segmentación de listas de suscriptores](assets/message-to-subscribers-uc-1.png)

   1. En el editor de expresiones, introduzca la expresión para recuperar las direcciones de correo electrónico de los suscriptores. [Más información](expression/expressionadvanced.md).

      Este ejemplo muestra una expresión que incluye referencias a campos de asignación:

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      En este ejemplo, se utilizan estas funciones:

      | Función | Descripción | Ejemplo |
      | --- | --- | --- |
      | `entry` | Hace referencia a un elemento de mapa según el área de nombres seleccionada | Consulte una lista de suscripción específica |
      | `firstEntryKey` | Recupera la primera clave de entrada de un mapa | Recuperación de la primera dirección de correo electrónico de los suscriptores |

      En este ejemplo, la lista de suscripción se denomina `daily-email`. Las direcciones de correo electrónico se definen como claves en el mapa `subscribers`, que está vinculado al mapa de la lista de suscripción.

      Más información sobre [referencias a campos](expression/field-references.md) en expresiones.

      ![Configuración de correo electrónico con contenido personalizado para suscriptores](assets/message-to-subscribers-uc-2.png)

   1. En el cuadro de diálogo **[!UICONTROL Agregar una expresión]**, haga clic en **[!UICONTROL Aceptar]**.

>[!CAUTION]
>
>La anulación de direcciones de correo electrónico solo debe utilizarse para casos de uso específicos. La mayoría de las veces, no es necesario cambiar la dirección de correo electrónico porque el valor definido como la dirección principal en los **[!UICONTROL Campos de ejecución]** es el que debe usarse. [Más información](../configuration/primary-email-addresses.md)
