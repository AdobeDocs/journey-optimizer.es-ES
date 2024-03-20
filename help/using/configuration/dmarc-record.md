---
solution: Journey Optimizer
product: journey optimizer
title: Registro DMARC
description: Obtenga información sobre cómo establecer el registro DMARC en Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdominio, dominio, correo, dmarc, registro
exl-id: f9e217f8-5aa8-4d3a-96fc-65defcb5d340
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 12%

---

# Registro DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Establecimiento del registro DMARC"
>abstract="DMARC es un método de autenticación por correo electrónico que permite a los propietarios del dominio proteger su dominio de un uso no autorizado y evitar problemas de entregabilidad con los proveedores de buzones de correo.<br>Como parte del cumplimiento de las mejores prácticas del sector, Google y Yahoo! le exigen que tenga un registro DMARC para cualquier dominio que utilice para enviarles un correo electrónico."

## ¿Qué es DMARC? {#what-is-dmarc}

La autenticación de mensajes basada en dominios, sistemas de informes y conformidad (DMARC) es un método de autenticación por correo electrónico que permite a los propietarios de dominios proteger su dominio contra el uso no autorizado. Al ofrecer una política clara a los proveedores de correo electrónico y de servicios de Internet (ISP), ayuda a evitar que actores maliciosos envíen correos electrónicos que afirman ser de su dominio. La implementación de DMARC reduce el riesgo de que los correos electrónicos legítimos se marquen como correo no deseado o se rechacen y mejora su entregabilidad

