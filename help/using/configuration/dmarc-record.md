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
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Registro DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Definición del registro DMARC"
>abstract="Establezca el registro DMARC para evitar problemas de envío con los ISP"

>[!CAUTION]
>
>Tras los recientes anuncios de Gmail y Yahoo para remitentes masivos, Journey Optimizer ahora es compatible con la tecnología de autenticación DMARC. //Debe actualizar todos los subdominios que ya ha creado en la instancia para incluir la compatibilidad con DMARC.//

Es importante hacerlo para el 1 de febrero. Doc llegará pronto.

Comienza el

Tiene dos opciones:

* Hágalo por su cuenta a partir de ahora: configúrelo con su departamento de TI cuando desee

* Hazlo en AJO, pero en ese caso tendrás que esperar hasta el 30 de enero

   * Delegación completa: puede hacerlo el 30 de enero (versión de AJO)

   * CNAME planifíquelo con su departamento de TI para que no tarde mucho tiempo, pero tiene que planificarlo

Como parte de las prácticas recomendadas en el sector, Google y Yahoo requerirán que tenga un registro DMARC para cualquier dominio que utilice para enviarles correo electrónico. Este nuevo requisito comienza el **1 de febrero de 2024**.

Obtenga más información sobre los requisitos de Google y Yahoo para el registro DMARC en [esta sección](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Obtenga más información sobre los cambios anunciados en Google y Yahoo en [esta página](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

DMARC, que significa **Autenticación de mensajes, creación de informes y conformidad basados en dominio**, es un protocolo de autenticación de correo electrónico que le ayuda a protegerse contra la suplantación de correo electrónico, el phishing y otras actividades fraudulentas.

* Autenticación de correo electrónico:

   * SPF (Marco de Política del Remitente): DMARC se basa en SPF para autenticar la identidad del servidor de correo remitente. SPF ayuda a verificar que el mensaje de correo electrónico proviene de una fuente autorizada comprobando la dirección IP del servidor remitente con una lista de direcciones IP autorizadas para el dominio.
   * DKIM (DomainKeys Identified Mail): DMARC también utiliza DKIM para añadir una firma digital a los mensajes de correo electrónico, lo que permite al destinatario verificar la integridad y autenticidad del mensaje.

* DMARC ayuda a evitar que actores maliciosos envíen correos electrónicos que parecen provenir de su dominio. Al configurar DMARC, puede especificar cómo deben gestionar los proveedores de correo electrónico los mensajes que no superan las comprobaciones de autenticación, lo que reduce la probabilidad de que los correos electrónicos de phishing lleguen a los destinatarios.

* DMARC ayuda a mejorar la capacidad de envío de correos electrónicos al proporcionar una política clara para que los proveedores de correo electrónico la sigan cuando encuentren mensajes que aleguen ser de su dominio. Esto puede reducir las posibilidades de que los correos electrónicos legítimos se marquen como correo no deseado o se rechacen.

* Al implementar DMARC, puede proteger la reputación de su marca asegurándose de que las partes no autorizadas no puedan abusar de su dominio para realizar phishing u otras actividades maliciosas. Esto es especialmente importante para las empresas y organizaciones que dependen de la comunicación por correo electrónico con clientes y socios.

La configuración de un registro DMARC implica agregar un registro TXT DNS a la configuración DNS del dominio. Este registro especifica la directiva DMARC, como si se deben poner en cuarentena o rechazar los mensajes que no superan la autenticación. La implementación de DMARC es un paso proactivo para mejorar la seguridad del correo electrónico y proteger tanto a su organización como a sus destinatarios de las amenazas basadas en el correo electrónico.

[Obtenga más información sobre DMARC en la Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=es){target="_blank"} para comprender mejor el impacto de DMARC en la capacidad de envío de correo electrónico.

Si no añade DMARC, se le pondrá en cuarentena (al menos).

asegúrese de tener una bandeja de entrada original donde pueda recibir mensajes en el control: administra esta bandeja de entrada (no debe ser la bandeja de entrada de Adobe)

La recomendación es 24 porque generalmente si es menor, evalúe su capacidad / compruebe su > chat GPT

Google y Yahoo, y probablemente todos los demás ISP principales

para CNAME en el flujo de edición, debe volver a descargar el archivo CSV (no para delegación completa).

nuevo registro DMARC

En RN > anteponga. Todos los subdominios deben actualizarse con compatibilidad con DMARC



