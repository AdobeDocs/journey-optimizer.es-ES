---
solution: Journey Optimizer
product: journey optimizer
title: Creación de su primer recorrido
description: Pasos clave para crear su primer recorrido con Adobe Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, primero, inicio, inicio rápido, segmento, evento, acción
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 22%

---

# Creación de su primer recorrido{#jo-quick-start}

## Requisitos previos{#start-prerequisites}

Para enviar mensajes con recorridos, se requieren las siguientes configuraciones:

1. **Configurar un evento**: si desea configurar los recorridos de forma unitaria cuando se reciba un evento, debe configurar un evento. Puede definir la información esperada y cómo procesarla. Este paso lo realiza un **usuario técnico**. [Más información](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Creación de segmentos**: el recorrido también puede escuchar segmentos de Adobe Experience Platform para enviar mensajes en lote a un conjunto específico de perfiles. Para ello, debe crear segmentos. [Más información](../segment/about-segments.md).

   ![](assets/segment2.png)

1. **Configuración de la fuente de datos**: puede definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos, por ejemplo en las condiciones. También se configura una fuente de datos integrada de Adobe Experience Platform en el momento del aprovisionamiento. Este paso no es necesario si solo se aprovechan los datos de los eventos durante el recorrido. Este paso lo realiza un **usuario técnico**. [Más información](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurar una acción**: Si utiliza un sistema de terceros para enviar mensajes, puede crear una acción personalizada. Obtenga más información en esta [sección](../action/action.md). Este paso lo realiza un **usuario técnico**. Si utiliza las funciones de mensajes integradas de Journey Optimizer, solo tiene que añadir una acción de canal al recorrido y diseñar el contenido.

   ![](assets/custom2.png)

## Cree su recorrido{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Cree su recorrido"
>abstract="Esta pantalla muestra la lista de recorridos existentes. Abra un recorrido o haga clic en “Crear recorrido” y combine las diferentes actividades de evento, orquestación y acción para crear sus escenarios multicanal de varios pasos."

Este paso lo realiza el **usuario empresarial**. Aquí es donde crea sus recorridos. Combine las distintas actividades de evento, orquestación y acción para crear sus escenarios de canal cruzado de varios pasos.

Estos son los pasos principales para enviar mensajes a través de recorridos:

1. En la sección del menú ADMINISTRACIÓN DE RECORRIDOS , haga clic en **[!UICONTROL Recorridos]**. Se muestra la lista de recorridos.

   ![](assets/interface-journeys.png)

1. Haga clic en **[!UICONTROL Crear Recorrido]** para crear un nuevo recorrido.

1. Edite las propiedades del recorrido en el panel de configuración que se muestra en el lado derecho. Obtenga más información en esta [sección](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Para empezar, arrastre y suelte un evento o un **Leer segmento** actividad desde la paleta al lienzo. Para obtener más información sobre el diseño de recorrido, consulte [esta sección](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Arrastre y suelte los siguientes pasos que el individuo debe seguir. Por ejemplo, puede añadir una condición seguida de una acción del canal. Para obtener más información sobre las actividades, consulte [esta sección](using-the-journey-designer.md).

1. Pruebe el recorrido con perfiles de prueba. Obtenga más información en esta [sección](testing-the-journey.md)

1. Publique el recorrido para activarlo. Obtenga más información en esta [sección](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Monitorice el recorrido con las herramientas de sistema de informes dedicadas para medir la efectividad de su recorrido. Obtenga más información en esta [sección](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## Definir las propiedades del recorrido {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Propiedades del recorrido"
>abstract="Esta sección muestra las propiedades del recorrido. De forma predeterminada, los parámetros de solo lectura están ocultos. La configuración disponible depende del estado del recorrido, de los permisos y de la configuración del producto."

Haga clic en el icono de lápiz, en la parte superior derecha para acceder a las propiedades del recorrido.

Puede cambiar el nombre del recorrido, añadir una descripción, permitir la reentrada, elegir las fechas de inicio y finalización y, como usuario administrador, definir una **[!UICONTROL Tiempo de espera y error]** duración.

Para los recorridos en directo, esta pantalla muestra la fecha de publicación y el nombre del usuario que publicó el recorrido.

La variable **Copiar detalles técnicos** le permite copiar información técnica sobre el recorrido que el equipo de asistencia puede utilizar para solucionar problemas. Se copia la siguiente información: UID de JourneyVersion, OrgID, orgName, sandboxName, lastDedeployBy, lastDedeployAt.

![](assets/journey32.png)

### Entrada{#entrance}

De forma predeterminada, los nuevos recorridos permiten volver a entrar. Puede desmarcar la casilla **Permitir la reentrada** para recorridos de &quot;una toma&quot;, por ejemplo, si desea ofrecer un regalo único cuando una persona entra en una tienda.

Cuando la variable **Permitir la reentrada** está activada, la opción **Período de espera de reentrada** se muestra. Este campo permite definir el tiempo de espera antes de permitir que un perfil vuelva a entrar en el recorrido en recorridos unitarios (empezando por un evento o una calificación de segmentos). Esto evita que los recorridos se activen varias veces por error para el mismo evento. De forma predeterminada, el campo se establece en 5 minutos.

Obtenga más información sobre la administración de la entrada de perfiles en [esta sección](entry-management.md).

### Administrar acceso {#access}

Para asignar etiquetas de uso de datos principales o personalizadas al recorrido, haga clic en el botón **[!UICONTROL Administrar acceso]** botón. [Obtenga más información sobre Control de acceso a nivel de objeto (OLA)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### Zona horaria y zona horaria del perfil {#timezone}

La zona horaria se define en el nivel de recorrido.

Puede introducir una zona horaria fija o utilizar perfiles de Adobe Experience Platform para definir la zona horaria del recorrido.

Si se define una zona horaria en el perfil de Adobe Experience Platform, se puede recuperar en el recorrido .

Para obtener más información sobre la administración de huso horario, consulte [esta página](../building-journeys/timezone-management.md).

### Fechas de inicio y finalización {#dates}

Puede definir una **Fecha de inicio**. Si no ha especificado ninguno, se definirá automáticamente en el momento de la publicación.

También puede agregar una **Fecha final**. Esto permite que los perfiles salgan automáticamente cuando se alcanza la fecha. Si no especifica una fecha de finalización, los perfiles pueden permanecer hasta el tiempo de espera de recorrido predeterminado (generalmente 30 días, 7 días con la oferta de complemento Escudo de salud). La única excepción son los recorridos recurrentes de segmentos leídos con **Forzar la reentrada en la recurrencia** activado, que finalizan en la fecha de inicio de la siguiente aparición.

### Tiempo de espera y error en las actividades de recorrido {#timeout_and_error}

Al editar una acción o actividad de condición, puede definir una ruta alternativa en caso de error o de tiempo de espera. Si el procesamiento de la actividad que interroga a un sistema de terceros supera el tiempo de espera definido en las propiedades del recorrido (**[!UICONTROL Tiempo de espera y error]** ), se elige la segunda ruta para realizar una posible acción de reserva.

Los valores autorizados están entre 1 y 30 segundos.

Le recomendamos que defina una **[!UICONTROL Tiempo de espera y error]** si el recorrido distingue entre horas (ejemplo: reaccionar a la ubicación en tiempo real de una persona) porque no puede retrasar la acción durante más de unos segundos. Si el recorrido es menos sensible al tiempo, puede utilizar un valor más largo para dar más tiempo al sistema llamado para enviar una respuesta válida.

Recorrido también utiliza un tiempo de espera global. Consulte la [sección siguiente](#global_timeout).

### Tiempo de espera de recorrido global {#global_timeout}

Además del [timeout](#timeout_and_error) utilizado en actividades de recorrido, también existe un tiempo de espera de recorrido global que no se muestra en la interfaz y que no se puede cambiar. Este tiempo de espera detendrá el progreso de las personas en el recorrido 30 días después de su entrada. Esto significa que el recorrido de una persona no puede durar más de 30 días. Después del tiempo de espera de 30 días, se eliminan los datos del individuo. Las personas que sigan fluyendo en el recorrido al final del tiempo de espera se detendrán y se tendrán en cuenta como errores en los informes.

>[!NOTE]
>
>Los recorridos no reaccionan directamente a las solicitudes de exclusión, acceso o eliminación de privacidad. Sin embargo, el tiempo de espera global garantiza que las personas nunca permanezcan más de 30 días en ningún recorrido.

Debido al tiempo de espera de recorrido de 30 días, cuando no se permite la reentrada del recorrido, no podemos asegurarnos de que el bloqueo de reentrada funcione más de 30 días. De hecho, como eliminamos toda la información sobre las personas que entraron en el recorrido 30 días después de su entrada, no podemos conocer a la persona ingresada anteriormente, hace más de 30 días.

