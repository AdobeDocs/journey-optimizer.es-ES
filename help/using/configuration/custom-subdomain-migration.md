---
solution: Journey Optimizer
product: journey optimizer
title: Migración de un subdominio de correo electrónico desde CNAME a una delegación personalizada
description: Obtenga información sobre cómo migrar un subdominio de correo electrónico o de página de aterrizaje de delegación CNAME a delegación personalizada en Journey Optimizer.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Intermediate
keywords: subdominio, delegación, migración, CNAME, delegación personalizada
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 316553be4f04e4fc0ae11bc767f7e48f64fc5ccd
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 5%

---

# Migración de un subdominio de correo electrónico desde CNAME a una delegación personalizada {#migrate-cname-to-custom}

>[!AVAILABILITY]
>
>Esta funcionalidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

Si el subdominio está configurado actualmente con [CNAME](about-subdomain-delegation.md#cname-subdomain-setup), puede migrarlo al método de **[!UICONTROL delegación personalizada]** para cumplir con las directivas de seguridad de su compañía. Esto le proporciona total propiedad y control sobre los subdominios y certificados dentro de [!DNL Journey Optimizer]. [Más información sobre los subdominios personalizados](delegate-custom-subdomain.md)

Como parte de este proceso, debe:

* [Elimine los registros DNS existentes](#delete-dns) de su solución de alojamiento
* [Cargar el certificado SSL](#upload-ssl-certificate) obtenido de la entidad emisora de certificados
* Complete los [pasos del bucle de comentarios](#feedback-loop) comprobando la propiedad del dominio y la dirección de correo electrónico del informe
* [Copie el registro de validación de URL de CDN SSL](#copy-ssl-cdn-url-record) generado por Adobe en su plataforma de alojamiento

Para migrar el subdominio, siga los pasos a continuación.

## Antes de empezar {#before-you-begin}

Antes de iniciar el proceso de migración, revise la información importante que aparece a continuación.

>[!IMPORTANT]
>
>Solo puede migrar un subdominio configurado con el [método CNAME](delegate-subdomain.md#cname-subdomain-setup).

* Asegúrese de que el método de delegación **personalizada está habilitado** para su organización (esta capacidad está actualmente en disponibilidad limitada; póngase en contacto con su representante de Adobe para obtener acceso). [Más información](delegate-custom-subdomain.md)
* Asegúrese de que no haya configuraciones de canal activas que utilicen este subdominio. El proceso de migración interrumpirá su funcionalidad.
* Asegúrese de que no haya campañas o recorridos activos que utilicen una configuración de canal vinculada a este subdominio, ya que esto puede provocar interrupciones en la entrega.
* Tenga en cuenta que el tiempo de inactividad comienza en cuanto entra en el flujo de migración. El subdominio se mueve a **[!UICONTROL Borrador]** durante el proceso y no estará disponible hasta que se complete la instalación.
* Por lo tanto, se recomienda **realizar los pasos previos a la migración antes de iniciar el proceso de migración**, a fin de tener el certificado SSL listo y reducir el tiempo de inactividad. [Más información](#start-migration)

## Iniciar la migración {#start-migration}

Siga los pasos a continuación para comenzar a migrar un subdominio determinado.

1. Vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Subdominios]**.

1. Seleccione un subdominio configurado con CNAME y ábralo.

1. Puede usar la sección **[!UICONTROL Generación de CSR previa a la migración]** para generar la CSR y enviarla a la entidad emisora de certificados y tener el certificado SSL listo cuando se inicie el proceso de migración. [Descubra cómo](#send-csr-to-ca)

   >[!IMPORTANT]
   >
   >Los pasos previos a la migración son opcionales en esta fase, pero se recomienda encarecidamente. Completarlos **antes de** de iniciar la migración reduce el tiempo de inactividad y ayuda a garantizar una transición sin problemas.

   ![](assets/subdomain-migrate-pre-migration-csr.png){width="70%"}

1. Seleccione **[!UICONTROL Migrar ahora]** en la sección dedicada.

   <!--![](assets/subdomain-migrate-to-custom.png){width=90%}-->

1. Revise la [información mostrada](#before-you-begin).

   >[!WARNING]
   >
   >El tiempo de inactividad comienza en cuanto entra en el flujo de migración, por lo que debe asegurarse de que no afecte a sus campañas y recorridos activos.

1. Haga clic en **[!UICONTROL Sí]**. El subdominio pasa al estado **[!UICONTROL Borrador]** y no estará disponible hasta que se complete la instalación.

## Generar y enviar el CSR a la autoridad de certificación {#send-csr-to-ca}

Para completar la migración, necesita un certificado SSL emitido por una autoridad de certificación (CA). Para recibir este certificado SSL, primero debe generar una Solicitud de firma de certificado (CSR) y enviarla a la CA.

Tanto si ya ha iniciado el proceso de migración como si no, siga los pasos a continuación para generar y enviar su nuevo CSR.

1. Haga clic en **[!UICONTROL Regenerar CSR]**.

1. Rellene el formulario que muestra y vuelve a generar la solicitud de firma de certificado (CSR).

   ![](assets/subdomain-migrate-regenerate-csr.png){width="60%"}

   >[!NOTE]
   >
   >La longitud de la clave puede ser de 2048 o 4096 bits únicamente. No se puede cambiar después de enviar el subdominio.

1. Haga clic en **[!UICONTROL Descargar CSR]** y guarde el formulario en el equipo local.

1. Envíelo a la autoridad de certificación (CA) para obtener su certificado SSL. Antes de enviar esta CSR a su CA para su firma, hay que tener en cuenta algunos puntos importantes:

   * La CSR descargada del paso 3 solo es para data.subdomain.com.

   * Sin embargo, el certificado debe cubrir tanto data.subdomain.com como cdn.subdomain.com como entradas de nombres alternativos del sujeto (SAN) dentro de un solo certificado. Por ejemplo, si delega example.adobe.com, data.subdomain.com corresponde a data.example.adobe.com y cdn.subdomain.com a cdn.example.adobe.com.

   * Los subdominios Data (data.example.adobe.com) y CDN (cdn.example.adobe.com) deben agregarse como entradas del mismo nivel en el mismo certificado.

   * La mayoría de las CA le permiten agregar SAN adicionales (como el subdominio CDN) durante el proceso de firma

      * A través del portal de CA (recomendado, si está disponible), o
      * Solicitándola manualmente con su equipo de asistencia si la opción del portal no está disponible.

   * Una vez firmada, la CA emitirá un único certificado que abarcará tanto el dominio de datos como el subdominio de CDN.

## Eliminar registros DNS existentes {#delete-dns}

Después de iniciar el proceso de migración, debe eliminar los registros DNS existentes de la solución de alojamiento. Siga los pasos a continuación.

1. Se muestra la lista de registros configurados actualmente en los servidores DNS.

1. Vaya a la solución de alojamiento de dominios y elimine las entradas CNAME existentes de su alojamiento DNS.

1. Asegúrese de que se hayan eliminado todos los registros DNS. Una vez finalizado, marque la casilla &quot;Confirmo que he eliminado los registros necesarios del sitio de alojamiento&quot;.

   ![](assets/subdomain-migrate-delete-dns.png){width="75%"}

## Cargar el certificado SSL {#upload-ssl-certificate}

En la sección **[!UICONTROL Certificado SSL]**, debe cargar un nuevo certificado SSL en [!DNL Journey Optimizer].

Antes de ello, compruebe lo siguiente:

* Si ya ha enviado su CSR a la entidad emisora de certificados como parte de los [pasos previos a la migración](#start-migration), asegúrese de que ha recibido su certificado SSL.

* Si aún no lo has hecho, sigue los pasos para [generar, descargar y enviar el CSR](#send-csr-to-ca).

<!--
    * Click **[!UICONTROL Regenerate CSR]** and fill the form to generate the Certificate Signing Request.

    * Click **[!UICONTROL Download CSR]** to save the form to your local computer.

    * Send the CSR to the Certificate Authority to get your SSL certificate.-->

1. Una vez que haya recuperado su certificado SSL, haga clic en **[!UICONTROL Cargar certificado]**.

   ![](assets/subdomain-migrate-ssl-certificate.png){width="75%"}

1. Cargue el certificado SSL a [!DNL Journey Optimizer] en formato .pem con la cadena de certificados completa. Este es un ejemplo de formato de archivo .pem:

   ```
   -----BEGIN CERTIFICATE-----
   MIIDXTCCAkWgAwIBAgIJALc3... (base64 encoded data)
   -----END CERTIFICATE-----
   ```
1. Marque la casilla &quot;Confirmo que he cargado el certificado SSL&quot;.

## Completo bucle de comentarios {#feedback-loop}

A continuación, complete los pasos del bucle de comentarios para verificar la propiedad del dominio y la dirección de correo electrónico del sistema de informes.

![](assets/subdomain-migrate-feedback-loop.png){width="75%"}

El proceso es el mismo que al configurar un nuevo subdominio personalizado. Siga los pasos detallados en la página [Configurar un subdominio personalizado](delegate-custom-subdomain.md#feedback-loop-steps).

## Copiar el registro de validación de URL de CDN SSL {#copy-ssl-cdn-url-record}

Para completar el proceso de migración, copie el registro de validación de URL de CDN SSL generado por Adobe en la plataforma de alojamiento. El proceso es el mismo que al configurar un nuevo subdominio personalizado. Siga los pasos detallados en la página [Configurar un subdominio personalizado](delegate-custom-subdomain.md#copy-ssl-cdn-url-record).

Después del envío, debe esperar hasta que Adobe realice las comprobaciones necesarias, que pueden tardar hasta tres horas. [Más información](delegate-subdomain.md#submit-subdomain)

Una vez que el subdominio vuelva a estar activo, no es necesario realizar cambios en las configuraciones de canal existentes que lo utilizan; siguen funcionando como antes.

**Consulte también**

* [Configuración de un subdominio personalizado](delegate-custom-subdomain.md)
* [Métodos de delegación de subdominios](about-subdomain-delegation.md#subdomain-delegation-methods)
