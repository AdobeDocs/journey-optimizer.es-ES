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
hide: true
hidefromtoc: true
source-git-commit: b67b53b7a3ea6d2daee223a5579696d0e5637c44
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Actualización obligatoria de DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Obtenga más información sobre la actualización obligatoria de DMARC"
>abstract="Como parte de las prácticas recomendadas del sector, Google y Yahoo requerirán que tenga un **Registro DMARC** para cualquier dominio que utilice para enviarles correo electrónico, a partir del **1 de febrero de 2024**. <br>Por lo tanto, debe asegurarse de tener configurado el registro DMARC para todos los subdominios que ha delegado en Adobe en Journey Optimizer."

Como parte de las prácticas recomendadas del sector, Google y Yahoo requerirán que tenga un **Registro DMARC** para cualquier dominio que utilice para enviarles correos electrónicos. Este nuevo requisito comienza el **1 de febrero de 2024**.

Obtenga más información sobre los requisitos de Google y Yahoo en [esta sección](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Si no se cumple este nuevo requisito de Gmail y Yahoo, se espera que el resultado sea que los correos electrónicos lleguen a la carpeta de correo no deseado o que se bloqueen.

Por lo tanto, Adobe recomienda encarecidamente que se asegure de que tiene configurado el registro DMARC para todos los subdominios que ha delegado en Adobe en [!DNL Journey Optimizer]. Siga los pasos a continuación que se aplican a su caso:

<!--
* Set up DMARC on your subdomains, or on the parent domain of your subdomains, **in your hosting solution**. You can do it as of now.

* Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI** - with no extra work on your hosting solution. This feature will be available on January 30, 2024.

    >[!CAUTION]
    >
    >If you have set up [CNAME delegation](delegate-subdomain.md#cname-subdomain-delegation) for your sending subdomains, it will also require some entry into your hosting solution. Make sure you coordinate with your IT department so that they can perform the update as soon as the [!DNL Journey Optimizer] feature is available (on January 30, 2024). (and be ready on February 1st, 2024)

    More details on the [!DNL Journey Optimizer] DMARC upcoming feature will come soon.
-->

* Si tiene [totalmente delegado](delegate-subdomain.md#full-subdomain-delegation) Para enviar subdominios al Adobe, siga una de las dos opciones a continuación:

   * Configure DMARC en el dominio principal de los subdominios delegados **en su solución de alojamiento**.

   * Configuración de DMARC en los subdominios delegados **uso de la próxima función de [!DNL Journey Optimizer] IU de administración** - sin trabajo adicional en su solución de alojamiento.

* Si ha configurado [Delegación CNAME](delegate-subdomain.md#cname-subdomain-delegation) para los subdominios de envío, siga una de las dos opciones a continuación:
   * Configure DMARC en los subdominios o en el dominio principal de los subdominios **en su solución de alojamiento**.
   * Configuración de DMARC en los subdominios delegados **uso de la próxima función de [!DNL Journey Optimizer] IU de administración**. Sin embargo, también requerirá la entrada en su solución de alojamiento. Por lo tanto, asegúrese de coordinarse con su departamento de TI para que pueda realizar la actualización en cuanto el [!DNL Journey Optimizer] Esta función está disponible (el 30 de enero). <!--and be ready on February 1st, 2024-->

Más detalles sobre la [!DNL Journey Optimizer] La próxima función de DMARC llegará pronto.

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
>Obtenga más información sobre la implementación de DMARC en la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} para comprender mejor el impacto en la capacidad de envío de correo electrónico.
