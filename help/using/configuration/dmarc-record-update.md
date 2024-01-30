---
solution: Journey Optimizer
product: journey optimizer
title: Cumplir con el nuevo requisito de DMARC
description: Descubra por qué y cuándo debe establecer el registro DMARC en Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdominio, dominio, correo, dmarc, registro
source-git-commit: 11d42198436319cebb67446527e9fd8d0f80cfbc
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 6%

---

# Cumplir con el nuevo requisito de DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Más información sobre la actualización obligatoria de DMARC"
>abstract="Como parte de las prácticas recomendadas del sector, Google y Yahoo requerirán que tenga un **Registro DMARC** para cualquier dominio que utilice para enviarles correo electrónico, a partir del **1 de febrero de 2024**.<br>Por lo tanto, asegúrese de tener configurado el registro DMARC para todos los subdominios que ha delegado en Adobe en Journey Optimizer."

Autenticación de mensajes, creación de informes y conformidad basados en dominio (DMARC) es un método de autenticación por correo electrónico que permite a los propietarios de dominios proteger su dominio contra el uso no autorizado. Al ofrecer una política clara a los proveedores de correo electrónico/ISP, ayuda a evitar que actores maliciosos envíen correos electrónicos que afirman ser de su dominio. La implementación de DMARC reduce el riesgo de que los correos electrónicos legítimos se marquen como correo no deseado o se rechacen, y mejora la capacidad de envío de correos electrónicos.


Como parte de las prácticas recomendadas del sector, Google y Yahoo! exigen que un **Registro DMARC** para cualquier dominio que utilice para enviarles correos electrónicos. Este nuevo requisito se aplica a partir de **1 de febrero de 2024**. [Más información](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html#dmarc){target="_blank"}

>[!CAUTION]
>
>No cumplir con este nuevo requisito de Gmail y Yahoo! se espera que el resultado sea que los correos electrónicos lleguen a la carpeta de correo no deseado o que se bloqueen.

Por lo tanto, Adobe recomienda encarecidamente que se asegure de que tiene configurado el registro DMARC para todos los subdominios que ha delegado en Adobe en [!DNL Journey Optimizer]. Siga los pasos a continuación que se aplican a su caso:

* Si tiene [totalmente delegado](delegate-subdomain.md#full-subdomain-delegation) Para enviar subdominios al Adobe, siga una de las opciones a continuación:

   * Configure DMARC en el dominio principal de los subdominios delegados **en su solución de alojamiento**.
o
   * Configuración de DMARC en los subdominios delegados **en el[!DNL Journey Optimizer]** interfaz de usuario de configuración: sin trabajo adicional en su solución de alojamiento. [Descubra cómo](dmarc-record.md#implement-dmarc)

* Si ha configurado los subdominios de envío con [CNAME](delegate-subdomain.md#cname-subdomain-delegation), siga una de las opciones siguientes:

   * Configure DMARC en los subdominios o en el dominio principal de los subdominios **en su solución de alojamiento**.
o
   * Configuración de DMARC en los subdominios delegados **en el[!DNL Journey Optimizer]** interfaz de usuario de configuración. [Descubra cómo](dmarc-record.md#implement-dmarc)

     Sin embargo, con la delegación CNAME, también se requerirá la entrada en la solución de alojamiento. Por lo tanto, asegúrese de coordinarse con su departamento de TI para que pueda realizar la actualización en cuanto el [!DNL Journey Optimizer] Esta función está disponible (el 30 de enero). [Más información](dmarc-record.md#implement-dmarc)

**A partir del 30 de enero tendrá a su disposición una interfaz de autoservicio para la implementación de DMARC. Obtenga más información en [esta sección](dmarc-record.md#implement-dmarc).**

Las escalas de tiempo más recientes compartidas por Google y Yahoo son las siguientes:

* Google:

   * **Febrero de 2024** - Se iniciarán las devoluciones temporales diseñadas para advertir del incumplimiento. Los correos electrónicos se enviarán con normalidad después de un breve retraso si aún no cumple los requisitos. Si cumple totalmente los requisitos, no habrá devoluciones temporales y no se verá afectado.

   * **Abril de 2024** - Los bloques comenzarán para los remitentes que no cumplan con el requisito DMARC. Al principio, solo se bloqueará una parte del correo electrónico no conforme y el porcentaje de correos electrónicos bloqueados aumentará con el tiempo.

   * **1 de junio de 2024** : Cualquier remitente que no cumpla totalmente los requisitos experimentará un bloqueo.

* Yahoo no ha proporcionado fechas exactas, pero ha dicho que &quot;el despliegue de la aplicación comenzará en febrero de 2024. La aplicación se implantará gradualmente&quot;.

>[!NOTE]
>
>Si tiene alguna pregunta o necesita asistencia, póngase en contacto con su consultor de capacidad de envío de Adobes o con su representante del Adobe.

**Vínculos útiles**

* Obtenga más información sobre DMARC en la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"}
* Encuentre más orientación acerca de estos cambios en la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html){target="_blank"}
* Leer más [Anuncio de Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Leer más [Yahoo! anuncio](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}
