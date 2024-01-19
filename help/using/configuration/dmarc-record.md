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
source-git-commit: f9d3234a64ad659660c2d2c4ad24ab5c240cb857
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Registro DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Definición del registro DMARC"
>abstract="Establezca el registro DMARC para evitar problemas de envío con los ISP. Como parte de las prácticas recomendadas en el sector, Google y Yahoo requieren que tenga un registro DMARC para cualquier dominio que utilice para enviarles correo electrónico."

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

Por lo tanto, Adobe recomienda encarecidamente que se asegure de que tiene configurado el registro DMARC para todos los subdominios que ha delegado en Adobe en [!DNL Journey Optimizer]. Siga una de las dos opciones a continuación:

* Configure DMARC en los subdominios o en el dominio principal de los subdominios, **en su solución de alojamiento**.

* Configuración de DMARC en los subdominios delegados **uso de la nueva función en la [!DNL Journey Optimizer] IU de administración** - sin trabajo adicional en su solución de alojamiento. [Más información](#implement-dmarc)

  >[!CAUTION]
  >
  >Si ha configurado [Delegación CNAME](delegate-subdomain.md#cname-subdomain-delegation) para los subdominios de envío, también se requiere alguna entrada en la solución de alojamiento. Asegúrese de coordinar con su departamento de TI para que pueda realizar la actualización tan pronto como el [!DNL Journey Optimizer] Esta función está disponible (el 30 de enero de 2024). <!--and be ready on February 1st, 2024-->

>[!NOTE]
>
>Obtenga más información sobre la implementación de DMARC en la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} para comprender mejor el impacto en la capacidad de envío de correo electrónico.

## ¿Qué es DMARC?

DMARC, que significa **Autenticación de mensajes, creación de informes y conformidad basados en dominio**, es un protocolo de autenticación de correo electrónico que le ayuda a protegerse contra la suplantación de correo electrónico, el phishing y otras actividades fraudulentas.

* Autenticación de correo electrónico:

   * SPF (Marco de Política del Remitente): DMARC se basa en SPF para autenticar la identidad del servidor de correo remitente. SPF ayuda a verificar que el mensaje de correo electrónico proviene de una fuente autorizada comprobando la dirección IP del servidor remitente con una lista de direcciones IP autorizadas para el dominio.
   * DKIM (DomainKeys Identified Mail): DMARC también utiliza DKIM para añadir una firma digital a los mensajes de correo electrónico, lo que permite al destinatario verificar la integridad y autenticidad del mensaje.

* DMARC ayuda a evitar que actores maliciosos envíen correos electrónicos que parecen provenir de su dominio. Al configurar DMARC, puede especificar cómo deben gestionar los proveedores de correo electrónico los mensajes que no superan las comprobaciones de autenticación, lo que reduce la probabilidad de que los correos electrónicos de phishing lleguen a los destinatarios.

* DMARC ayuda a mejorar la capacidad de envío de correos electrónicos al proporcionar una política clara para que los proveedores de correo electrónico la sigan cuando encuentren mensajes que aleguen ser de su dominio. Esto puede reducir las posibilidades de que los correos electrónicos legítimos se marquen como correo no deseado o se rechacen.

* Al implementar DMARC, puede proteger la reputación de su marca asegurándose de que las partes no autorizadas no puedan abusar de su dominio para realizar phishing u otras actividades maliciosas. Esto es especialmente importante para las empresas y organizaciones que dependen de la comunicación por correo electrónico con clientes y socios.

La configuración de un registro DMARC implica agregar un registro TXT DNS a la configuración DNS del dominio. Este registro especifica la directiva DMARC, como si se deben poner en cuarentena o rechazar los mensajes que no superan la autenticación. La implementación de DMARC es un paso proactivo para mejorar la seguridad del correo electrónico y proteger tanto a su organización como a sus destinatarios de las amenazas basadas en el correo electrónico.

## Implementación de DMARC {#implement-dmarc}

* Si no añade DMARC, se le pondrá en cuarentena (al menos).

* Asegúrese de tener una bandeja de entrada original donde pueda recibir en el control: administra esta bandeja de entrada (no debe ser la bandeja de entrada de Adobe)

La recomendación es 24 porque generalmente esto es lo que tienen los ISP.
si es menor, evalúe su capacidad / compruebe su > chat GPT

Si se detecta un registro DMARC, puede copiar y pegar los mismos valores que se enumeran o cambiarlos si es necesario.

Si no coloca nada, se utilizarán los valores predeterminados.

### Subdominios totalmente delegados

### Subdominios delegados mediante CNAME

para CNAME en el flujo de edición, debe volver a descargar el archivo CSV (no para delegación completa)





