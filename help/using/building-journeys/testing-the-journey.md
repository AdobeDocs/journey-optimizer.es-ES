---
solution: Journey Optimizer
product: journey optimizer
title: Prueba del recorrido
description: Aprenda a probar el recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: comprobación, recorrido, comprobación, error, solución de problemas
exl-id: 9937d9b5-df5e-4686-83ac-573c4eba983a
source-git-commit: 7c0b0fe67a5a2665f7cf7bdce4a36207d7bcef56
workflow-type: tm+mt
source-wordcount: '1522'
ht-degree: 11%

---

# Prueba del recorrido{#testing_the_journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_test"
>title="Prueba del recorrido"
>abstract="Utilice perfiles de prueba para probar el recorrido antes de publicarlo. Esto permite analizar el flujo de los particulares en el recorrido y solucionar los problemas antes de la publicación."

Utilice perfiles de prueba para probar el recorrido antes de publicarlo. Este modo le permite ejecutar una prueba del recorrido e identificar problemas mediante los perfiles de prueba.

Solo los perfiles de prueba pueden introducir un recorrido en el modo de prueba. Puede crear nuevos perfiles de prueba o convertir los perfiles existentes en perfiles de prueba. Obtenga más información sobre los perfiles de prueba en [esta sección](../audience/creating-test-profiles.md).

