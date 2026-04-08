---
solution: Journey Optimizer
product: journey optimizer
title: Segmentación de ruta
description: Aprenda a utilizar la segmentación de rutas en recorrido
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: segmentación, reglas, recorrido, ruta, optimización, personalización
exl-id: b30ce5c9-a0e2-4601-97a3-5bec648368e4
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 7%

---

# Aproveche la segmentación de rutas {#targeting}

>[!CONTEXTUALHELP]
>id="ajo_path_targeting_fallback"
>title="¿Qué es la ruta de reserva?"
>abstract="Las rutas de reserva permiten que el público introduzca una ruta alternativa cuando no se cumplen las reglas de segmentación. </br>Si no selecciona esta opción, los públicos que no cumplan los requisitos para una regla de segmentación no entrarán en la ruta de reserva y saldrán del recorrido."

>[!AVAILABILITY]
>
>Actualmente, esta capacidad está en disponibilidad limitada. Para solicitar acceso, póngase en contacto con su representante de Adobe.

Las reglas de segmentación le permiten determinar reglas o cualificaciones específicas que deben cumplirse para que un cliente pueda entrar en una de las rutas de recorrido, según segmentos de audiencia específicos <!-- depending on profile attributes or contextual attributes-->.

A diferencia de la experimentación, que es una asignación aleatoria de una ruta determinada, la segmentación es determinista en términos de garantizar que la audiencia o el perfil adecuados entren en la ruta especificada.

<!--
With targeting, specific rules can be defined based on:

* **User profile attributes** such as location (eg. geo-targeting), age, or preferences. For example, users in the US receive a "Golden Gate" promotion, while users in France receive an "Eiffel Tower" promotion.

* **Contextual data** such as device type (eg. device-targeting), time of day, or session details. For example, desktop users receive desktop-optimized content, while mobile users receive mobile-optimized content.

* **Audiences** which can be used to include or exclude profiles that have a particular audience membership.
-->

Para configurar la segmentación en un recorrido, siga los pasos a continuación.

1. En la sección **[!UICONTROL Orchestration]**, arrastre y suelte la actividad **[!UICONTROL Optimize]** en el lienzo de recorrido.

1. Añada una etiqueta opcional que pueda resultar útil para identificar la actividad en los registros de los modos de prueba y creación de informes.

1. Seleccione **[!UICONTROL Regla de segmentación]** de la lista desplegable **[!UICONTROL Método]**.

   ![Selección de regla de segmentación en la actividad de optimización](assets/journey-optimize-targeting.png){width=60%}

1. Haga clic en **[!UICONTROL Crear regla de segmentación]**.

1. Haga clic en **[!UICONTROL Crear regla]** > **[!UICONTROL Crear nuevo]** y use el generador de reglas para definir los criterios.

   ![Interfaz del generador de reglas para crear criterios de segmentación](assets/journey-targeting-create-rule.png){width=100%}

   Por ejemplo, defina una regla para los miembros Gold del programa Loyalty (`loyalty.status.equals("Gold", false)`) y una regla para los demás miembros (`loyalty.status.notEqualTo("Gold", false)`).

   ![Regla de segmentación de estado de fidelidad para miembros oro y no oro](assets/journey-targeting-rule.png)

