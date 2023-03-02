---
title: Añadir restricciones a una oferta
description: Obtenga información sobre cómo definir las condiciones para que se muestre una oferta
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: ccaad8c4d9d26c0fd968e627e7a6bf853f232000
workflow-type: tm+mt
source-wordcount: '1735'
ht-degree: 2%

---

# Añadir restricciones a una oferta {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="Acerca de las restricciones de oferta"
>abstract="Con las restricciones, se puede especificar cómo se prioriza y presenta la oferta al usuario en comparación con otras ofertas."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="Acerca de las restricciones de oferta"
>abstract="Con las restricciones, se puede especificar cómo se prioriza y presenta la oferta al usuario en comparación con otras ofertas."

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="Acerca de la prioridad de oferta"
>abstract="En este campo, se puede especificar la configuración de prioridad para la oferta. Prioridad es un número que se utiliza para clasificar ofertas que cumplen todas las restricciones, como elegibilidad, fechas y límite."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="Establecer prioridad"
>abstract="La prioridad ayuda a definir la prioridad de la oferta en comparación con otras si el usuario cumple los requisitos para más de una oferta. Cuanto más alta sea la prioridad de una oferta, más alta será su prioridad en comparación con otras ofertas."

Las restricciones permiten definir las condiciones en las que se mostrará una oferta.

