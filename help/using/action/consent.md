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
source-git-commit: d549e4fdb7cd71e450cd00e4fa8707ae03ce0aff
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 82%

---

# Trabajar con políticas de consentimiento {#consent-management}

<!--Adobe Experience Platform allows you to easily adopt and enforce marketing policies to respect the consent preferences of your customers. Consent policies are defined in Adobe Experience Platform. Refer to [this documentation](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#consent-policy).

In Journey Optimizer, you can apply these consent policies to your custom actions. For example, you can define consent policies to exclude customers who have not consented to receive email, push or SMS communication.-->

Sus datos pueden estar sujetos a restricciones de uso definidas por su organización o por regulaciones legales. Por lo tanto, es importante asegurarse de que las operaciones de datos de Journey Optimizer cumplan con lo siguiente [políticas de uso de datos](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=es){target="_blank"}. These policies are Adobe Experience Platform rules defining which [marketing actions](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html#marketing-actions){target="_blank"} tiene permiso para realizar tareas en los datos.

Un tipo de políticas de uso de datos disponibles es **directivas de consentimiento**. Permiten adoptar y aplicar fácilmente políticas de marketing que respeten las preferencias de consentimiento de los clientes. [Más información sobre la aplicación de políticas](https://experienceleague.adobe.com/docs/experience-platform/data-governance/enforcement/auto-enforcement.html){target="_blank"}

>[!IMPORTANT]
>
>Actualmente, las políticas de consentimiento solo están disponibles para las organizaciones que han adquirido el Adobe **Healthcare Shield** o **Escudo de seguridad y privacidad** ofertas de complementos.

Por ejemplo, puede [crear directivas de consentimiento](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=es#consent-policy){target="_blank"} en Experience Platform para excluir a los clientes que no hayan aceptado recibir comunicaciones por correo electrónico, push o SMS.

En Journey Optimizer, el consentimiento se define en varios niveles. Puede aplicar directivas de consentimiento a las acciones personalizadas de recorrido:

* Cuándo **configuración de una acción personalizada**, puede definir un canal y una acción de marketing. [Más información](#consent-custom-action)
* Al añadir la variable **acción personalizada en un recorrido**, puede definir una acción de marketing adicional. [Más información](#consent-journey)

## Notas importantes {#important-notes}

En Journey Optimizer, el consentimiento se puede utilizar en las acciones personalizadas. Si desea utilizarlo con las funciones de mensajes integrados, debe utilizar una actividad de condición para filtrar a los clientes en su recorrido.

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

## Configuración de la acción personalizada {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action"
>title="Definir una acción de marketing requerida"
>abstract="La Acción de marketing requerida permite definir la acción de marketing relacionada con la acción personalizada. Por ejemplo, si utiliza esa acción personalizada para enviar correos electrónicos, puede seleccionar Segmentación por correo electrónico. Cuando se utilizan en un recorrido, todas las directivas de consentimiento asociadas a esa acción de marketing se recuperan y se aprovechan. Esto no se puede modificar en el lienzo."

Al configurar una acción personalizada, se pueden utilizar dos campos para la administración de consentimiento.

El campo **Canal** permite seleccionar el canal relacionado con esta acción personalizada: **Correo electrónico**, **SMS** o **Notificaciones automáticas**. Rellenará automáticamente el campo **Acción de marketing necesaria** con la acción de marketing predeterminada para el canal seleccionado. Si selecciona **otros**, no se definirá ninguna acción de marketing de forma predeterminada.

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

Puede definir una **Acción de marketing adicional** para establecer el tipo de acción personalizada. Esto le permite definir el propósito de la acción personalizada en este recorrido. Además de la acción de marketing necesaria, que suele ser específica de un canal, puede definir una acción de marketing adicional que será específica de la acción personalizada en este recorrido en particular. Por ejemplo: una comunicación de entrenamiento, una newsletter, una comunicación de fitness, etc. Se aplicarán la acción de marketing necesaria y la acción de marketing adicional.

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
