---
solution: Journey Optimizer
product: journey optimizer
title: Administración de husos horarios
description: Obtenga información acerca de la administración de husos horarios
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: zona horaria, propiedades, recorrido, condición, hora, fecha, personalizado
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/PdwGEuWqJcncbkokE0eOhMaEk9L0AmCJ--VZBxxtDDU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 996
ht-degree: 8%

---

# Administración de husos horarios {#timezone_management}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a establecer la zona horaria de un recorrido, ya sea una zona horaria fija o una tomada de cada perfil, para controlar cuándo se ejecutan las actividades basadas en la hora, como condiciones horarias, condiciones de fecha y esperas personalizadas.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="Zona horaria del recorrido"
>abstract="La configuración de la zona horaria determina la zona horaria del recorrido. Cuando se utiliza una zona horaria fija, es la misma para todas las personas que entran en el recorrido."


Puede definir una zona horaria en las [propiedades](../building-journeys/journey-properties.md#timezone) de su recorrido.

Para acceder a las propiedades del recorrido, seleccione el icono de lápiz en la parte superior derecha de la pantalla.

Esta zona horaria se utilizará para cada actividad del recorrido que contenga un elemento de hora como:

* [Condición de tiempo](../building-journeys/conditions.md#time_condition)
* [Condición de fecha](../building-journeys/conditions.md#date_condition)
* [Espera personalizada](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Puede seleccionar una [zona horaria fija](#fixed-timezone) o elegir usar la zona horaria [definida en el perfil de usuario](#timezone-from-profiles).

## Definir una zona horaria fija {#fixed-timezone}

La zona horaria puede ser fija. Borre la zona horaria predefinida y elija una en la lista desplegable. Si utiliza una zona horaria fija, será la misma para todas las personas que entren en el recorrido.

Para ello, en el panel **[!UICONTROL Propiedades del Recorrido]**, seleccione una zona horaria.

![Menú desplegable de selección de zona horaria en las propiedades del recorrido](assets/journey72.png)

## Usar zona horaria del perfil {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="Usar zona horaria del perfil"
>abstract="Esta opción utiliza la zona horaria del perfil en tiempo real en las actividades **Esperar** y **Condición**. Si se ha definido una zona horaria para un perfil, se recuperará y se usará en el recorrido. De lo contrario, la zona horaria será la definida en el campo de zona horaria anterior."

Si el evento de entrada del recorrido tiene un área de nombres, lo que significa que el recorrido puede llegar al servicio Perfil del cliente en tiempo real de [!DNL Adobe Experience Platform], puede que desee utilizar la zona horaria definida en el nivel de perfil. Para ello, en **Properties**, marque **Usar zona horaria del perfil en esperas y condiciones**. Esta opción no está activada de forma predeterminada.

Si se ha definido una zona horaria para un perfil, el recorrido la recupera y la utiliza. Si no es así, la zona horaria utilizada es la definida en el campo de zona horaria.

![Configuración de zona horaria del perfil en fuentes de datos para sincronización personalizada](assets/journey73.png)

>[!NOTE]
>
>La zona horaria del perfil funciona con el campo **timeZone** existente en el grupo de campos **Detalles de preferencia**.

## Uso de zonas horarias en expresiones {#timezone-in-expressions}

Las fechas de inicio y finalización de un recorrido no se pueden vincular a una zona horaria específica. Se asocian automáticamente al huso horario de la instancia.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo establecer la configuración de huso horario en las propiedades del recorrido de trabajo de Adobe Journey Optimizer, eligiendo entre una zona horaria fija aplicada a todos los perfiles o una zona horaria por perfil procedente del Perfil del cliente en tiempo real.

**Intenciones:**
* Establezca una zona horaria fija en un recorrido para que todos los perfiles sigan la misma referencia horaria para las condiciones y esperas
* Habilite la zona horaria por perfil para que las actividades de Espera y Condición utilicen la preferencia de zona horaria almacenada de cada individuo
* Comprender qué actividades de recorrido se ven afectadas por la configuración del huso horario de recorrido
* Identifique el grupo de campos de perfil que almacena el valor de zona horaria individual

**Glosario:**
* **Zona horaria fija**: Zona horaria única seleccionada en Propiedades de Recorrido que se aplica uniformemente a todos los perfiles que entran en el recorrido *(específico del producto)*
* **Zona horaria del perfil**: La zona horaria individual almacenada en el campo `timeZone` del grupo de campos Detalles de preferencia, que se usa cuando la opción &quot;Usar zona horaria del perfil en esperas y condiciones&quot; está habilitada *(específica del producto)*
* **Grupo de campos Detalles de preferencia**: el grupo de campos XDM que contiene el atributo `timeZone` utilizado para la resolución de zona horaria de nivel de perfil

**Protecciones:**
* La opción &quot;Usar zona horaria del perfil en esperas y condiciones&quot; solo está disponible cuando el evento de entrada del recorrido tiene un área de nombres (es decir, el recorrido puede acceder al servicio Perfil del cliente en tiempo real)
* La opción no está activada de forma predeterminada; se utiliza la zona horaria fija a menos que se active explícitamente
* Si la opción está activada pero no se ha definido ninguna zona horaria en el perfil, el recorrido vuelve a la zona horaria fija definida en las propiedades del recorrido
* Las fechas de inicio y finalización del recorrido no se pueden vincular a una zona horaria específica; se asocian automáticamente a la zona horaria de la instancia

**Terminología:**
* Nombre canónico: Time zone management — Acrónimo: none — variantes: timezone configuration, recorrido time zone
* Sinónimos: &quot;zona horaria fija&quot; = &quot;misma para todas las personas&quot;; &quot;zona horaria del perfil&quot; = &quot;Usar zona horaria del perfil en esperas y condiciones&quot;
* No confunda: &quot;zona horaria de recorrido&quot; (se aplica a las actividades) ≠ &quot;zona horaria de instancia&quot; (se aplica a las fechas de inicio y finalización del recorrido, configuradas automáticamente).

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Dónde se establece el huso horario de un recorrido?** — en el panel Propiedades del Recorrido, a la que se puede acceder mediante el icono de lápiz situado en la parte superior derecha del lienzo de recorrido.
* **Q: ¿Qué actividades utilizan la zona horaria de recorrido?** — Condiciones de tiempo, condiciones de fecha y actividades de espera personalizadas.
* **Q: ¿Cómo hago para que cada perfil siga su propia zona horaria local?** — En Propiedades del Recorrido, active la opción &quot;Usar zona horaria del perfil en esperas y condiciones&quot;. Esto requiere que el recorrido tenga un área de nombres para poder llegar al servicio Perfil del cliente en tiempo real.
* **Q: ¿Qué sucede si un perfil no tiene definida una zona horaria y la opción de zona horaria del perfil está habilitada?** — El recorrido vuelve al huso horario fijo definido en el campo huso horario de Propiedades del Recorrido.
* **Q: ¿Qué campo de perfil almacena la zona horaria del individuo?** — El campo `timeZone` dentro del grupo de campos Detalles de preferencia en el esquema de perfil.
* **Q: ¿Puedo establecer las fechas de inicio y finalización del recorrido en una zona horaria específica?** — No. Las fechas de inicio y finalización del recorrido se asocian automáticamente con el huso horario de la instancia y no se pueden vincular a un huso horario personalizado.

+++
