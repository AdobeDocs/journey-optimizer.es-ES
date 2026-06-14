---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del seguimiento de URL
description: Obtenga información sobre cómo configurar el seguimiento de URL en el nivel de configuración de canal de correo electrónico
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: ajustes, correo electrónico, configuración
exl-id: 5a12280c-b937-4cd9-a1ef-563bab48e42e
TQID: https://experienceleague.adobe.com/q1T-efX3vK77d1PfKA8mWU73w6Cj4-H95RynkHHg16U
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fae48155-b23f-40d2-a252-a25bce350b4d
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 521
ht-degree: 61%

---

# Seguimiento de URL {#url-tracking}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a definir los parámetros de seguimiento de URL en el nivel de configuración del canal de correo electrónico para que se adjunten a los vínculos de contenido y se capturen en los análisis web y los informes de rendimiento.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Definir los parámetros de seguimiento de URL"
>abstract="Utilice esta sección para adjuntar automáticamente parámetros de seguimiento a las direcciones URL presentes en el contenido del correo electrónico. Esta función es opcional."

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="Previsualizar los parámetros de seguimiento de URL"
>abstract="Revise cómo se adjuntarán los parámetros de seguimiento a las direcciones URL presentes en el contenido del correo electrónico."

Al configurar una nueva [configuración de canal de correo electrónico](email-settings.md), puede definir **[!UICONTROL parámetros de seguimiento de URL]** para medir la eficacia de sus esfuerzos de marketing entre canales. La activación de esta función es opcional.

Los parámetros definidos en la sección correspondiente se anexan al final de las direcciones URL incluidas en el contenido del mensaje de correo electrónico. A continuación, puede capturar estos parámetros en herramientas de análisis web como Adobe Analytics o Google Analytics y crear varios informes de rendimiento.

>[!NOTE]
>
>El orden de los parámetros de seguimiento de URL que se anexan a la dirección URL es aleatorio y no se puede controlar. Si el sistema requiere que los parámetros se introduzcan en un orden concreto, deberá analizarlos y reordenarlos por su cuenta.

Puede añadir hasta 10 parámetros de seguimiento con el botón **[!UICONTROL Añadir nuevo parámetro]**.

![](assets/preset-url-tracking.png){width="80%"}

Para configurar un parámetro de seguimiento de URL, puede escribir directamente los valores deseados en los campos **[!UICONTROL Nombre]** y **[!UICONTROL Valor]**.

También puede editar cada campo **[!UICONTROL Valor]** con el [editor de personalización](../personalization/personalization-build-expressions.md). Haga clic en el icono de edición para abrir el editor. Desde allí, puede seleccionar los atributos contextuales disponibles y/o editar directamente el texto.

![](assets/preset-url-tracking-editor.png)

Están disponibles los siguientes valores predefinidos a través del editor de personalización:

* **ID de perfil de mensaje**: atributo orientado al mensaje que identifica de forma exclusiva cada mensaje enviado a cada perfil de destino en una entrega.

* **ID de oferta**: ID de la oferta que se ha utilizado en el correo electrónico.

* **ID de acción de origen**: ID de la acción de correo electrónico añadida al recorrido o a la campaña.

  >[!NOTE]
  >
  >Es posible que los recorridos que se cerraron o no se volvieron a publicar después de un cambio de producto no se puedan rellenar `context.system.source.actionId` en las direcciones URL de seguimiento, lo que da como resultado marcadores de posición vacíos (por ejemplo, `cid=em-acou-adob{}`). Para asegurarse de que los parámetros de seguimiento se rellenen correctamente, [vuelva a publicar el recorrido afectado](../building-journeys/publish-journey.md#journey-create-new-version) o quite la referencia a este campo de contexto para los recorridos cerrados. Obtenga más información en [Solucionar problemas de ejecución de recorrido en directo](../building-journeys/troubleshooting-execution.md#tracking-parameters-closed-journeys).

* **Nombre de acción de origen**: nombre de la acción de correo electrónico añadida al recorrido o a la campaña.

* **ID de origen**: ID del recorrido o de la campaña con el que se envió el correo electrónico.

* **Nombre de origen**: nombre del recorrido o de la campaña con el que se envió el correo electrónico.

* **ID de versión de origen**: ID de la versión de recorrido o campaña con la que se envió el correo electrónico.

>[!NOTE]
>
>Puede combinar la escritura de valores de texto y el uso de atributos contextuales desde el editor de personalización. Cada campo **[!UICONTROL Valor]** puede contener un número de caracteres hasta el límite de 5 KB.

<!--You can drag and drop the parameters to reorder them.-->

A continuación, se muestran ejemplos de URL compatibles con Adobe Analytics y Google Analytics.

* URL compatible con Adobe Analytics: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* URL compatible con Google Analytics: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

Puede obtener una vista previa dinámica de la URL de seguimiento resultante. Cada vez que se añade, edita o quita un parámetro, la vista previa se actualiza automáticamente.

![](assets/preset-url-tracking-preview.png)

>[!NOTE]
>
>También puede añadir parámetros de seguimiento personalizados dinámicos a los vínculos presentes en el contenido del correo electrónico. [Más información](surface-personalization.md#personalize-url-tracking)
