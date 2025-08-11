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
source-git-commit: 8b755351e25ecae9a2058e63919d6512ea0bf153
workflow-type: ht
source-wordcount: '431'
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

* Si ha configurado los subdominios de envío con [CNAME](delegate-subdomain.md#cname-subdomain-setup), siga una de estas opciones:

   * Configure DMARC en los subdominios o en el dominio principal de los subdominios **en su solución de alojamiento**.
o
   * Configure DMARC en los subdominios delegados **en la interfaz de usuario de configuración de[!DNL Journey Optimizer]**. [Descubra cómo](dmarc-record.md#implement-dmarc)

  Sin embargo, la configuración CNAME también requiere algunas entradas adicionales en la solución de alojamiento. Por lo tanto, asegúrese de coordinar con su departamento de TI para que puedan realizar la actualización detallada en [esta sección](dmarc-record.md#implement-dmarc).

<!--The most recent timelines shared by Google and Yahoo! are as follows:

* Google:

    * **February 2024** – Temporary bounces designed to provide warning of non-compliance will begin. Emails will still be delivered as normal after a short delay if you are not yet in compliance. If you are fully in compliance there will be no temporary bounces and you will not be affected.

    * **April 2024** – Blocks will begin for senders who are not in compliance with DMARC requirement. Only a portion of non-compliant email will be blocked at first, with the percentage blocked increasing over time.

    * **June 1st, 2024** – Any sender not in full compliance will experience blocking.

* Yahoo! has not provided exact dates, but has said "the rollout of enforcement will begin in February 2024. Enforcement will be gradually rolled out".
-->

>[!NOTE]
>
>Si tiene alguna pregunta o necesita ayuda, póngase en contacto con su consultor del equipo de entregabilidad de Adobe o con su representante de Adobe.

**Vínculos útiles**

* Obtenga más información sobre DMARC en la [Guía de prácticas recomendadas sobre la entregabilidad](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=es#about){target="_blank"}.
* Lea el [anuncio de Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}.
* Lea el [anuncio de Yahoo! ](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
