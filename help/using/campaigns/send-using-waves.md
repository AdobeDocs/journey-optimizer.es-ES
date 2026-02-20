---
solution: Journey Optimizer
product: journey optimizer
title: Envío mediante olas
description: Programe los mensajes de campaña salientes para que se entreguen en lotes controlados a lo largo del tiempo. El envío de ondas admite la entrega y ayuda a mantener la reputación del remitente.
feature: Campaigns
topic: Campaign scheduling
role: User
level: Intermediate
keywords: olas, lotes, programación, campaña, recorrido, capacidad de entrega
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 1%

---

# Envío mediante olas en campañas {#send-using-waves}

Puede dividir el envío de mensajes de campaña salientes en varios lotes (olas) y programarlos a lo largo del tiempo. El envío de ondas ayuda a equilibrar la carga, evitar sistemas descendentes abrumadores (como centros de llamadas o páginas de aterrizaje) y admite la capacidad de envío y la reputación del remitente, especialmente para envíos de gran volumen.

<!--
>[!CAUTION]
>
>Wave sending applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

Journey Optimizer permite definir el número de olas, su tamaño (como porcentaje de la audiencia o como números absolutos) y cuándo se ejecuta cada ola.

## Limitaciones y barreras {#limitations-guardrails}

* El envío de ondas solo se aplica a **acciones salientes** (correo electrónico, SMS, push, correo directo).
* Debe definir al menos **2 olas** y puede agregar **10 ondas**.
* El intervalo mínimo entre el inicio de dos olas es de **30 minutos**.
* No se puede iniciar una ola antes del inicio de la campaña o en el pasado.

## Configurar el envío de olas {#configure-wave-sending}

Para configurar cómo y cuándo enviar olas en una campaña, siga los pasos a continuación.

1. Cree o abra una [campaña de acción](create-campaign.md) que contenga una acción saliente (por ejemplo, correo electrónico, SMS, push).

1. En la ficha **[!UICONTROL Programar]** de la campaña, seleccione **[!UICONTROL Enviar acciones de campaña en olas]**.

   ![](assets/campaign-wave-option.png){width="100%"}

   >[!NOTE]
   >
   >La opción **[!UICONTROL Enviar acciones de campaña en olas]** solo se muestra cuando se selecciona una acción saliente en la pestaña **[!UICONTROL Acciones]** de la campaña. [Más información](campaign-action.md)

1. Defina el número de olas que desee enviar (por ejemplo, 4).

   >[!NOTE]
   >
   >Se deben definir al menos 2 olas y se pueden añadir hasta 10.

1. Elija cómo definir el tamaño y el tiempo de la onda como se detalla a continuación.

### Olas iguales {#equal-waves}

De forma predeterminada, la audiencia se divide en olas de igual tamaño. Programe el tiempo para la primera ola y establezca un intervalo fijo entre el inicio de cada ola (por ejemplo, 2 horas).

![](assets/campaign-equal-waves.png){width="80%"}

>[!NOTE]
>
>El intervalo mínimo entre el inicio de dos olas es de **30 minutos**.

A continuación, el sistema programa automáticamente las olas siguientes (por ejemplo, la primera ola a las 9:00 AM, la segunda a las 11:00 AM, la tercera a las 1:00 PM y la cuarta a las 3:00 PM).

### Distribución personalizada {#custom-distribution}

Seleccione la opción **[!UICONTROL Distribución personalizada]** para definir el tamaño de cada ola como un porcentaje de la audiencia total (por ejemplo, 15%, 20%, 25%, 40%).

![](assets/campaign-wave-percentage.png){width="80%"}

>[!NOTE]
>
>El total en todas las olas debe ser igual al 100%. Si no es así, se muestra un mensaje de advertencia.<!--are the waves actually sent or does the system prevent user from saving the campaign?-->

Seleccione **[!UICONTROL Números]** para definir el tamaño de cada ola como un número absoluto de perfiles (por ejemplo, 10 000; 50 000).

![](assets/campaign-wave-numbers.png){width="80%"}

>[!NOTE]
>
>Al utilizar números, el sistema no valida que la suma cubra toda la audiencia; debe asegurarse de que el tamaño de las olas cubra la audiencia a la que desea enviar. Obtenga más información en las [preguntas más frecuentes](#faq).

### Programación personalizada {#custom-schedule}

Seleccione **[!UICONTROL Programar cada ola]** para definir una fecha y hora de inicio específicas para cada ola. Las olas no necesitan espaciarse uniformemente (por ejemplo, 9:00 a.m., 11:00 a.m., 5:00 p.m., 8:30 p.m.).

![](assets/campaign-wave-custom-schedule.png){width="80%"}

>[!NOTE]
>
>El intervalo mínimo entre el inicio de dos olas es de **30 minutos**.

## Casos de uso {#use-cases}

El envío de ondas le ayuda a controlar cuándo y cuántos mensajes se emiten, lo que puede mejorar la capacidad de envío, proteger la reputación del remitente y alinear los envíos con su capacidad operativa. Considere la posibilidad de utilizar olas en estos escenarios:

* **Centro de llamadas o administración de respuestas:** Limite la cantidad de mensajes que se emiten por día o por hora para que los equipos intermedios (por ejemplo, el Servicio de atención al cliente) puedan administrar las respuestas. Por ejemplo, envíe 20 mensajes al día para que coincidan con la capacidad del centro de llamadas.

  ![](assets/campaign-waves-ex-call-center.png){width="75%"}

* **Alto volumen y capacidad de entrega:** Evite enviar una campaña muy grande de una sola vez. Distribuya la entrega a lo largo del tiempo para ayudar a mantener la reputación del remitente y reducir el riesgo de ser marcado como correo no deseado.

  ![](assets/campaign-waves-ex-high-volume.png){width="75%"}

* **Aumento progresivo:** Al usar una nueva plataforma o IP, aumente progresivamente el volumen (por ejemplo, 10% en la primera ola, luego 15%, 20%, etc.) para generar reputación de forma gradual.

  ![](assets/campaign-waves-ex-ramp-up.png){width="75%"}

## Preguntas frecuentes {#faq}

+++ ¿Qué sucede si la suma de los tamaños de onda no es igual a la audiencia total?

* Si la suma de los tamaños de ola **supera** la audiencia (por ejemplo, programa 100 000 en la primera ola para una audiencia de 100 000), la primera ola se enviará a la audiencia completa y las olas restantes no tendrán a nadie a quien enviar; no se ejecutarán.
* Si la suma **es menor que la audiencia (por ejemplo, si define cuatro olas que suman un total de 40 000 perfiles para una audiencia de 100 000), solo los perfiles incluidos en esas olas recibirán el mensaje.** El resto de la audiencia no recibirá la comunicación y no se volverá a intentar usarla en olas posteriores.

+++

+++ ¿Puedo asignar diferentes segmentos o criterios a olas individuales?

Solo se puede definir el tamaño y el tiempo de las olas. La selección de destinatarios es la misma para toda la campaña; no se pueden asignar segmentos o criterios diferentes a olas individuales.

+++

## Próximos pasos {#next}

* [Programe la campaña de acción](campaign-schedule.md): establezca la fecha de inicio, la fecha de finalización, la frecuencia y el control de velocidad.
* [Revise y active la campaña](review-activate-campaign.md): compruebe la campaña e inicie sesión.
