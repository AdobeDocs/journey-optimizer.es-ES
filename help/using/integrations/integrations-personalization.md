---
solution: Journey Optimizer
product: journey optimizer
title: Habilitar integraciones externas
description: Integre integraciones externas en el proceso de creación de canales para enriquecer el contenido con información personalizada y dinámica
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: integración
source-git-commit: 4cc3c959fe08c1d574a5d041bf7721441bc96f97
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 1%

---


# Uso de integraciones externas para la personalización {#integrations-personalization}

Antes de usar integraciones externas en el contenido, confirme que un administrador ha **configurado y activado** cada integración (extremo, autenticación, directivas, carga de respuesta y activación) como se describe en [Trabajar con integraciones](integrations.md).

Puede agregar hasta **3** integraciones por **[!UICONTROL fragmento]** y hasta **5** en el mensaje. Las integraciones que solo provienen de fragmentos no se contabilizan en **5**.

## Aplicación de la personalización de la integración al contenido {#apply-integration-personalization}

Como experto en marketing, puede utilizar integraciones configuradas para personalizar el contenido. Siga estos pasos:

1. Acceda al contenido de su campaña y haga clic en **[!UICONTROL Agregar personalización]** desde su **[!UICONTROL Componentes]** de texto o HTML.

   [Más información sobre los componentes](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Vaya a la sección **[!UICONTROL Integraciones]** y haga clic en **[!UICONTROL Abrir integraciones]** para ver todas las integraciones activas.

   Tenga en cuenta que **los fragmentos de Journey Optimizer** están disponibles con las integraciones, pero solo admiten canales salientes. Una vez publicado un fragmento, la adición y el guardado de nuevas integraciones están desactivados para evitar el impacto en los recorridos y campañas existentes.

   ![](assets/external-integration-content-2.png)

1. Seleccione una integración y haga clic en **[!UICONTROL Guardar]**.

   ![](assets/external-integration-content-3.png)

1. Habilite el modo **[!UICONTROL Pills]** para desbloquear el menú de integración avanzada.

   ![](assets/external-integration-content-4.png)

1. Al crear la personalización de la integración, el asistente de integraciones incluye un campo **`required`** que define cómo interactúan los errores o la falta de datos con el contenido predeterminado:

   * **`required=true`** (predeterminado): se detiene el procesamiento de ese mensaje. El envío se excluye con **`ExternalDataLookupExclusion`** y esa exclusión se registra en el **conjunto de datos de comentarios del mensaje**.
   * **`required=false`**: la variable de resultado se establece en **`null`** y el procesamiento continúa. Utilice texto predeterminado, reserva o lógica condicional en la plantilla para que los perfiles no reciban contenido vacío cuando la integración no devuelva datos.

     ![](assets/external-integration-content-8.png)

1. Para completar la configuración de la integración, defina los atributos de la integración, que se especificaron anteriormente durante [configuración](integrations.md#configure).

   Puede asignar valores a estos atributos mediante valores estáticos, que permanecen constantes, o atributos de perfil, que extraen información de forma dinámica de los perfiles de usuario.

   ![](assets/external-integration-content-5.png)

1. Una vez definidos los atributos de integración, ahora puede usar los campos de integración en el contenido para mensajes personalizados haciendo clic en el icono ![agregar](assets/do-not-localize/Smock_Add_18_N.svg).

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >Los tokens de la plantilla solo deben utilizar campos que el administrador exponga en la configuración de la integración. Por ejemplo, `{{weatherResponse.temperature}}` es válido cuando se expone `temperature`; `{{weatherResponse.humidity}}` se rechaza en el editor si `humidity` no se expuso.

1. Haga clic en **[!UICONTROL Guardar]**.

La personalización de la integración ahora se aplica correctamente al contenido, lo que garantiza que cada destinatario reciba una experiencia relevante y adaptada en función de los atributos que haya configurado.

![](assets/external-integration-content-7.png)

<!--

## Map one API call to another {#map-integration-chain}

You can **chain** integrations so that values returned by one active integration drive the inputs (path, headers, or query parameters) of another. That lets you build a real-time data flow in a single message without custom code.

Before you start, make sure that:

* An administrator has configured and activated every integration you need. See [Configure your Integration](integrations.md).
* Variable path placeholders, headers, and query parameters are set up in the integration configuration with marketer-facing labels.
* The administrator exposed the response fields you need in each integration's **[!UICONTROL Response payload]** so they appear when authoring.

In the below example, a reservation system integration returns a flight booking reference from the profile context. A separate flight-information integration expects that reference as a **path variable**. In the personalization editor, you map the second integration's variable to a field from the first integration's response, instead of a static value or profile attribute alone.

1. Open your message or fragment and place the cursor where you want personalized content (for example, a **[!UICONTROL Text]** field).

1. Open the personalization editor and go to **[!UICONTROL Integrations]** → **[!UICONTROL Open integrations]**.

1. Select the integration whose output will supply the downstream input (in the example, the reservation or profile API that returns the flight identifier).

1. Define that integration's inputs as usual—static values, profile attributes, or other allowed mappings—then save so its response is available for chaining.

    >[!NOTE]
    >
    > Fields must appear in the administrator-defined response payload for each integration. You cannot reference response properties that were not exposed in configuration.

1. Select the **second** integration (for example, the API that needs the flight number or booking reference on the URL path).

1. For each input that must come from the first call—often a **path variable** or **variable** header/query parameter—choose the mapping source that references the **first integration's response** (for example, the flight booking reference field from the reservation payload). Do not use a static test value if you need live, profile-specific data.

1. Insert the response tokens you need in the content (for example, destination name from the flight API, loyalty balance from a loyalty integration) using the ![add](assets/do-not-localize/Smock_Add_18_N.svg) control.

1. Save the personalization.

When you **simulate** or send, Journey Optimizer resolves integrations in order: the first call runs with the profile context you configured; its output is used to build the second request. Different integrations may run at simulation time and at send time according to your setup and channel behavior.

-->

## Vídeo práctico {#video}

Este vídeo muestra cómo **Integraciones** conectan Adobe Journey Optimizer a API externas para que pueda extraer datos y contenido en directo en **canales salientes**, correo electrónico, SMS y push para una personalización más relevante.

>[!VIDEO](https://video.tv.adobe.com/v/3484121/?captions=spa&learn=on)
