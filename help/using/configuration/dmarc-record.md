---
solution: Journey Optimizer
product: journey optimizer
title: Registro DMARC
description: Aprenda a establecer un registro DMARC en Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdominio, dominio, correo, dmarc, registro
exl-id: f9e217f8-5aa8-4d3a-96fc-65defcb5d340
source-git-commit: e539d694e8fb91b6a8c7ba7ff5a2bb0905651f81
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 11%

---

# Registro DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Establecimiento del registro DMARC"
>abstract="DMARC es un método de autenticación por correo electrónico que permite a los propietarios del dominio proteger su dominio de un uso no autorizado y evitar problemas de entregabilidad con los proveedores de buzones de correo.<br>Como parte del cumplimiento de las mejores prácticas del sector, Google y Yahoo! le exigen que tenga un registro DMARC para cualquier dominio que utilice para enviarles un correo electrónico."

## ¿Qué es DMARC? {#what-is-dmarc}

La autenticación de mensajes basada en dominios, sistemas de informes y conformidad (DMARC) es un método de autenticación por correo electrónico que permite a los propietarios de dominios proteger su dominio contra el uso no autorizado. Al ofrecer un directiva claro a los proveedores de correo electrónico y proveedores de servicios de Internet (ISP), ayuda a evitar que actores malintencionados envíen correos electrónicos que afirman ser de su dominio. La implementación de DMARC reduce el riesgo de que los correos electrónicos legítimos se marquen como correo no deseado o se rechacen y mejora su entregabilidad