1. Configure las variables **[!UICONTROL Idoneidad de oferta]**. [Más información](#eligibility)

   ![](../assets/offer-eligibility.png)

1. Defina el **[!UICONTROL Prioridad]** de la oferta comparada con otras si el usuario cumple los requisitos para más de una oferta. Cuanto más alta sea la prioridad de una oferta, más alta será su prioridad en comparación con otras ofertas.

   ![](../assets/offer-priority.png)

1. Especifique la oferta **[!UICONTROL Límite]**, es decir, el número de veces que se presentará la oferta. [Más información](#capping)

   ![](../assets/offer-capping.png)

1. Clic **[!UICONTROL Siguiente]** para confirmar todas las restricciones definidas.

Por ejemplo, si establece las restricciones siguientes:

![](../assets/offer-constraints-example.png)

* La oferta se considerará para los usuarios que coincidan únicamente con la regla de decisión &quot;Clientes de fidelidad de oro&quot;.
* La prioridad de la oferta se establece en &quot;50&quot;, lo que significa que la oferta se presentará antes que las ofertas con una prioridad entre 1 y 49 y después de las que tienen una prioridad de al menos 51.
* La oferta se presentará solo una vez por usuario en todas las ubicaciones.

## Idoneidad {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="Definir idoneidad"
>abstract="De forma predeterminada, cualquier perfil puede optar a la presentación de la oferta, pero se pueden utilizar segmentos o reglas de decisión para restringir la oferta a perfiles específicos."

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="Acerca de los requisitos de oferta"
>abstract="En esta sección, puede utilizar reglas de decisión para determinar qué usuarios cumplen los requisitos para la oferta."
>additional-url="https://video.tv.adobe.com/v/329373" text="Ver vídeo de demostración"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="Estimación total del perfil"
>abstract="Al seleccionar segmentos o reglas de decisión, puede ver información sobre los perfiles cualificados estimados."

El **[!UICONTROL Idoneidad de oferta]** permite restringir la oferta a perfiles específicos que defina mediante segmentos o reglas de decisión.

>[!NOTE]
>
>Más información sobre el uso de **segmentos** frente **reglas de decisión** in [esta sección](#segments-vs-decision-rules).

* De forma predeterminada, la variable **[!UICONTROL Todos los visitantes]** está seleccionada, lo que significa que cualquier perfil puede optar a la presentación de la oferta.

   ![](../assets/offer-eligibility-default.png)

* También puede limitar la presentación de la oferta a los miembros de uno o varios [Segmentos de Adobe Experience Platform](../../segment/about-segments.md).

   Para ello, active la variable **[!UICONTROL Visitantes que pertenecen a uno o varios segmentos]** y, a continuación, añada uno o varios segmentos desde el panel izquierdo y combínelos con la opción **[!UICONTROL Y]** / **[!UICONTROL O]** operadores lógicos.

   ![](../assets/offer-eligibility-segment.png)

* Si desea asociar una [regla de decisión](../offer-library/creating-decision-rules.md) para añadir la oferta, seleccione **[!UICONTROL Por regla de decisión definida]**, luego arrastre la regla deseada del panel izquierdo al **[!UICONTROL Regla de decisión]** área.

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >Actualmente no se admiten ofertas basadas en eventos en [!DNL Journey Optimizer]. Si crea una regla de decisión basada en un [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}, no podrá aprovecharlo en una oferta de.

Al seleccionar segmentos o reglas de decisión, puede ver información sobre los perfiles cualificados estimados. Clic **[!UICONTROL Actualizar]** para actualizar los datos.

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>Las estimaciones de perfil no están disponibles cuando los parámetros de regla incluyen datos que no están en el perfil, como datos de contexto. Por ejemplo, una regla de idoneidad que requiere que el clima actual sea de ≥80 grados.

### Uso de segmentos frente a reglas de decisión {#segments-vs-decision-rules}

Para aplicar una restricción, puede restringir la selección de ofertas a los miembros de una o varias **Segmentos de Adobe Experience Platform**, o puede usar una **regla de decisión**, ambas soluciones correspondientes a diferentes usos.

Básicamente, el resultado de un segmento es una lista de perfiles, mientras que una regla de decisión es una función ejecutada a petición en un único perfil durante el proceso de toma de decisiones. A continuación se detalla la diferencia entre estos dos usos.

* **Segmentos**

   Por un lado, los segmentos son un grupo de perfiles de Adobe Experience Platform que coinciden con una lógica determinada en función de atributos de perfil y eventos de experiencia. Sin embargo, Administración de ofertas no vuelve a calcular el segmento, que puede no estar actualizado al presentar la oferta.

   Más información sobre los segmentos en [esta sección](../../segment/about-segments.md).

* **Reglas de decisión**

   Por otro lado, una regla de decisión se basa en los datos disponibles en Adobe Experience Platform y determina a quién se puede mostrar una oferta. Una vez seleccionada en una oferta o una decisión para una ubicación determinada, la regla se ejecuta cada vez que se toma una decisión, lo que garantiza que cada perfil obtenga la última y la mejor oferta.

   Obtenga más información sobre las reglas de decisión en [esta sección](creating-decision-rules.md).

## Límite {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="Acerca del límite de ofertas"
>abstract="En este campo, se puede especificar cuántas veces se puede presentar la oferta."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="Usar límite"
>abstract="Para evitar saturar a sus clientes, utilice la restricción para definir el número máximo de veces que se puede presentar una oferta."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="Definición de la frecuencia de límite"
>abstract="Puede elegir restablecer el contador de límite de oferta diariamente, semanalmente o mensualmente."

[!CONTEXTUALHELP]
>id=&quot;ajo_decisioning_frequency_capping_impression&quot;
>title=&quot;Impresión&quot;
>abstract=&quot;El uso de impresiones como eventos de límite solo está disponible para canales entrantes.&quot;

El límite se utiliza como restricción para definir el número máximo de veces que se puede presentar una oferta.

Limitar el número de veces que los usuarios obtienen ofertas específicas le permite evitar saturar a sus clientes y, por lo tanto, optimizar cada punto de contacto con la mejor oferta.

Para definir el límite, siga los pasos a continuación.

1. Defina el número de veces que se puede presentar la oferta.

   ![](../assets/offer-capping-times.png)

   >[!NOTE]
   >
   >El número debe ser un número entero bueno que 0.

1. Especifique si desea que el límite se aplique a todos los usuarios o a un perfil específico:

   ![](../assets/offer-capping-total.png)

   * Seleccionar **[!UICONTROL En total]** para definir cuántas veces se puede proponer una oferta en la audiencia de destinatario combinada, es decir, en todos los usuarios.

      Por ejemplo, si es un minorista de electrónica con una &quot;oferta de venta de televisores&quot;, quiere que la oferta solo se devuelva 200 veces en todos los perfiles.

   * Seleccionar **[!UICONTROL Por perfil]** para definir cuántas veces se puede proponer una oferta al mismo usuario.

      Por ejemplo, si es un banco con una oferta de &quot;tarjeta de crédito Platinum&quot;, no desea que esta oferta se muestre más de 5 veces por perfil. De hecho, cree que si el usuario ha visto la oferta 5 veces y no ha actuado en consecuencia, tiene una mayor oportunidad de actuar en la siguiente mejor oferta.
   <!--
    Set the **[!UICONTROL Frequency]** to define how often the capping count is reset. To do so, define the time period for the counting (daily, weekly or monthly) and enter the number of days/weeks/months of your choice.
    ![](../assets/offer-capping-frequency.png)
    >[!NOTE]
    >
    >The reset happens at 12am UTC, on the day that you defined or on the first day of the week/month when applicable. The week start day is Sunday.
    
    For example, if you want the capping count to be reset every 2 weeks, select **[!UICONTROL Weekly]** from the **[!UICONTROL Repeat]** drop-down list and type **2** in the other field. The reset will happen every other Sunday at 12pm UTC.
    -->

1. Si ha definido varios [representaciones](add-representations.md) para la oferta, especifique si desea aplicar un límite **[!UICONTROL En todas las ubicaciones]** o **[!UICONTROL Para cada ubicación]**.

   ![](../assets/offer-capping-placement.png)

   * **[!UICONTROL En todas las ubicaciones]**: los recuentos de límite totalizarán todas las decisiones en las ubicaciones asociadas con la oferta.

      Por ejemplo, si una oferta tiene un **Correo electrónico** ubicación y una **Web** y se establece el límite en **2 por perfil en todas las ubicaciones**, cada perfil podría recibir la oferta hasta dos veces en total, independientemente de la combinación de ubicaciones.

   * **[!UICONTROL Para cada ubicación]**: los recuentos de límite aplicarán recuentos de decisión para cada ubicación por separado.

      Por ejemplo, si una oferta tiene un **Correo electrónico** ubicación y una **Web** y se establece el límite en **2 por perfil para cada ubicación**, cada perfil podría recibir la oferta hasta dos veces para la ubicación de correo electrónico y otras dos veces para la ubicación web.

1. Una vez guardada y aprobada, si la oferta se ha presentado el número de veces especificado en este campo según los criterios y el periodo de tiempo definido, se detendrá su entrega.

El número de veces que se propone una oferta se calcula en el momento de la preparación del correo electrónico. Por ejemplo, si prepara un mensaje de correo electrónico con una serie de ofertas, esos números se cuentan hasta el límite máximo, independientemente de si se envía o no el correo electrónico.

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>Los contadores de límite se restablecerán cuando la oferta caduque o 2 años después de la fecha de inicio de la oferta, lo que ocurra primero. Obtenga información sobre cómo definir la fecha de una oferta en [esta sección](creating-personalized-offers.md#create-offer).

### Impacto del cambio de fechas en el límite {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="Cambiar fechas puede afectar al límite"
>abstract="Si se aplica un límite a esta oferta, este puede verse afectado al cambiar la fecha de inicio o finalización."

Debe proceder con cuidado al cambiar la fecha de una oferta, ya que esto puede tener un impacto en el límite si se cumplen las siguientes condiciones:

* La oferta es [aprobado](#review).
* [Límite](#capping) ya se ha aplicado a la oferta.
* El límite se define por perfil.

>[!NOTE]
>
>Obtenga información sobre cómo definir la fecha de una oferta en [esta sección](creating-personalized-offers.md#create-offer).

Límite por perfil almacena los recuentos de límite de cada perfil. Al cambiar la fecha de inicio y finalización de una oferta aprobada, el recuento de límite de algunos perfiles podría verse afectado según los diferentes escenarios que se describen a continuación.

![](../assets/offer-capping-change-date.png)

Estos son los posibles escenarios en los que **cambio de una fecha de inicio de oferta**:

| Escenario:<br>Si... | Qué sucede:<br>entonces... | Posible impacto en el recuento de límite |
|--- |--- |--- |
| ... la fecha de inicio de la oferta se actualiza antes de que comience la fecha de inicio de la oferta original, | ... el recuento límite comienza en la nueva fecha de inicio. | No |
| ... la nueva fecha de inicio es anterior a la fecha de finalización actual, | ... el límite seguirá con una nueva fecha de inicio y se arrastrará el recuento de límite anterior de cada perfil. | No |
| ... la nueva fecha de inicio es posterior a la fecha de finalización actual, | ... el límite actual caducará y el nuevo recuento de límite volverá a empezar desde 0 para todos los perfiles en la nueva fecha de inicio. | Sí |

Estos son los posibles escenarios en los que **ampliación de una fecha de finalización de oferta**:

| Escenario:<br>Si... | Qué sucede:<br>entonces... | Posible impacto en el recuento de límite |
|--- |--- |--- |
| ... se produce una solicitud de toma de decisiones antes de la fecha de finalización de la oferta original, | ... se actualizará el recuento de límite y se arrastrará el recuento de límite anterior de cada perfil. | No |
| ... no se produce ninguna solicitud de toma de decisiones antes de la fecha de finalización original, | ... el recuento de límite se restablecerá en la fecha de finalización original de cada perfil. El nuevo recuento de límite volverá a empezar desde 0 para cualquier nueva solicitud de toma de decisiones que se produzca después de la fecha de finalización original. | Sí |

**Ejemplo**

Supongamos que tiene una oferta con una fecha de inicio original establecida en **Enero de 1**, con caducidad para **Enero de 31**.

1. Los perfiles X, Y y Z se presentan en la oferta.
1. Activado **Enero de 10**, la fecha de finalización de la oferta se cambia a **15 de febrero**.
1. **Del 11 de enero al 31 de enero**, solo se presenta el perfil Z en la oferta.

   * Debido a que una solicitud de toma de decisiones se produjo antes de la fecha de finalización original **para el perfil Z**, la fecha de finalización de la oferta se puede ampliar a **15 de febrero**.
   * Sin embargo, como no se produjo ninguna actividad antes de la fecha de finalización original de **Perfiles X e Y**, sus contadores caducarán y sus recuentos de límite se restablecerán a 0 en **Enero de 31**.

![](../assets/offer-capping-change-date-ex.png)
