---
solution: Journey Optimizer
product: journey optimizer
title: Horas tranquilas
description: Obtenga información sobre cómo evitar que las comunicaciones se envíen durante períodos específicos mediante reglas de horas de inactividad
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: horas tranquilas, exclusiones horarias, reglas empresariales, conjuntos de reglas, programación, campañas
exl-id: [TO BE GENERATED]
hide: yes
hidefromtoc: yes
source-git-commit: 11bccd63afa1bf5aafcd1dff70c8193ea754d256
workflow-type: tm+mt
source-wordcount: 980
ht-degree: 9%

---

# Horas tranquilas {#quiet-hours}

>[!AVAILABILITY]
>
>Ahora mismo, las horas tranquilas solo están disponibles para un conjunto de organizaciones (disponibilidad limitada). Para que se añada a la lista de espera, póngase en contacto con su representante de Adobe.

Las horas tranquilas le permiten definir exclusiones basadas en el tiempo para los canales de correo electrónico, SMS, push y WhatsApp. Garantizan que no se envíen mensajes durante períodos de tiempo específicos, lo que le ayuda a respetar las preferencias de los clientes y los requisitos de cumplimiento.

Puede aplicar horas tranquilas a través de conjuntos de reglas, que se pueden asignar a acciones individuales en campañas o recorridos para un control preciso.

## Por qué utilizar las horas tranquilas {#why-quiet-hours}

Las horas tranquilas le ayudan a mejorar la experiencia del cliente y a mantener el cumplimiento de las normas de varias formas:

* **Respetar las preferencias del cliente**: Evite enviar mensajes en momentos inconvenientes (por ejemplo, tarde por la noche o temprano por la mañana), lo que puede afectar negativamente la reputación de la marca y la lealtad del cliente.

* **Mejore la participación**: Al enviar mensajes cuando es más probable que los clientes los vean y actúen en consecuencia, aumenta la eficacia de sus comunicaciones.

* **Cumplimiento legal**: Ciertos estados y regiones prohíben los mensajes de marketing SMS durante horas específicas. Las horas de silencio le ayudan a cumplir con las regulaciones como la TCPA y las leyes de SMS específicas del estado.

* **Optimizar tiempo**: Si ha transcurrido demasiado tiempo desde que se programó un mensaje, puede que ya no sea relevante. Las horas de silencio le permiten descartar mensajes obsoletos o mantenerlos hasta un momento adecuado.

## Cómo funcionan las horas tranquilas {#how-quiet-hours-work}

Las horas tranquilas se implementan mediante reglas comerciales que crea y aplica a sus campañas y recorridos mediante conjuntos de reglas.

Cuando se programa el envío de un mensaje durante un período de horas de inactividad, [!DNL Adobe Journey Optimizer] realiza una de las dos acciones según la configuración:

* **Descartar**: el mensaje se suprime de forma permanente y nunca se envía.
* **Cola**: El mensaje se retiene y se envía automáticamente en cuanto finaliza el período de horas de inactividad.

El sistema evalúa las horas tranquilas en función de la zona horaria del destinatario, que puede ser:

* Zona horaria especificada en el perfil del cliente
* Zona horaria deducida basada en otros datos de perfil y evento
* Zona horaria fija que especifique en la regla

>[!NOTE]
>
>Ventana de presupresión: El sistema comienza a suprimir las comunicaciones 30 minutos antes del inicio de las horas de silencio, lo que garantiza que no se envíen mensajes una vez que comience el periodo de silencio.

## Crear una regla de horas tranquilas {#create-quiet-hours-rule}

Para crear una regla de horas tranquilas:

1. Vaya a **[!UICONTROL Administración]** > **[!UICONTROL Reglas de negocio]**.

1. En la sección **[!UICONTROL Conjuntos de reglas]**, cree un nuevo conjunto de reglas o seleccione uno existente al que desee agregar la regla de horas silenciosas.

1. Haga clic en **[!UICONTROL Crear regla]** y seleccione **[!UICONTROL Horas silenciosas]** como tipo de regla.

