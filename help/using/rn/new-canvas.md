---
solution: Journey Optimizer
product: journey optimizer
title: Nueva interfaz de recorrido
feature: Release Notes
topic: Content Management
description: Obtenga información acerca del nuevo modelo de recorrido simplificado, la interfaz de usuario del lienzo de recorrido rediseñada y la creación de informes en directo presentada para los recorridos de Journey Optimizer.
keywords: lienzo de recorrido, nuevo modelo de recorrido, creación de informes en directo, diseñador de recorrido
role: User
level: Beginner, Intermediate
hide: true
exl-id: 03828fca-dde7-4b3b-b890-2c007d1245cc
TQID: https://experienceleague.adobe.com/-QKSnBRN9yPYEq5ay9wD-uf4lLduJqmtlFWDnLYt1gk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 1f2a71d3323b6a64b346a83aa58b23aed035eb29
workflow-type: tm+mt
source-wordcount: 727
ht-degree: 1%

---

# Bienvenido al Diseñador de recorridos mejorado {#new-canvas}

[!DNL Journey Optimizer] ahora ofrece un **modelo de recorrido simplificado** que busca mejorar la experiencia del usuario y los procesos internos. A partir de la versión de abril, podrá beneficiarse de las siguientes funciones:

* Un lienzo de recorrido **rediseñado** se ha diseñado para ofrecer una experiencia de interfaz de usuario modernizada
* Una interfaz de usuario de **creación de informes en vivo** disponible directamente en el lienzo del recorrido

>[!NOTE]
>
>Tenga en cuenta que el despliegue de esta función será progresivo. Es posible que no vea los cambios de inmediato.

Para obtener más información acerca de cómo generar recorridos en el nuevo lienzo, vea [usar el diseñador de recorridos](../building-journeys/using-the-journey-designer.md#canvas-capabilities).

## Actualizaciones en el modelo de recorrido {#updates-journey-model}

El nuevo modelo de recorrido estará activo junto al existente, lo que significa que habrá recorridos que usen **dos modelos diferentes**:

* El modelo heredado
* El nuevo modelo

Todos los recorridos del modelo heredado permanecerán en él. Aún puede editarlos, probarlos o publicarlos. Cualquier nueva versión creada a partir de un recorrido en el modelo heredado también permanecerá en él. No hay **cambios funcionales** alrededor de esos recorridos.

Como puede ver en la captura de pantalla siguiente, los nodos tienen forma redondeada, que es la interfaz de usuario antigua para recorridos en el modelo heredado.

![Lienzo de recorrido heredado que muestra nodos de actividad de forma redonda para AirportBeacon y correo electrónico, conectado en un flujo horizontal simple](assets/new-canvas.png)

Sin embargo, cuando **cree un nuevo recorrido** o **duplique uno existente**, estará en el nuevo modelo. Los recorridos en el modelo heredado seguirán siendo compatibles hasta que la mayoría de los clientes pasen al nuevo.

Hay una limitación al nuevo modelo de recorrido; **no será posible copiar y pegar actividades del modelo heredado en el nuevo y viceversa**. Si desea hacerlo, le recomendamos que duplique el recorrido heredado para cambiarlo al nuevo modelo y, a continuación, copie las actividades.

En la captura de pantalla siguiente, puede ver la interfaz de usuario rediseñada para el lienzo de recorrido (solo disponible con el nuevo modelo):

![Lienzo de recorrido rediseñado que muestra cuadros de actividad (miembros de fidelidad leen la audiencia, la condición) que se ramifica en las actividades de correo electrónico de bienvenida y mensajes de Slack](assets/new-canvas2.png)

**Cualquier característica nueva agregada al diseñador de recorrido (incluidos los informes en vivo) solo estará disponible para los recorridos en el nuevo modelo a partir de este momento.**

## Diseño de lienzo de recorrido mejorado {#improved-canvas-design}

Con el nuevo modelo de recorrido presentamos una nueva y mejorada **interfaz de usuario de lienzo de recorrido**, que se adapta perfectamente a las soluciones de [!DNL Adobe CX Enterprise] y al ecosistema de la aplicación, lo que ofrece una experiencia de usuario intuitiva y eficiente. Cualquier recorrido en el nuevo modelo estará en ese nuevo diseño.

![Demostración animada del nuevo diseño de lienzo de recorrido, que muestra un recorrido con los nodos Inicio, una actividad de audiencia de lectura para miembros Lealtad y Finalización](assets/new-canvas3.gif)

Las actividades ahora se representan mediante cuadros cuadrados con las siguientes capacidades:

* La primera línea representa el tipo de actividad que a menudo se sobrescribe con información más contextual (en Leer audiencias, contiene el nombre de la audiencia seleccionada) o con una etiqueta personalizada, si define una.
* La segunda línea siempre representa el tipo de actividad.

![Cuadro de actividad que muestra la etiqueta de actividad &quot;Miembros socio&quot; en la primera línea y el tipo de actividad &quot;Leer audiencia&quot; en la segunda línea](assets/new-canvas4.png)

Esta nueva interfaz de usuario mejora la legibilidad del lienzo de recorrido al proporcionar **tipos y etiquetas de actividad más claros**.

También permite al equipo de productos añadir más información en el lienzo con menos clics. Un ejemplo de &quot;más información&quot; sería la inclusión de informes en directo en el lienzo de recorrido, donde puede ver perfiles que entran y salen de sus actividades debido a errores.

![Cuadro de actividad con métricas de informes activos que muestran 56 perfiles ingresados y 0 errores para la actividad de los miembros socio](assets/new-canvas5.png)

## Creación de informes en directo en el lienzo de recorrido {#live-reporting-canvas}

Además de la distribución mejorada del lienzo de recorrido, se está presentando una nueva característica para permitir que los usuarios vean las métricas de informes en tiempo real de **las últimas 24 horas**, llamada informes en vivo, directamente dentro del lienzo de recorrido. Esto complementa el [informe en vivo de recorrido](../reports/journey-live-report.md) existente.

Para cada actividad dentro de cada recorrido activo que utilice el nuevo modelo, tiene acceso a:


* Recuento de perfiles que entran en esta actividad.
* Recuento de perfiles que salen de esta actividad debido a un error.

![Lienzo de recorrido en vivo que muestra los recuentos de errores y entradas de cada actividad, incluidos los perfiles de prueba, la condición y varias acciones personalizadas de Slack en diferentes rutas](assets/new-canvas6bis.png)

<!--
`
With every live journey on the new model, you will be able to see two types of "last 24 hours" reporting information:

* On a **new insert**, you will see:
    * The number of profiles that have been exported for audience-triggered journeys. You will see the number of profiles available in the last export job alongside the time when that export has been made.
    * The number of profiles who exited the journey
    * The percentage of errors
    ![](assets/new-canvas7.png)
* **On each activity**, you will see the number of profiles who entered that activity and the number who exited because of an error:
    ![](assets/new-canvas8.png)
-->
<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
