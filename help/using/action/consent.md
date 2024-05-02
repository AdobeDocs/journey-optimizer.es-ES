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
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 72%

---

# Trabajar con políticas de consentimiento {#consent-management}

Sus datos pueden estar sujetos a restricciones de uso definidas por su organización o por la normativa legal. Por lo tanto, es importante asegurarse de que las operaciones de datos de Journey Optimizer cumplan con las [políticas de uso de datos](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=es){target="_blank"}. These policies are Adobe Experience Platform rules defining which [marketing actions](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=es#marketing-actions){target="_blank"} y que tiene permiso para realizar tareas en los datos.

Un tipo de políticas de uso de datos disponibles es **políticas de consentimiento**. Le permiten adoptar y aplicar fácilmente políticas de marketing que respeten las preferencias de consentimiento de sus clientes. [Más información sobre la aplicación de políticas](https://experienceleague.adobe.com/docs/experience-platform/data-governance/enforcement/auto-enforcement.html?lang=es){target="_blank"}

>[!IMPORTANT]
>
>Actualmente, las políticas de consentimiento solo están disponibles para las organizaciones que han adquirido las ofertas sobre el programa de **Protección sanitaria** y el programa de **Protección de la seguridad y la privacidad**.

Por ejemplo, puede [crear políticas de consentimiento](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=es#consent-policy){target="_blank"} en Experience Platform para excluir a los clientes que no hayan aceptado recibir comunicaciones por correo electrónico, push o SMS.

* Para los canales salientes nativos (correo electrónico, push, SMS, correo postal), la lógica es la siguiente:

   * De forma predeterminada, si un perfil se ha excluido de la recepción de comunicaciones por su parte, el perfil correspondiente se excluye de las entregas posteriores.

   * Si tiene el Adobe **Healthcare Shield** o **Escudo de seguridad y privacidad**, puede crear una directiva de consentimiento personalizada que anule la lógica predeterminada. Por ejemplo, puede definir una directiva para enviar mensajes de correo electrónico únicamente a todas las personas que se hayan suscrito. En ausencia de una directiva personalizada, se aplica la directiva predeterminada.

  Para aplicar una directiva personalizada, debe definir una acción de marketing en esa directiva y asociarla a una superficie de canal. [Más información](#surface-marketing-actions)

En el nivel de recorrido, puede aplicar estas políticas de consentimiento a sus acciones personalizadas. 

* Al **configurar una acción personalizada**, puede definir un canal y una acción de marketing. [Más información](#consent-custom-action)
* Al añadir la **acción personalizada en un recorrido**, puede definir una acción de marketing adicional. [Más información](#consent-journey)

## Aprovechamiento de las políticas de consentimiento mediante superficies de canal {#surface-marketing-actions}

En [!DNL Journey Optimizer], Experience Platform gestiona el consentimiento [Esquema de consentimiento](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=es){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=es#choice-values){target="_blank"}.

Para modificar el valor del campo de consentimiento, puede crear una directiva de consentimiento personalizada en la que defina una acción de marketing y las condiciones en las que se realiza dicha acción. [Más información sobre las acciones de marketing](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=es#marketing-actions){target="_blank"}

Por ejemplo, si desea crear una política de consentimiento para dirigirse solo a perfiles que hayan aceptado recibir comunicaciones por correo electrónico, siga los pasos a continuación.

1. Asegúrese de que su organización ha adquirido el Adobe **Healthcare Shield** o **Escudo de seguridad y privacidad** ofertas de complementos. [Más información](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html?lang=es){target="_blank"}

1. En Adobe Experience Platform, cree una directiva personalizada (desde el **[!UICONTROL Privacidad]** > **[!UICONTROL Políticas]** menú). [Descubra cómo](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#create-policy){target="_blank"}

   <!--![](assets/consent-policy-create.png)-->

1. Elija la **[!UICONTROL Política de consentimiento]** escriba y configure una condición como se indica a continuación. [Obtenga información sobre cómo configurar directivas de consentimiento](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=es#consent-policy){target="_blank"}

   1. En el **[!UICONTROL If]** , seleccione la **[!UICONTROL Segmentación de correo electrónico]** acción de marketing predeterminada.

      <!--![](assets/consent-policy-marketing-action.png)-->

      >[!NOTE]
      >
      >Las acciones de marketing principales proporcionadas previamente por Adobe se enumeran en [esta tabla](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=en#core-actions){target="_blank"}. The steps to create a custom marketing action are listed in [this section](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#create-marketing-action){target="_blank"}.

   1. Seleccione lo que sucede cuando se aplica la acción de marketing. En este ejemplo, seleccione **[!UICONTROL Consentimiento de marketing por correo electrónico]**.

   ![](assets/consent-policy-then.png)

1. Guardar y [habilitar](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#enable){target="_blank"} esta política.

1. En Journey Optimizer, cree una superficie de correo electrónico. [Descubra cómo](../configuration/channel-surfaces.md#create-channel-surface)

1. En los detalles de la superficie de correo electrónico, seleccione la **[!UICONTROL Segmentación de correo electrónico]** acción de marketing.

   ![](assets/surface-marketing-action.png)

Todas las políticas de consentimiento asociadas con esa acción de marketing se aprovechan automáticamente para respetar las preferencias de los clientes.

Por lo tanto, en este ejemplo, cualquier [email](../email/create-email.md) el uso de esa superficie en una campaña o un recorrido solo se envía a los perfiles que han aceptado recibir correos electrónicos suyos. Se excluyen los perfiles que no hayan aceptado recibir comunicaciones por correo electrónico.

## Aprovechamiento de las políticas de consentimiento mediante acciones personalizadas {#journey-custom-actions}

### Notas importantes {#important-notes}

En Journey Optimizer, el consentimiento también se puede aprovechar en acciones personalizadas. Si desea utilizarlo con las funciones de mensajes integrados, debe utilizar una actividad de condición para filtrar a los clientes en su recorrido.

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
