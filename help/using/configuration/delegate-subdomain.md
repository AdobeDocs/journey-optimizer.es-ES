---
solution: Journey Optimizer
product: journey optimizer
title: Delegar un subdominio
description: Obtenga información sobre cómo delegar los subdominios.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdominio, delegación, dominio, DNS
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: 142e56ce36389da5c2e28bbafa1a1bf59be50d74
workflow-type: tm+mt
source-wordcount: '1906'
ht-degree: 16%

---

# Delegar un subdominio {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="Delegación de subdominios"
>abstract="Journey Optimizer permite delegar los subdominios a Adobe. Puede delegar completamente un subdominio a Adobe, que es el método recomendado. </br>También puede crear un subdominio mediante CNAME para que apunte a registros específicos de Adobe, pero este método requiere que mantenga y administre registros DNS por su cuenta."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation#subdomain-delegation-methods" text="Métodos de configuración de subdominios"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="Delegación de subdominios"
>abstract="Para empezar a enviar correos electrónicos, delegará el subdominio a Adobe. Una vez delegado, se configurarán los registros DNS, las bandejas de entrada, el remitente y las direcciones de respuesta y devolución."

La delegación de nombres de dominio es un método que permite al propietario de un nombre de dominio (técnicamente: una zona DNS) delegar una subdivisión del mismo (técnicamente: una zona DNS debajo de ella, que se puede llamar subzona) a otra entidad. Básicamente, como cliente, si administra el área &quot;example.com&quot;, puede delegar la subzona &quot;marketing.example.com&quot; a Adobe.

>[!NOTE]
>
>Obtenga más información acerca de la delegación de subdominios y los diferentes métodos disponibles con [!DNL Journey Optimizer] en [esta sección](about-subdomain-delegation.md).

Puede:

