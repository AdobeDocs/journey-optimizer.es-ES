---
solution: Journey Optimizer
product: journey optimizer
title: Preguntas frecuentes
description: Preguntas frecuentes sobre actividades activas
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e7e994ca-aa0c-4e86-8710-c87430b74188
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 0%

---

# Preguntas frecuentes {#mobile-live-faq}

## Preguntas generales

+++¿Cuál es la diferencia entre una actividad en directo y una notificación push?

La actividad en directo proporciona actualizaciones persistentes y en tiempo real en la pantalla de bloqueo y en Dynamic Island sin que los usuarios tengan que desbloquear su dispositivo. Las notificaciones push son alertas temporales que desaparecen una vez descartadas. La actividad activa permanece visible y se puede actualizar varias veces hasta que finalice de forma explícita.

+++

+++¿Cuántas instancias de actividad en directo pueden estar activas a la vez?

Una aplicación de iOS puede ejecutar varias instancias de actividad en directo simultáneamente, incluidas varias que utilicen el mismo tipo `ActivityAttributes`.

Los desarrolladores no imponen ningún límite estricto sobre cuántas instancias de actividad en directo de un tipo de atributo determinado pueden existir. Puede iniciar tantos como requiera la lógica de la aplicación, por ejemplo, uno por envío o recorrido en curso. Sin embargo, iOS aplica un límite de nivel del sistema en cuanto a cuántas instancias de actividad activas pueden estar activas o visibles a la vez.

En la práctica:

* iOS suele admitir hasta cinco instancias de actividad en directo simultáneas por aplicación.

* Si supera este número, el sistema puede dejar de mostrar algunas instancias de actividad o finalizar las anteriores para conservar recursos.

* Cada instancia de actividad en directo tiene un(a) `Activity.id` único(a), que permite actualizarlo o finalizarlo por separado.

+++

+++¿Los usuarios deben tener la aplicación abierta para recibir actualizaciones de actividades en directo?

No. La actividad en directo se puede iniciar, actualizar y finalizar de forma remota, incluso cuando la aplicación está completamente cerrada, una de las ventajas clave de la función.

+++

+++¿Qué versiones de iOS admiten la actividad en directo?

* iOS 16.1+: compatibilidad básica con actividades en directo
* iOS 17.2+: funcionalidad de push a inicio (inicio remoto sin abrir la aplicación)
* iOS 18+: Compatibilidad con canales de difusión para actividades en directo basadas en audiencias
+++

+++¿Durante cuánto tiempo puede permanecer activa una actividad Live?

Apple limita la actividad en vivo a **8 horas de actualizaciones activas**. Después de eso, el sistema finaliza automáticamente la actividad, aunque puede permanecer visible en un estado estático durante **12 horas adicionales** antes de la eliminación. También puede finalizar una actividad en vivo antes estableciendo un `dismissalDate` o llamando explícitamente a `activity.end()` en su aplicación.

+++

### Preguntas para desarrolladores

+++¿Debo crear una extensión de widget independiente para la actividad en directo?

Sí. La actividad en directo se muestra a través de WidgetKit, por lo que debe crear una extensión de widget en el proyecto Xcode e implementar `ActivityConfiguration`.
[Más información sobre la configuración del widget](mobile-live-configuration-sdk.md)

+++

+++¿Puedo usar la misma clase `LiveActivityAttributes` para la actividad en directo local y remota?

Sí. La misma clase de atributos funciona para la actividad en directo iniciada localmente y a distancia (push-to-start). Debe asegurarse de registrarlo con `Messaging.registerLiveActivity()`.

+++

+++¿Qué sucede si envío una actualización para una actividad en directo que no existe?

Si envía un evento de actualización o finalización para un(a) `liveActivityID` o `channelID` inexistente, la solicitud fallará de forma silenciosa en el dispositivo. Asegúrese siempre de rastrear qué instancias de actividad en directo están activas para cada usuario.

+++

+++¿Puedo probar la actividad en directo en el simulador de iOS?

Sí, puede probar la actividad en directo iniciada localmente y remotamente en el simulador de iOS.

* **Local**: esto incluye la creación, actualización y finalización de una actividad en vivo directamente desde su aplicación usando **API de ActivityKit**.

* **Remoto**: para probar la funcionalidad de la actividad Live de forma remota, integra nuestro SDK de mensajería en tu aplicación y usa las API de ejecución proporcionadas para enviar el inicio, la actualización y el final remotos a tu dispositivo de prueba o simulador de iOS. Es similar a la forma en que se pueden probar las notificaciones push con la integración de SDK de Adobe.

+++

+++¿Cómo gestiono las actualizaciones cuando la aplicación está en segundo plano?

SDK lo gestiona automáticamente. Una vez registrada, la actividad Live recibe actualizaciones incluso cuando finaliza la aplicación. No se requieren modos de fondo adicionales.
+++

+++¿Cuál es la diferencia entre `liveActivityID` y `channelID`?

* `liveActivityID`: se usa para una actividad en directo individual (unitaria) dirigida a usuarios específicos. Cada ID representa una instancia de actividad en directo única.
* `channelID`: se usa para la actividad de difusión en directo enviada a las audiencias. Todos los usuarios de la audiencia reciben las mismas actualizaciones en el mismo canal.
+++