DMARC también ofrece sistema de informes en los mensajes que fallan la autenticación, junto con control sobre el manejo de correos electrónicos que no pasan la validación DMARC. Según el directiva](#dmarc-policies) de DMARC implementado[, estos correos electrónicos se pueden supervisar, poner en cuarentena o rechazar. Estas capacidades le permiten tomar medidas para mitigar y abordar posibles errores.

Para ayudarle a evitar problemas de entregabilidad mientras obtiene control sobre el correo que falla la autenticación, [!DNL Journey Optimizer] ahora es compatible con la tecnología DMARC directamente en su interfaz de administración. [Más información](#implement-dmarc)

### ¿Cómo funciona DMARC? {#how-dmarc-works}

SPF y DKIM se utilizan para asociar un correo electrónico a un dominio y trabajar juntos para autenticar correo electrónico. DMARC lleva esto un paso más allá y ayuda a prevenir la suplantación de identidad al hacer coincidir el dominio verificado por DKIM y SPF.

>[!NOTE]
>
>En Journey Optimizer, SPF y DKIM están configurados automáticamente.

Para pasar DMARC, un mensaje debe pasar SPF o DKIM:

* SPF (Marco de Política del Remitente) ayuda a verificar que el mensaje de correo electrónico proviene de una fuente autorizada comprobando la dirección IP del servidor remitente con una lista de direcciones IP autorizadas para el dominio.
* DKIM (DomainKeys Identified Mail) agrega un Firma digital a correo electrónico mensajes, lo que permite al destinatario verificar la integridad y autenticidad del mensaje.

Si ambos o ninguno de estos fallan la autenticación, DMARC fallará y la correo electrónico se entregará de acuerdo con su directiva DMARC seleccionada.

<!--DMARC requires alignment between the 'From" and 'Return-Path' address.-->

### Políticas DMARC {#dmarc-policies}

Si un correo electrónico no supera la autenticación DMARC, puede decidir qué acción se aplicará a ese mensaje. DMARC tiene tres directiva opciones:

* Monitor (p=ninguno): indica al proveedor de buzones/ISP que haga lo que normalmente haría con el mensaje.
* Cuarentena (p=quarantine): indica al proveedor del buzón/ISP que entregue el correo que no pasa DMARC a la carpeta de correo no deseado del destinatario.
* Reject (p=reject): indica al proveedor/ISP del buzón que bloquee el correo que no pasa DMARC, lo que provoca un rechazo.

>[!NOTE]
>
>Aprenda a establecer la directiva de DMARC en [!DNL Journey Optimizer] [esta sección](#set-up-dmarc).

## Actualización de requisitos de DMARC {#dmarc-update}

Como parte del cumplimiento de las prácticas recomendadas del sector, Google y Yahoo! ambas requieren que tenga un **registro** DMARC para cualquier dominio que utilice para enviarles correo electrónico de imagen. Este nuevo requisito se aplica desde el **1 de febrero de 2024**. 

>[!CAUTION]
>
>Se espera que el incumplimiento de este nuevo requisito de Gmail y Yahoo! provoque que los correos electrónicos acaben en la carpeta de spam o sean bloqueados.

Por consiguiente, Adobe Systems recomienda encarecidamente que realice las siguientes acciones:

* Asegúrese de tener el registro **DMARC configurado para** todos los subdominios que ya ha delegado **en Adobe Systems en [!DNL Journey Optimizer].** [Descubra cómo](#check-subdomains-for-dmarc)

* Al **delegar cualquier subdominio** nuevo a Adobe Systems, puede **configurar DMARC** directamente **en la interfaz** de [!DNL Journey Optimizer] administración. [Descubra cómo](#implement-dmarc)

## Implementar DMARC en [!DNL Journey Optimizer] {#implement-dmarc}

La [!DNL Journey Optimizer] interfaz de administración le permite configurar el registro DMARC para todos los subdominios que ya ha delegado o está delegando en Adobe Systems. A continuación se describen los pasos detallados.

### Compruebe los subdominios existentes de DMARC {#check-subdomains-for-dmarc}

Para asegurarse de que tiene un registro DMARC configurado para todos los subdominios que ha delegado en [!DNL Journey Optimizer], seguir los pasos siguientes.

1. Acceda al **[!UICONTROL menú Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL configuración]** de ]**correo electrónico >**[!UICONTROL  subdominios y, a continuación, haga clic en **[!UICONTROL Configurar subdominio]**.

1. Para cada subdominio delegado, compruebe la **[!UICONTROL columna Registro]** DMARC. Si no se encuentra ningún registro para un subdominio determinado, se elimina la reproducción de la alerta.

   ![](assets/dmarc-record-alert.png)

   >[!CAUTION]
   >
   >Para cumplir con el nuevo requisito de Gmail y Yahoo!, y evitar problemas de entrega con los principales ISP, se recomienda configurar el registro DMARC para todos los subdominios delegados. [Más información](dmarc-record-update.md)

1. Seleccione un subdominio sin registro de DMARC asociado y rellene la sección **[!UICONTROL registro de DMARC]** según las necesidades de su organización. Los pasos para rellenar los campos de registro de DMARC se detallan en [esta sección](#implement-dmarc).

   <!--![](assets/dmarc-record-edit-full.png)-->

   >[!NOTE]
   >
   >Dependiendo de si se encuentra un registro de DMARC con el dominio principal o no, puede elegir utilizar los valores del dominio principal o hacer que Adobe administre el registro de DMARC. [Más información](#implement-dmarc)

1. Si está editando un subdominio:

   * [Totalmente delegado](delegate-subdomain.md#full-subdomain-delegation) a Adobe Systems, no se requiere ninguna otra acción.

   * Al configurar con [CNAME,](delegate-subdomain.md#cname-subdomain-delegation) debe copiar el registro DNS para DMARC en su solución de hospedaje para generar los registros DNS coincidentes.

     ![](assets/dmarc-record-edit-cname.png)

     Asegúrese de que el registro DNS se ha generado en su solución de alojamiento de dominio y marque la casilla &quot;Confirmo...&quot;.

1. Guarde los cambios.

### Configuración de DMARC para nuevos subdominios {#set-up-dmarc}

Al delegar nuevos subdominios a Adobe Systems en [!DNL Journey Optimizer], se creará un registro DMARC en DNS para su dominio. Siga los pasos a continuación para implementar DMARC.

>[!CAUTION]
>
>Para cumplir con el nuevo requisito de Gmail y Yahoo!, y evitar problemas de envío con los principales ISP, se recomienda configurar el registro de DMARC para todos los subdominios delegados. [Más información](dmarc-record-update.md)

<!--If you fail to comply with the new requirement from Gmail and Yahoo! to have DMARC record for all sending domains, your emails are expected to land into the spam folder or to get blocked.-->

1. Configure un nuevo subdominio. [Descubra cómo](delegate-subdomain.md)

1. Vaya a la sección **[!UICONTROL registro de DMARC]**.

1. Si hay un registro DMARC disponible en el dominio principal asociado al subdominio, se muestran dos opciones:

   ![](assets/dmarc-record-found.png)

   * **[!UICONTROL Administrar con Adobe Systems]**: Puede tener Adobe Systems administrar el registro DMARC para su subdominio. Siga los pasos detallados en [esta sección](#manage-dmarc-with-adobe).

   * **[!UICONTROL Administrar por su cuenta]**: <!--This option is selected by default.-->Esta opción le permite administrar el registro DMARC fuera de [!DNL Journey Optimizer], utilizando los valores de su dominio principal. Estos valores se muestran en la interfaz, pero no puede editarlos.

     ![](assets/dmarc-record-found-own.png){width="80%"}

1. Si no se encuentra ningún registro de DMARC en el dominio principal, solo está disponible la opción **[!UICONTROL Administrar con Adobe]**. Siga los pasos [debajo de](#manage-dmarc-with-adobe) para configurar el registro de DMARC para su subdominio.

   ![](assets/dmarc-record-not-found.png){width="80%"}

### Administración de registros de DMARC con Adobe {#manage-dmarc-with-adobe}

Para permitir que Adobe Systems administrar el registro DMARC por usted, seleccione la **[!UICONTROL opción Administrar con Adobe Systems]** y seguir los pasos que se indican a continuación.

>[!NOTE]
>
>Si lo recupera [!DNL Journey Optimizer], puede usar los mismos valores resaltados en la interfaz o cambiarlos según necesite.

![](assets/dmarc-record-with-adobe-ex.png){width="80%"}

>[!NOTE]
>
>Si no agrega ningún valor, se utilizarán los valores predeterminados precompletados.

1. Defina la acción que realizará el servidor destinatario si DMARC falla. En función de la [directiva](#dmarc-policies) DMARC que desee aplicar, seleccione una de las tres opciones:

   * **[!UICONTROL Ninguno]** (valor predeterminado): indica al receptor que no realice ninguna acción contra los mensajes que no superan la autenticación DMARC, pero que aún envían correo electrónico informes al remitente.
   * **[!UICONTROL Cuarentena]**: le dice al servidor de correo electrónico receptor que cuarentena correo electrónico que falle la autenticación DMARC, esto generalmente significa colocar esos mensajes en la carpeta de correo no deseado o basura del destinatario.
   * **[!UICONTROL Rechazar]**: indica al receptor que deniegue completamente (rebote) cualquier correo electrónico del dominio en el que se produzca un error en la autenticación. Con esta directiva habilitada, solo correo electrónico que se verifique como 100% autenticada por su dominio igualado tendrá la oportunidad de bandeja de entrada ubicación.

   >[!NOTE]
   >
   >Como práctica recomendada, se recomienda implementar lentamente DMARC implementación escalando su directiva DMARC de **Ninguno**, a **Cuarentena**, a Rechazar a **medida** que comprende el impacto potencial de DMARC.

1. Opcionalmente, agregue una o más direcciones de correo electrónico de su elección para indicar dónde **debe ir dentro de su organización los informes** de DMARC sobre correos electrónicos en los que [se producen errores en la autenticación](#how-dmarc-works) . Puede agregar hasta cinco direcciones para cada informe.

   >[!NOTE]
   >
   >Asegúrese de que dispone de una bandeja de entrada original (no de Adobe) en el control donde puede recibir dichos informes.

   Los ISP generan dos informes diferentes que los remitentes pueden recibir a través de las etiquetas RUA/RUF en su directiva de DMARC:

   * **Informes agregados** (RUA): no contienen ninguna PII (información de identificación personal) que pueda ser confidencial con respecto al RGPD.
   * **Informes** forenses de fallos (RUF): contienen direcciones correo electrónico sensibles al RGPD. Antes de usarlo, verifique internamente cómo manejar la información que debe ser compatible con RGPD.

   >[!NOTE]
   >
   >Estos informes altamente técnicos proporcionan una visión general de los correos electrónicos que se intentan suplantar. Se digieren mejor a través de una herramienta terceros.

1. Seleccione el **porcentaje** de correos electrónicos aplicable para DMARC.

   Este porcentaje depende de su confianza en su infraestructura correo electrónico y de la tolerancia a los falsos positivos (correos electrónicos legítimos marcados como fraudulentos). Es común que las organizaciones empiecen con la directiva de DMARC establecida en **None**, aumenten gradualmente el porcentaje de directiva de DMARC y supervisen de cerca el impacto en la entrega de correo electrónico legítimo.

   >[!NOTE]
   >
   >Trabaje con los administradores de correo electrónico y el equipo de TI para aumentar gradualmente el porcentaje a medida que vaya ganando confianza en las prácticas de autenticación de correo electrónico.

   Como práctica recomendada, establezca una tasa de conformidad con DMARC alta, idealmente cercana al 100 %, para maximizar los beneficios de seguridad y minimizar el riesgo de falsos positivos.

1. Seleccione un **intervalo de informe** entre 24 y 168 horas. Permite a los propietarios de dominios recibir actualizaciones periódicas sobre los resultados de correo electrónico autenticación y tomar las medidas necesarias para mejorar la seguridad correo electrónico.

<!--The DMARC reporting interval is specified in the DMARC policy published in the DNS (Domain Name System) records for a domain. The reporting interval can be set to daily, weekly, or another specified frequency, depending on the domain owner's preferences.

The default value (24 hours) is generally the email providers' expectation.

**********

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
