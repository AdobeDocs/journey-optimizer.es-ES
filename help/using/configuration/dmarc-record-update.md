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
hide: true
hidefromtoc: true
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# Actualización importante del registro DMARC{#dmarc-record}


>[!CAUTION]
>
>Tras los recientes anuncios de Gmail y Yahoo para remitentes masivos, Journey Optimizer ahora es compatible con la tecnología de autenticación DMARC.

Como parte de las prácticas recomendadas en el sector, Google y Yahoo requerirán que tenga un registro DMARC para cualquier dominio que utilice para enviarles correo electrónico. Este nuevo requisito comienza el **1 de febrero de 2024**.

Obtenga más información sobre los requisitos de Google y Yahoo para el registro DMARC en [esta sección](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Obtenga más información sobre los cambios anunciados en Google y Yahoo en [esta página](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

A continuación, tendrá una acción o pasos siguientes para la sección que indicará:

Debe configurarlo para todos los subdominios.
* Si ha delegado completamente el dominio a nosotros, tiene dos opciones
   * Configure DMARC en el dominio principal del dominio delegado en su solución de alojamiento, O
   * Configure DMARC en un dominio delegado con nuestra próxima función en la IU de administración sin trabajar en la solución de alojamiento
* Si ha configurado CNAME para los dominios de envío, tiene dos opciones
   * Configure DMARC en el subdominio O dominio principal del subdominio en la solución de alojamiento, O
   * Configure DMARC con nuestra próxima función en la IU de administración. Sin embargo, requerirá no solo nuestra interfaz de usuario, sino también la entrada en la solución de alojamiento.

Próximamente, obtendrá más información sobre nuestra próxima función.

Además, puede incluir el impacto si no se configura copiando la sección correspondiente a DMARC de la sección siguiente (copiada del vínculo anterior). Ahora, o sacamos sólo cosas relacionadas con DMARC. O bien, aquí puede explicar que el anuncio es para DMARC y un clic para su cancelación de suscripción, y aquí está la última información sobre los plazos para ambas funciones.

Se han recibido actualizaciones de los plazos desde el anuncio original en octubre.

Las escalas de tiempo más recientes tienen este aspecto:

Gmail:

* Febrero de 2024: Empezarán las devoluciones temporales diseñadas para advertir del incumplimiento. Los correos electrónicos se enviarán con normalidad después de un breve retraso si aún no cumple los requisitos. Si cumple totalmente con las normas, no habrá devoluciones temporales y no notará nada.
* Abril de 2024: los bloques comenzarán para los remitentes que no cumplan con todo, excepto List-Unsubscribe 1-Click. Al principio, solo se bloqueará una parte del correo electrónico no conforme y el % bloqueado aumentará con el tiempo.
* 1 de junio de 2024: Cualquier remitente que no cumpla totalmente los requisitos, incluida la cancelación de la suscripción a una lista con un clic, experimentará un bloqueo.

Yahoo:

No ha proporcionado fechas exactas, pero ha dicho que &quot;el despliegue de la aplicación comenzará en febrero de 2024. La aplicación se implantará gradualmente&quot;.
