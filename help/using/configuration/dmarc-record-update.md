---
solution: Journey Optimizer
product: journey optimizer
title: Actualización obligatoria de DMARC
description: Descubra por qué y cuándo debe establecer el registro DMARC en Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: subdominio, dominio, correo, dmarc, registro
source-git-commit: 49cb9734d66dc1aa2a3531c71a687aac00834d82
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Actualización obligatoria de DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Obtenga más información sobre la actualización obligatoria de DMARC"
>abstract="Como parte de las prácticas recomendadas del sector, Google y Yahoo requerirán que tenga un **Registro DMARC** para cualquier dominio que utilice para enviarles correos electrónicos. Este nuevo requisito comienza el **1 de febrero de 2024**. <br>Por lo tanto, Adobe recomienda encarecidamente que se asegure de que tiene configurado el registro DMARC para todos los subdominios que ha delegado en Adobe en Journey Optimizer."

Como parte de las prácticas recomendadas del sector, Google y Yahoo requerirán que tenga un **Registro DMARC** para cualquier dominio que utilice para enviarles correos electrónicos. Este nuevo requisito comienza el **1 de febrero de 2024**.

>[!CAUTION]
>
>Si no se cumple este nuevo requisito de Gmail y Yahoo, se espera que el resultado sea que los correos electrónicos lleguen a la carpeta de correo no deseado o que se bloqueen.

Obtenga más información sobre los requisitos de Google y Yahoo en [esta sección](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Por lo tanto, Adobe recomienda encarecidamente que se asegure de que tiene configurado el registro DMARC para todos los subdominios que ha delegado en Adobe en [!DNL Journey Optimizer]. Siga una de las dos opciones a continuación:

* Configure DMARC en los subdominios o en el dominio principal de los subdominios, **en su solución de alojamiento**.

* Configuración de DMARC en los subdominios delegados **uso de la próxima función de [!DNL Journey Optimizer] IU de administración** - sin trabajo adicional en su solución de alojamiento.

  >[!WARNING]
  >
  >Si ha configurado [Delegación CNAME](delegate-subdomain.md#cname-subdomain-delegation) para los subdominios de envío, también se requiere alguna entrada en la solución de alojamiento. Asegúrese de coordinar con su departamento de TI para que pueda realizar la actualización tan pronto como el [!DNL Journey Optimizer] Esta función está disponible (el 30 de enero de 2024). <!--and be ready on February 1st, 2024-->

  Más detalles sobre la [!DNL Journey Optimizer] La próxima función de DMARC llegará pronto.

<!--
* If you have [fully delegated](delegate-subdomain.md#full-subdomain-delegation) your sending subdomains to Adobe, follow either one of the two options below:

    * Set up DMARC on your subdomains or on the parent domain of your subdomains **in your hosting solution**.

    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI** - with no extra work on your hosting solution.

* If you have set up [CNAME delegation](delegate-subdomain.md#cname-subdomain-delegation) for your sending subdomains, follow either one of the two options below:
    * Set up DMARC on your subdomains or on the parent domain of your subdomains **in your hosting solution**.
    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI**. However, it will also require entry in your hosting solution. Consequently, make sure you coordinate with your IT department so that they can perform the update as soon as the [!DNL Journey Optimizer] feature is available (on January, 30) - and be ready on February 1st, 2024.
    
-->

>[!NOTE]
>
>Si tiene alguna pregunta o necesita asistencia, póngase en contacto con su consultor de capacidad de envío de Adobes o con su representante del Adobe.

Las escalas de tiempo más recientes compartidas por Google y Yahoo son las siguientes:

* Google:

   * **Febrero de 2024** - Se iniciarán las devoluciones temporales diseñadas para advertir del incumplimiento. Los correos electrónicos se enviarán con normalidad después de un breve retraso si aún no cumple los requisitos. Si cumple totalmente los requisitos, no habrá devoluciones temporales y no se verá afectado.

   * **Abril de 2024** - Los bloques comenzarán para los remitentes que no cumplan con el requisito DMARC. Al principio, solo se bloqueará una parte del correo electrónico no conforme y el porcentaje de correos electrónicos bloqueados aumentará con el tiempo.

   * **1 de junio de 2024** : Cualquier remitente que no cumpla totalmente los requisitos experimentará un bloqueo.

* Yahoo no ha proporcionado fechas exactas, pero ha dicho que &quot;el despliegue de la aplicación comenzará en febrero de 2024. La aplicación se implantará gradualmente&quot;.

>[!NOTE]
>
>Obtenga más información sobre DMARC en la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} para comprender mejor el impacto de la implementación de DMARC en la capacidad de envío de correo electrónico.
