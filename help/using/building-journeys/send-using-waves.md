---
solution: Journey Optimizer
product: journey optimizer
title: Envío mediante olas en recorridos
description: Programar mensajes de recorrido salientes para que se entreguen en lotes controlados (olas) a lo largo del tiempo. El envío de ondas en recorridos de lectura-audiencia ayuda a equilibrar la carga y la capacidad de envío.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
mini-toc-levels: 1
keywords: olas, lotes, programación, recorrido, lectura de audiencia, entrega
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 1%

---

# Envío mediante olas en recorridos {#send-using-waves-journeys}

>[!AVAILABILITY]
>
>Esta función se encuentra en disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

Puede enviar mensajes salientes desde un recorrido en lotes (olas) a lo largo del tiempo en lugar de todos a la vez. El envío de ondas ayuda a equilibrar la carga, evitar sistemas descendentes abrumadores (como centros de llamadas o páginas de aterrizaje) y admite la capacidad de envío y la reputación del remitente, especialmente para recorridos de audiencia de lectura de gran volumen.

<!--
>[!CAUTION]
>
>Wave sending is available for read audience journeys only and applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

Puede configurarlo en el nivel de recorrido cuando define cómo entra la audiencia y cómo se programan las acciones. Se define el número de olas, su tamaño (como porcentaje de la audiencia o como números absolutos) y cuándo se ejecuta cada ola.

## Limitaciones y barreras {#limitations-guardrails}

