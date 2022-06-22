---
solution: Journey Optimizer
title: Consentimiento
description: Consentimiento
feature: Actions
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: 8a68d1e6d498ef3055c703d4e73471ab6d7bff40
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Gestión del consentimiento (beta) {#consent-management}

Adobe Experience Platform le permite adoptar y aplicar fácilmente políticas de marketing que respeten las preferencias de consentimiento de sus clientes. Las políticas de consentimiento se definen en Adobe Experience Platform. Consulte [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=en#consent-policy).

En Journey Optimizer, puede aplicar estas directivas de consentimiento a sus acciones personalizadas. Por ejemplo, puede definir políticas de consentimiento para excluir a los clientes que no hayan aceptado recibir comunicaciones por correo electrónico, push o SMS.

>[!NOTE]
>
>Esta función se presenta como una versión beta privada. No está disponible para todos los clientes de Journey Optimizer.

En Journey Optimizer, el consentimiento se define en varios niveles:

* when **configuración de una acción personalizada**, puede definir un canal y una acción de marketing. Consulte esta [sección](../action/consent.md#consent-custom-action).
* al agregar la variable **acción personalizada en un recorrido**, puede definir una acción de marketing adicional. Consulte esta [sección](../action/consent.md#consent-journey).

## Notas importantes {#important-notes}

En Journey Optimizer, el consentimiento se puede aprovechar en las acciones personalizadas. Si desea utilizarla con las funcionalidades de los mensajes integrados, debe utilizar una actividad de condición para filtrar clientes en su recorrido.

Con la administración de consentimiento, se analizan dos actividades de recorrido:

* Leer segmento: se tiene en cuenta el segmento recuperado.
* Acción personalizada: la administración de consentimiento tiene en cuenta los atributos utilizados ([parámetros de acción](../action/about-custom-action-configuration.md#define-the-message-parameters)) así como las acciones de marketing definidas (acción de marketing necesaria y acción de marketing adicional).

El consentimiento solo se aplica cuando se establece una acción de marketing (obligatoria o adicional) en el nivel de acción personalizada.

No se tienen en cuenta todas las demás actividades utilizadas en un recorrido. Si inicia el recorrido con una calificación de segmento, no se tiene en cuenta el segmento.

En un recorrido, si un perfil se excluye mediante una política de consentimiento en una acción personalizada, el mensaje no se le envía, pero continúa con el recorrido. El perfil no va a la ruta de tiempo de espera y error al utilizar una condición.

Antes de actualizar las directivas en una acción personalizada ubicada en un recorrido, asegúrese de que el recorrido no tenga errores.

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

## Configuración de la acción personalizada {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_admin"
>title="Definir una acción de marketing necesaria"
>abstract="La acción de marketing requerida le permite definir la acción de marketing relacionada con su acción personalizada. Por ejemplo, si utiliza esa acción personalizada para enviar correos electrónicos, puede seleccionar la segmentación por correo electrónico. Cuando se utiliza en un recorrido, todas las políticas de consentimiento asociadas con esa acción de marketing se recuperan y se aprovechan. Esto no se puede modificar en el lienzo."

Al configurar una acción personalizada, se pueden utilizar dos campos para la gestión del consentimiento.

La variable **Canal** permite seleccionar el canal relacionado con esta acción personalizada: **Correo electrónico**, **SMS** o **Notificaciones push**. Rellenará previamente el **Acción de marketing necesaria** con la acción de marketing predeterminada para el canal seleccionado. Si selecciona **other**, no se definirá ninguna acción de marketing de forma predeterminada.

![](assets/consent1.png)

La variable **Acción de marketing necesaria** permite definir la acción de marketing relacionada con la acción personalizada. Por ejemplo, si utiliza esa acción personalizada para enviar correos electrónicos, puede seleccionar **Segmentación por correo electrónico**. Cuando se utiliza en un recorrido, todas las políticas de consentimiento asociadas con esa acción de marketing se recuperan y se aprovechan. Se selecciona una acción de marketing predeterminada, pero puede hacer clic en la flecha hacia abajo para seleccionar cualquier acción de marketing disponible en la lista.

![](assets/consent2.png)

Para ciertos tipos de comunicaciones importantes, por ejemplo un mensaje transaccional enviado para restablecer la contraseña del cliente, es posible que no desee aplicar una directiva de consentimiento. A continuación, seleccione **Ninguna** en el **Acción de marketing necesaria** campo .

Los demás pasos para configurar una acción personalizada se detallan en [esta sección](../action/about-custom-action-configuration.md#consent-management).

### Construcción del recorrido {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_canvas"
>title="Acción de marketing necesaria"
>abstract="Se define una acción de marketing necesaria al crear una acción personalizada. Esta acción de marketing necesaria no se puede eliminar de la acción ni modificar."

>[!CONTEXTUALHELP]
>id="ajo_consent_additional_marketing_action_canvas"
>title="Acción de marketing adicional"
>abstract="Agregue otra acción de marketing además de la requerida. Se aplicarán las políticas de consentimiento relacionadas con ambas acciones de marketing."

>[!CONTEXTUALHELP]
>id="ajo_consent_refresh_policies_canvas"
>title="Visualizar las políticas de consentimiento que se aplicarán durante la ejecución"
>abstract="Las acciones de marketing incorporan políticas de consentimiento que combinan parámetros de acción y valores de consentimiento de perfil individuales para filtrar a los usuarios. Obtenga la definición más reciente de estas directivas haciendo clic en el botón para actualizar."

Al añadir la acción personalizada en un recorrido, varias opciones permiten administrar el consentimiento. Haga clic en el **Mostrar campos de solo lectura** para mostrar todos los parámetros.

La variable **Canal** y **Acción de marketing necesaria**, definidos al configurar la acción personalizada, se muestran en la parte superior de la pantalla. Estos campos no se pueden modificar.

![](assets/consent4.png)

Puede definir una **Acción de marketing adicional** para establecer el tipo de acción personalizada. Esto le permite definir el propósito de la acción personalizada en este recorrido. Además de la acción de marketing necesaria, que suele ser específica de un canal, puede definir una acción de marketing adicional que será específica de la acción personalizada en este recorrido en particular. Por ejemplo: una comunicación de entrenamiento, un boletín, una comunicación de fitness, etc. Se aplicarán la acción de marketing necesaria y la acción de marketing adicional.

![](assets/consent3.png)

Haga clic en el **Actualizar directivas** , en la parte inferior de la pantalla, para actualizar y comprobar la lista de directivas que se tienen en cuenta para esta acción personalizada. Esto es solo para fines informativos, mientras se crea un recorrido. Con los recorridos activos, las políticas de consentimiento se recuperan y actualizan automáticamente cada 6 horas.

![](assets/consent5.png)

<!--
The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* action parameters defined in the custom action, see this [section](../action/about-custom-action-configuration.md#define-the-message-parameters) 
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-segment.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

Los demás pasos para configurar una acción personalizada en un recorrido se detallan en [esta sección](../building-journeys/using-custom-actions.md).
