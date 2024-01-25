---
solution: Journey Optimizer
product: journey optimizer
title: Registro DMARC
description: Obtenga información sobre cómo establecer el registro DMARC en Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: subdominio, dominio, correo, dmarc, registro
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 5%

---

# Registro DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Establecer el registro DMARC"
>abstract="Establezca el registro DMARC para evitar problemas de entregabilidad con los ISP. Como parte del cumplimiento de las prácticas recomendadas en el sector, Google y Yahoo requieren que tenga un registro DMARC para cualquier dominio que utilice para enviarles correo electrónico."

>[!CAUTION]
>
>Tras los recientes anuncios de Gmail y Yahoo para remitentes masivos, Journey Optimizer ahora es compatible con la tecnología de autenticación DMARC.

<!--TO ADD TO AJO HOME PAGE (first tab)

>[!TAB Mandatory DMARC update]

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them, starting on **February 1st, 2024**. Make sure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in Journey Optimizer.

[![image](using/assets/do-not-localize/learn-more-button.svg)](using/configuration/dmarc-record-update.md)
-->

Como parte de las prácticas recomendadas del sector, Google y Yahoo requerirán que tenga un **Registro DMARC** para cualquier dominio que utilice para enviarles correos electrónicos. Este nuevo requisito comienza el **1 de febrero de 2024**.

Obtenga más información sobre los requisitos de Google y Yahoo en [esta sección](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Si no se cumple este nuevo requisito de Gmail y Yahoo, se espera que el resultado sea que los correos electrónicos lleguen a la carpeta de correo no deseado o que se bloqueen.

Por lo tanto, Adobe recomienda encarecidamente que se asegure de que tiene configurado el registro DMARC para todos los subdominios que ha delegado en Adobe en [!DNL Journey Optimizer]. Siga los pasos a continuación que se aplican a su caso:

* Si tiene [totalmente delegado](delegate-subdomain.md#full-subdomain-delegation) Para enviar subdominios al Adobe, siga una de las dos opciones a continuación:

   * Configure DMARC en el dominio principal de los subdominios delegados **en su solución de alojamiento**.

   * Configuración de DMARC en los subdominios delegados **uso de la próxima función de [!DNL Journey Optimizer] IU de administración** - sin trabajo adicional en su solución de alojamiento.

* Si ha configurado [Delegación CNAME](delegate-subdomain.md#cname-subdomain-delegation) para los subdominios de envío, siga una de las dos opciones a continuación:

   * Configure DMARC en los subdominios o en el dominio principal de los subdominios **en su solución de alojamiento**.

   * Configuración de DMARC en los subdominios delegados **uso de la próxima función de [!DNL Journey Optimizer] IU de administración**. Sin embargo, también requerirá la entrada en su solución de alojamiento. Por lo tanto, asegúrese de coordinarse con su departamento de TI para que pueda realizar la actualización en cuanto el [!DNL Journey Optimizer] Esta función está disponible (el 30 de enero). <!--and be ready on February 1st, 2024-->

**Más detalles sobre la [!DNL Journey Optimizer] La próxima función de DMARC llegará pronto.**

>[!NOTE]
>
>Obtenga más información sobre la implementación de DMARC en la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} para comprender mejor el impacto en la capacidad de envío de correo electrónico.

## ¿Qué es DMARC?

DMARC, que significa **Autenticación de mensajes, creación de informes y conformidad basados en dominio**, es un método o protocolo de autenticación de correo electrónico que permite a los propietarios de dominio proteger su dominio de un uso no autorizado.

Ofrece una forma de autenticar el dominio del remitente y ayuda a evitar que agentes maliciosos envíen correos electrónicos que parecen provenir de su dominio.

DMARC también proporciona comentarios sobre el estado de autenticación de correo electrónico y permite a los remitentes controlar qué sucede con los correos electrónicos que no se autentican correctamente. Esto incluye opciones para monitorizar, poner en cuarentena o rechazar correo según la política DMARC que se haya implementado.

<!--Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.-->

DMARC tiene tres opciones de directiva:

* Monitor (p=none): indica al proveedor del buzón/ISP que haga lo que normalmente haría con el mensaje.
* Cuarentena (p=quarantine): indica al proveedor del buzón/ISP que envíe el correo que no pasa DMARC a la carpeta de correo no deseado o correo no deseado del destinatario.
* Reject (p=reject): indica al proveedor/ISP del buzón que bloquee el correo que no pasa DMARC, lo que provoca un rechazo.

## ¿Cómo funciona DMARC?

SPF y DKIM se utilizan para asociar un correo electrónico con un dominio y trabajar juntos para autenticar el correo electrónico. DMARC lleva esto un paso más allá y ayuda a evitar la suplantación de identidad haciendo coincidir el dominio comprobado por DKIM y SPF. Para pasar DMARC, un mensaje debe pasar SPF o DKIM. Si ambas fallan en la autenticación, DMARC fallará y el correo electrónico se enviará según la política DMARC seleccionada.

* SPF (Marco de Política del Remitente): DMARC se basa en SPF para autenticar la identidad del servidor de correo remitente. SPF ayuda a verificar que el mensaje de correo electrónico proviene de una fuente autorizada comprobando la dirección IP del servidor remitente con una lista de direcciones IP autorizadas para el dominio.
* DKIM (DomainKeys Identified Mail): DMARC también utiliza DKIM para añadir una firma digital a los mensajes de correo electrónico, lo que permite al destinatario verificar la integridad y autenticidad del mensaje.

>[!NOTE]
>
>DMARC requiere la alineación entre las direcciones &quot;De&quot; y &quot;Return-Path&quot;.


<!--

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

-->


## Implementación de DMARC {#implement-dmarc}

Para implementar DMARC, siga los pasos a continuación que se aplican a su caso.

* Si no añade DMARC, se le pondrá en cuarentena (al menos).

### Subdominios totalmente delegados

Establezca la acción que realizará el servidor de destinatario si DMARC falla.

DMARC tiene tres opciones de directiva:

* Monitor (p=none): indica al proveedor del buzón/ISP que haga lo que normalmente haría con el mensaje. Este es el valor predeterminado.
* Cuarentena (p=quarantine): indica al proveedor del buzón/ISP que envíe el correo que no pasa DMARC a la carpeta de correo no deseado o correo no deseado del destinatario.
* Reject (p=reject): indica al proveedor/ISP del buzón que bloquee el correo que no pasa DMARC, lo que provoca un rechazo.

Correos electrónicos para recibir informes agregados de DMARC e informes forenses de errores de DMARC: puede añadir hasta 5 direcciones.

* Asegúrese de tener una bandeja de entrada original donde pueda recibir en el control: administra esta bandeja de entrada (no debe ser la bandeja de entrada de Adobe)

Porcentaje aplicable de correos electrónicos para aplicar DMARC:

Intervalo de creación de informes: la recomendación es 24 porque, por lo general, esto es lo que tienen los ISP.
si es menor, evalúe su capacidad / compruebe su > chat GPT

Si se detecta un registro DMARC, puede copiar y pegar los mismos valores que se enumeran o cambiarlos si es necesario.

Si no coloca nada, se utilizarán los valores predeterminados.

### Subdominios delegados mediante CNAME

para CNAME en el flujo de edición, debe volver a descargar el archivo CSV (no para delegación completa)





