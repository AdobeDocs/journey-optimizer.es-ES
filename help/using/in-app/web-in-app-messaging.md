---
title: Configuración de la compatibilidad con la mensajería web en la aplicación en Web SDK
description: Obtenga información sobre cómo configurar la extensión de etiquetas Web SDK para admitir la mensajería en la aplicación web.
feature: In App
topic: Content Management
role: Developer
level: Intermediate
keywords: en la aplicación, mensaje, sdk web, configuración
source-git-commit: 4a7f98ce24af02658620485840d11190c0954c09
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 0%

---

# Configuración de la compatibilidad con la mensajería web en la aplicación en Web SDK

Los mensajes en la aplicación son notificaciones que puede enviar a los usuarios dentro de su aplicación web, guiándolos a puntos de interés específicos.

Puede utilizar estas notificaciones para diferentes fines, como promocionar nuevas funciones, presentar ofertas especiales o facilitar la incorporación del usuario.

Con los mensajes en la aplicación, puede interactuar de forma eficaz con su audiencia y dirigirla a aspectos importantes de su aplicación.

## Requisitos previos {#prerequisites}

### Versión de la extensión de etiquetas Web SDK {#extension-version}

La funcionalidad de mensajería en la aplicación web requiere la última versión de la extensión de etiquetas Web SDK.

### Configuración de un CSP para mensajería web en la aplicación {#csp}

Al configurar la mensajería web en la aplicación, debe incluir la siguiente directiva en su CSP:

```
default-src  blob:;
```

