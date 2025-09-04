---
solution: Journey Optimizer
product: journey optimizer
title: Actividad de condición
description: Descubra más información sobre la actividad de condición
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: actividad, condición, lienzo, recorrido, optimización
badge: label="Disponibilidad limitada" type="Informative"
hidefromtoc: true
hide: true
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
source-git-commit: 27ae100873fee1a790c7e1e757248f9c3af8e24a
workflow-type: tm+mt
source-wordcount: '1197'
ht-degree: 3%

---

# Optimización de actividad {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Optimización de actividad"
>abstract="La actividad **Optimizar** le permite definir el progreso de las personas en su recorrido mediante la creación de varias rutas basadas en criterios específicos, incluida la experimentación, el direccionamiento y las condiciones específicas."

>[!AVAILABILITY]
>
>Esta capacidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

La actividad **Optimizar** le permite definir el progreso de las personas en su recorrido mediante la creación de múltiples **rutas** basadas en criterios específicos, incluida la experimentación, el direccionamiento y las condiciones específicas, lo que garantiza la máxima participación y éxito para crear recorridos altamente personalizados y eficaces.

Una **ruta de acceso de recorrido** puede consistir en cualquiera de las siguientes opciones:

* secuenciación de las comunicaciones;
* el tiempo transcurrido entre ellas;
* número de comunicaciones;
* o cualquier combinación de estas tres variables.

Por ejemplo, una ruta podría contener un correo electrónico, otra podría contener dos mensajes SMS y una tercera podría contener un correo electrónico, un nodo [Wait](wait-activity.md) de dos horas y, a continuación, un mensaje SMS.

<!--With this feature, [!DNL Journey Optimizer] empowers you with the tools to deliver personalized and optimized paths to your audience, ensuring maximum engagement and success to create highly customized and effective journeys.-->

A través de la actividad **Optimizar** puede:

* Ejecutar [experimentos de ruta](#experimentation)
* Aprovechar [reglas de segmentación](#targeting) en cada ruta de recorrido
* Aplicar [condiciones](#conditions) a sus rutas

![](assets/journey-optimize.png)

Una vez que el recorrido está activo, los perfiles se evalúan según los criterios definidos y, en función de los criterios coincidentes, se envían por la ruta adecuada desde el recorrido.

## Usar experimentación {#experimentation}

La experimentación le permite probar diferentes rutas en función de una división aleatoria para determinar cuál tiene el mejor rendimiento según las métricas de éxito predefinidas.

Para configurar la experimentación de rutas en un recorrido, siga los pasos a continuación.

Supongamos que desea comparar tres rutas:

* una ruta con un correo electrónico;
* una segunda ruta con un nodo **[!UICONTROL Wait]** de dos días y un correo electrónico;
* una tercera ruta con un correo electrónico y luego un mensaje SMS.

1. En la sección **[!UICONTROL Orchestration]**, arrastre y suelte la actividad **[!UICONTROL Optimize]** en el lienzo de recorrido.

1. Añada una etiqueta opcional que pueda resultar útil para identificar la actividad en los registros de los modos de prueba y creación de informes.

1. Seleccione **[!UICONTROL Experimento]** de la lista desplegable **[!UICONTROL Método]**.

   ![](assets/journey-optimize-experiment.png){width=75%}

1. Haga clic en **[!UICONTROL Crear experimento]**.

1. Seleccione la **[!UICONTROL métrica de éxito]** que desee establecer para su experimento.

   <!--Need to have the list of all default metrics + a description for each.
    Explain why the metric selection is important.
    Are there custom metrics? If so explain.
    If possible, add best practices and examples for each metrics (could even be a dedicated section).
    Consider adding an example in this step: For this example, select this metric to test xxx.
    -->

   ![](assets/journey-optimize-experiment-metrics.png){width=70%}

<!--1. Change the **[!UICONTROL Title]** of your treatment to better differentiate them.-->

1. Puede elegir agregar un grupo **[!UICONTROL Holdout]** a su entrega. Este grupo no recibirá ningún contenido de este experimento.

   >[!NOTE]
   >
   >Al activar la barra de alternancia, se llevará automáticamente el 10% de su población. Puede ajustar este porcentaje si es necesario.

   <!--
    [!IMPORTANT]
    >
    >DOES THIS APPLY TO PATH EXPERIMENT? When a holdout group is used in an action for path experimentation, the holdout assignment only applies to that specific action. After the action is completed, profiles in the holdout group will continue down the journey path and can receive messages from other actions. Therefore, ensure that any subsequent messages do not rely on the receipt of a message by a profile that might be in a holdout group. If they do, you may need to remove the holdout assignment.-->

1. Puede asignar un porcentaje preciso a cada **[!UICONTROL Tratamiento]**, o simplemente cambiar en la barra de alternancia **[!UICONTROL Distribuir uniformemente]**.

   ![](assets/journey-optimize-experiment-treatments.png){width=80%}

1. Haga clic en **[!UICONTROL Crear]**.

1. Defina los elementos que desee para cada rama resultante del experimento, por ejemplo:

   * Arrastre y suelte una actividad [Email](../email/create-email.md) en la primera rama (**Tratamiento A**).

   * Arrastre y suelte una actividad [Wait](wait-activity.md) de dos días en la primera rama, seguida de una actividad [Email](../email/create-email.md) (**Tratamiento B**).

   * Arrastre y suelte una actividad [Email](../email/create-email.md) en la tercera rama, seguida de una actividad [SMS](../sms/create-sms.md) (**Tratamiento C**).

   ![](assets/journey-optimize-experiment-ex.png){width=100%}

1. Opcionalmente, use **[!UICONTROL Agregar una ruta alternativa en caso de tiempo de espera o error]** para definir una acción de reserva. [Más información](using-the-journey-designer.md#paths)

1. Seleccione una acción de canal y use el botón **[!UICONTROL Editar contenido]** para acceder a las herramientas de diseño.

   ![](assets/journey-optimize-experiment-edit-content.png){width=70%}

1. Desde allí, con el panel izquierdo puede navegar entre los diferentes contenidos para cada acción de su experimento. Diseñe todo el contenido según sea necesario.

   ![](assets/journey-optimize-experiment-content.png){width=100%}

1. [Publicar](publishing-the-journey.md) su recorrido.

Una vez que el recorrido está activo, los usuarios se asignan aleatoriamente para seguir diferentes rutas. [!DNL Journey Optimizer] realiza un seguimiento de la ruta de acceso que tiene el mejor rendimiento y proporciona perspectivas procesables.

Siga el éxito de su recorrido con el [informe de recorrido](../reports/journey-global-report-cja.md) de Optimización/Experimento. <!--Need a doc page on reporting specific to path experimentation in journey - [Path experimentation journey report](../xxx) such as what we have for [Experimentation campaign report](../reports/campaign-global-report-cja-experimentation.md)-->

### Casos de uso de experimentos {#uc-experiment}

Los siguientes ejemplos muestran cómo usar la actividad **[!UICONTROL Optimizar]** con el método **[!UICONTROL Experimento]** para determinar qué ruta funciona mejor en general.

+++Eficacia de canal

Compruebe si el envío del primer mensaje por correo electrónico o por SMS genera conversiones más altas.

* Utilice la tasa de conversión como métrica de optimización (por ejemplo: compras, registros).

<!--![](assets/journey-optimize-experiment-uc.png)-->

+++

+++Frecuencia del mensaje

Ejecute un experimento para comprobar si enviar un correo electrónico en lugar de tres durante una semana resulta en más compras.

* Utilice las compras o la tasa de cancelación de suscripción como métrica de optimización.

+++

+++Tiempo de espera entre comunicaciones

Compare una espera de 24 horas con una espera de 72 horas antes de un seguimiento para determinar qué tiempo maximiza la participación.

* Utilice la tasa de pulsaciones o los ingresos como métrica de optimización.

+++

## Aproveche la segmentación {#targeting}

La segmentación le permite determinar reglas o cualificaciones específicas que deben cumplirse para que un cliente pueda entrar en una de las rutas de recorrido, según segmentos de audiencia específicos <!-- depending on profile attributes or contextual attributes-->.

A diferencia de la experimentación, que es una asignación aleatoria de una ruta determinada, la segmentación es determinista en términos de garantizar que la audiencia o el perfil adecuados entren en la ruta especificada.

<!--With targeting, specific rules can be defined based on:

* **User profile attributes** such as location (eg. geo-targeting), age, or preferences. For example, users in the US receive a "Golden Gate" promotion, while users in France receive an "Eiffel Tower" promotion.

* **Contextual data** such as device type (eg. device-targeting), time of day, or session details. For example, desktop users receive desktop-optimized content, while mobile users receive mobile-optimized content.

* **Audiences** which can be used to include or exclude profiles that have a particular audience membership.-->

Para configurar la segmentación en un recorrido, siga los pasos a continuación.

1. En la sección **[!UICONTROL Orchestration]**, arrastre y suelte la actividad **[!UICONTROL Optimize]** en el lienzo de recorrido.

1. Añada una etiqueta opcional que pueda resultar útil para identificar la actividad en los registros de los modos de prueba y creación de informes.

1. Seleccione **[!UICONTROL Regla de segmentación]** de la lista desplegable **[!UICONTROL Método]**.

   ![](assets/journey-optimize-targeting.png){width=75%}

1. Haga clic en **[!UICONTROL Crear regla de segmentación]**.

1. Utilice el generador de reglas para definir los criterios. Por ejemplo, defina una regla para los miembros Gold del programa Loyalty (`loyalty.status.equals("Gold", false)`) y una regla para los demás miembros (`loyalty.status.notEqualTo("Gold", false)`).

   ![](assets/journey-targeting-rule.png)

1. Seleccione **[!UICONTROL Habilitar contenido de reserva]** según sea necesario. El contenido de reserva permite que su audiencia reciba un contenido predeterminado cuando no se cumplen las reglas de segmentación. Si no selecciona esta opción, las audiencias que no cumplan los requisitos para una regla de segmentación definida anteriormente no introducen una ruta de reserva.

1. Guarde la configuración de reglas de segmentación.

1. De nuevo en el recorrido, suelte acciones específicas para personalizar cada ruta. Por ejemplo, cree un correo electrónico con ofertas personalizadas para los miembros de Gold Loyalty y un recordatorio SMS para todos los demás miembros.

   ![](assets/journey-targeting-paths.png)

1. Opcionalmente, use **[!UICONTROL Agregar una ruta alternativa en caso de tiempo de espera o error]** para definir una acción de reserva. [Más información](using-the-journey-designer.md#paths)

1. Diseñe el contenido apropiado para cada acción correspondiente a un grupo definido por la configuración de reglas de segmentación. Puede navegar sin problemas entre los diferentes contenidos para cada acción.

   ![](assets/journey-targeting-design.png)

   En este ejemplo, diseñe un correo electrónico con ofertas especiales para los miembros oro y un recordatorio SMS para los demás miembros.

1. [Publicar](publishing-the-journey.md) su recorrido.

Una vez que el recorrido está activo, la ruta especificada para cada segmento se procesa para que los miembros oro introduzcan la ruta con las ofertas de correo electrónico, mientras que los demás miembros introducen la ruta con el recordatorio de SMS.

### Casos de uso de segmentación {#uc-targeting}

Los siguientes ejemplos muestran cómo usar la actividad **[!UICONTROL Optimizar]** con el método **[!UICONTROL Segmentación]** para personalizar rutas para diferentes subaudiencias.

+++Canales específicos de segmentos

Los miembros con estatus Gold pueden recibir ofertas personalizadas por correo electrónico, mientras que el resto de los miembros reciben recordatorios por SMS.

* Utilice los ingresos por perfil o la tasa de conversión como métrica de optimización.

<!--![](assets/journey-optimize-targeting-uc.png)-->

+++

+++Segmentación basada en el comportamiento

A los clientes que abrieron un correo electrónico pero no hicieron clic se les puede enviar una notificación push, mientras que a los que no abrieron se les envía un SMS.

* Utilice la tasa de pulsaciones o las conversiones descendentes como métrica de optimización.

+++

+++Segmentación del historial de compras

Los clientes que hayan realizado compras recientemente pueden optar por una breve ruta de &quot;agradecimiento + venta cruzada&quot;, mientras que aquellos que no tengan historial de compras ya no tendrán un recorrido de crianza.

* Utilice la tasa de compra repetida o la tasa de participación como métrica de optimización.

+++

## Añada una condición  {#conditions}

Puede agregar una condición para definir cómo progresan las personas a través del recorrido creando varias rutas basadas en criterios específicos. También puede configurar una ruta alternativa para gestionar tiempos de espera o errores, lo que garantiza una experiencia sin problemas.

![](assets/journey-condition.png)

Obtenga información sobre cómo definir una condición en [esta sección](conditions.md).

Los siguientes tipos de condiciones están disponibles:

* [Condición de Data Source](condition-activity.md#data_source_condition)
* [Condición de tiempo](condition-activity.md#time_condition)
* [División porcentual](condition-activity.md#percentage_split)
* [Condición de fecha](condition-activity.md#date_condition)
* [Límite de perfil](condition-activity.md#profile_cap)