>[!NOTE]
>
>Antes de probar el recorrido, debe resolver todos los errores. Obtenga información sobre cómo comprobar errores antes de probar en [esta sección](../building-journeys/troubleshooting.md#checking-for-errors-before-testing).

Para utilizar el modo de prueba, siga estos pasos:

1. Para activar el modo de prueba, active la variable **[!UICONTROL Prueba]** , situado en la esquina superior derecha.

   ![](assets/journeytest1.png)

1. Si el recorrido tiene al menos uno **Esperar** actividad, configure el **[!UICONTROL Tiempo de espera]** para definir el tiempo que durará cada actividad de espera y tiempo de espera de evento en el modo de prueba. El tiempo predeterminado es 10 segundos para esperas y tiempos de espera de evento. Esto garantizará que obtenga los resultados de la prueba rápidamente.

   ![](assets/journeytest_wait.png)

   >[!NOTE]
   >
   >Cuando se utiliza un evento de reacción con un tiempo de espera en un recorrido, el tiempo de espera predeterminado y el valor mínimo son 40 segundos. Consulte [esta sección](../building-journeys/reaction-events.md).

1. Utilice el **[!UICONTROL Déclencheur de un evento]** para configurar y enviar eventos al recorrido.

   ![](assets/journeyuctest1.png)

1. Configure los diferentes campos esperados. En el **Identificador de perfil** , introduzca el valor del campo utilizado para identificar el perfil de prueba. Puede ser la dirección de correo electrónico, por ejemplo. Asegúrese de enviar eventos relacionados con los perfiles de prueba. Consulte [esta sección](#firing_events).

   ![](assets/journeyuctest1-bis.png)

1. Una vez recibidos los eventos, haga clic en **[!UICONTROL Mostrar registro]** para ver el resultado de la prueba y verificarlo. Consulte [esta sección](#viewing_logs).

   ![](assets/journeyuctest2.png)

1. Si hay algún error, desactive el modo de prueba, modifique el recorrido y pruebe de nuevo. Una vez realizadas las pruebas, puede publicar el recorrido. Consulte [esta página](../building-journeys/publishing-the-journey.md).

## Notas importantes {#important_notes}

* En el modo de prueba, puede activar eventos mediante la interfaz.
* Solo se permite a las personas marcadas como &quot;perfiles de prueba&quot; en el servicio Perfil del cliente en tiempo real entrar en el recorrido probado. Consulte esta [sección](../audience/creating-test-profiles.md).
* El modo de prueba solo está disponible en recorridos de borrador que utilizan un área de nombres. El modo de prueba debe comprobar si una persona que entra en el recorrido es un perfil de prueba o no y, por lo tanto, debe poder acceder a Adobe Experience Platform.
* El número máximo de perfiles de prueba que puede introducir un recorrido durante una sesión de prueba es de 100.
* Al deshabilitar el modo de prueba, se vacían las recorridos de todas las personas que lo ingresaron en el pasado o que se encuentran actualmente en él. También borra la creación de informes.
* Puede habilitar/deshabilitar el modo de prueba tantas veces como sea necesario.
* No puede modificar el recorrido cuando el modo de prueba está activado. En el modo de prueba, puede publicar directamente el recorrido, sin necesidad de desactivar el modo de prueba antes.
* Al llegar a una división, siempre se elige la rama superior. Puede reorganizar la posición de las ramas divididas si desea que la prueba elija una ruta diferente.
* Para optimizar el rendimiento y evitar el uso de recursos obsoletos, todos los recorridos del modo de prueba que no se hayan activado durante una semana volverán al **Borrador** estado.
* Los eventos activados por el modo de prueba se almacenan en conjuntos de datos dedicados. Estos conjuntos de datos están etiquetados de la siguiente manera: `JOtestmode - <schema of your event>`

## Déclencheur de eventos {#firing_events}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_configuration"
>title="Configurar el modo de prueba"
>abstract="Si el recorrido contiene varios eventos, utilice el menú desplegable para seleccionar un evento. A continuación, configure para cada evento los campos pasados y la ejecución del envío del evento."

Utilice el **[!UICONTROL Déclencheur de un evento]** para configurar un evento que hará que una persona entre en el recorrido.

>[!NOTE]
>
>Cuando se almacena en déclencheur un evento en modo de prueba, se genera un evento real, lo que significa que también se producirá un recorrido que escuche este evento.

Como requisito previo, debe saber qué perfiles están marcados como perfiles de prueba en Adobe Experience Platform. De hecho, el modo de prueba solo permite estos perfiles en la recorrido y el evento debe contener un ID. El ID esperado depende de la configuración del evento. Puede ser un ECID o una dirección de correo electrónico, por ejemplo. El valor de esta clave debe añadirse en **Identificador de perfil** field.

Si el recorrido contiene varios eventos, utilice el menú desplegable para seleccionar un evento. A continuación, configure para cada evento los campos pasados y la ejecución del envío del evento. La interfaz de le ayuda a pasar la información correcta en la carga útil de evento y a asegurarse de que el tipo de información es correcto. El modo de prueba guarda los últimos parámetros utilizados en una sesión de prueba para su uso posterior.

![](assets/journeytest4.png)

La interfaz de le permite pasar parámetros de evento simples. Si desea pasar colecciones u otros objetos avanzados en el evento, puede hacer clic en **[!UICONTROL Vista de código]** para ver el código completo de la carga útil y modificarlo. Por ejemplo, puede copiar y pegar información de evento preparada por un usuario técnico.

![](assets/journeytest5.png)

Un usuario técnico también puede utilizar esta interfaz para componer cargas útiles de eventos y eventos de déclencheur sin tener que utilizar una herramienta de terceros.

Al hacer clic en **[!UICONTROL Enviar]** botón, comienza la prueba. La progresión del individuo en el recorrido se representa mediante un flujo visual. El camino se vuelve verde progresivamente a medida que el individuo se mueve a través del recorrido. Si se produce un error, se muestra un símbolo de advertencia en el paso correspondiente. Puede colocar el cursor sobre él para mostrar más información sobre el error y acceder a los detalles completos (cuando estén disponibles).

![](assets/journeytest6.png)

Cuando se selecciona un perfil de prueba diferente en la pantalla de configuración de evento y se vuelve a ejecutar la prueba, el flujo visual se borra y muestra la ruta del nuevo individuo.

Al abrir un recorrido en prueba, la ruta mostrada corresponde a la última prueba ejecutada.

## Modo de prueba para recorridos basados en reglas {#test-rule-based}

El modo de prueba también está disponible para recorridos que utilizan un evento basado en reglas. Para obtener más información sobre los eventos basados en reglas, consulte [esta página](../event/about-events.md).

Al activar un evento, la variable **Configuración de eventos** La pantalla de permite definir los parámetros de evento que se superarán en la prueba. Para ver la condición de ID de evento, haga clic en el icono de información de objeto en la esquina superior derecha. También hay disponible información del objeto junto a cada campo que forma parte de la evaluación de reglas.

![](assets/jo-event8.png)

## Modo de prueba para eventos empresariales {#test-business}

Cuando se utiliza un [evento empresarial](../event/about-events.md), utilice el modo de prueba para almacenar en déclencheur una sola entrada del perfil de prueba en el recorrido, simular el evento y pasar el ID de perfil correcto. Debe pasar los parámetros de evento y el identificador del perfil de prueba que va a introducir el recorrido en la prueba. En el modo de prueba, no hay ningún modo de &quot;Vista de código&quot; disponible para los recorridos basados en eventos empresariales.

Tenga en cuenta que cuando se déclencheur un evento empresarial por primera vez, no se puede cambiar la definición de evento empresarial en la misma sesión de prueba. Solo puede hacer que la misma persona o una persona diferente entren en el recorrido pasando el mismo identificador u otro. Si desea cambiar los parámetros de evento empresarial, debe detener e iniciar de nuevo el modo de prueba.

## Ver registros {#viewing_logs}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_logs"
>title="Registros del modo de prueba"
>abstract="El botón Mostrar registro muestra los resultados de las pruebas en formato JSON. Estos resultados muestran el número de particulares dentro del recorrido y su estado."

El **[!UICONTROL Mostrar registro]** permite ver los resultados de la prueba. Esta página muestra la información actual del recorrido en formato JSON. Un botón permite copiar nodos completos. Debe actualizar manualmente la página para actualizar los resultados de la prueba de la recorrido.

![](assets/journeytest3.png)


>[!NOTE]
>
>En los registros de prueba, en caso de error al llamar a un sistema de terceros (fuente de datos o acción), se muestran el código de error y la respuesta de error.

Se muestra el número de individuos (técnicamente, se denominan instancias) que están actualmente dentro del recorrido. Esta es una información útil que se muestra para cada individuo:

* _Id_: el ID interno del individuo en la recorrido. Se puede utilizar con fines de depuración.
* _etapa actual_: la etapa en la que el individuo se encuentra en el recorrido. Recomendamos añadir etiquetas a las actividades para identificarlas más fácilmente.
* _etapa actual_ > fase: el estado del recorrido de la persona (en ejecución, terminado, error o tiempo de espera agotado). Para obtener más información, vaya más abajo.
* _etapa actual_ > _extraInfo_: descripción del error y otra información contextual.
* _etapa actual_ > _fetchErrors_: información sobre los errores de recuperación de datos que se produjeron durante este paso.
* _externalKeys_: el valor de la fórmula clave definida en el evento.
* _enrichedData_: los datos que el recorrido ha recuperado si el recorrido utiliza fuentes de datos.
* _transitionHistory_: lista de pasos que ha seguido el usuario. Para los eventos, se muestra la carga útil.
* _actionExecutionErrors_ : información sobre los errores producidos.

Estos son los diferentes estados del recorrido de un individuo:

* _Ejecutando_: la persona se encuentra actualmente en el recorrido.
* _Finalizado_: el individuo se encuentra al final del recorrido.
* _Error_: el individuo se detiene en el recorrido debido a un error.
* _Tiempo agotado_: el individuo se detiene en el recorrido debido a un paso que tomó demasiado tiempo.

Cuando se activa un evento con el modo de prueba, se genera automáticamente un conjunto de datos con el nombre del origen.

El modo de prueba crea automáticamente un Evento de experiencia y lo envía a Adobe Experience Platform. El nombre del origen de este evento de experiencia es &quot;Eventos de prueba del Journey Orchestration&quot;.

