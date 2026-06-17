---
solution: Journey Optimizer
product: journey optimizer
title: Optimización del tiempo de envío para la mensajería móvil
description: Aprenda a configurar y utilizar la optimización del tiempo de envío para la mensajería móvil en Adobe Journey Optimizer.
feature: SMS
topic: Send Time Optimization
role: User
level: Intermediate
exl-id: 56ff1000-7799-40ff-8f03-2f5868d05e7b
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: f03a3a13-9e99-4c7c-a1ae-0f4d07ced35c
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 84aa39bfd480e5bcaa8a58c5ec29f1990e5ddc6f
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 1%

---


# Optimización del tiempo de envío para la mensajería móvil {#sms-send-time-optimization}

>[!AVAILABILITY]
>
>La optimización del tiempo de envío para mensajería móvil (SMS, RCS y WhatsApp) está disponible a partir del H2 de 2026 y se aplica tanto a Recorridos como a Campañas.

## Información general {#overview}

La optimización del tiempo de envío (STO) para mensajería móvil permite a los especialistas en marketing ir más allá de la programación por lotes y explosiones utilizando perspectivas impulsadas por IA para determinar la hora de envío óptima para cada perfil individual. En lugar de enviar mensajes a toda la audiencia a la vez, Adobe Journey Optimizer analiza los patrones de participación históricos de cada perfil y predice cuándo es más probable que esa persona abra, haga clic o responda a un mensaje SMS, RCS o WhatsApp.

Al enviar mensajes en el momento de mayor participación prevista, STO ayuda a aumentar las tasas de apertura, las tasas de pulsaciones y el ROI general de la campaña, sin necesidad de segmentar la audiencia manualmente por zona horaria o cohorte de comportamiento. STO para mensajería móvil es compatible con todos los canales SMS, RCS y WhatsApp y está disponible tanto en contextos de Recorrido como de ejecución de campaña.

## Requisitos previos {#prerequisites}

Antes de habilitar la optimización del tiempo de envío para la mensajería móvil, compruebe lo siguiente:

- Su organización está aprovisionada para Adobe Journey Optimizer y para al menos uno de los canales de SMS, RCS o WhatsApp.
- Existe un volumen suficiente de datos de participación móvil históricos, incluidos eventos de envío, aperturas, clics en vínculos y respuestas, para la audiencia de destino en Adobe Experience Platform (AEP). El modelo de IA requiere un historial de interacciones previo para generar predicciones fiables por perfil.
- La superficie de canal relevante (SMS, RCS o WhatsApp) está configurada y activa en la instancia de AJO. Consulte [Configurar superficies de canal SMS](../sms/sms-configuration.md) para obtener instrucciones de configuración.
- En los casos de uso basados en Recorrido, la Recorrido debe diseñarse para que el nodo de acción del mensaje no se vea limitado por nodos de espera o de evento ascendentes cuyos tiempos de espera entren en conflicto con la ventana de entrega de STO.

>[!NOTE]
>
>Los perfiles con datos de participación históricos insuficientes vuelven a un tiempo de envío predeterminado que se define durante la configuración. Las predicciones de STO se generan y puntúan en el nivel de perfil individual.

## Funcionamiento {#how-it-works}

STO para mensajería móvil se basa en un modelo de IA creado específicamente que procesa las señales de participación históricas de cada perfil para prever el período de entrega óptimo. Los siguientes pasos describen el flujo de extremo a extremo.

### &#x200B;1. Ingesta de datos y formación sobre modelos

El modelo de IA ingiere continuamente eventos de participación móvil almacenados en Adobe Experience Platform, incluidas las marcas de tiempo de apertura de mensajes, los eventos de clic en vínculos, las horas de respuesta y los registros de envío históricos. Estas señales forman los datos de formación utilizados para aprender los patrones de comportamiento de cada perfil, como las horas de interacción preferidas, las tendencias del día de la semana y la capacidad de respuesta en los husos horarios. El modelo se vuelve a entrenar progresivamente para seguir siendo sensible a los cambios en el comportamiento de la participación.

### &#x200B;2. Puntuación de predicción por perfil

Una vez entrenado, el modelo puntúa cada perfil en la audiencia de destino y produce una ventana de tiempo de envío óptima. Esta predicción se escribe de nuevo en el perfil de AEP como un atributo calculado, lo que lo hace disponible para los Recorridos y las campañas en el momento de la ejecución sin necesidad de llamadas de API adicionales o búsquedas en tiempo real durante el envío del mensaje.

### &#x200B;3. Recorrido de programación de tiempo de ejecución

Cuando un Recorrido que contiene un nodo de acción SMS, RCS o WhatsApp habilitado para STO está activo, el tiempo de ejecución de Recorrido lee el atributo de tiempo de envío predicho de cada perfil correspondiente a medida que el perfil alcanza el nodo de acción. El mensaje se mantiene dentro de la ventana de optimización configurada y se envía cuando llega el tiempo óptimo predicho. Si el tiempo predicho ya ha pasado o cae fuera de la ventana, se aplica el comportamiento de reserva configurado.