DMARC también ofrece informes sobre los mensajes que no superan la autenticación, junto con control sobre el tratamiento de los correos electrónicos que no superan la validación DMARC. Según el implementado [directiva DMARC](#dmarc-policies)Sin embargo, estos correos electrónicos se pueden monitorizar, poner en cuarentena o rechazar. Estas funcionalidades le permiten realizar acciones para mitigar y abordar posibles errores.

Para ayudarle a evitar problemas de envío y, al mismo tiempo, obtener control sobre el correo que falla en la autenticación, [!DNL Journey Optimizer] ahora admite la tecnología DMARC directamente en su interfaz de administración. [Más información](#implement-dmarc)

### ¿Cómo funciona DMARC? {#how-dmarc-works}

SPF y DKIM se utilizan para asociar un correo electrónico con un dominio y trabajar juntos para autenticar el correo electrónico. DMARC lleva esto un paso más allá y ayuda a evitar la suplantación de identidad haciendo coincidir el dominio comprobado por DKIM y SPF.

>[!NOTE]
>
>En Journey Optimizer, SPF y DKIM están configurados automáticamente.

Para pasar DMARC, un mensaje debe pasar SPF o DKIM:

* SPF (Marco de Política del Remitente) ayuda a verificar que el mensaje de correo electrónico proviene de una fuente autorizada comprobando la dirección IP del servidor remitente con una lista de direcciones IP autorizadas para el dominio.
* DKIM (DomainKeys Identified Mail) añade una firma digital a los mensajes de correo electrónico, lo que permite al destinatario verificar la integridad y autenticidad del mensaje.

Si ambas o alguna de estas falla en la autenticación, DMARC fallará y el correo electrónico se enviará según la política DMARC seleccionada.

<!--DMARC requires alignment between the 'From" and 'Return-Path' address.-->

### Directivas de DMARC {#dmarc-policies}

Si un correo electrónico no supera la autenticación DMARC, puede decidir qué acción se aplicará a ese mensaje. DMARC tiene tres opciones de directiva:

* Monitor (p=none): indica al proveedor del buzón/ISP que haga lo que normalmente haría con el mensaje.
* Cuarentena (p=quarantine): indica al proveedor del buzón/ISP que envíe el correo que no pasa DMARC a la carpeta de correo no deseado o correo no deseado del destinatario.
* Reject (p=reject): indica al proveedor/ISP del buzón que bloquee el correo que no pasa DMARC, lo que provoca un rechazo.

>[!NOTE]
>
>Obtenga información sobre cómo establecer la directiva DMARC con [!DNL Journey Optimizer] in [esta sección](#set-up-dmarc).

## Actualización de requisitos de DMARC {#dmarc-update}

Como parte del cumplimiento de las prácticas recomendadas del sector, Google y Yahoo! requiere que tenga un... **Registro DMARC** para cualquier dominio que utilice para enviarles correos electrónicos. Este nuevo requisito se aplica desde el **1 de febrero de 2024**. 

>[!CAUTION]
>
>Se espera que el incumplimiento de este nuevo requisito de Gmail y Yahoo! provoque que los correos electrónicos acaben en la carpeta de spam o sean bloqueados.

Por lo tanto, el Adobe recomienda encarecidamente que realice las siguientes acciones:

* Asegúrese de tener **Registro DMARC** configurado para **todos los subdominios que ya ha delegado** al Adobe en [!DNL Journey Optimizer]. [Descubra cómo](#check-subdomains-for-dmarc)

* Cuándo **delegación de cualquier nuevo subdominio** al Adobe, puede **configuración de DMARC** directamente **en el [!DNL Journey Optimizer] interfaz de administración**. [Descubra cómo](#implement-dmarc)

## Implementación de DMARC en [!DNL Journey Optimizer] {#implement-dmarc}

El [!DNL Journey Optimizer] La interfaz de administración de le permite configurar el registro DMARC para todos los subdominios que ya ha delegado o que está delegando a Adobe. A continuación se describen los pasos detallados.

### Comprobar los subdominios existentes para DMARC {#check-subdomains-for-dmarc}

Para asegurarse de que tiene configurado el registro DMARC para todos los subdominios delegados en [!DNL Journey Optimizer], siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Canales]** > **[!UICONTROL Subdominios]** y haga clic en **[!UICONTROL Configuración del subdominio]**.

1. Para cada subdominio delegado, marque **[!UICONTROL Registro DMARC]** columna. Si no se ha encontrado ningún registro para un subdominio determinado, se muestra una alerta.

   ![](assets/dmarc-record-alert.png)

   >[!CAUTION]
   >
   >Para cumplir con el nuevo requisito de Gmail y Yahoo!, y evitar problemas de entrega con los principales ISP, se recomienda configurar el registro DMARC para todos los subdominios delegados. [Más información](dmarc-record-update.md)

1. Seleccione un subdominio sin registro DMARC asociado y rellene la variable **[!UICONTROL Registro DMARC]** de acuerdo con las necesidades de su organización. Los pasos para rellenar los campos de registro DMARC se detallan en [esta sección](#implement-dmarc).

1. Tenga en cuenta las dos opciones siguientes:

   * Si está editando un subdominio configurado con [CNAME](delegate-subdomain.md#cname-subdomain-delegation)Además, debe copiar el registro DNS de DMARC en la solución de alojamiento para generar los registros DNS coincidentes.

     ![](assets/dmarc-record-edit-cname.png)

     Asegúrese de que el registro DNS se haya generado en la solución de alojamiento de dominios y marque la casilla &quot;Confirmo...&quot;.

   * Si está editando un subdominio [totalmente delegado](delegate-subdomain.md#full-subdomain-delegation) para almacenar en Adobe, simplemente rellene el **[!UICONTROL Registro DMARC]** campos detallados en [esta sección](#implement-dmarc). No se requiere ninguna otra acción.

     ![](assets/dmarc-record-edit-full.png)

1. Guarde los cambios.

### Configuración de DMARC para nuevos subdominios {#set-up-dmarc}

Al delegar nuevos subdominios al Adobe en [!DNL Journey Optimizer], se creará un registro DMARC en DNS para su dominio. Siga los pasos a continuación para implementar DMARC.

>[!CAUTION]
>
>Para cumplir con el nuevo requisito de Gmail y Yahoo!, y evitar problemas de entrega con los principales ISP, se recomienda configurar el registro DMARC para todos los subdominios delegados. [Más información](dmarc-record-update.md)

<!--If you fail to comply with the new requirement from Gmail and Yahoo! to have DMARC record for all sending domains, your emails are expected to land into the spam folder or to get blocked.-->

1. Configure un nuevo subdominio. [Descubra cómo](delegate-subdomain.md)

1. Vaya a la **[!UICONTROL Registro DMARC]** sección.

   Si el subdominio tiene un registro DMARC existente y si lo recupera [!DNL Journey Optimizer], puede utilizar los mismos valores que aparecen resaltados en la interfaz o cambiarlos según sea necesario.

   ![](assets/dmarc-record-found.png)

   >[!NOTE]
   >
   >Si no añade ningún valor, se utilizarán los valores predeterminados rellenados previamente.

1. Defina la acción que realizará el servidor de destinatario si DMARC falla. Según la variable [directiva DMARC](#dmarc-policies) Si desea aplicar, seleccione una de las tres opciones:

   * **[!UICONTROL Ninguno]** (valor predeterminado): Indica al destinatario que no realice acciones contra los mensajes que no superen la autenticación DMARC, pero que, aun así, envíe informes de correo electrónico al remitente.
   * **[!UICONTROL Cuarentena]**: Indica al servidor de correo electrónico receptor que ponga en cuarentena el correo electrónico que falla en la autenticación DMARC. Esto generalmente significa colocar esos mensajes en la carpeta de correo no deseado o correo no deseado del destinatario.
   * **[!UICONTROL Rechazar]**: Indica al destinatario que deniegue (devuelva) completamente cualquier correo electrónico del dominio que falle en la autenticación. Con esta directiva habilitada, solo los correos electrónicos verificados como 100 % autenticados por el dominio tendrán la oportunidad de colocarse en la bandeja de entrada.

   >[!NOTE]
   >
   >Como práctica recomendada, se recomienda implementar lentamente la implementación de DMARC escalando la directiva DMARC de **Ninguno**, a **Cuarentena**, a **Rechazar** a medida que comprenda el impacto potencial de DMARC.

1. De forma opcional, añada una o más direcciones de correo electrónico de su elección para indicar dónde **Informes DMARC** en correos electrónicos que [autenticación fallida](#how-dmarc-works) debe pertenecer a su organización. Se pueden agregar hasta cinco direcciones para cada informe.

   >[!NOTE]
   >
   >Asegúrese de tener una bandeja de entrada (no un Adobe) original en el control donde pueda recibir esos informes.

   Los ISP generan dos informes diferentes que los remitentes pueden recibir a través de las etiquetas RUA/RUF en su directiva DMARC:

   * **Informes agregados** (RUA): No contienen ninguna PII (información de identificación personal) que pueda ser sensible al RGPD.
   * **Informes de fallos forenses** (RUF): Contienen direcciones de correo electrónico sensibles al RGPD. Antes de utilizar, compruebe internamente cómo tratar la información que necesita cumplir con el RGPD.

   >[!NOTE]
   >
   >Estos informes, de carácter muy técnico, proporcionan una visión general de los correos electrónicos que se intentan suplantar. Se digieren mejor mediante una herramienta de terceros.

1. Seleccione el **porcentaje aplicable** de correos electrónicos para DMARC.

   Este porcentaje depende de la confianza que tenga en la infraestructura de correo electrónico y de la tolerancia de los falsos positivos (los correos electrónicos legítimos se marcan como fraudulentos). Es común que las organizaciones empiecen con la directiva DMARC establecida en **Ninguno**, aumente gradualmente el porcentaje de política de DMARC y monitorice de cerca el impacto en la entrega de correo electrónico legítimo.

   >[!NOTE]
   >
   >Trabaje con los administradores de correo electrónico y el equipo de TI para aumentar gradualmente el porcentaje a medida que vaya ganando confianza en las prácticas de autenticación de correo electrónico.

   Como práctica recomendada, el objetivo es lograr una tasa de cumplimiento de la DMARC alta, idealmente cercana al 100 %, para maximizar los beneficios de seguridad y minimizar al mismo tiempo el riesgo de falsos positivos.

1. Seleccione una **intervalo de informes** entre 24 y 168 horas. Permite a los propietarios de dominio recibir actualizaciones regulares de los resultados de autenticación por correo electrónico y tomar las medidas necesarias para mejorar la seguridad del correo electrónico.

   <!--The DMARC reporting interval is specified in the DMARC policy published in the DNS (Domain Name System) records for a domain. The reporting interval can be set to daily, weekly, or another specified frequency, depending on the domain owner's preferences.

    The default value (24 hours) is generally the email providers' expectation.-->


<!--

Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.

DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

## What are the benefits of DMARC? {#dmarc-benefits}

The key benefits or DMARC are as folllows:

* DMARC allows email receivers to easily identify the authentication of emails, which could potentially improve delivery.

* It offers reporting on which messages fail SPF and/or DKIM, enabling senders to gain visibility.

* This increased visibility allows for steps to be taken to mitigate further errors. It gives senders a degree of control over what happens with mail that does not pass either of these authentication methods.

-->
