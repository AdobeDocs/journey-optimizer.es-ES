---
title: Prueba del canal personalizado
description: Obtenga información sobre cómo probar la conexión, simular contenido y probar los mensajes de canal personalizados en Adobe Journey Optimizer antes de activarlos.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 2%

---


# Prueba del canal personalizado {#test-custom-channel}

Antes de activar un recorrido o una campaña que utilice un canal personalizado, compruebe que el punto de conexión sea accesible, que la autenticación funcione y que los tokens de personalización se resuelvan correctamente para los perfiles de destinatario.

## Prueba de la conexión desde el Generador de canales {#test-connection}

Mientras un canal personalizado está en estado **[!UICONTROL Borrador]**, usa el botón **[!UICONTROL Probar]** del Generador de canales para enviar una solicitud de prueba a tu punto final y validar la conexión de extremo a extremo antes de activarla. [Más información](create-custom-channel.md#test-connection)

Esta prueba confirma:

* Que se puede acceder al extremo desde las direcciones IP salientes de [!DNL Journey Optimizer].
* Que las credenciales de autenticación configuradas son válidas.
* Que el extremo devuelve una respuesta HTTP 2xx.

Compruebe los registros del sistema externo para confirmar que la solicitud de prueba se recibió con los encabezados y la estructura de carga esperados.

## Simulación del contenido con perfiles de prueba {#simulate-content}

La característica **[!UICONTROL Simular contenido]** resuelve las expresiones de personalización con perfiles de prueba para que pueda inspeccionar la carga útil exacta que se enviará antes de que se envíe un mensaje real.

1. En la pantalla de acción de recorrido o de edición de campaña, haga clic en **[!UICONTROL Simular contenido]**.

1. Haga clic en **[!UICONTROL Agregar perfil de prueba]** y seleccione uno o más perfiles. [Más información sobre cómo crear perfiles de prueba](../audience/creating-test-profiles.md)

1. Revise la carga útil resuelta en el panel de vista previa. Para cada perfil de prueba, compruebe:

   * Todos los tokens de personalización (por ejemplo, `{{profile.person.name.firstName}}`) se han reemplazado con los valores esperados del perfil.
   * No quedan tokens sin resolver (se muestran como cadenas vacías o sintaxis `{{...}}` literal).
   * Se rellenan los campos de carga útil requeridos.
   * Las funciones de ayuda producen el resultado formateado esperado.

>[!TIP]
>
>Realice pruebas con varios perfiles que representen diferentes segmentos de audiencia para detectar casos extremos; por ejemplo, perfiles a los que les faltan atributos opcionales, conjuntos de caracteres no latinos o valores nulos en campos personalizados.

## Envío de una prueba {#send-proof}

Para validar la entrega de extremo a extremo antes de activarlo, envíe una prueba a un conjunto de destinatarios de prueba:

1. En el panel **[!UICONTROL Simular contenido]**, cambie a la pestaña **[!UICONTROL Enviar prueba]**.

1. Añada los perfiles que desee utilizar. Puede cargar un archivo CSV con perfiles que no estén definidos como perfiles de prueba en [!DNL Journey Optimizer].

1. Haga clic en **[!UICONTROL Enviar revisión]**. [!DNL Journey Optimizer] llama a su extremo externo con la carga útil personalizada para cada perfil seleccionado.

1. Compruebe el sistema externo para confirmar que se recibieron las cargas útiles de prueba. En el caso de los canales de mensajería (por ejemplo, WeChat o Kakao Talk), compruebe que el mensaje aparece en el dispositivo de destino o en la aplicación de mensajería.

El resultado de la prueba se muestra con los mismos patrones de validación que la prueba por correo electrónico: los campos obligatorios, las discrepancias de tipos y los errores de validación de esquema aparecen antes de que se envíe la prueba.

Más información sobre cómo enviar pruebas en [campañas](../campaigns/create-campaign.md#send-proof) y [recorridos](../building-journeys/testing-the-journey.md).

## Prueba en el modo de prueba de recorrido {#test-journey}

Para la validación de recorrido de extremo a extremo, active el recorrido en **[!UICONTROL Modo de prueba]**:

1. En el lienzo del recorrido, haga clic en **[!UICONTROL Probar]** en el área superior derecha.

1. Configure el evento de déclencheur o seleccione un perfil de prueba para un recorrido activado por audiencia.

1. Haga clic en **[!UICONTROL Déclencheur un evento]** o permita que el perfil entre a través de una actividad de **[!UICONTROL Leer audiencia]**.

1. Observe el flujo en el lienzo. Cuando un perfil alcanza el nodo de acción del canal personalizado, [!DNL Journey Optimizer] llama al extremo externo con la carga útil personalizada.

1. Compruebe los registros del sistema externo para confirmar que la solicitud se recibió correctamente.

1. Haga clic en **[!UICONTROL Detener prueba]** cuando haya terminado.

Obtenga más información sobre los recorridos de prueba en [modo de prueba](../building-journeys/testing-the-journey.md).

## Simulación de un recorrido {#simulate-journey}

El modo **Simulation** de [!DNL Journey Optimizer] le permite validar su recorrido de extremo a extremo mediante usuarios simulados (entidades temporales similares a perfiles que no persisten en Adobe Experience Platform) sin que sea necesario crear previamente perfiles de prueba.

En el caso de los canales personalizados, la simulación resuelve las expresiones de personalización y procesa la previsualización de carga útil para cada usuario simulado, de modo que puede verificar que el contenido correcto se entregaría antes de publicarse.

Para simular un recorrido con un canal personalizado:

1. En el lienzo del recorrido, haz clic en **[!UICONTROL Simular]** en el área superior derecha.

1. Agregue usuarios simulados manualmente o genérelos con la opción **[!UICONTROL Simulación rápida]** con tecnología de IA.

1. Configure los eventos de entrada necesarios y, a continuación, almacene en déclencheur los usuarios simulados a través del recorrido.

1. Cuando un usuario simulado llega al nodo de acción del canal personalizado, inspeccione la carga útil resuelta en el panel de vista previa para confirmar que los tokens de personalización y la estructura de carga útil son correctos.

>[!NOTE]
>
>La simulación está disponible tanto para recorridos en borrador como activos, y utiliza usuarios simulados temporales que no cuentan para cuotas de perfil o llamadas de extremo reales.

[Más información sobre la simulación de recorrido](../building-journeys/simulate-journey-gs.md)

## Lista de comprobación previa a la activación {#checklist}

Antes de activar el recorrido o la campaña, confirme lo siguiente:

* La prueba de conexión del Generador de canales se realizó correctamente (extremo accesible, autenticación válida).
* Las cargas simuladas muestran los valores esperados para todos los perfiles de prueba.
* No quedan tokens de personalización sin resolver en la carga.
* Se rellenan todos los campos de carga útil requeridos.
* Su sistema externo envió y recibió correctamente una prueba.
* Las rutas de error en la actividad de acción de recorrido (si está configurada) administran los escenarios de error según lo esperado.

Una vez finalizada la prueba, proceda a activarla. [Descubra cómo](create-custom-experience.md#activate)
