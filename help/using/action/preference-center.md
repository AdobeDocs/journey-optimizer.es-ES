---
solution: Journey Optimizer
product: journey optimizer
title: Administre las preferencias de sus clientes
description: Obtenga información sobre cómo administrar las preferencias de los usuarios mediante el uso de directivas de consentimiento
feature: Journeys, Privacy, Consent Management, Landing Pages
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: políticas, gobernanza, plataforma, consentimiento, escudo sanitario
hide: true
hidefromtoc: true
source-git-commit: 0aa29a163e337359ea4455edee57bc49fd06a020
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 4%

---

# Administre las preferencias de sus clientes {#preference-center}

>[!AVAILABILITY]
>
>Actualmente, esta funcionalidad solo está disponible para las organizaciones que han adquirido las ofertas adicionales de Adobe **Healthcare Shield** o **Privacy and Security Shield**.

En un ecosistema moderno de automatización de marketing, las marcas interactúan con los clientes en varios puntos de contacto, lo que provoca el riesgo de una comunicación irrelevante o excesiva, lo que provoca la desvinculación, quejas de spam y riesgos de cumplimiento normativo. Por este motivo, necesitan administrar las preferencias de sus clientes para obtener perspectivas en tiempo real sobre su audiencia y ofrecer una comunicación personalizada y respetuosa.

Con [!DNL Adobe Journey Optimizer], mediante el uso de [directivas de consentimiento](consent.md), puede respetar las preferencias de sus clientes<!-- in terms of **channels** and **topics**-->. Esto garantiza que [!DNL Journey Optimizer] solo se oriente a los clientes en función de sus opciones<!-- their preferred channels and on the subscription topics-->, respetando al mismo tiempo su consentimiento.

Para administrar las preferencias de los usuarios con [!DNL Journey Optimizer], puede:

* Recupere el consentimiento de los clientes para optar por su inclusión o exclusión de cualquier canal saliente nativo. Por ejemplo, cree una directiva de consentimiento en [!DNL Experience Platform] para excluir a los clientes que no hayan aceptado recibir comunicaciones para un canal determinado. Luego aplique esta directiva de consentimiento en [!DNL Journey Optimizer] mediante una configuración de canal de correo electrónico. [Descubra cómo](consent.md#surface-marketing-actions)

  >[!NOTE]
  >
  >Los canales admitidos son Correo electrónico, Push, SMS e InApp.<!--To check-->

* Pregunte a sus clientes a qué temas desean suscribirse (como el tipo de comunicaciones que aceptan recibir o no). [Descubra cómo](#manage-preferences)

>[!IMPORTANT]
>
>El consentimiento tiene prioridad sobre las preferencias. Por ejemplo, uno de sus clientes indicó que su canal preferido es el correo electrónico y que aceptaron recibir boletines <!-- they are interested in yoga-->; sin embargo, si optaron por no recibir comunicaciones suyas, no podrán recibir ningún boletín por correo electrónico que usted esté enviando<!-- on yoga-->.

## Registrar y respetar preferencias {#manage-preferences}

Con las directivas de consentimiento de [!DNL Journey Optimizer], puede administrar las preferencias de sus clientes de forma centralizada. Esto le permite asegurarse de que solo se dirige a los clientes en función de los temas que han seleccionado, respetando al mismo tiempo sus opciones de consentimiento. Para realizar esto, siga los pasos a continuación.

Supongamos que desea dirigirse a sus clientes mediante recorridos y campañas en función de sus preferencias de comunicación en varios temas de suscripción (*Boletines*, *Ofertas* y *Nuevos lanzamientos de productos*).

1. Defina los atributos de preferencia con el operador booleano en el nivel de perfil <!--how??-->. Por ejemplo, puede especificar:

   * Newsletter_Email: Booleano (Verdadero/Falso)
   * Ofertas: booleano (verdadero/falso)
   * Nuevos lanzamientos de productos: booleano (verdadero/falso)

   Estos atributos se capturan en el esquema de un [conjunto de datos](../data/get-started-datasets.md) habilitado para el perfil y se asignan al [perfil unificado del cliente](../audience/get-started-profiles.md).

   >[!NOTE]
   >
   >El consentimiento del cliente y las preferencias de contacto son temas complejos. Para conocer cómo se pueden recopilar, procesar y filtrar las preferencias de consentimiento y contexto en [!DNL Experience Platform], se recomienda leer los siguientes documentos:
   >
   >* Para obtener más información sobre los grupos de campos de esquema necesarios para recopilar datos de consentimiento, consulte [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/consent/adobe/overview){target="_blank"}. Detalla cómo procesar los datos de consentimiento que ha recopilado de sus clientes e integrarlos en sus perfiles de cliente almacenados.
   >* Para obtener más información sobre el grupo de campos Consentimiento y preferencia, consulte [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/consents#ingest){target="_blank"}.
   >* Para agregar campos de preferencias personalizadas al esquema, siga los pasos de [esta sección](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/consent/adobe/dataset#custom-consent){target="_blank"}.

1. Cree una página para capturar las preferencias de los clientes. Utilice uno de los siguientes métodos:

   * Cree una página web para registrar las preferencias de sus clientes con [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/home){target="_blank"}.

   * Use una [!DNL Journey Optimizer] [página de aterrizaje](../landing-pages/create-lp.md) que incluya formularios para capturar las preferencias de sus clientes mediante datos de perfil.  [Más información en formularios](../landing-pages/lp-forms.md) <!--Forms not released/announced yet - TBC-->

     >[!NOTE]
     >
     >Asegúrese de que el dominio de la página de aterrizaje que está utilizando pertenece a la marca de nivel superior y no a una submarca. Esto sirve para garantizar la confianza entre los usuarios finales. <!--Please clarify-->

1. En esta página, los clientes pueden actualizar sus preferencias, como las suscripciones por temas, seleccionando o desmarcando casillas de verificación.

   Cada acción almacena en déclencheur un evento de consentimiento que se guarda con los atributos de perfil correspondientes (`True` para la inclusión, `False` para la exclusión) mediante la ingesta de los datos en el esquema del conjunto de datos habilitado para el perfil <!-- that contains the corresponding preference fields-->.

   <!--Record your users' preferences through the web page or landing page that you created. The data is saved against the corresponding profile, meaning that the preference data is ingested into a Profile-enabled dataset whose schema contains consent/preference fields.-->

   Por ejemplo, un usuario cuya dirección de correo electrónico es john.black@lumamail.com acepta recibir ofertas pero no quiere recibir boletines.

   El conjunto de datos de perfil correspondiente se actualiza de la siguiente manera:

   | Atributo = ID de correo electrónico | Atributo = Ofertas | Atributo = Newsletters |
   |---------|----------|---------|
   | john.black@lumamail.com | Y | N |

   >[!NOTE]
   >
   >Los eventos de consentimiento entrantes se alimentan del perfil del cliente, lo que garantiza actualizaciones en tiempo real. Cada perfil refleja sus opciones más recientes en las preferencias de suscripción.

1. En Adobe Experience Platform, cree una política personalizada (en el menú **[!UICONTROL Privacidad]** > **[!UICONTROL Políticas]**). [Descubra cómo](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=es#create-policy){target="_blank"}

   >[!AVAILABILITY]
   >
   >Actualmente, las políticas de consentimiento solo están disponibles para las organizaciones que han adquirido las ofertas adicionales de Adobe **Healthcare Shield** o **Privacy and Security Shield**. [Más información sobre las directivas de consentimiento](consent.md)

   Para utilizar directivas de consentimiento, los atributos de preferencia deben estar presentes en los datos del perfil. Por este motivo, debe definir estos atributos en el nivel de perfil (como se describe en el paso 1).

1. Elija el tipo de **[!UICONTROL Política de consentimiento]** y configure una condición como se indica a continuación. [Obtenga información sobre cómo configurar directivas de consentimiento](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=es#consent-policy){target="_blank"}

<!--Consent policies are comprised of two logical components:

* **If**: The condition that will trigger the policy check, based on a certain marketing action (email, SMS, push, custom action, etc.) being performed, the presence of certain data usage labels, or a combination of the two.

* **Then**: The consent attribute must be present for a profile to be included in the action that triggered the policy. More than one field can also be selected.-->

    Por ejemplo, para enviar comunicaciones solo a los clientes que no hayan optado por no recibir boletines de correo electrónico, cree una directiva personalizada y defina la siguiente condición:
    
    * Si **[!UICONTROL Acción de marketing]** es igual a **[!UICONTROL Correo electrónico]**
    
    * Entonces **[!UICONTROL Correo electrónico del boletín]** no existe **[!UICONTROL falso]** O **[!UICONTROL Correo electrónico del boletín]** no es igual a **[!UICONTROL falso]**
    
    ![](assets/consent-policy-email-newsletter.png){width=100%}
    
    >[!TIP]
    >
    >El conjunto de datos habilitado para el perfil debe incluir el atributo de perfil **[!UICONTROL Newsletter_Email]** con el valor establecido en `true` (como se describe en el paso 1.)

1. Una vez creada la directiva de consentimiento, utilícela en [!DNL Journey Optimizer] con [configuraciones de canal](consent.md#surface-marketing-actions) o [acciones personalizadas de recorrido](consent.md#journey-custom-actions).

1. Ahora puede usar estas configuraciones de canal o acciones personalizadas en sus recorridos y campañas para asegurarse de que se cumplan las preferencias de sus clientes de <!--targeted-->.