* Delegar completamente un subdominio: [Más información](#set-up-subdomain)
* Crear un subdominio con CNAME para que apunte a registros específicos de Adobe: [Más información](#set-up-subdomain)

La **delegación de subdominios completa** es el método recomendado. Obtenga más información sobre las diferencias entre los distintos métodos de configuración de subdominios en [esta sección](about-subdomain-delegation.md#subdomain-delegation-methods).

## Mecanismos de protección {#guardrails}

Al configurar subdominios en [!DNL Journey Optimizer], siga las protecciones y recomendaciones que se describen a continuación.

* De manera predeterminada, [!DNL Journey Optimizer] le permite delegar **un máximo de 10 subdominios**. Sin embargo, según el contrato de licencia, puede delegar hasta 100 subdominios. Póngase en contacto con la persona de contacto de Adobe para obtener más información sobre el número de subdominios a los que tiene derecho.

* No se admite el envío paralelo de subdominios en [!DNL Journey Optimizer]. Si intenta enviar un subdominio para delegación cuando otro está en estado **[!UICONTROL Procesando]**, recibirá un mensaje de error.

* No se permite delegar un subdominio no válido a Adobe. Asegúrese de introducir un subdominio válido que sea propiedad de su organización, como marketing.yourcompany.com.

* No puede usar el mismo dominio de envío para enviar mensajes desde [!DNL Adobe Journey Optimizer] y desde otro producto, como [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage].

* No se admite la delegación de un dominio principal y un subdominio. Por ejemplo, si delegó subdomain.domain.com, no puede delegar email.subdomain.domain.com. Del mismo modo, si delegó email.subdomain.domain.com, no puede delegar subdomain.domain.com.

## Acceder a subdominios delegados {#access-delegated-subdomains}

Todos los subdominios delegados se muestran en el menú **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Subdominios]**. Los filtros están disponibles para ayudarle a refinar la lista (fecha de delegación, usuario o estado).

<!--![](assets/subdomain-list.png)-->

La columna **[!UICONTROL Estado]** proporciona información sobre el proceso de delegación de subdominios:

* **[!UICONTROL Borrador]**: la delegación de subdominios se ha guardado como borrador. Haga clic en el nombre del subdominio para reanudar el proceso de delegación.
* **[!UICONTROL Procesando]**: el subdominio está pasando por varias comprobaciones de configuración antes de poder usarse,
* **[!UICONTROL Éxito]**: el subdominio ha pasado correctamente por las comprobaciones y se puede utilizar para enviar mensajes,
* **[!UICONTROL Error]**: una o varias comprobaciones han fallado después de enviar la delegación de subdominios.

Para obtener información detallada sobre un subdominio con el estado **[!UICONTROL Correcto]**, ábralo en la lista.

![](assets/subdomain-delegated.png)

Puede hacer lo siguiente:

* Recupere el nombre de subdominio (solo lectura) configurado durante el proceso de delegación, así como las direcciones URL generadas (recursos, páginas espejo y direcciones URL de seguimiento).

* Agregue un registro TXT de verificación del sitio de Google al subdominio para asegurarse de que está verificado (consulte [Agregar un registro TXT de Google a un subdominio](google-txt.md)).

>[!CAUTION]
>
>La configuración del subdominio es **común a todos los entornos**. Por lo tanto, cualquier modificación en un subdominio también afectará a las zonas protegidas de producción.

## Configuración de un subdominio en Journey Optimizer {#set-up-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="Generar los registros DNS coincidentes"
>abstract="Para delegar completamente un nuevo subdominio a Adobe, debe copiar y pegar la información del servidor de nombres de Adobe que se muestra en la interfaz de Journey Optimizer en la solución de alojamiento de dominios para generar los registros DNS coincidentes. Para delegar un subdominio mediante CNAME, también debe copiar y pegar el registro de validación de URL de CDN SSL. Una vez realizadas las comprobaciones correctamente, el subdominio está listo para utilizarse para enviar mensajes."

Para configurar un nuevo subdominio en [!DNL Journey Optimizer], siga los pasos a continuación.
<!--
>[!NOTE]
>
>This section describes how to set up a subdomain using the full delegation. The custom delegation method is detailed in [this section](#setup-custom-subdomain).-->

1. Acceda al menú **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Subdominios]** y haga clic en **[!UICONTROL Configurar subdominio]**.

   <!--![](assets/subdomain-delegate.png)-->

1. En la sección **[!UICONTROL Configurar método]**, seleccione:

   * Delegado completamente: [Más información](about-subdomain-delegation.md#full-subdomain-delegation)
   * Configuración de CNAME: [Más información](about-subdomain-delegation.md#cname-subdomain-setup)

     Aprenda a configurar subdominios con CNAME en esta [sección dedicada](#cname-subdomain-setup)

   <!--![](assets/subdomain-method-full.png)-->

1. Especifique el nombre del subdominio que desea delegar.

   ![](assets/subdomain-name.png)
<!--
    >[!CAUTION]
    >
    >Delegating an invalid subdomain to Adobe is not allowed. Make sure you enter a valid subdomain which is owned by your organization, such as marketing.yourcompany.com.
    >
    >You cannot use the same sending domain to send out messages from [!DNL Adobe Journey Optimizer] and from another product, such as [!DNL Adobe Campaign] or [!DNL Adobe Marketo Engage].

    Capital letters are not allowed in subdomains. TBC by PM-->

1. Configure **[!UICONTROL registro de DMARC]** en la sección dedicada. Si el subdominio tiene un [registro DMARC](dmarc-record.md) existente y [!DNL Journey Optimizer] lo ha recuperado, puede usar los mismos valores o cambiarlos según sea necesario. Si no añade ningún valor, se utilizarán los valores predeterminados. [Aprenda a administrar el registro de DMARC](dmarc-record.md#set-up-dmarc)

   ![](assets/dmarc-record-found.png)

1. En la sección **[!UICONTROL Registro DNS]**, se muestra la lista de registros que se van a colocar en los servidores DNS. Copie estos registros, uno por uno o descargando un archivo CSV, y luego vaya a la solución de alojamiento de dominios para generar los registros DNS coincidentes.

1. Asegúrese de que todos los registros DNS se hayan generado en la solución de alojamiento de dominios. Si todo está configurado correctamente, marque la casilla &quot;Confirmo...&quot;.

   ![](assets/subdomain-submit.png)

1. Si está configurando un subdominio con **CNAME**, vaya a [esta sección](#cname-subdomain-setup).

1. Haga clic en **[!UICONTROL Enviar]** para que Adobe realice las comprobaciones necesarias. [Más información](#submit-subdomain)

## Configurar un subdominio con CNAME {#cname-subdomain-setup}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="Generar los registros de validación y DNS coincidentes"
>abstract="Para delegar un subdominio mediante CNAME, debe copiar y pegar la información del servidor de nombres de Adobe y el registro de validación de URL de CDN SSL que se muestra en la interfaz de Journey Optimizer en la plataforma de alojamiento. Una vez realizadas las comprobaciones correctamente, el subdominio está listo para utilizarse para enviar mensajes."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="Copiar el registro de validación"
>abstract="Adobe genera un registro de validación. Debe crear el registro correspondiente en su plataforma de alojamiento para la validación de URL de CDN."

Al configurar un subdominio, puede utilizar CNAME para señalar registros específicos de Adobe. Con esta configuración, tanto usted como Adobe comparten la responsabilidad de mantener DNS.

>[!CAUTION]
>
>Se recomienda el método CNAME si las políticas de su organización restringen el método de delegación de subdominios completo. Este enfoque requiere que mantenga y administre los registros DNS por su cuenta.
>
>Adobe no podrá ayudarle a cambiar, mantener o administrar DNS para un subdominio configurado mediante el método CNAME.

Para configurar un subdominio mediante CNAME, siga los pasos a continuación.

1. Realice todos los pasos descritos en [esta sección](#set-up-subdomain).

1. Antes de enviar la configuración del subdominio, tiene que completar un paso más: haga clic en **[!UICONTROL Continuar]**. Espere hasta que Adobe compruebe que los registros se generan sin errores en la solución de alojamiento. Este proceso puede tardar hasta 2 minutos.

   >[!NOTE]
   >
   >Asegúrese de que todos los registros se hayan creado correctamente antes de continuar.

1. Adobe genera un registro de validación de URL de CDN SSL. Copie este registro de validación en la plataforma de alojamiento. Si ha creado correctamente este registro en su solución de alojamiento, marque la casilla &quot;Confirmo...&quot;.

1. Haga clic en **[!UICONTROL Enviar]** para que Adobe realice las comprobaciones necesarias. [Más información](#submit-subdomain)

➡️ [Aprenda a crear un subdominio mediante CNAME para que apunte a registros específicos de Adobe en este vídeo](#video)

## Envío de la configuración del subdominio {#submit-subdomain}

Para completar la delegación de subdominios, siga los pasos a continuación.

1. Haga clic en **[!UICONTROL Enviar]**.

   >[!NOTE]
   >
   >Si se produce un error al intentar enviar un subdominio personalizado, consulte [esta sección](#check-list).


1. Puede crear los registros y enviar la configuración del subdominio más adelante utilizando el botón **[!UICONTROL Guardar como borrador]**.

   >[!NOTE]
   >
   >A continuación, podrá reanudar la delegación de subdominios abriéndola desde la lista de subdominios.

1. El subdominio se muestra en la lista con el estado **[!UICONTROL Procesando]**. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](#access-delegated-subdomains).

   <!--![](assets/subdomain-processing.png)-->

1. Antes de poder utilizar ese subdominio para enviar mensajes, debe esperar hasta que Adobe realice las comprobaciones necesarias, que pueden tardar hasta tres horas. [Más información](#subdomain-validation).

   >[!NOTE]
   >
   >Asegúrese de que todos los registros se hayan creado correctamente antes de continuar.

### Validación de subdominios {#subdomain-validation}

Las comprobaciones y acciones siguientes se ejecutan hasta que se verifica el subdominio y se puede utilizar para enviar mensajes.

Estos pasos los realiza Adobe y pueden tomar **hasta tres horas**.

1. **Validación previa**: Adobe comprueba si el subdominio se ha delegado a Adobe DNS (registro NS, registro SOA, configuración de zona, registro de propiedad). Si el paso de prevalidación falla, se devuelve un error junto con el motivo correspondiente; de lo contrario, Adobe pasa al siguiente paso.

1. **Configurar DNS para el dominio**:

   * **registro MX**: registro de intercambio de correo: registro del servidor de correo que procesa los correos electrónicos entrantes enviados al subdominio.
   * **registro SPF**: registro Marco de directivas de remitente: enumera las direcciones IP de los servidores de correo que pueden enviar correos electrónicos desde el subdominio.
   * **Registro de DKIM**: Registro estándar de DomainKeys Identified Mail: utiliza el cifrado de clave pública y privada para autenticar el mensaje y evitar la suplantación de identidad.
   * **A**: asignación de IP predeterminada.
   * **CNAME**: un registro CNAME o de nombre canónico es un tipo de registro DNS que asigna un nombre de alias a un nombre de dominio verdadero o canónico.

1. **Crear direcciones URL de seguimiento y espejo**: si el dominio es email.example.com, el dominio de seguimiento o reflejo será data.email.example.com. Se protege instalando el certificado SSL.

1. **Aprovisionar CDN CloudFront**: si CDN no está ya configurado, Adobe lo aprovisiona para el ID de su organización.

1. **Crear dominio CDN**: si el dominio es email.example.com, el dominio CDN será cdn.email.example.com.

1. **Crear y adjuntar certificado SSL de CDN**: Adobe crea el certificado de CDN para el dominio de CDN y adjunta el certificado al dominio de CDN.

1. **Crear DNS de reenvío**: si este es el primer subdominio que delega, Adobe creará el DNS de reenvío necesario para crear registros PTR, uno para cada una de las direcciones IP.

1. **Crear registro PTR**: Los ISP requieren el registro PTR, también conocido como registro DNS inverso, para que no marquen los correos electrónicos como correo no deseado. Gmail también recomienda tener registros PTR para cada IP. Adobe crea registros PTR solo cuando se delega un subdominio por primera vez, uno para cada IP y todas las direcciones IP que apuntan a ese subdominio. Por ejemplo, si la dirección IP es *192.1.2.1* y el subdominio es *email.example.com*, el registro PTR será: *192.1.2.1PTR r1.email.example.com*. Puede actualizar el registro PTR posteriormente para que apunte al nuevo dominio delegado. [Más información sobre los registros PTR](ptr-records.md)

Una vez que las comprobaciones son correctas, el subdominio obtiene el estado **[!UICONTROL Success]**. Está listo para utilizarse para enviar mensajes.

El subdominio se marcará como **[!UICONTROL Error]** si no se puede crear el registro de validación en la solución de alojamiento.

Al validar el registro, Adobe crea automáticamente el registro PTR para el subdominio. [Más información](ptr-records.md)

## Anular la delegación de un subdominio {#undelegate-subdomain}

Si desea desdelegar un subdominio, póngase en contacto con su representante de Adobe.

Sin embargo, debe realizar varios pasos en la interfaz de usuario antes de ponerse en contacto con Adobe.

>[!NOTE]
>
>Solo puede anular la delegación de subdominios con el estado **[!UICONTROL Correcto]**. Los subdominios con los estados **[!UICONTROL Borrador]** y **[!UICONTROL Error]** simplemente se pueden eliminar de la interfaz de usuario.

Primero, realice los siguientes pasos en [!DNL Journey Optimizer]:

1. Desactive todas las configuraciones de canal asociadas con el subdominio. [Descubra cómo](../configuration/channel-surfaces.md#deactivate-a-surface)

1. Anule la delegación de cualquier subdominio de página de aterrizaje, subdominio de SMS y subdominio web asociado a este subdominio.

   Debe generar una solicitud dedicada para cada [página de aterrizaje](../landing-pages/lp-subdomains.md#undelegate-subdomain), [SMS](../sms/sms-subdomains.md#undelegate-subdomain) o [subdominio web](../web/web-delegated-subdomains.md#undelegate-subdomain).

1. Detenga las campañas activas asociadas a los subdominios. [Descubra cómo](../campaigns/modify-stop-campaign.md#stop)

1. Detenga los recorridos activos asociados a los subdominios. [Descubra cómo](../building-journeys/end-journey.md#stop-journey)

1. Apunte los [registros PTR](ptr-records.md#edit-ptr-record) vinculados al subdominio a otro subdominio.

   Si este es el único subdominio delegado, puede omitir este paso.

Una vez finalizado, póngase en contacto con el representante de Adobe con el subdominio que desee desdelegar.

Una vez que Adobe administra la solicitud, el dominio no delegado ya no se muestra en la página de inventario de subdominios.

>[!CAUTION]
>
>Después de desdelegar un subdominio, se aplica lo siguiente:
>
>* No puede reactivar las configuraciones de canal que utilizaban ese subdominio.
>* No puede volver a delegar el mismo subdominio a través de la interfaz de usuario. Si desea hacerlo, póngase en contacto con su representante de Adobe.

## Vídeo práctico{#video}

Aprenda a crear un subdominio con CNAME para que apunte a registros específicos de Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
