---
title: Probar experiencias basadas en código
description: Obtenga información sobre cómo probar experiencias basadas en código en Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 9a1c148c-a6c3-406b-8f2e-1cf8b8239e75
source-git-commit: effc706cfa56eca21cde0f26fe7b6332d3728b74
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 24%

---

# Probar experiencias basadas en código {#test-code-based}

## Vista previa de la experiencia basada en código {#preview-code-based}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Vista previa de la experiencia basada en código"
>abstract="Obtenga una simulación del aspecto que tendrá su experiencia basada en código."

Para mostrar una previsualización de la experiencia basada en código modificada, siga los pasos a continuación.

>[!CAUTION]
>
>Debe tener perfiles de prueba disponibles para simular qué ofertas se les enviarán. Aprenda a [crear perfiles de prueba](../audience/creating-test-profiles.md).

1. En el recorrido o la campaña, desde el editor de personalización o la pantalla de edición de contenido, seleccione **[!UICONTROL Simular contenido]**.

   ![](assets/code-based-campaign-simulate.png)

1. Haga clic en **[!UICONTROL Administrar perfiles de prueba]** para seleccionar uno o más perfiles de prueba.

1. Se muestra una previsualización de la experiencia modificada basada en código.

Encontrará información detallada sobre cómo seleccionar perfiles de prueba y obtener una vista previa del contenido en [esta sección](../content-management/preview.md).

>[!NOTE]
>
>Actualmente no puedes simular contenido desde la interfaz de usuario en una campaña o recorrido de experiencia basado en código usando [Decisioning](../experience-decisioning/gs-experience-decisioning.md). Hay una solución disponible en [esta sección](../experience-decisioning/create-decision.md#test-and-publish).


## Previsualización en el dispositivo {#preview-on-device}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device"
>title="Previsualización de la experiencia basada en código en un dispositivo real"
>abstract="Obtenga una previsualización de sus experiencias personalizadas directamente en el explorador o en sus dispositivos móviles, para ver cómo se ven en dispositivos reales."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_web"
>title="Previsualización de la experiencia web basada en código en un dispositivo"
>abstract="Escanee el código QR o copie el vínculo para previsualizarlo en el dispositivo."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_mobile"
>title="Previsualización de la experiencia móvil basada en código en un dispositivo"
>abstract="Escanee el código QR o copie el vínculo para previsualizarlo en el dispositivo. Una vez conectado, introduzca el pin en el dispositivo. Es posible que tenga que reiniciar la aplicación para ver los cambios cada vez que actualice los vínculos de previsualización."

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_refresh"
>title="Actualice el vínculo de previsualización para que se refleje la vista actual"
>abstract="La previsualización en el dispositivo mostrará el contenido a partir del momento en que creó o actualizó el vínculo de previsualización. Si ha modificado el contenido o ha seleccionado un perfil de prueba o tratamiento diferente, actualice la previsualización para que se refleje la vista actual."

Al crear experiencias basadas en código para páginas web o aplicaciones móviles, puede obtener una vista previa de sus experiencias personalizadas directamente en el explorador o en sus dispositivos móviles, para ver cómo se ven estas experiencias en dispositivos reales.

>[!WARNING]
>
>La vista previa en el dispositivo no está disponible al usar los atributos contextuales [directivas de decisión](../experience-decisioning/create-decision.md) o [personalización](../personalization/personalization-build-expressions.md).

1. En la pantalla **[!UICONTROL Simular]**, haga clic en el botón **[!UICONTROL Abrir opciones de vista previa]**. Las opciones de vista previa dependen de la plataforma seleccionada en la [configuración basada en código](code-based-configuration.md#create-code-based-configuration).

1. Si usa una [plataforma web](code-based-configuration.md#web) en su configuración basada en código, el campo de solo lectura de **[!UICONTROL URL de vista previa del dispositivo]** está rellenado previamente con la URL ingresada para la configuración de canal actual.

   ![](assets/preview-on-device-web.png)

   Puede:

   * Seleccione el botón **[!UICONTROL Copiar vínculo]** y pegue el vínculo en una pestaña del explorador. También puede compartir el vínculo con su equipo y las partes interesadas, que pueden obtener una vista previa de la nueva experiencia en cualquier explorador antes de que los cambios se activen.

   * Haz clic en **[!UICONTROL Abrir en ficha nueva]** para abrir el vínculo en el explorador actual.

   * Escanee el código QR con su dispositivo móvil para abrir el vínculo de vista previa en un navegador móvil.

1. Si usa [plataformas móviles](code-based-configuration.md#mobile) (iOS/Android) en su configuración basada en código, el campo de solo lectura **[!UICONTROL Vínculo profundo]** está rellenado previamente con el valor de **[!UICONTROL Vista previa de URL]** introducido en la configuración de canal de la plataforma seleccionada.

   Alterne entre las pestañas **[!UICONTROL iOS]** y **[!DNL Android]** para obtener una vista previa de su experiencia en la plataforma que elija.

   ![](assets/preview-on-device-mobile.png)

   Puede:

   * Seleccione el botón **[!UICONTROL Copiar vínculo]** y comparta el vínculo con su equipo y las partes interesadas, que pueden obtener una vista previa de la nueva experiencia en cualquier explorador móvil antes de que los cambios se activen.

   * Escanee el código QR con su dispositivo móvil para abrir el vínculo de vista previa directamente en la aplicación móvil. Debes introducir el PIN en tu dispositivo para establecer la sesión de [Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/implement-assurance){target="_blank"}.

     >[!NOTE]
     >
     >**Adobe Experience Platform Assurance** es un producto de Adobe Experience Cloud que te ayudará a inspeccionar, probar, simular y validar la forma en que recopilas datos o sirves experiencias en tu aplicación móvil. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/assurance/home){target="_blank"}

1. Si está usando cualquier [otra plataforma](code-based-configuration.md#other) en su configuración basada en código, elija el [URI de superficie](code-based-surface.md#surface-uri) que desee previsualizar en la lista desplegable.

   ![](assets/preview-on-device-other.png)

   * Seleccione el botón **[!UICONTROL Copiar vínculo]** para pegar el vínculo en una pestaña del explorador o compártalo con su equipo y las partes interesadas.

   * Si ha añadido varios URI a la configuración (hasta 10), puede seleccionar cualquiera de ellos para previsualizarlos.

1. Se generan vínculos de vista previa para el perfil de prueba seleccionado y, si usa [Experimento de contenido](../content-management/content-experiment.md) en su recorrido o campaña, para el tratamiento seleccionado.

   <!--If you have modified the content or selected a different treatment or test profile, scroll down to the bottom of the **[!UICONTROL Preview on device]** pop-up and click **[!UICONTROL Refresh preview link]** to reflect the current state.

   ![](assets/preview-on-device-refresh.png)-->

   <!--When creating a content experiment, you need to select a given treatment and click the **[!UICONTROL Simulate content]** button to obtain the link corresponding to that treatment, then select another treatment, click the **[!UICONTROL Simulate content]** button to obtain a new preview link, and so on.-->

   Al actualizar el contenido o seleccionar un perfil de prueba o un tratamiento diferentes, el vínculo de vista previa se actualiza automáticamente. Puede copiar el vínculo en diferentes pestañas del explorador y comparar las experiencias.
