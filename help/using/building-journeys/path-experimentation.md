---
solution: Journey Optimizer
product: journey optimizer
title: Experimentación de rutas
description: Aprenda a utilizar la experimentación de rutas en recorrido
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: experimentación, experimento, recorrido, ruta, optimización, pruebas A/B, multi-armed bandit, escalar el ganador
exl-id: 7241ade3-577c-4bb3-b0c3-017133871ca5
source-git-commit: 9cf7479bcdb12e5d2ebadfcf977b17738a97536d
workflow-type: tm+mt
source-wordcount: '1107'
ht-degree: 4%

---

# Usar experimentación de rutas {#experimentation}

>[!CONTEXTUALHELP]
>id="ajo_path_experiment_success_metric"
>title="Métrica de éxito"
>abstract="La métrica de éxito se utiliza para rastrear y evaluar el tratamiento con mejor rendimiento de un experimento. "
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/orchestrate-journeys/create-journey/success-metrics" text="Configuración y seguimiento de la métrica de recorrido"

La experimentación le permite probar diferentes rutas en función de una división aleatoria para determinar cuál tiene el mejor rendimiento según las métricas de éxito predefinidas.

Para configurar la experimentación de rutas en un recorrido, siga los pasos a continuación.

Supongamos que desea comparar tres rutas:

* una ruta con un correo electrónico;
* una segunda ruta con un nodo **[!UICONTROL Wait]** de dos días y un correo electrónico;
* una tercera ruta con un correo electrónico y luego un mensaje SMS.

1. En la sección **[!UICONTROL Orchestration]**, arrastre y suelte la actividad **[!UICONTROL Optimize]** en el lienzo de recorrido.

1. Añada una etiqueta opcional que pueda resultar útil para identificar la actividad en los registros de los modos de prueba y creación de informes.

1. Seleccione **[!UICONTROL Experimento]** de la lista desplegable **[!UICONTROL Método]**.

   ![Panel de configuración del experimento de ruta](assets/journey-optimize-experiment.png){width=65%}

1. Haga clic en **[!UICONTROL Crear experimento]**.

1. Seleccione la **[!UICONTROL métrica de éxito]** que desee establecer para su experimento. Obtenga más información sobre las métricas disponibles y cómo configurar la lista en [esta sección](success-metrics.md).

   ![Selección de métricas principales y adicionales para el experimento](assets/journey-optimize-experiment-metrics.png){width=80%}

1. Seleccione **[!UICONTROL Tipo de experimento]** para el experimento de ruta:

   * **[!UICONTROL Experimento A/B]**: defina la división de tráfico entre tratamientos al principio de la prueba. El rendimiento se evalúa en función de la métrica principal que haya elegido; los informes muestran el alza observada entre los tratamientos.

   * **[!UICONTROL Bandido multibrazo]** — La división del tráfico entre tratamientos se gestiona automáticamente. Cada 7 días, se revisa el rendimiento de la métrica principal y los pesos se ajustan en consecuencia. Los informes siguen mostrando un alza, al igual que en las pruebas A/B.

   ![Menú desplegable de tipo de experimento en el experimento de ruta](assets/journey-path-experiment-type.png){width=80%}

   ➡️ [Más información acerca de la diferencia entre los experimentos de bandidos A/B y multibrazo](../content-management/mab-vs-ab.md)

1. Puede elegir agregar un grupo **[!UICONTROL Holdout]** a su entrega. Este grupo no entrará en ninguna ruta desde este experimento.

   >[!NOTE]
   >
   >Al activar la barra de alternancia, se llevará automáticamente el 10% de su población. Puede ajustar este porcentaje si es necesario.

   <!--
    DOES THIS APPLY TO PATH EXPERIMENT?
    IMPORTANT: When a holdout group is used in an action for path experimentation, the holdout assignment only applies to that specific action. After the action is completed, profiles in the holdout group will continue down the journey path and can receive messages from other actions. Therefore, ensure that any subsequent messages do not rely on the receipt of a message by a profile that might be in a holdout group. If they do, you may need to remove the holdout assignment.-->

