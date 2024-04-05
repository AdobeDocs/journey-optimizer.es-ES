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
exl-id: 15b10a61-6ecd-4ffa-b1c2-21e862263f6d
source-git-commit: 61bd9ce680c56b0eb8737804fb013dbad430f1cc
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 100%

---

# Cumplir con el nuevo requisito de DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Más información sobre la actualización obligatoria de DMARC"
>abstract="Como parte del cumplimiento de las prácticas recomendadas del sector, Google y Yahoo requerirán que se tenga un **registro DMARC** para cualquier dominio que se utilice para enviarles un correo electrónico, a partir del **1 de febrero de 2024**.<br>Por lo tanto, asegúrese de tener configurado el registro DMARC para todos los subdominios que ha delegado en Adobe en Journey Optimizer."

La autenticación de mensajes basada en dominios, sistemas de informes y conformidad (DMARC) es un método de autenticación por correo electrónico que permite a los propietarios de dominios proteger su dominio contra el uso no autorizado. Al ofrecer una política clara a los proveedores de correo electrónico/ISP, ayuda a evitar que actores maliciosos envíen correos electrónicos que afirman ser de su dominio. La implementación de DMARC reduce el riesgo de que los correos electrónicos legítimos se marquen como correo no deseado o se rechacen y mejora su entregabilidad

Como parte del cumplimiento de las prácticas recomendadas del sector, Google y Yahoo! exigen el **registro DMARC** para cualquier dominio que se utilice para enviarles correos electrónicos. Este nuevo requisito se aplica desde el **1 de febrero de 2024**. 

>[!CAUTION]
>
>Se espera que el incumplimiento de este nuevo requisito de Gmail y Yahoo! provoque que los correos electrónicos acaben en la carpeta de spam o sean bloqueados.

Por consiguiente, Adobe le recomienda encarecidamente que se asegure de tener configurado el registro DMARC para todos los subdominios que haya delegado a Adobe en [!DNL Journey Optimizer].  Siga estos pasos que se aplican a su caso:

* Si ha [delegado completamente](delegate-subdomain.md#full-subdomain-delegation) sus subdominios a Adobe, elija una de las siguientes opciones:

   * Configure DMARC en el dominio principal de los subdominios delegados **en su solución de alojamiento**.
o
   * Configure DMARC en los subdominios delegados **en la interfaz de usuario de configuración de[!DNL Journey Optimizer]**: sin trabajo adicional en su solución de alojamiento. [Descubra cómo](dmarc-record.md#implement-dmarc)

* Si ha configurado los subdominios de envío con [CNAME](delegate-subdomain.md#cname-subdomain-delegation), siga una de estas opciones:

   * Configure DMARC en los subdominios o en el dominio principal de los subdominios **en su solución de alojamiento**.
o
   * Configure DMARC en los subdominios delegados **en la interfaz de usuario de configuración de[!DNL Journey Optimizer]**. [Descubra cómo](dmarc-record.md#implement-dmarc)

  >[!IMPORTANT]
  >
  >Sin embargo, la configuración CNAME también requiere algunas entradas adicionales en la solución de alojamiento. Por lo tanto, asegúrese de coordinar con su departamento de TI para que puedan realizar la actualización detallada en [esta sección](dmarc-record.md#implement-dmarc).

Las cronologías más recientes compartidas por Google y Yahoo son las siguientes:

* Google:

   * **Febrero de 2024**: se iniciarán los rechazos temporales para advertir del incumplimiento. Los correos electrónicos se seguirán enviando con normalidad después de un breve retraso si aún no cumple los requisitos. Si cumple totalmente los requisitos, no habrá rechazos temporales y no se verá afectado.

   * **Abril de 2024**: comenzarán los bloqueos para los remitentes que no cumplan con el requisito DMARC. Al principio, solo se bloqueará una parte del correo electrónico no conforme y el porcentaje de correos electrónicos bloqueados aumentará con el tiempo.

   * **1 de junio de 2024**: cualquier remitente que no cumpla totalmente los requisitos experimentará un bloqueo.

* Yahoo no ha proporcionado fechas exactas, pero ha dicho que “el despliegue de la implementación comenzará en febrero de 2024. La aplicación se implantará gradualmente”.

>[!NOTE]
>
>Si tiene alguna pregunta o necesita ayuda, póngase en contacto con su consultor del equipo de entregabilidad de Adobe o con su representante de Adobe.

**Vínculos útiles**

* Obtenga más información sobre DMARC en la [Guía de prácticas recomendadas sobre la entregabilidad](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=es#about){target="_blank"}
* Lea el [anuncio de Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Lea [ el anuncio de Yahoo!](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
