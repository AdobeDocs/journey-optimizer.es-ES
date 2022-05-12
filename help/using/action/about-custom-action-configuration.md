---
solution: Journey Optimizer
title: Configurar una acción personalizada
description: Obtenga información sobre cómo configurar una acción personalizada
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: bb582374f69e5c4113e22c7caed1a23d2c9ac231
workflow-type: tm+mt
source-wordcount: '1496'
ht-degree: 4%

---

# Configurar una acción personalizada {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Acciones personalizadas"
>abstract="Si utiliza un sistema de terceros para enviar mensajes o si desea que los recorridos envíen llamadas de API a un sistema de terceros, utilice acciones personalizadas para configurar su conexión con el recorrido. Por ejemplo, puede conectarse a los siguientes sistemas con acciones personalizadas: Epsilon, Slack, [Desarrollador de Adobe](https://developer.adobe.com/), Firebase, etc."

Si utiliza un sistema de terceros para enviar mensajes o si desea que los recorridos envíen llamadas de API a un sistema de terceros, utilice acciones personalizadas para configurar su conexión con el recorrido. Por ejemplo, puede conectarse a los siguientes sistemas con acciones personalizadas: Epsilon, Slack, [Desarrollador de Adobe](https://developer.adobe.com){target=&quot;_blank&quot;}, Firebase, etc.

Las acciones personalizadas son acciones adicionales definidas por usuarios técnicos y que se ponen a disposición de los especialistas en marketing. Una vez configurados, aparecen en la paleta izquierda del recorrido, en la **[!UICONTROL Action]** categoría. Obtenga más información en [esta página](../building-journeys/about-journey-activities.md#action-activities).

## Limitaciones{#custom-actions-limitations}

Las acciones personalizadas incluyen algunas limitaciones enumeradas en [esta página](../start/limitations.md).

En los parámetros de acción personalizados, puede pasar una colección simple, así como una colección de objetos. Obtenga más información sobre las limitaciones de recopilación en [esta página](../building-journeys/collections.md#limitations).

Tenga en cuenta también que los parámetros de acciones personalizadas tienen un formato esperado (por ejemplo: string, decimal, etc.). Debe tener cuidado de respetar estos formatos esperados. Obtenga más información en esta [caso de uso](../building-journeys/collections.md).

## Pasos de configuración {#configuration-steps}

Estos son los pasos principales necesarios para configurar una acción personalizada:

1. En la sección del menú ADMINISTRACIÓN , seleccione **[!UICONTROL Configurations]**. En el  **[!UICONTROL Actions]** , haga clic en **[!UICONTROL Manage]**. Haga clic en **[!UICONTROL Create Action]** para crear una nueva acción. El panel de configuración de acciones se abre en el lado derecho de la pantalla.

   ![](assets/custom2.png)

1. Escriba un nombre para la acción.

   >[!NOTE]
   >
   >No utilice espacios ni caracteres especiales. No utilice más de 30 caracteres.

1. Añada una descripción a la acción. Este paso es opcional.
1. El número de recorridos que utilizan esta acción se muestra en la **[!UICONTROL Used in]** campo . Puede hacer clic en el botón **[!UICONTROL View journeys]** para mostrar la lista de recorridos que utilizan esta acción.
1. Seleccione el canal relacionado con esta acción personalizada: **Correo electrónico**, **SMS** o **Notificaciones push**. Rellenará previamente el campo de acción de marketing requerido con la acción de marketing predeterminada para el canal seleccionado. Si selecciona **other**, no se definirá ninguna acción de marketing.
1. Si desea aplicar una regla de consentimiento a esta acción personalizada, seleccione la **Acción de marketing necesaria**. Consulte [esta sección](../action/about-custom-action-configuration.md#consent-management).
1. Defina los diferentes **[!UICONTROL URL Configuration]** parámetros. Consulte [esta sección](../action/about-custom-action-configuration.md#url-configuration).
1. Configure las variables **[!UICONTROL Authentication]** para obtener más información. Esta configuración es la misma que para las fuentes de datos.  Consulte [esta sección](../datasource/external-data-sources.md#custom-authentication-mode).
1. Defina el **[!UICONTROL Action parameters]**. Consulte [esta sección](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. 
1. Haga clic en **[!UICONTROL Save]**.

   La acción personalizada ahora está configurada y lista para utilizarse en sus recorridos. Consulte [esta página](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Cuando se utiliza una acción personalizada en un recorrido, la mayoría de los parámetros son de solo lectura. Solo puede modificar el **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** y **[!UICONTROL Authentication]** para obtener más información.

## Configuración de URL {#url-configuration}

Al configurar una acción personalizada, debe definir lo siguiente **[!UICONTROL URL Configuration]** parámetros:

![](assets/journeyurlconfiguration.png)

1. En el **[!UICONTROL URL]** especifique la URL del servicio externo:

   * Si la dirección URL es estática, introduzca la dirección URL en este campo.

   * Si la dirección URL incluye una ruta dinámica, introduzca únicamente la parte estática de la dirección URL, es decir, el esquema, el host, el puerto y, opcionalmente, una parte estática de la ruta.

      Ejemplo: `https://xxx.yyy.com/somethingstatic/`

      Al agregar la acción personalizada a un recorrido, especificará la ruta dinámica de la dirección URL. [Más información](../building-journeys/using-custom-actions.md).
   >[!NOTE]
   >
   >Por motivos de seguridad, recomendamos encarecidamente que utilice el esquema HTTPS para la dirección URL. No permitimos el uso de direcciones de Adobe que no sean públicas ni de direcciones IP.
   >
   >Solo se permiten los puertos predeterminados al definir una acción personalizada: 80 para http y 443 para https.

1. Seleccione la llamada **[!UICONTROL Method]**: puede ser **[!UICONTROL POST]** o **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > La variable **DELETE** no es compatible. Si necesita actualizar un recurso existente, seleccione la opción **PUT** método.

1. En el **[!UICONTROL Headers]** , defina los encabezados HTTP del mensaje de solicitud que se enviarán al servicio externo:
   1. Para añadir un campo de encabezado, haga clic en **[!UICONTROL Add a header field]**.
   1. Introduzca la clave del campo de encabezado.
   1. Para establecer un valor dinámico para el par clave-valor, seleccione **[!UICONTROL Variable]**. De lo contrario, seleccione **[!UICONTROL Constant]**.

      Por ejemplo, para una marca de tiempo, puede establecer un valor dinámico.

   1. Si ha seleccionado **[!UICONTROL Constant]** y, a continuación, introduzca el valor constante.

      Si ha seleccionado **[!UICONTROL Variable]**, especificará esta variable al agregar la acción personalizada a un recorrido. [Más información](../building-journeys/using-custom-actions.md).

      ![](assets/journeyurlconfiguration2.png)

   1. Para eliminar un campo de encabezado, elija el campo de encabezado y haga clic en el botón **[!UICONTROL Delete]** icono.
   La variable **[!UICONTROL Content-Type]** y **[!UICONTROL Charset]** los campos de encabezado se establecen de forma predeterminada. Estos campos no se pueden modificar ni eliminar.

   Después de agregar la acción personalizada a un recorrido, puede agregarle campos de encabezado si el recorrido está en estado de borrador. Si no desea que el recorrido se vea afectado por los cambios de configuración, duplique la acción personalizada y añada los campos del encabezado a la nueva acción personalizada.

   >[!NOTE]
   >
   >Los encabezados se validan según las reglas de análisis de campos. Obtenga más información en [esta documentación](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Definir los parámetros de acción {#define-the-message-parameters}

![](assets/messageparameterssection.png)

En el **[!UICONTROL Action parameters]** , pegue un ejemplo de la carga útil JSON para enviarla al servicio externo.

![](assets/customactionpayloadmessage.png)

>[!NOTE]
>
>Los nombres de campo de la carga útil no pueden contener &quot;.&quot; carácter. No pueden empezar con un carácter &quot;$&quot;.

Puede definir el tipo de parámetro (p. ej.: string, integer, etc.).

También tendrá la opción de especificar si un parámetro es una constante o una variable:

* Constante significa que el valor del parámetro se define en el panel de configuración de acciones mediante un perfil técnico. El valor siempre será el mismo en todos los recorridos. No variará y el especialista en marketing no lo verá al utilizar la acción personalizada en el recorrido. Podría ser, por ejemplo, un ID que el sistema de terceros espera. En ese caso, el campo a la derecha de la constante o variable de alternancia es el valor pasado.
* Variable significa que el valor del parámetro variará. Los especialistas en marketing que utilicen esta acción personalizada en un recorrido podrán pasar el valor que deseen o especificar dónde recuperar el valor de este parámetro (por ejemplo, desde el evento, desde Adobe Experience Platform, etc.). En ese caso, el campo a la derecha de la constante o variable de alternancia es la etiqueta que los especialistas en marketing verán en el recorrido para asignar un nombre a este parámetro.

![](assets/customactionpayloadmessage2.png)

## Gestión de consentimiento {#consent-management}

Los clientes ahora pueden definir políticas de consentimiento, relacionadas con la privacidad, para controlar los datos salientes durante la ejecución de la acción. Una política de consentimiento funciona como una expresión en atributos de perfil, estableciendo reglas para definir si una acción se puede ejecutar para el perfil dado o no.

Consent sur custom action, pas message encore Conxent a tel type de comunication ou use de tel type de donnée champs dans profile qui vont sticker ce permission coté AEP nuvelles regles de type policy auj gouvernance policy. Ejemplo de ejemplo de Restric email targeting. Etiqueta asociada (C4/C5) a de las acciones de marketing. Busque su destino final y escriba de acción de marketing. Ex SFTP crée une dest qui va exporter des données vers ce sftp, tu flague ce sftp avec une acción de marketing. Egelement noción de acción de marketing rajoutée hace una acción personalizada, correo electrónico/SMS/acción de marketing push. Personalizado.

Etiquetas: conjunto de datos quand tu def (où stock tes données), gouvernance de datos onglet, pr chaque attribut tu peux definir le label asocié un atributo cet. Código de país etiquetado C3/C4. Etiquetas ootb, tu peux en def d&#39;autres en fonction besoin.



— Comentarios de Jira —

describa la &quot;acción de marketing adicional&quot; como una forma en que un profesional puede explicar la &quot;intención&quot; de una acción personalizada, por ejemplo: mi acción personalizada es sobre comunicación de ejercicios, boletín, comunicación de fitness, etc.

Describa el alcance del consentimiento para la primera versión :

- Se tienen en cuenta las acciones y atributos de marketing utilizados en la personalización en la acción personalizada
- Para los recorridos activados por segmentos (iniciados con un segmento de lectura), se tienen en cuenta los atributos utilizados como criterios en ese segmento
- No se tienen en cuenta todas las actividades utilizadas en un recorrido, excepto un segmento de lectura o una acción personalizada
- No se tiene en cuenta la calificación de segmentos, aunque se utilice para iniciar un recorrido

Describir que un perfil excluido por una directiva de consentimiento en una acción personalizada seguirá pasando por el recorrido (iso con lista de mensajes y supresión)

Recordatorio para describir la latencia esperada: https://wiki.corp.adobe.com/display/DMSArchitecture/Consent+Latency
+ latencia correcta de AJO de 1h a 6h

dos tipos de latencia que deberíamos documentar:

- Latencia del usuario, en esa Carolina Infante, no estoy seguro de lo que podemos decir, mirando esto:

¿Podemos confirmar si necesitamos o no que ocurra el &quot;UPS Projection/Export&quot;, para actualizar el campo &quot;contentTo&quot; a nivel de perfil (sabiendo que esto es lo que usamos en tiempo de ejecución)? Porque si este es el caso, supongo que deberíamos decir que tomaría hasta 48h, pero si no, solo estamos hablando de &quot;latencia de ingesta + latencia de recopilación&quot; (por lo que unos segundos o unas pocas horas el peor caso si hay picos o interrupciones en la ingesta y/o si el cliente tarda mucho tiempo en recopilar una actualización del usuario).

- La latencia de la política de consentimiento, diría &quot;hasta 6 horas&quot;, ya que los recorridos en vivo retirarán las políticas de consentimiento cada 6 horas. Carolina Infante , ¿sabe si nos vemos afectados por la latencia del filtro?