1. Puede asignar un porcentaje preciso a cada **[!UICONTROL Tratamiento]**, o simplemente cambiar en la barra de alternancia **[!UICONTROL Distribuir uniformemente]**.

   ![Regulador de asignación de tratamiento con distribución porcentual](assets/journey-optimize-experiment-treatments.png){width=80%}

1. Habilite el experimento de escalado automático para desplegar automáticamente la variación ganadora del experimento. [Más información sobre cómo escalar al ganador](#scale-winner)

1. Haga clic en **[!UICONTROL Crear]**.

1. Defina los elementos que desee para cada rama resultante del experimento, por ejemplo:

   * Arrastre y suelte una actividad [Email](../email/create-email.md) en la primera rama (**Tratamiento A**).

   * Arrastre y suelte una actividad [Wait](wait-activity.md) de dos días en la primera rama, seguida de una actividad [Email](../email/create-email.md) (**Tratamiento B**).

   * Arrastre y suelte una actividad [Email](../email/create-email.md) en la tercera rama, seguida de una actividad [SMS](../sms/create-sms.md) (**Tratamiento C**).

   ![Ejemplo de experimento de ruta con tres rutas de tratamiento](assets/journey-optimize-experiment-ex.png){width=100%}

1. De manera opcional, use **[!UICONTROL Agregar una ruta alternativa en caso de tiempo de espera o error]** para definir una acción de reserva. [Más información](using-the-journey-designer.md#paths)

1. [Publicar](publish-journey.md) su recorrido.

<!--

    Select a channel action and use the **[!UICONTROL Edit content]** button to access the design tools.

    ![Edit content button in channel action activity](assets/journey-optimize-experiment-edit-content.png){width=70%}

    From there, using the left pane you can navigate between the different contents for each action in your experiment. Select each content and design it as needed.

    ![Content selection panel showing treatments for experiment](assets/journey-optimize-experiment-content.png){width=100%}

-->

Una vez que el recorrido está activo, los usuarios se asignan aleatoriamente para seguir diferentes rutas. [!DNL Journey Optimizer] realiza un seguimiento de la ruta de acceso que tiene el mejor rendimiento y proporciona perspectivas procesables.

Siga el éxito del recorrido con el informe Experimento de ruta de Recorrido. [Más información](../reports/journey-global-report-cja-experimentation.md)

<!--REMOVED WITH GA

>[!CAUTION]
>
>Do not edit the metadata of a path experiment once it has been published. Editing the metadata will disrupt the calculation and reporting of experiment results.
-->

## Casos de uso de experimentos {#uc-experiment}

Los siguientes ejemplos muestran cómo usar la actividad **[!UICONTROL Optimizar]** con el método **[!UICONTROL Experimento]** para determinar qué ruta funciona mejor en general.

+++Eficacia de canal

Compruebe si el envío del primer mensaje por correo electrónico o por SMS genera conversiones más altas.

➡️ Utilice la tasa de conversión como métrica de éxito (por ejemplo: compras, registros).

![Experimento de eficacia de canal que compara correo electrónico con SMS](assets/journey-optimize-experiment-uc-channel.png)

+++

+++Frecuencia del mensaje

Ejecute un experimento para comprobar si enviar un correo electrónico en lugar de tres durante una semana resulta en más compras.

➡️ Use compras o la tasa de cancelación de suscripción como métrica de éxito.

![Experimento de frecuencia de mensajes que prueba un correo electrónico en comparación con tres correos electrónicos](assets/journey-optimize-experiment-uc-frequency.png)

+++

+++Tiempo de espera entre comunicaciones

Compare una espera de 24 horas con una espera de 72 horas antes de un seguimiento para determinar qué tiempo maximiza la participación.

➡️: utilice la tasa de pulsaciones o los ingresos como métrica de éxito.

![Experimento de tiempo de espera que compara retrasos de 24 horas con retrasos de 72 horas](assets/journey-optimize-experiment-uc-wait.png)

+++

## Escalar el ganador {#scale-winner}

>[!AVAILABILITY]
>
>Para los experimentos de rutas, la función Escalar el ganador solo está disponible en recorridos unitarios (activados por eventos y cualificaciones de audiencia).
>
>No está disponible para recorridos de audiencia de lectura.

Escalar el ganador permite desplegar automática o manualmente la variación ganadora de un experimento para todo el público. Esta función garantiza que, una vez que se determina un ganador, puede amplificar su alcance y efectividad sin monitorizar constantemente el experimento.

Puede elegir entre dos modos:

* **Escalado automático**: configure las opciones de escalado automático al crear su experimento eligiendo el momento y las condiciones para escalar el tratamiento ganador o una opción de reserva si no aparece ningún ganador.

* **Escalado manual**: revise manualmente los resultados del experimento e inicie el despliegue del tratamiento ganador, manteniendo un control total sobre el tiempo y las decisiones.

### Escalado automático {#autoscaling}

El escalado automático permite establecer reglas predefinidas sobre cuándo implementar el tratamiento ganador o una alternativa, en función de los resultados del experimento.

Tenga en cuenta que una vez que se ha producido el escalado automático, el escalado manual ya no está disponible.

Para habilitar el escalado automático en los experimentos:

1. Configure el recorrido y el experimento según sea necesario. [Más información](#experimentation)

1. Active la opción de escalado automático al configurar el experimento.

   ![Opción de escalado automático en el experimento de ruta](assets/journey-optimize-autoscale.png)

1. Seleccione cuándo se debe escalar el ganador:

   * En cuanto se encuentre el ganador.
   * Después de que el experimento esté activo durante el tiempo seleccionado.

   La hora de escalado automático debe programarse antes de la fecha de finalización del experimento. Si se establece para una hora posterior a la fecha de finalización, aparecerá una advertencia de validación y el recorrido no se publicará.

   ![Selección automática de tiempo en escala en el experimento de ruta](assets/journey-optimize-autoscale-time.png)

1. Elija el comportamiento de reserva si no se encuentra ningún ganador por tiempo de escala:

   * Continuar el experimento hasta que termine según lo programado.
   * Escalar el tratamiento alternativo después de un tiempo especificado.

Una vez cumplidos todos los parámetros, el tratamiento ganador o alternativo se envía a su audiencia.

### Escalado manual {#manual-scaling}

La escala manual le permite revisar los resultados de los experimentos y decidir cuándo implementar el tratamiento ganador según su propia programación.

Tenga en cuenta que si escala manualmente al ganador antes de la hora programada de escalado automático, se cancela la escala automática.

Para escalar manualmente el ganador de los experimentos:

1. Configure el recorrido y el experimento según sea necesario. [Más información](#experimentation)

1. Deje que el experimento se ejecute hasta que se identifique un ganador o se alcance la relevancia estadística.

1. Abra el recorrido y seleccione la actividad **[!UICONTROL Optimizar]** que contiene el experimento de ruta.

   Revise los resultados en la vista **[!UICONTROL Experimento de ruta]** para identificar el tratamiento de mayor rendimiento.

   ![Ganador de escala manual en el experimento de ruta](assets/journey-optimize-manual-scale-winner.png)

1. Haga clic en **[!UICONTROL Escalar tratamiento]** para insertar el tratamiento ganador al resto de la audiencia.

   <!--![](assets/journey-optimize-scale-treatment.png)-->

1. Seleccione el tratamiento que desee escalar en el menú desplegable y haga clic en **[!UICONTROL Escalar]**.

   ![Escalar selección de tratamiento en experimento de ruta](assets/journey-optimize-scale-treatment.png){width=80%}

Tenga en cuenta que escalar el tratamiento puede tomar hasta una hora. Recibirá una notificación una vez que finalice el proceso de escalado manual.