Para obtener más información sobre cómo configurar un CSP, consulte [Documentación de recopilación de datos](https://experienceleague.adobe.com/docs/experience-platform/edge/use-cases/configuring-a-csp.html?lang=es){target="_blank"}.

## Configuración de la mensajería en la aplicación web mediante la extensión de etiquetas Web SDK {#tag-extension}

Consulte la [página de configuración de la extensión de etiquetas Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=es){target="_blank"} para saber dónde puede encontrar la configuración que se describe a continuación.

Después de haber [instalado](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=es#install-the-web-sdk-tag-extension){target="_blank"} la extensión de etiquetas Web SDK, siga los pasos a continuación para configurar la extensión para la mensajería web en la aplicación.

En la sección **[!UICONTROL Personalization]**, marque la opción **[!UICONTROL Habilitar almacenamiento personalizado]**. Esta opción permite a Web SDK realizar un seguimiento de las experiencias que el usuario ha visto en las cargas de página.

![Imagen que muestra la opción de almacenamiento personalizado en la página de configuración de la extensión de etiqueta.](assets/enable-personalization-storage.png)

La mensajería web en la aplicación admite dos tipos de déclencheur:

* [Envío de datos a Experience Platform](#send-data-platform)
* [Activación manual de mensajes](#manual-trigger)

Consulte las secciones siguientes para configurar la extensión de etiquetas Web SDK según los déclencheur que desee utilizar.

### Pasos de configuración para el déclencheur **[!UICONTROL Enviar datos al Experience Platform]** {#send-data-platform}

1. Seleccione la propiedad tag que contiene su extensión Web SDK y [cree una nueva regla](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/managing-resources/rules.html#create-a-rule){target="_blank"} con la siguiente configuración:

   * **[!UICONTROL Extensión]**: [!UICONTROL Principal]
   * **[!UICONTROL Tipo de evento]**: [!UICONTROL Biblioteca cargada (Principio de página)]

   ![Imagen que muestra la pantalla de configuración del evento.](assets/rule-configuration.png)

1. Seleccione **[!UICONTROL Conservar cambios]** para guardar la configuración del evento.

1. Ahora necesita agregar una acción a la regla que creó, en la sección [!DNL Actions], seleccione **[!UICONTROL Agregar]**.

   Usar la siguiente configuración de **[!UICONTROL Acción]**:

   * **[!UICONTROL Extensión]**: [!UICONTROL Adobe Experience Platform Web SDK]
   * **[!UICONTROL Tipo de acción]**: [!UICONTROL Enviar evento]

   ![Imagen que muestra la pantalla de edición de regla.](assets/add-action.png)

1. En el lado derecho de la pantalla, en la sección **[!UICONTROL Personalization]**, habilite la opción **[!UICONTROL Procesar decisiones de personalización visuales]**.

   ![Imagen que muestra la pantalla de configuración de personalización.](assets/render-visual-personalization.png)

1. En el lado derecho de la pantalla, en la sección **[!UICONTROL Contexto de decisión]**, defina los pares de **[!UICONTROL Clave]**/**[!UICONTROL Valor]** que utilizó en la configuración de su campaña para cumplir los requisitos para el mensaje en la aplicación.

   ![Imagen que muestra la pantalla de configuración de personalización.](assets/decision-context.png)

1. Seleccione **[!UICONTROL Conservar cambios]** para guardar la configuración.

1. A continuación, debe agregar la regla recién creada a la biblioteca de propiedades de etiquetas. Para ello, vaya a **[!UICONTROL Flujo de publicación]** y seleccione la regla que creó anteriormente.

   ![Imagen que muestra la pantalla de la biblioteca.](assets/add-rule-to-library.png)

1. Después de agregar la regla a la biblioteca, seleccione **[!UICONTROL Guardar y generar en desarrollo]**.

   ![Imagen que muestra la pantalla de configuración de personalización.](assets/publish-flow.png)

El proceso de configuración se ha completado y el mensaje está listo para mostrarse a los usuarios.

### Pasos de configuración para utilizar déclencheur manuales {#manual-trigger}

1. Seleccione la propiedad tag que contiene su extensión Web SDK y [cree una nueva regla](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/managing-resources/rules.html#create-a-rule){target="_blank"} con la siguiente configuración:

   * **[!UICONTROL Extensión]**: [!UICONTROL Principal]
   * **[!UICONTROL Tipo de evento]**: [!UICONTROL Haga clic]

1. Configure el déclencheur de un elemento específico de la página, identificado por un selector CSS de su elección.

   ![Imagen que muestra la pantalla de configuración del evento.](assets/event-configuration-manual.png)

1. Debe agregar una acción a la regla que ha creado. En la sección [!DNL Actions], seleccione **[!UICONTROL Agregar]** y use la siguiente configuración de **[!UICONTROL Acción]**:

   * **[!UICONTROL Extensión]**: [!UICONTROL Adobe Experience Platform Web SDK]
   * **[!UICONTROL Tipo de acción]**: [!UICONTROL Evaluar conjuntos de reglas]

   ![Imagen que muestra la pantalla de edición de regla.](assets/add-action.png)

1. En el lado derecho de la pantalla, habilite la opción **[!UICONTROL Procesar decisiones de personalización visuales]**.

   ![Imagen que muestra la pantalla de configuración de personalización.](assets/manual-trigger-render.png)

1. En el lado derecho de la pantalla, en la sección **[!UICONTROL Contexto de decisión]**, defina los pares de **[!UICONTROL Clave]**/**[!UICONTROL Valor]** que utilizó en la configuración de su campaña para cumplir los requisitos para el mensaje en la aplicación.

   ![Imagen que muestra la pantalla de configuración de personalización.](assets/manual-trigger-decision-context.png)

1. Seleccione **[!UICONTROL Conservar cambios]** para guardar la configuración.

1. Añada la regla recién creada a la biblioteca de propiedades de etiquetas. Para ello, vaya a **[!UICONTROL Flujo de publicación]** y seleccione la regla que creó anteriormente.

   ![Imagen que muestra la pantalla de la biblioteca.](assets/add-rule-to-library.png)

1. Después de agregar la regla a la biblioteca, seleccione **[!UICONTROL Guardar y generar en desarrollo]**.

   ![Imagen que muestra la pantalla de configuración de personalización.](assets/publish-flow.png)

El proceso de configuración se ha completado y el mensaje está listo para mostrarse a los usuarios.

## Configuración de la mensajería web en la aplicación mediante la biblioteca web JavaScript de SDK {#js-library}

Como alternativa al uso de la extensión de etiquetas Web SDK, también puede configurar la mensajería en la aplicación web directamente desde la biblioteca JavaScript de Web SDK.

Puede mostrar mensajes web en la aplicación desde Adobe Journey Optimizer de dos formas.

### Método 1: Recuperación automática del contenido personalizado {#automatic}

Para que Web SDK recupere automáticamente el contenido de personalización al cargar la página, utilice el comando `sendEvent`, como se muestra en el ejemplo siguiente.

```js
  alloy("sendEvent", {
      renderDecisions: true,
      personalization: {
          surfaces: ['#welcome']
      }
  });
```

### Método 2: Recuperación manual del contenido de personalización en función de la acción del usuario {#manual}

Para mostrar el contenido personalizado solo después de que el usuario realice una acción específica, utilice el comando `evaluateRulesets` como se muestra en el ejemplo siguiente.

En este ejemplo, el contenido de personalización se muestra cuando un usuario hace clic en el botón **[!UICONTROL Comprar ahora]** del sitio web.

```js
 alloy("evaluateRulesets", {
     renderDecisions: true,
     personalization: {
         decisionContext: {
             "userAction": "buy_now"
         }
     }
 });
```

### Configuración del almacenamiento de personalización {#personalization-storage}

Puede elegir mostrar mensajes en la aplicación a los usuarios una cantidad determinada de veces, o cada vez que visiten una página, mediante la opción de configuración `personalizationStorageEnabled`.

En la [configuración de Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=es){target="_blank"} establezca la opción `personalizationStorageEnabled` según sus necesidades:

* `personalizationStorageEnabled: true` almacena en déclencheur el mensaje en la aplicación con la frecuencia que definiste en tu [campaña](create-in-app-web.md#configure-inapp).
* `personalizationStorageEnabled: false` almacena en déclencheur el mensaje en la aplicación en cada carga de página.
