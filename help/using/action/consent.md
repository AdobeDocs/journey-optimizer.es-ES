---
solution: Journey Optimizer
product: journey optimizer
title: Trabajar con políticas de consentimiento
description: Aprenda a trabajar con las directivas de consentimiento de Adobe Experience Platform
feature: Journeys, Actions, Custom Actions, Privacy, Consent Management
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: directivas, gobernanza, plataforma, escudo de atención sanitaria, consentimiento
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: 334527cbad3363b77d14dd447e06d4e8da79daec
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 100%

---

# Trabajar con políticas de consentimiento {#consent-management}

Sus datos pueden estar sujetos a restricciones de uso definidas por su organización o por la normativa legal. Por lo tanto, es importante asegurarse de que las operaciones de datos de Journey Optimizer cumplan con las [políticas de uso de datos](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=es){target="_blank"}. These policies are Adobe Experience Platform rules defining which [marketing actions](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=es#marketing-actions){target="_blank"} y que tiene permiso para realizar tareas en los datos.

Un tipo de políticas de uso de datos disponibles es **políticas de consentimiento**. Le permiten adoptar y aplicar fácilmente políticas de marketing que respeten las preferencias de consentimiento de sus clientes. [Más información sobre la aplicación de políticas](https://experienceleague.adobe.com/docs/experience-platform/data-governance/enforcement/auto-enforcement.html?lang=es){target="_blank"}

>[!IMPORTANT]
>
>Actualmente, las políticas de consentimiento solo están disponibles para las organizaciones que han adquirido las ofertas sobre el programa de **Protección sanitaria** y el programa de **Protección de la seguridad y la privacidad**.

Por ejemplo, puede [crear políticas de consentimiento](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=es#consent-policy){target="_blank"} en Experience Platform para excluir a los clientes que no hayan aceptado recibir comunicaciones por correo electrónico, push o SMS.

<!--* For the native outbound channels (Email, Push, SMS, Direct mail), the logic is as follows:

    * By default, if a profile has opted out from receiving communications from you, the corresponding profile is excluded from subsequent deliveries.

    * If you have the Adobe **Healthcare Shield** or **Privacy and Security Shield**, you can create a custom consent policy that overrides the default logic. For example, you can define a policy to only send email messages to all individuals who have opted in. In the absence of a custom policy, the default policy applies.
    
    To apply a custom policy, you need to define a marketing action in that policy and associate it to a channel surface. [Learn more](#marketing-actions)-->

En el nivel de recorrido, puede aplicar estas políticas de consentimiento a sus acciones personalizadas. 

* Al **configurar una acción personalizada**, puede definir un canal y una acción de marketing. [Más información](#consent-custom-action)
* Al añadir la **acción personalizada en un recorrido**, puede definir una acción de marketing adicional. [Más información](#consent-journey)

<!--

## Leverage consent policies through channel surfaces {#marketing-actions}

In [!DNL Journey Optimizer], consent is handled by the Experience Platform [Consent schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target="_blank"}.

To modify the consent field value, you can create a custom consent policy in which you define a marketing action and the conditions under which that action is performed. [Learn more on marketing actions](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html#marketing-actions){target="_blank"}

For example, if you want to create a consent policy to target only profiles who have consented to receive email communications, follow the steps below.

1. Make sure your organization has purchased the Adobe **Healthcare Shield** or **Privacy and Security Shield** add-on offerings. [Learn more](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html){target="_blank"}

1. In Adobe Experience Platform, create a custom policy (from the **[!UICONTROL Privacy]** > **[!UICONTROL Policies]** menu). [Learn how](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#create-policy){target="_blank"}

    ![](assets/consent-policy-create.png)

1. Choose the **[!UICONTROL Consent policy]** type and configure a condition as follows. [Learn how to configure consent policies](https://experienceleague-review.corp.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#consent-policy){target="_blank"}

    1. Under the **[!UICONTROL If]** section, select the **[!UICONTROL Email Targeting]** default marketing action.

        ![](assets/consent-policy-marketing-action.png)

        >[!NOTE]
        >
        >The core marketing actions provided out-of-the-box by Adobe are listed in [this table](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=en#core-actions){target="_blank"}. The steps to create a custom marketing action are listed in [this section](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#create-marketing-action){target="_blank"}.

    1. Select what happens when the marketing action applies. In this example, select **[!UICONTROL Email Marketing Consent]**.

    ![](assets/consent-policy-then.png)

1. Save and [enable](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#enable){target="_blank"} this policy.

1. In Journey Optimizer, create an email surface. [Learn how](../configuration/channel-surfaces.md#create-channel-surface)

1. In the email surface details, select the **[!UICONTROL Email Targeting]** marketing action.

    ![](assets/surface-marketing-action.png)

All consent policies associated with that marketing action are automatically leveraged in order to respect the preferences of your customers.

Therefore, in this example, any [email](../email/create-email.md) using that surface in a campaign or a journey is only sent to the profiles who have consented to receive emails from you. Profiles who have not consented to receive email communications are excluded.-->

## Aprovechamiento de las políticas de consentimiento mediante acciones personalizadas {#journey-custom-actions}

### Notas importantes {#important-notes}

En Journey Optimizer, el consentimiento se puede<!--also -->aprovechar en las acciones personalizadas. Si desea utilizarlo con las funciones de mensajes integrados, debe utilizar una actividad de condición para filtrar a los clientes en su recorrido.

Con la administración de consentimiento, se analizan dos actividades de recorrido:

* Leer público: se tiene en cuenta el público recuperado.
* Acción personalizada: la administración de consentimiento tiene en cuenta los atributos utilizados ([parámetros de acción](../action/about-custom-action-configuration.md#define-the-message-parameters)) así como la acción o acciones de marketing definidas (acciones de marketing requerida y adicional).
* No se admiten los atributos que forman parte de un grupo de campos que utilizan el esquema de unión predeterminado. Estos atributos se ocultarán en la interfaz. Debe crear otro grupo de campos con un esquema diferente.
* Las directivas de consentimiento solo se aplican cuando una acción de marketing (obligatoria o adicional) se establece en el nivel de acción personalizada.

No se tienen en cuenta todas las demás actividades utilizadas en un recorrido. Si inicia el recorrido con Calificación de público, no se tiene en cuenta el público.

En un recorrido, si un perfil queda excluido por una directiva de consentimiento en una acción personalizada, no se le envía el mensaje, pero continúa con el recorrido. El perfil no va a la ruta de tiempo de espera y error cuando se utiliza una condición.

Antes de actualizar las directivas de una acción personalizada ubicada en un recorrido, asegúrese de que el recorrido no tenga errores.

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

### Configuración de la acción personalizada {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action"
>title="Definir una acción de marketing requerida"
>abstract="La Acción de marketing requerida permite definir la acción de marketing relacionada con la acción personalizada. Por ejemplo, si utiliza esa acción personalizada para enviar correos electrónicos, puede seleccionar Segmentación por correo electrónico. Cuando se utilizan en un recorrido, todas las directivas de consentimiento asociadas a esa acción de marketing se recuperan y se aprovechan. Esto no se puede modificar en el lienzo."

Al configurar una acción personalizada, se pueden utilizar dos campos para la administración de consentimiento.

El campo **Canal** permite seleccionar el canal relacionado con esta acción personalizada: **Correo electrónico**, **SMS** o **Notificaciones push**. Rellena automáticamente el campo **Acción de marketing necesaria** con la acción de marketing predeterminada para el canal seleccionado. Si selecciona **otros**, no se define ninguna acción de marketing de forma predeterminada.

![](assets/consent1.png)

La **Acción de marketing necesaria** permite definir la acción de marketing relacionada con la acción personalizada. Por ejemplo, si utiliza esa acción personalizada para enviar correos electrónicos, puede seleccionar **Segmentación por correo electrónico**. Cuando se utilizan en un recorrido, todas las directivas de consentimiento asociadas a esa acción de marketing se recuperan y se aprovechan. Se selecciona una acción de marketing predeterminada, pero puede hacer clic en la flecha abajo para seleccionar cualquier acción de marketing disponible en la lista.

![](assets/consent2.png)

En determinados tipos de comunicaciones importantes, por ejemplo, un mensaje transaccional enviado para restablecer la contraseña del cliente, es posible que no desee aplicar una directiva de consentimiento. A continuación, seleccione **Ninguno** en el campo **Acción de marketing requerida**.

Los demás pasos para configurar una acción personalizada se detallan en [esta sección](../action/about-custom-action-configuration.md#consent-management).

### Construcción del recorrido {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_canvas"
>title="Acción de marketing requerida"
>abstract="Se define una acción de marketing requerida al crear una acción personalizada. Esta acción de marketing requerida no se puede eliminar de la acción ni modificar."

>[!CONTEXTUALHELP]
>id="ajo_consent_additional_marketing_action_canvas"
>title="Acción de marketing adicional"
>abstract="Agregue otra acción de marketing además de la requerida. Se aplicarán las directivas de consentimiento relacionadas con ambas acciones de marketing."

>[!CONTEXTUALHELP]
>id="ajo_consent_refresh_policies_canvas"
>title="Visualizar las directivas de consentimiento que se aplicarán durante la ejecución"
>abstract="Las acciones de marketing incorporan directivas de consentimiento que combinan parámetros de acción y valores de consentimiento de perfil individuales para filtrar a los usuarios. Obtenga la definición más reciente de estas directivas haciendo clic en el botón para actualizar."

Al agregar la acción personalizada en un recorrido, varias opciones permiten administrar el consentimiento. Haga clic en **Mostrar campos de solo lectura** para mostrar todos los parámetros.

La variable **Canal** y **Acción de marketing necesaria**, definida al configurar la acción personalizada, se muestra en la parte superior de la pantalla. Estos campos no se pueden modificar.

![](assets/consent4.png)

Puede definir una **Acción de marketing adicional** para establecer el tipo de acción personalizada. Esto le permite definir el propósito de la acción personalizada en este recorrido. Además de la acción de marketing necesaria, que suele ser específica de un canal, puede definir una acción de marketing adicional que es específica de la acción personalizada en este recorrido en particular. Por ejemplo: una comunicación de entrenamiento, una Newsletter, una comunicación de fitness, etc. Se aplican la acción de marketing necesaria y la acción de marketing adicional.

![](assets/consent3.png)

Haga clic en **Actualizar directivas**, en la parte inferior de la pantalla, para actualizar y comprobar la lista de directivas que se tienen en cuenta en esta acción personalizada. Esto es solo para fines informativos mientras se crea un recorrido. Con los recorridos activos, las directivas de consentimiento se recuperan y se actualizan automáticamente cada seis horas.

![](assets/consent5.png)

<!--
The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* action parameters defined in the custom action, see this [section](../action/about-custom-action-configuration.md#define-the-message-parameters) 
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-audience.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

Los demás pasos para configurar una acción personalizada en un recorrido se detallan en [esta sección](../building-journeys/using-custom-actions.md).