* El envío de ondas solo está disponible para recorridos de audiencia de lectura con los tipos de programador **[!DNL As soon as possible]** y **[!UICONTROL Once]**. Más información sobre la [programación de recorrido](read-audience.md#schedule).
* El envío de ondas no está disponible para recorridos recurrentes, activados por eventos, de evento empresarial, de modo de prueba o de ejecución en seco.
* Debe definir al menos **2 olas** y puede agregar **10 ondas**.
* El intervalo mínimo entre el inicio de dos olas es de **30 minutos**.
* No se puede iniciar una ola antes del inicio del recorrido o en el pasado.
* Dividir la audiencia en olas puede tardar hasta 1 hora. Es posible que los perfiles no entren en el recorrido hasta entonces.
* Dentro de una sola versión de recorrido, dos olas nunca se ejecutan al mismo tiempo. La siguiente ola comienza solo después de que haya finalizado la anterior. Por ejemplo, si las olas se programan con una diferencia de 1 hora pero la primera ola se ejecuta durante 2 horas, la segunda ola se inicia cuando finaliza la primera ola, no a su hora programada.
* Los inicios de ola se pueden retrasar cuando la plataforma aplica límites de cuota o cuando la capacidad del sistema está bajo una carga pesada.

## Configuración del envío de ondas en un recorrido {#configure-wave-sending}

1. Inicie el recorrido con una actividad [Leer audiencia](read-audience.md).

1. Haga doble clic en la actividad **[!UICONTROL Leer audiencia]** para abrir sus propiedades y seleccione la opción **[!UICONTROL Enviar acción de recorrido en olas]**.

   ![](assets/journey-wave-option.png){width="100%"}

1. Establezca el **número de olas** (por ejemplo, 4).

   ![](assets/journey-wave-number.png){width="80%"}

   >[!NOTE]
   >
   >Se deben definir al menos 2 olas y se pueden añadir hasta 10.

1. Elija cómo definir el tamaño y el tiempo de la onda como se detalla a continuación.

### Olas iguales {#equal-waves}

De forma predeterminada, la audiencia se divide en olas de igual tamaño. Establezca un intervalo fijo entre el inicio de cada ola (por ejemplo, 2 horas).

![](assets/journey-equal-waves.png){width="70%"}

>[!NOTE]
>
>El intervalo mínimo entre el inicio de dos olas es de **30 minutos**.

A continuación, el sistema programa automáticamente las olas siguientes (por ejemplo, la primera ola a las 9:00 AM, la segunda a las 11:00 AM, la tercera a las 1:00 PM y la cuarta a las 3:00 PM).

### Distribución personalizada {#custom-distribution}

Seleccione la opción **[!UICONTROL Distribución personalizada]** para definir el tamaño de cada ola como un porcentaje de la audiencia total (por ejemplo, 15%, 20%, 25%, 40%).

![](assets/journey-wave-percentage.png){width="70%"}

>[!NOTE]
>
>El total en todas las olas debe ser igual al 100%. Si no es así, se muestra un mensaje de advertencia.<!--are the waves actually sent or does the system prevent user from saving the journey?-->

Seleccione **[!UICONTROL Números]** para definir el tamaño de cada ola como un número absoluto de perfiles (por ejemplo, 10 000; 50 000).

![](assets/journey-wave-numbers.png){width="70%"}

>[!NOTE]
>
>Al utilizar números, el sistema no valida que la suma cubra toda la audiencia; debe asegurarse de que el tamaño de las olas cubra la audiencia a la que desea enviar. Obtenga más información en las [preguntas más frecuentes](#faq).

### Programación personalizada {#custom-schedule}

Seleccione **[!UICONTROL Programar cada ola]** para definir una fecha y hora de inicio específicas para cada ola. Las olas no necesitan espaciarse uniformemente (por ejemplo, 9:00 a.m., 11:00 a.m., 5:00 p.m., 8:30 p.m.).

![](assets/journey-wave-custom-schedule.png){width="70%"}

>[!NOTE]
>
>El intervalo mínimo entre el inicio de dos olas es de **30 minutos**.

## Casos de uso {#use-cases}

El envío de ondas le ayuda a controlar cuándo y cuántos mensajes se emiten, lo que puede mejorar la capacidad de envío, proteger la reputación del remitente y alinear los envíos con su capacidad operativa. Considere la posibilidad de utilizar olas en estos escenarios:

* **Centro de llamadas o administración de respuestas:** Limite la cantidad de mensajes que se emiten por día o por hora para que los equipos intermedios (por ejemplo, el Servicio de atención al cliente) puedan administrar las respuestas. Por ejemplo, envíe 20 mensajes al día para que coincidan con la capacidad del centro de llamadas.

  ![](assets/journey-waves-ex-call-center.png){width="55%"}

* **Alto volumen y capacidad de entrega:** Evite enviar un recorrido muy grande de una sola vez. Distribuya la entrega a lo largo del tiempo para ayudar a mantener la reputación del remitente y reducir el riesgo de ser marcado como correo no deseado.

  ![](assets/journey-waves-ex-high-volume.png){width="55%"}

* **Aumento progresivo:** Al usar una nueva plataforma o IP, aumente progresivamente el volumen (por ejemplo, 10% en la primera ola, luego 15%, 20%, etc.) para generar reputación de forma gradual.

  ![](assets/journey-waves-ex-ramp-up.png){width="55%"}

## Preguntas frecuentes {#faq}

+++ ¿Qué sucede si la suma de los tamaños de onda no es igual a la audiencia total?

* Si la suma de los tamaños de ola **supera** la audiencia (por ejemplo, programa 100 000 en la primera ola para una audiencia de 100 000), la primera ola se enviará a la audiencia completa y las olas restantes no tendrán a nadie a quien enviar; no se ejecutarán.
* Si la suma **es menor que la audiencia (por ejemplo, si define cuatro olas que suman un total de 40 000 perfiles para una audiencia de 100 000), solo los perfiles incluidos en esas olas recibirán el mensaje.** El resto de la audiencia no recibirá la comunicación y no se volverá a intentar usarla en olas posteriores.

+++

+++ ¿Puedo asignar diferentes segmentos o criterios a olas individuales?

Solo se puede definir el tamaño y el tiempo de las olas. La misma audiencia fluye a través del recorrido; no se pueden asignar segmentos o criterios diferentes a olas individuales.

+++

## Consulte también {#see-also}

* [Usar una audiencia en un recorrido](read-audience.md): configure la actividad Leer audiencia.
