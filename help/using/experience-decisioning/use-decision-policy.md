---
title: Uso de políticas de decisión en mensajes
description: Aprenda a utilizar las políticas de decisión en los mensajes.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
version: Journey Orchestration
exl-id: 35fc3cf2-1b91-4f30-ad71-f9d7d2a0291c
source-git-commit: 71a5b2163500b26ef3ea61e55d18cad539bfeb7f
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 3%

---

# Uso de políticas de decisión en mensajes {#create-decision}

Una vez que haya agregado una política de decisión al contenido, puede utilizar atributos de los elementos de decisión devueltos para la personalización. Para ello, inserte primero el código de la directiva de decisión en el contenido.

>[!CAUTION]
>
>Las directivas de decisión están disponibles para todos los clientes de los canales **Experiencia basada en código**, **SMS** y **Notificación push**.
>
>La toma de decisiones para el canal **Correo electrónico** solo está disponible en disponibilidad limitada. Para solicitar acceso, póngase en contacto con su representante de Adobe. Más información sobre [etiquetas de disponibilidad](../rn/releases.md#availability-labels).

## Inserción del código de la política de decisión {#insert}

>[!BEGINTABS]

>[!TAB Experiencia basada en código]

1. Edite su experiencia basada en código y vaya a **[!UICONTROL Directiva de decisiones]**.

2. Seleccione **[!UICONTROL Insertar directiva]** para agregar el código de la directiva de decisión.

   ![](assets/decision-code-based-add-decision.png)

>[!NOTE]
>
>En el caso de las experiencias basadas en código, si la política de decisión contiene elementos de decisión, incluidos fragmentos, puede aprovechar estos fragmentos en el código de la política de decisión. [Aprenda a aprovechar fragmentos](fragments-decision-policies.md)

>[!TAB Correo electrónico]

1. Abra **Personalization Editor** y vaya a **[!UICONTROL Directivas de decisión]**.

2. Seleccione **[!UICONTROL Insertar sintaxis]** para agregar el código para la directiva de decisión.

   ![](assets/decision-policy-add.png)

   >[!NOTE]
   >
   >Si no aparece la opción de inserción, es posible que ya se haya configurado una directiva de decisión para el componente principal.

3. Si todavía no se ha asignado ninguna ubicación al componente, seleccione una en la lista y haga clic en **[!UICONTROL Asignar]**.

   ![](assets/decision-policy-placement.png)

>[!TAB SMS]

1. Abra **Personalization Editor** y vaya a **[!UICONTROL Directivas de decisión]**.

2. Seleccione **[!UICONTROL Insertar sintaxis]** para agregar el código para la directiva de decisión.

   ![](assets/decision-policy-add-sms-insert-syntax.png)

>[!TAB Push]

1. Abra **Personalization Editor** y vaya a **[!UICONTROL Directivas de decisión]**.

2. Seleccione **[!UICONTROL Insertar sintaxis]** para agregar el código para la directiva de decisión.

   ![](assets/decision-policy-add-push-insert-syntax.png)

>[!IMPORTANT]
>
>Experience Decisioning con notificaciones push requiere una versión específica de Mobile SDK. Antes de implementar esta característica, compruebe [las notas de la versión](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"} para identificar la versión requerida y asegúrese de haber actualizado según corresponda. También puede ver todas las versiones de SDK disponibles para su plataforma en [esta sección](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}.

>[!ENDTABS]

Se agrega el código de la política de decisión. Ahora puede utilizar atributos de los elementos de decisión devueltos para personalizar el contenido.

>[!NOTE]
>
>Para los canales de correo electrónico y de experiencia basados en código, repita esta secuencia una vez por cada elemento de decisión que desee devolver. Por ejemplo, si eligió devolver 2 elementos al [crear la decisión](create-decision-policy.md), repita la secuencia dos veces. Para los canales SMS y Push, solo se puede devolver un elemento de decisión.

## Personalizar con atributos de elementos de decisión {#attributes}

Después de agregar el código para una directiva de decisión en el contenido, todos los atributos de los elementos de decisión devueltos quedan disponibles para la personalización. [Aprenda a trabajar con la personalización](../personalization/personalize.md).

Los atributos se almacenan en el [esquema de catálogo](catalogs.md) &quot;Ofertas&quot;. Se muestran en las siguientes carpetas desde el editor de personalización:
* **Atributos personalizados**: carpeta `_\<imsOrg\>`
* **Atributos estándar**: carpeta `_experience`

Los atributos de elemento de decisión y los atributos contextuales no son compatibles de forma predeterminada en [!DNL Journey Optimizer] fragmentos. Sin embargo, puede utilizar variables globales en su lugar, como se describe a continuación.

![](assets/decision-code-based-decision-attributes.png)

Para agregar un atributo, haga clic en el icono **`+`** junto al atributo. Puede agregar tantos atributos como sea necesario. También puede incluir otros atributos de personalización, como datos de perfil.

* Para los canales **Email** y **Code-based**, ajuste los atributos dentro del bucle `#each` usando corchetes `[ ]` y agregue una coma antes de la etiqueta de cierre `/each`.

  +++Ver ejemplo

  ![](assets/decision-code-based-wrap-code.png)

  +++

* Para los canales **SMS** y **Push**, asegúrese de insertar atributos después del código de sintaxis para la directiva de decisión. Esta sintaxis siempre debe mantenerse en la línea 1.

  +++Ver ejemplo

  ![](assets/decision-added-sms.png)

  +++

  >[!NOTE]
  >Si inserta un atributo de recurso de imagen en contenido SMS o push (por ejemplo, en el título o el cuerpo), el valor del atributo se muestra como una URL. La imagen en sí no se procesa en esos campos.

* Para habilitar el seguimiento de elementos de decisión, agregue el atributo `trackingToken`: `trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

## Previsualización y prueba del contenido

Después de crear el contenido, previsualícelo y pruébelo antes de activar el recorrido o la campaña. Los elementos de decisión se representan en función de los perfiles seleccionados en la interfaz de simulación. [Obtenga información sobre cómo obtener una vista previa y probar contenido](../content-management/preview-test.md).

## Próximos pasos {#final-steps}

Una vez que el contenido esté listo, revise y publique la campaña o el recorrido:

* [Publicación de un recorrido](../building-journeys/publish-journey.md)
* [Revisión y activación de una campaña](../campaigns/review-activate-campaign.md)

En el caso de las experiencias basadas en código, tan pronto como el desarrollador realice una llamada de API o SDK para recuperar contenido para la superficie definida en la configuración de canal, los cambios se aplicarán a su página web o aplicación.

>[!NOTE]
>
>Actualmente no puedes simular contenido basado en decisiones para campañas o recorridos de [experiencia basada en código](../code-based/create-code-based.md). Hay una solución alternativa disponible [aquí](../code-based/code-based-decisioning-implementations.md).

## Uso de paneles de informes

Para ver el rendimiento de sus decisiones, puede ver las métricas de toma de decisiones integradas en la campaña o el informe de recorrido, o crear paneles personalizados de Customer Journey Analytics para medir el rendimiento y obtener información sobre cómo se entregan las políticas de decisión y las ofertas y cómo se relacionan con ellas. [Más información acerca de los informes de decisiones](cja-reporting.md).

![](../reports/assets/cja-decisioning-item-performance.png)