1. También puede hacer clic en **[!UICONTROL Crear regla]** > **[!UICONTROL Seleccionar regla]** para seleccionar una regla de segmentación existente creada desde el menú **[!UICONTROL Reglas]**. [Más información](../experience-decisioning/rules.md)

   ![Seleccione una regla de segmentación existente del menú Reglas](assets/journey-targeting-select-rule.png){width=70%}

   En este caso, la fórmula que compone la regla simplemente se copia en la actividad de recorrido. Cualquier cambio posterior a esa regla desde el menú **[!UICONTROL Reglas]** no afectará la copia del recorrido.

   >[!AVAILABILITY]
   >
   >[La creación de reglas de segmentación](../experience-decisioning/rules.md#create) desde el menú [!DNL Journey Optimizer] dedicado está disponible actualmente para las organizaciones que han adquirido la oferta del complemento Decisioning y están disponibles bajo demanda para las demás organizaciones (disponibilidad limitada).
   >
   >Esta capacidad se implementará progresivamente para todos los clientes. Mientras tanto, póngase en contacto con su representante de Adobe para obtener acceso.

1. Después de agregar una regla, aún puede modificarla. Elija **[!UICONTROL Editar en línea]** para actualizarla sobre la marcha usando el generador de reglas o **[!UICONTROL Seleccionar regla]** para recoger otra regla existente.

   ![Editar opciones de reglas en línea o Seleccionar opciones de reglas para modificar las reglas de segmentación](assets/journey-targeting-modify-rule.png){width=100%}

   >[!NOTE]
   >
   >La edición de una regla en línea no afecta a la regla existente desde la que se origina.

1. Seleccione la opción **[!UICONTROL Habilitar ruta de acceso de reserva]** según sea necesario. Esta acción crea una ruta de reserva para la audiencia que no cumple ninguna de las reglas de segmentación definidas anteriormente.

   >[!NOTE]
   >
   >Si no selecciona esta opción, las audiencias que no cumplan los requisitos para una regla de segmentación no entran en la ruta de reserva y salen del recorrido.

1. Haga clic en **[!UICONTROL Crear]** para guardar la configuración de la regla de segmentación.

1. De nuevo en el recorrido, suelte acciones específicas para personalizar cada ruta. Por ejemplo, cree un correo electrónico con ofertas personalizadas para los miembros de Gold Loyalty y un recordatorio SMS para todos los demás miembros.

   ![Rutas de Recorrido con correo electrónico para miembros Gold y SMS para otros](assets/journey-targeting-paths.png)

1. Si seleccionó la opción **[!UICONTROL Habilitar contenido de reserva]** al definir la configuración de regla, defina una o más acciones para la ruta de reserva que se agregó automáticamente.

   ![Configuración de ruta de acceso de reserva para perfiles no calificados](assets/journey-targeting-fallback.png){width=70%}

1. De forma opcional, use **[!UICONTROL Agregar una ruta alternativa en caso de tiempo de espera o error]** para definir una acción alternativa en caso de que se produzcan problemas. [Más información](using-the-journey-designer.md#paths)

1. Diseñe el contenido apropiado para cada acción correspondiente a cada grupo definido por la configuración de reglas de segmentación.

   En este ejemplo, diseñe un correo electrónico con ofertas especiales para los miembros Gold y un recordatorio SMS para los demás miembros.<!--You can seamlessly navigate between the different contents for each action. ![Content design panel for targeting rule actions](assets/journey-targeting-design.png)-->

1. [Publicar](publish-journey.md) su recorrido.

Una vez que el recorrido está activo, la ruta especificada para cada segmento se procesa para que los miembros oro introduzcan la ruta con las ofertas de correo electrónico, mientras que los demás miembros introducen la ruta con el recordatorio de SMS.

Siga el éxito de su recorrido con el informe de Recorrido. [Más información](../reports/journey-global-report-cja.md#targeting)

## Casos de uso de reglas de segmentación {#uc-targeting}

Los siguientes ejemplos muestran cómo usar la actividad **[!UICONTROL Optimizar]** con el método **[!UICONTROL Regla de segmentación]** para personalizar rutas para diferentes subaudiencias.

+++Canales específicos de segmentos

Los miembros con estatus Gold pueden recibir ofertas personalizadas por correo electrónico, mientras que el resto de los miembros reciben recordatorios por SMS.

<!--➡️ Use the revenue per profile or conversion rate as the optimization metric.-->

![Canales específicos de segmentos dirigidos a miembros Gold con correo electrónico y otros con SMS](assets/journey-optimize-targeting-uc-segment.png)

+++

+++Segmentación basada en el comportamiento

A los clientes que abrieron un correo electrónico pero no hicieron clic se les puede enviar una notificación push, mientras que a los que no abrieron se les envía un SMS.

<!--➡️ Use the click-through rate or downstream conversions as the optimization metric.-->

![Direccionamiento basado en el comportamiento para la participación por correo electrónico con la reserva push o SMS](assets/journey-optimize-targeting-uc-behavior.png)

+++

+++Segmentación del historial de compras

Los clientes que hayan realizado compras recientemente pueden optar por una breve ruta de &quot;agradecimiento + venta cruzada&quot;, mientras que aquellos que no tengan historial de compras ya no tendrán un recorrido de crianza.

<!--➡️ Use the repeat purchase rate or engagement rate as the optimization metric.-->

![Segmentación del historial de compras con ruta de venta cruzada para compradores y ruta de crianza para no compradores](assets/journey-optimize-targeting-uc-purchase.png)

+++
