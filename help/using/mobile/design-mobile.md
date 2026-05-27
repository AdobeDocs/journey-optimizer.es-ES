---
solution: Journey Optimizer
product: journey optimizer
title: Creación de un mensaje SMS/RCS/MMS
description: Obtenga información sobre cómo crear un mensaje SMS/RCS/MMS en Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
source-git-commit: 30eecc21809cf818ae7530187782b370240830e7
workflow-type: tm+mt
source-wordcount: '1456'
ht-degree: 2%

---

# Diseño de un mensaje móvil {#design-mobile}

Puede diseñar y enviar mensajes de texto (SMS), de comunicación enriquecida (RCS) y multimedia (MMS) con Adobe Journey Optimizer. Primero debe agregar una acción de mensaje móvil en un recorrido o una campaña y luego definir el contenido del mensaje móvil, como se detalla a continuación. Adobe Journey Optimizer también ofrece funciones para probar los mensajes de Mobile antes de enviarlos, de modo que pueda comprobar el procesamiento, los atributos de personalización y cualquier otra configuración.

De acuerdo con las normas y regulaciones del sector, todos los mensajes de marketing SMS/RCS/MMS deben contener una forma para que los perfiles puedan cancelar la suscripción fácilmente. Para ello, los perfiles de SMS pueden responder con las palabras clave de inclusión y exclusión. [Aprenda a administrar la exclusión](../privacy/opt-out.md#opt-out-decision-management)

## Definición del contenido de RCS{#rcs-content}

RCS permite enviar mensajes visualmente enriquecidos con imágenes, vídeos, carruseles y botones interactivos, entregados a través de la aplicación de mensajería nativa en dispositivos compatibles. Los mensajes se envían desde un remitente verificado y de marca. Cuando el dispositivo o el operador de un perfil no admite RCS, Journey Optimizer vuelve automáticamente a un SMS estándar.

Cada mensaje RCS requiere un **[!UICONTROL texto de reserva predeterminado]**: una versión de SMS de texto sin formato entregada a perfiles cuyo dispositivo o operador no admite RCS. No se puede activar una campaña sin ella.

Tenga en cuenta lo siguiente al escribir texto de reserva:

* **Manténgalo conciso.** Los mensajes SMS están limitados a 160 caracteres por segmento; los mensajes más largos se dividen en varias partes y pueden conllevar cargos adicionales.
* **Incluir direcciones URL clave.** Si el mensaje RCS se vincula a una URL mediante botones de acción, agregue una URL abreviada al texto de reserva para que los perfiles SMS puedan llegar al destino.
* **Evitar referencias de solo RCS.** No mencione elementos visuales, carruseles o funciones interactivas que no estén disponibles en SMS simples.
* **Personalization es compatible.** Puede utilizar tokens de personalización en texto de reserva para mantener la coherencia del mensaje en ambas versiones.

Para definir el contenido del mensaje RCS, siga los pasos a continuación.

1. En el panel de creación, elija **[!UICONTROL Tipo de contenido]**:

   +++ Texto

   Cuerpo de texto sin formato con botones interactivos opcionales. Ideal para notificaciones, alertas, recordatorios y flujos de conversación donde no se necesitan imágenes.

   +++

   +++ Medios

   Una imagen o un vídeo independientes con texto opcional y botones interactivos. Utilícelo cuando un solo elemento visual (una imagen de producto, un titular o un clip de vídeo) sea el punto focal del mensaje.

   1. En el menú Encabezado, escriba una **[!UICONTROL URL multimedia]** que apunte a la imagen o al vídeo que se va a mostrar.

   1. Si el contenido es un archivo de vídeo, si lo desea, escriba una **[!UICONTROL URL en miniatura]**.

   +++

   +++ Tarjeta

   Una tarjeta estructurada que combina una imagen o un vídeo, un título, un texto independiente y botones de acción. Utilícela para presentar un producto, una oferta o un elemento de contenido en formato de marca.

   1. Escriba un **[!UICONTROL Título]** y **[!UICONTROL Descripción]**.

   1. Escriba una **[!UICONTROL URL multimedia]** que apunte a la imagen o al vídeo que se va a mostrar.

   1. Si el contenido es un archivo de vídeo, si lo desea, escriba una **[!UICONTROL URL en miniatura]**.

   +++

   +++ Carrusel

   Una serie de tarjetas enriquecidas desplazable horizontalmente en un solo mensaje, cada una con su propia imagen, título, descripción y botones. Ideal para catálogos de productos o promociones. Se requiere un mínimo de 2 tarjetas.

   1. Seleccione un **[!UICONTROL Ancho de tarjeta]** para controlar el ancho de visualización de cada tarjeta.
   1. Para cada tarjeta, escribe **[!UICONTROL Título]** y **[!UICONTROL Descripción]**.

   1. Escriba una **[!UICONTROL URL multimedia]** que apunte a la imagen o al vídeo de esa tarjeta.

   1. De manera opcional, seleccione un **[!UICONTROL alto de medios]** y agregue botones de acción sugeridos.

   +++

   +++ Ubicación

   Envía un pin de mapa a un conjunto de coordenadas, que se muestra como una previsualización de mapa en línea en el hilo de mensajes del perfil. Utilícela para compartir la dirección de una tienda, un lugar de celebración o un área de servicio.

   1. Escriba el decimal **[!UICONTROL Latitud]** y **[!UICONTROL Longitud]** de la ubicación.

   1. Opcionalmente, escriba un **[!UICONTROL nombre de ubicación]** para mostrarlo como una etiqueta en el pin del mapa.

   +++

1. En el campo **[!UICONTROL Texto del mensaje]**, escriba el contenido del mensaje. Puede utilizar la personalización para adaptar el texto a cada perfil. Tenga en cuenta que los límites de caracteres varían según el tipo de mensaje: 3072 caracteres para medios enriquecidos (únicos) y 160 para RCS básicos.

1. Use el **[!UICONTROL editor de Personalization]** para definir contenido, agregar personalización y contenido dinámico. Puede utilizar cualquier atributo, como el nombre del perfil o la ciudad, por ejemplo. También puede definir reglas condicionales.

1. Opcionalmente, agregue **[!UICONTROL Acciones sugeridas]**, botones interactivos que permiten que los perfiles actúen con un solo toque.

1. Escriba una **[!UICONTROL Etiqueta]** en su **[!UICONTROL Acción]**.

1. Elija su **[!UICONTROL tipo de acción]**:

   * **[!UICONTROL Responder]**: devuelve una respuesta de texto predefinida al agente de RCS en nombre del perfil. Utilícelo para capturar la intención, impulsar flujos de conversación o déclencheur eventos de recorrido descendentes. No se requieren campos adicionales, el texto de respuesta coincide con la etiqueta del botón.

   * **[!UICONTROL Abrir URL]**: redirige el perfil a una página web, a un vínculo profundo o a un destino dentro de la aplicación. Admite tokens de personalización y parámetros de seguimiento de UTM, por ejemplo `https://www.example.com/offers?id={{profile.userId}}`.

   * **[!UICONTROL Número de teléfono de marcado]**: abre el marcador del dispositivo con un número de teléfono especificado ya rellenado, listo para que el perfil llame.

   * **[!UICONTROL Ver ubicación]**: abre la aplicación de mapas predeterminada del dispositivo en una ubicación especificada. Proporcione el decimal **[!UICONTROL Latitud]** y **[!UICONTROL Longitud]** de la ubicación que se va a mostrar.

1. En el campo **[!UICONTROL Texto de reserva predeterminado]**, escriba la versión de texto sin formato del mensaje SMS. Esto es obligatorio y se entrega a perfiles cuyo dispositivo o operador no admite RCS.

1. En el menú desplegable **[!UICONTROL Webview]**, elige el tamaño de tu **[!UICONTROL Webview]** al enviar una acción **[!UICONTROL Abrir URL]**.

1. Haga clic en **[!UICONTROL Guardar]** y compruebe el mensaje en la vista previa. Ahora puede probar y comprobar el contenido del mensaje como se detalla en [esta sección](send-mobile-message.md).

## Definición del contenido de los SMS{#sms-content}

>[!CONTEXTUALHELP]
>id="ajo_message_sms_content"
>title="Definición del contenido de los SMS"
>abstract="Personalice y personalice su mensaje móvil mediante el editor de personalización para definir el contenido e incorporar elementos dinámicos."

Para configurar el contenido del mensaje, siga los pasos a continuación. La configuración de MMS se detalla en [esta sección](#mms-content).

1. En la pantalla de configuración del recorrido o la campaña, haga clic en el botón **[!UICONTROL Editar contenido]** para configurar el contenido del mensaje de Mobile.

1. Haga clic en el campo **[!UICONTROL Mensaje]** para abrir el editor de personalización.

   ![](assets/sms-content.png)

1. Genere mensajes móviles atractivos y adaptados a su audiencia con [AI Assistant para generar texto](../content-management/generative-text.md).

1. Utilice el editor de personalización para definir contenido, añadir personalización y contenido dinámico. Puede utilizar cualquier atributo, como el nombre del perfil o la ciudad, por ejemplo. También puede definir reglas condicionales. Vaya a las páginas siguientes para obtener más información sobre [personalización](../personalization/personalize.md) y [contenido dinámico](../personalization/get-started-dynamic-content.md) en el editor de personalización.

1. Después de definir el contenido, puede agregar direcciones URL rastreadas al mensaje. Para ello, acceda al menú **[!UICONTROL Funciones de ayuda]** y seleccione **[!UICONTROL Ayudantes]**.

   ![](assets/sms_tracking_1.png)

1. Seleccione **[!UICONTROL Url]** y haga clic en **[!UICONTROL Agregar URL]**. Obtenga más información acerca de la función de ayuda `Url` en [esta sección](../personalization/functions/helpers.md#url).

   ![](assets/sms_tracking_2.png)

1. Para acortar la dirección URL, péguela en el campo `originalUrl` y haga clic en **[!UICONTROL Guardar]**.

   >[!CAUTION]
   >
   >Para utilizar la función de acortamiento de URL, primero debe configurar un subdominio que luego se vinculará a la configuración. [Más información](mobile-subdomains.md)
   >
   > La duración de las URL cortas es de 30 días. Después de este período, ya no se podrá obtener acceso a estas direcciones URL cortas y se mostrará el mensaje: `404 short-code not found`.

1. Para agregar un vínculo profundo que abra una pantalla específica en su aplicación móvil, utilice la función de ayuda `Url` con el tipo `DEEPLINK`, como en el ejemplo siguiente. [Más información sobre los vínculos profundos](../email/deeplinks.md)

   ```
   {{url originalUrl='<<deeplink_url>>' type='DEEPLINK' action='CLICK'}}
   ```

   >[!CAUTION]
   >
   >Antes de usar la vinculación profunda, asegúrese de completar los [pasos de configuración](../email/deeplinks.md#configuration) correspondientes en Journey Optimizer e implementar la [administración de vínculos profundos](../email/deeplinks.md#mobile-implementation) en su aplicación móvil. Si no lo ha hecho, el vínculo profundo no dirigirá a los usuarios al contenido previsto en la aplicación.
   >
   >Además, asegúrese de que el seguimiento de vínculos esté habilitado en la sección **[!UICONTROL Acciones]** de su recorrido o campaña para que la URL se reescriba a través de los sistemas de Adobe.

1. Desde el menú **[!UICONTROL Decisioning]**, puedes personalizar y optimizar el contenido de tus mensajes móviles con **Decisioning**. Esta capacidad le permite utilizar puntuaciones de prioridad, fórmulas o modelos de IA para seleccionar y mostrar dinámicamente el mejor contenido a sus clientes.

   Para obtener más información sobre cómo crear y usar directivas de decisión en mensajes móviles, consulte [esta sección](../experience-decisioning/create-decision.md).

1. Haga clic en **[!UICONTROL Guardar]** y compruebe el mensaje en la vista previa. Ahora puede probar y comprobar el contenido del mensaje como se detalla en [esta sección](send-mobile-message.md).

## Definición del contenido de MMS{#mms-content}

Puede mejorar su comunicación enviando mensajes del Servicio de mensajes multimedia (MMS), lo que permite compartir medios como vídeos, imágenes, clips de audio y GIF, etc. Además, el MMS admite hasta 1600 caracteres de texto en el mensaje.

>[!NOTE]
>
> El canal MMS incluye algunas limitaciones en [esta página](../start/guardrails.md#sms-guardrails).

Para crear contenido MMS, siga estos pasos:

1. Cree un mensaje móvil como se describe en [esta sección](#create-sms-journey-campaign).

1. Edite su contenido SMS como se detalla en [esta sección](#sms-content).

1. Habilite la opción MMS para añadir contenido multimedia al contenido de SMS.

   ![](assets/sms_create_6.png)

1. Agregue un **[!UICONTROL Título]** a sus medios.

1. Escriba la URL del contenido en el campo **[!UICONTROL Medios]**.

   ![](assets/sms_create_7.png)

1. Haga clic en **[!UICONTROL Guardar]** y compruebe el mensaje en la vista previa. Ahora puede probar y comprobar el contenido del mensaje como se detalla a continuación.

Una vez que haya realizado las pruebas y validado el contenido, puede enviar el mensaje móvil a la audiencia. Estos pasos se detallan en [esta página](send-mobile-message.md)