+++¿Puedo personalizar el aspecto de Dynamic Island por separado de la pantalla de bloqueo?

Sí. `ActivityConfiguration` tiene cierres independientes para el contenido de pantalla bloqueada y el contenido de Dynamic Island (expandido, compacto y con estados mínimos), cada uno de los cuales se diseña de forma independiente.
+++

+++¿Debo almacenar los tokens push manualmente?

No. Al registrar un tipo de Actividad activa con `Messaging.registerLiveActivity()`, SDK recopila y administra automáticamente los tokens push.
+++

+++¿Hay límites en los inicios remotos de la actividad en directo?

Sí. Los inicios remotos a través de `ActivityKit` están sujetos a límites impuestos por el sistema. Si intenta ejecutar varias solicitudes de inicio en sucesión rápida, iOS puede rechazar nuevos inicios debido a cuotas de actividad activas o restricciones presupuestarias. Después de unos 5 intentos de inicio consecutivos, las solicitudes posteriores comienzan a fallar hasta que pasa un breve periodo de reutilización.

+++

+++¿Cuál es el presupuesto para actualizaciones de alta prioridad?

Apple no especifica un límite numérico exacto para las actualizaciones de actividad en directo de `(priority: 10)` de alta prioridad. El sistema mantiene un presupuesto interno dinámico que limita la frecuencia con la que se pueden enviar dichas actualizaciones. Si se emiten demasiadas actualizaciones de alta prioridad en un corto intervalo, iOS puede acelerar o retrasar las posteriores.

Para minimizar la restricción:

* **Niveles de prioridad de equilibrio**: combine actualizaciones estándar `(priority: 5)` y altas `(priority: 10)` según la importancia.
* **Usar la prioridad alta con moderación**: reserve la prioridad alta para actualizaciones en las que el tiempo sea un factor crítico, como el progreso de entrega, el estado del pedido o las puntuaciones deportivas en directo.
* **Admitir actualizaciones frecuentes**: incluye `NSSupportsLiveActivitiesFrequentUpdates` en `Info.plist` de tu aplicación y configúrelo en **SÍ** si necesitas actualizaciones frecuentes.

+++

### Preguntas del experto en marketing

+++¿Puedo personalizar el contenido de la actividad en directo para cada usuario en una campaña de difusión?

Las campañas de difusión envían el mismo contenido a todos los usuarios de la audiencia. Para contenido personalizado, utilice campañas unitarias (transaccionales) dirigidas a usuarios individuales.
+++

+++¿Cómo sé si mi actividad en directo se entregó correctamente?

[Supervise el análisis de su campaña](../reports/campaign-global-report-cja-activity.md) en Adobe Journey Optimizer. Puede hacer un seguimiento de las tasas de entrega, los errores y las métricas de participación. Considere también la posibilidad de implementar eventos de análisis personalizados en la aplicación.
+++

+++¿Puedo programar la actividad en vivo con antelación?

La llamada de API almacena en déclencheur la actividad Live inmediatamente. Sin embargo, puede programar sus llamadas de API a través de sus sistemas back-end o utilizar las funcionalidades de orquestación de Journey Optimizer para cronometrarlas correctamente.
+++

+++¿Qué sucede si envío un evento de &quot;inicio&quot; para una actividad en directo que ya existe?

Al iniciar de forma remota una actividad en directo mediante las API de ejecución de Adobe:

* Puede incluir un encabezado `x-request-id` en su solicitud. Lo ideal sería que hubiera una relación uno a uno entre cada `liveActivityID` y su correspondiente `x-request-id`. Esto garantiza que si se realizan varias solicitudes con la misma combinación de `x-request-id` y `liveActivityID`, solo se iniciará una instancia de actividad en directo en el dispositivo y se omitirán las solicitudes duplicadas.

* Si se omite el encabezado `x-request-id`, cada solicitud se trata de forma independiente, lo que puede dar como resultado que se creen varias instancias de actividad Live con el mismo `liveActivityID`. En estos casos, las actualizaciones futuras pueden fallar o aplicarse solo a una de las instancias activas.

* El valor `x-request-id` no se debe reutilizar en `liveActivityIDs` diferentes en solicitudes de API independientes.

+++

+++¿Puedo probar diferentes experiencias de actividad en directo A/B?

Sí. Cree varias campañas con diferentes estructuras de contenido y utilice las funciones de experimentación de Adobe Journey Optimizer para probar cuál de ellas tiene un mejor rendimiento. Asegúrese de que la aplicación admita todas las variaciones de estado del contenido.

+++

+++¿Con qué frecuencia debo actualizar una actividad en directo?

Actualice solo cuando haya cambios significativos en la información, ya que las actualizaciones demasiado frecuentes pueden agotar la batería y reducir la calidad de la experiencia del usuario. En situaciones en tiempo real, como el seguimiento de envíos, normalmente se acepta cada 30-60 segundos. Para el contenido que cambia más lentamente, como las puntuaciones deportivas, actualice solo los eventos significativos.