### &#x200B;4. Distribución de envío de campaña

Para las campañas, STO distribuye el envío entre la audiencia en función de las predicciones de cada perfil, en lugar de emitir un solo envío masivo. AJO escalona la entrega en la ventana de envío configurada de la campaña, respetando el tiempo óptimo predicho de cada perfil y permaneciendo dentro de los límites de ventana definidos.

>[!NOTE]
>
>Si el tiempo óptimo previsto de un perfil queda fuera de la ventana de envío configurada, el mensaje se envía en el límite más cercano (inicio o final de la ventana), el que esté más cerca de la predicción.

## Configurar optimización del tiempo de envío {#configure}

### Habilitar STO en una campaña {#configure-campaign}

1. En Journey Optimizer, vaya a **Campañas** y cree una nueva campaña o abra un borrador existente.
2. Seleccione **SMS**, **RCS** o **WhatsApp** como canal y complete los pasos de audiencia y contenido de mensaje.
3. En la sección **Programación**, seleccione **Optimización del tiempo de envío** en lugar de una fecha y hora de envío fijas.
4. Utilice la opción **Optimización del tiempo de envío** para habilitar la característica.
5. Configurar la **ventana de envío**: establezca la hora de inicio y finalización en la que AJO puede enviar mensajes. La ventana debe abarcar al menos una hora y puede extenderse hasta 24 horas.
6. Defina un **tiempo de envío de reserva** para perfiles que no tengan suficiente historial de participación para generar una predicción. Puede elegir enviar inmediatamente al abrir la ventana o a una hora fija dentro de la ventana.
7. Complete los pasos de restricción de frecuencia, revisión y activación, y luego active la campaña.

### Habilitar STO en un Recorrido {#configure-journey}

1. Abra o cree un Recorrido en el lienzo de Recorrido.
2. Agregue o seleccione un nodo de acción **SMS**, **RCS** o **WhatsApp**.
3. En el panel de configuración del nodo de acción, expanda la configuración **Hora de envío**.
4. Cambie **Optimización del tiempo de envío** al estado habilitado.
5. Establezca la **ventana de optimización**: la duración máxima (en horas) que el tiempo de ejecución puede retener un mensaje mientras espera el tiempo de entrega óptimo predicho. La ventana predeterminada es de seis horas; el máximo es de 24 horas.
6. Configure el **comportamiento de reserva** (envíe inmediatamente cuando un perfil entre en el nodo o espere hasta la siguiente ventana predicha disponible) para perfiles que no tengan datos de predicción.
7. Guarde la configuración del nodo y publique el Recorrido.

>[!NOTE]
>
>Cuando STO está activo en un nodo de acción de Recorrido, el tiempo de entrega efectivo de un perfil puede diferir del momento en que el perfil entra en el nodo hasta la longitud completa de la ventana de optimización configurada. Tenga en cuenta este retraso al diseñar nodos de espera ascendentes y establecer tiempos de espera en el nivel de Recorrido para evitar salidas de recorrido prematuras.

## Mecanismos de protección y limitaciones {#guardrails}

- STO solo se aplica a los mensajes SMS, RCS y WhatsApp salientes. Los flujos de respuesta entrantes y las sesiones de mensajería bidireccional no están sujetos a la programación de STO.
- Cada nodo de acción de Campaign o Recorrido admite una superficie de canal por cada mensaje con STO habilitado. No se admite la coordinación STO entre canales (por ejemplo, SMS y WhatsApp dentro de un solo nodo).
- El modelo de IA requiere un mínimo de 30 días de datos históricos de participación móvil por perfil para producir una predicción. Los perfiles por debajo de este umbral utilizan el tiempo de envío de reserva configurado.
- STO interactúa con las reglas de límite de frecuencia. Si la ventana de entrega prevista de un perfil limitado entra en conflicto con un límite, el mensaje se suprime según la regla de límite y no se vuelve a programar para una ventana posterior.
- Los indicadores de consentimiento, los registros de exclusión y las listas de supresión global siempre se aplican independientemente de la programación de STO. Un mensaje mantenido para una entrega optimizada sigue estando sujeto a comprobaciones de consentimiento en el momento del envío.
- STO no está disponible para mensajes transaccionales en los que los requisitos comerciales o regulatorios exigen una entrega inmediata.

## Temas relacionados {#related-topics}

- [Introducción a SMS, RCS y WhatsApp en Journey Optimizer](../sms/create-sms.md)
- [Configuración de superficies de canal SMS](../sms/sms-configuration.md)
- [Optimización del tiempo de envío para notificaciones push y de correo electrónico](../building-journeys/send-time-optimization.md)
- [Clasificación con tecnología de IA en Journey Optimizer](../offers/offer-activities/ai-ranking.md)
- [Notas de la versión de Journey Optimizer](../rn/release-notes.md)