1. Configure las opciones de las horas de silencio:

   * **Nombre de regla**: Asigne un nombre descriptivo a la regla.

   * **Período de tiempo**: defina cuándo se deben aplicar las horas de silencio:
      * **Horas del día**: establezca horas específicas (por ejemplo, de 8:00 PM a 8:00 AM)
      * **Días de la semana**: seleccione días específicos (por ejemplo, fines de semana)
      * **Fechas personalizadas**: elige fechas específicas del calendario (por ejemplo, días festivos)

   * **Zona horaria**: Seleccione cómo determinar la zona horaria:
      * **Zona horaria local del usuario**: use la zona horaria del perfil de cada destinatario
      * **Zona horaria específica**: aplique una zona horaria fija (por ejemplo, oriental, central)

   * **Acción**: elige lo que sucederá con los mensajes durante las horas de silencio:
      * **Descartar**: los mensajes se suprimen de forma permanente
      * **Cola**: los mensajes se retienen y se envían cuando terminan las horas de silencio

1. Haga clic en **[!UICONTROL Guardar]** para crear la regla.

## Aplicar horas tranquilas a campañas y recorridos {#apply-quiet-hours}

Una vez creada una regla de horas tranquilas, debe aplicarla a sus campañas o recorridos:

1. Abra la campaña o el recorrido donde desee aplicar las horas de silencio.

1. Desplácese hasta la acción (correo electrónico, SMS, push o WhatsApp) que desee controlar.

1. En la configuración de la acción, busque la sección **[!UICONTROL Conjunto de reglas]**.

1. Seleccione el conjunto de reglas que contiene la regla de horas tranquilas.

1. Guarde los cambios.

La regla de horas de silencio ahora se aplicará a esa acción específica. Todos los mensajes enviados a través de esta acción respetarán la configuración de las horas de silencio.

>[!NOTE]
>
>Las reglas de horas tranquilas se aplican tanto a las comunicaciones programadas como a las activadas por eventos. Asegúrese de que el conjunto de reglas esté configurado correctamente para administrar el caso de uso.

## Consideraciones sobre zonas horarias {#timezone-considerations}

Al usar la opción **Zona horaria local del usuario**, [!DNL Adobe Journey Optimizer] busca la información de zona horaria en el siguiente orden:

1. **Atributo de zona horaria del perfil**: La zona horaria especificada explícitamente en el perfil del cliente
2. **Zona horaria deducida**: Una zona horaria calculada en función de otros datos de perfil y señales de comportamiento

Si no se dispone de ninguna de estas opciones, es posible que el sistema no aplique correctamente las horas silenciosas. Asegúrese de que los perfiles de los clientes incluyan información de zona horaria para obtener resultados óptimos.

Cuando se usa una **zona horaria específica**, todos los destinatarios reciben (o no reciben) mensajes según esa única zona horaria, independientemente de su ubicación real.

## Mecanismos de protección y limitaciones {#guardrails-limitations}

Tenga en cuenta lo siguiente cuando utilice horas de inactividad:

* **Tiempo de activación**: una regla o un conjunto de reglas pueden tardar hasta 20 minutos en activarse por completo. Planifique en consecuencia al crear o modificar reglas.

* **Retraso en la activación de la campaña**: después de asociar las reglas de negocio, espere al menos 10 minutos antes de activar un recorrido o enviar una campaña para asegurarse de que las reglas se aplican correctamente.

* **Límites del conjunto de reglas**: Actualmente, puede tener hasta 3 conjuntos de reglas activos para el dominio del canal y 5 para el dominio de recorrido.

* **Tasa de publicación de mensajes**: cuando finalizan las horas silenciosas y se publican mensajes en cola, se envían a una tasa de hasta 5000 mensajes por segundo por organización.

* **No se admite en**: las reglas de horas de silencio no están disponibles actualmente para la orquestación de Campaign.

* **Ejecución en seco**: Las reglas de horas de silencio no se evalúan durante las ejecuciones de ejecución en seco de recorrido.

## Creación de informes {#reporting}

Puede realizar un seguimiento del impacto de las horas tranquilas en sus campañas y recorridos a través de las funciones de informes estándar:

* **Informe de todo tiempo**: la sección &quot;Razones de exclusión&quot; muestra el volumen de clientes que no recibieron comunicaciones debido a las reglas de horas de inactividad, junto con el nombre específico del conjunto de reglas.

* **Informe en vivo**: (Si está disponible) Muestra estadísticas en tiempo real de los perfiles que están esperando debido a horas de inactividad o que se descartaron debido a horas de inactividad.

## Próximos pasos {#next-steps}

Una vez configuradas y aplicadas las reglas de horas tranquilas, puede:

* Revise la campaña o el recorrido para asegurarse de que las reglas estén correctamente asociadas
* Activar la campaña o el recorrido
* Monitorice el impacto de las horas tranquilas en los informes