+++

+++¿Puedo segmentar usuarios en función de si tienen habilitada la actividad en directo?

Deberá trabajar con su equipo de desarrollo de para rastrear y pasar esta preferencia a Adobe Experience Platform como atributo de usuario y luego segmentar en función de ese atributo.

+++

### Preguntas de API

+++¿Cuál es la diferencia entre `timestamp` y `dismissal-date`?

* `timestamp`: la hora de epoch actual en que se produce el evento, necesaria para todos los eventos.
* `dismissal-date`: una hora futura en la que la actividad en directo debería descartarse automáticamente, necesaria solo para eventos de &quot;finalización&quot;.

+++

+++¿Debo enviar todos los campos `attributes` en cada llamada de actualización?

Sí, según su clase `LiveActivityAttribute`.

* Todos los campos del objeto de atributos, incluido `liveActivityData`, deben incluirse en cada llamada para el inicio, las actualizaciones o el final.
* Solo los campos `content-state` representan lo que realmente cambia dinámicamente en una actividad en ejecución.
* Incluya también un objeto de alerta para garantizar que la notificación push se trate como una notificación visible para el usuario, no como una notificación en segundo plano silenciosa. Necesario solo para casos de &quot;inicio&quot; y, por lo demás, opcional.

+++

+++¿En qué formato deben estar las marcas de tiempo epoch?

Utilice el tiempo de Unix epoch en **segundos**, no en milisegundos. Por ejemplo: `1759937682`

+++

+++¿Puedo usar el mismo(a) `requestId` para varias llamadas a la API?

No. Cada solicitud de API debe tener un(a) `requestId` único(a) para garantizar la idempotencia y un seguimiento adecuado. Utilice UUID o identificadores únicos similares.

+++

+++¿Qué autenticación se requiere para la API sin encabezado?

Consulte la [Documentación de campañas activadas por API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) para conocer los requisitos de autenticación, incluidos tokens de OAuth y claves de API.

+++

+++¿Qué sucede si falla mi llamada de API?

Implementar la lógica de reintentos con retroceso exponencial. Compruebe la respuesta de la API en busca de códigos de error y mensajes para diagnosticar problemas. Los errores comunes incluyen ID de campaña no válidos, cargas útiles mal formadas o problemas de autenticación.

+++

+++¿Puedo enviar actualizaciones de actividad en directo desde mis propios servidores back-end?

Sí, ese es el comportamiento deseado. El servidor llama a la API de Adobe Journey Optimizer sin encabezado para almacenar en déclencheur los eventos de actividad que se producen cuando la lógica empresarial lo requiere.

+++

+++¿Necesito una campaña diferente para los eventos de inicio, actualización y finalización?

No. Puede utilizar la misma campaña y cambiar el campo `event` en la carga útil. Sin embargo, algunas organizaciones prefieren campañas independientes para un mejor seguimiento de los análisis.

+++

### Preguntas sobre resolución de problemas

+++Mi actividad en directo comienza pero no se actualiza. ¿Cuál podría ser el problema?

Causas frecuentes:

* No coinciden `liveActivityID` o `channelID` entre las llamadas de inicio y actualización.
* `content-state` campos no coinciden con su estructura `ContentState`.
* La actividad Live ya ha finalizado.
* Problemas de conectividad de red en el dispositivo.
* La hora de la época utilizada como marca de tiempo no está actualizada.

+++

+++No se reconoce el campo `attributes-type`. ¿Qué debería comprobar?

* Asegúrese de que el nombre de clase coincida **exactamente** (con distinción de mayúsculas y minúsculas) con el nombre de estructura de Swift
* Compruebe que la estructura está correctamente definida y registrada
* Compruebe si hay errores tipográficos en la carga útil JSON
* Confirme que la versión de la aplicación instalada tiene la implementación de Actividad en directo.

+++

+++Los usuarios solo ven la actualización de la actividad en directo y no la notificación de alerta. ¿Se trata de un problema conocido?

No. El campo `alert` es opcional y iOS lo puede suprimir en determinadas condiciones, por ejemplo, en el modo No molestar. La actividad en directo se puede actualizar de forma silenciosa, que suele ser el comportamiento deseado. El campo de alerta es obligatorio para enviar inicios remotos; de lo contrario, Apple lo trata como una notificación en segundo plano silenciosa.

+++

+++¿Puedo eliminar o borrar todas las instancias de actividad en directo de un usuario?

Debe enviar un evento de &quot;finalización&quot; para cada instancia de actividad en directo activa. Realice un seguimiento de las instancias de actividades activas de cada usuario de sus sistemas para poder limpiarlas correctamente.

+++

+++Mi widget muestra &quot;Sin datos&quot; aunque envié una actualización. ¿Cuál podría ser el problema?

* Verifique que la implementación del widget acceda correctamente a `context.state` y `context.attributes`.
* Compruebe que los valores predeterminados o los estados de error se gestionan en la interfaz del widget.
* Utilice el protocolo `LiveActivityAssuranceDebuggable` para depurar el esquema.
* Realice pruebas con Adobe Assurance para ver si se reciben los datos.
+++
