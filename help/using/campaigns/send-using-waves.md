---
solution: Journey Optimizer
product: journey optimizer
title: Envío mediante olas
description: Programe los mensajes de campaña salientes para que se entreguen en lotes controlados a lo largo del tiempo. El envío de ondas admite la entrega y ayuda a mantener la reputación del remitente.
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: olas, lotes, programación, campaña, recorrido, capacidad de entrega
exl-id: 6d53d817-78f6-4d00-8ff0-8a848c618435
feature_v2: id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2: id: f7479fa1-474b-479d-8c98-f6cee5865a38id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
source-git-commit: 76fd78f66bc69b228b794bcd129a48b65028c1cb
workflow-type: tm+mt
source-wordcount: 966
ht-degree: 1%

---

# Envío mediante olas en campañas {#send-using-waves}

>[!BEGINSHADEBOX]

**En esta página:** Divida la entrega de la campaña saliente en lotes programados, llamados olas, para que pueda equilibrar la carga, proteger la reputación del remitente y mejorar la capacidad de entrega de los envíos de gran volumen.

>[!ENDSHADEBOX]

Puede dividir el envío de mensajes de campaña salientes en varios lotes (olas) y programarlos a lo largo del tiempo. El envío de ondas ayuda a equilibrar la carga, evitar sistemas descendentes abrumadores (como centros de llamadas o páginas de aterrizaje) y admite la capacidad de envío y la reputación del remitente, especialmente para envíos de gran volumen.

<!--
>[!CAUTION]
>
>Wave sending applies to **outbound** actions only (Email, SMS, Push, Direct mail).
-->

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

Seleccione **[!UICONTROL Números]** para definir el tamaño de cada ola como un número absoluto de perfiles (por ejemplo, 10 000; 50 000).

![](assets/campaign-wave-numbers.png){width="80%"}

>[!NOTE]
>* Al utilizar porcentajes, todas las olas deben sumar el 100%. Si no es así, se muestra una advertencia.
>* Cuando se usan números, el sistema no valida la cobertura; asegúrese de que los tamaños de onda cubran la audiencia a la que va dirigida. [Más información](#faq)

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

+++ ¿Se vuelve a evaluar la audiencia antes de cada ola o se corrige al inicio de la campaña?

La audiencia se **evalúa una vez** cuando se activa la campaña. En ese momento se toma una instantánea de los perfiles aptos que se utiliza para todas las olas (la pertenencia a la audiencia no se vuelve a evaluar antes de cada ola subsiguiente).

Sin embargo, **los atributos de perfil se leen en el momento en que se procesa cada ola**, no en la activación de la campaña. Esto significa que para las olas se extienden a lo largo de varios días:

* Los atributos de Personalization (por ejemplo, el nombre o el nivel de fidelidad de un perfil) reflejan el estado del perfil en el momento en que se ejecuta la oleada.
* **Las comprobaciones de consentimiento y supresión se aplican en el momento del envío para cada ola.** Si un perfil se excluye entre dos olas, no recibirá mensajes de las olas siguientes.

En resumen: *who* se incluye en la campaña se ha corregido por adelantado, pero *los datos utilizados para enviar a esos perfiles* reflejan su estado actual cuando se procesa su ola.

+++

## Próximos pasos {#next}

* [Programe la campaña de acción](campaign-schedule.md): establezca la fecha de inicio, la fecha de finalización, la frecuencia y el control de velocidad.
* [Revise y active la campaña](review-activate-campaign.md): compruebe la campaña e inicie sesión.
