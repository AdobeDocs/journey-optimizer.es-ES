---
title: Ayuda de búsqueda de datos externos
description: Guía completa para utilizar el Asistente para la búsqueda de datos externos para la personalización dinámica en Adobe Journey Optimizer.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
hide: true
hidefromtoc: true
badge: label="Disponibilidad limitada" type="Informative"
exl-id: eae8a09a-5d27-4a80-b21f-7f795d800602
source-git-commit: 5df643d2b0623d40779d155e406467d622d3d753
workflow-type: tm+mt
source-wordcount: '1198'
ht-degree: 1%

---

# Ayuda de búsqueda de datos externos

El asistente de `externalDataLookup` en el editor de personalización de [!DNL Journey Optimizer] se puede usar para recuperar dinámicamente datos de un extremo externo para usarlos en la generación de contenido para canales entrantes como la experiencia basada en código y los canales de mensajes web y en la aplicación.

>[!AVAILABILITY]
>
>Esta capacidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

Para usar el asistente, primero debe definir una acción en el menú **[!UICONTROL Administración]** > **[!UICONTROL Configuraciones]**. Una acción es donde se configuran los detalles de un extremo externo, como una dirección URL, un método GET vs. POST, parámetros de encabezado, parámetros de consulta, esquema JSON del cuerpo de POST y esquema JSON de respuesta.

Una vez definida la acción, se puede utilizar tanto:

* En recorrido, en una actividad de acción personalizada para recuperar contenido,
* En recorridos y campañas entrantes, en un asistente externo de DataLookup para recuperar datos en una acción entrante.

## Protecciones y limitaciones

Consulte también Acciones personalizadas en [!DNL Journey Optimizer] canales entrantes, campañas y Recorridos #GuardrailsandGuidelines.

* **Tiempo de espera predeterminado**: de manera predeterminada, [!DNL Journey Optimizer] utiliza un tiempo de espera de 300 ms al llamar a un extremo externo. Póngase en contacto con su representante de Adobe para aumentar este tiempo de espera para un punto final.
* **Exploración del esquema de respuesta y validación de expresiones**: en el editor de personalización, no se puede examinar el esquema de la respuesta del extremo al insertar expresiones. [!DNL Journey Optimizer] no valida las referencias a atributos JSON de la respuesta utilizada en las expresiones.
* **Tipos de datos admitidos para los parámetros**: los tipos de datos admitidos para los parámetros de variable de carga útil que se sustituirán mediante el asistente externalDataLookup son `String`, `Integer`, `Decimal`, `Boolean`, `listString`, `listInt`, `listInteger`, `listDecimal`.
* **Actualización automática para acciones actualizadas**: los cambios en una configuración de acción no se reflejan en las llamadas externalDataLookup correspondientes de campañas y recorridos activos. Para que se refleje un cambio, debe copiar o modificar cualquier campaña o recorrido activo que utilice la acción en un asistente de DataLookup externo.
* **Sustitución de variables**: por ahora, el uso de variables no es compatible con los parámetros de ayuda externalDataLookup.
* **Ruta dinámica**: por ahora, no se admite la ruta dinámica de URL.
* **Procesamiento de varias pasadas**: se admite el procesamiento de varias pasadas.
* **Autenticación**: por ahora, el asistente externalDataLookup no admite las opciones de autenticación de la configuración de acción. Mientras tanto, para la autenticación basada en claves de API u otras claves de autorización de texto sin formato, puede especificarlas como campos de encabezado en la configuración de acción.

## Configurar una acción y utilizar el asistente

Para definir una acción y utilizar el asistente para la personalización, siga estos pasos:

1. Cree una acción para configurar el extremo de la búsqueda. Esto solo debe hacerse una vez para cada punto de conexión y debe hacerlo un usuario técnico. [Aprenda a configurar una acción personalizada](../action/about-custom-action-configuration.md)

   Observe el ID de acción y cópielo.

   ![](assets/external-data-action.png)

1. Cree una campaña entrante o una acción de recorrido. Para este ejemplo, se muestra cómo utilizar el asistente externalDataLookup en una acción JSON de experiencia basada en código, pero se puede utilizar en un campo de personalización en cualquier canal entrante.

1. Edite el contenido de la acción, vaya a Funciones de ayuda en el editor de personalización y vaya a **[!UICONTROL Funciones de ayuda]** > **[!UICONTROL ayudantes]**.

1. Haga clic en el botón `+` para insertar el asistente externalDataLookup. La expresión de ayuda se inserta en el editor, con valores de marcador de posición para `actionId` y `result`.

   ![](assets/external-data-personalization.png)

   Reemplace los valores de marcador de posición de la siguiente manera:

   * `actionId`: pegue el ID de acción copiado anteriormente.
   * `result`: establezca el nombre que desee. Utilizará esta variable de resultado para acceder al contenido recuperado.

1. Agregue cualquier valor de parámetro de variable que se vaya a pasar como parte de la llamada al extremo. Por ejemplo, así es como se puede pasar un parámetro de idioma y un parámetro de elementos máximos.

   ![](assets/external-data-personalization-example.png)

1. Utilice la variable de resultado para acceder a los datos recuperados e insertarlos en el contenido para la acción entrante. Por ejemplo, así es como podría devolver una matriz JSON de elementos recuperados del extremo.

   ![](assets/external-data-personalization-result.png)

## Funcionamiento

### Ejecución en tiempo de ejecución

Cuando una acción entrante incluye un asistente externalDataLookup, se llama dinámicamente al extremo en el momento en que AEP Edge Network recibe y procesa la solicitud de personalización [!DNL Journey Optimizer].

Esto significa que el extremo externo debe poder gestionar al menos la misma carga y rendimiento simultáneos que el cliente envía para la superficie determinada a AEP Edge Network.

### Sintaxis

`{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}`

### Pasar parámetros

Cuando se llama al extremo externo, todos los valores de encabezado constante, parámetros de consulta y valor de carga útil de solicitud definidos en la acción se envían con los valores proporcionados en la configuración de acción.

Para cualquier valor de encabezado de variable, parámetro de consulta/ruta o valor de carga útil de solicitud, puede pasar valores dinámicamente mediante parámetros al asistente externalDataLookup.

Nombres de parámetros:

* Parámetros de encabezado: `header.<parameter-name>`
* Parámetros de consulta: `query.<parameter-name>`
* Parámetros de carga útil: `payload.<parameter-name>`
* Parámetros de ruta: `dynamic_path.<parameter-name>`

Por ejemplo:

```
{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}`
```

Los valores de parámetro pueden ser valores fijos o pueden personalizarse haciendo referencia a campos de perfil u otros atributos contextuales, por ejemplo:

```
{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
```

Los parámetros de carga útil se pueden proporcionar utilizando la notación de puntos para hacer referencia a atributos JSON anidados, por ejemplo:

```
{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}
```

### Acceso al resultado

Para acceder a los datos recuperados de una llamada de búsqueda de extremo externa, puede hacer referencia a los campos definidos en la carga útil de respuesta en la definición de acción mediante expresiones de personalización y funciones de ayuda.

Por ejemplo, si la carga útil de respuesta en la acción tiene este aspecto:

```
{
    "videos": [
        {
            "id": "integer",
            "title": "string",
            "description": "string",
            "thumbnail_url": "string",
            "video_page_url": "string",
            "url": "string",
            "video_type": "string",
            "start_timestamp": "dateOnly",
            "created_on": "dateOnly",
            ...
        }
    ]
}
```

Por ejemplo, puede recuperar y acceder a la descripción del primer vídeo en una acción de Experience HTML basada en código de esta manera:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Por ejemplo, puede recuperar y recorrer los elementos para devolver una matriz de elementos en una acción JSON de experiencia basada en código como la siguiente:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
[
{{#each result.videos as |item|}}
    {                                                  
        "title": "{{item.title}}",
        "url": "{{item.video_page_url}}",
        "thumbnail_url": "{{item.thumbnail_url}}",
        "start_timestamp": "{{item.start_timestamp}}"
    },
{{/each}}
]
```

## Resolución de problemas

### Tiempos de espera y gestión de errores

[!DNL Journey Optimizer] usa un tiempo de espera estricto al llamar al extremo externo para mantener características de rendimiento de alto rendimiento y baja latencia para AEP Edge Network.

Si se agota el tiempo de espera del extremo o hay algún otro tipo de error que llegue al extremo, la variable de resultado estará vacía. Cualquier referencia a atributos dentro de la variable de resultado en este caso también estará vacía. Si simplemente muestra el atributo en el contenido, se mostrará en blanco. Si intenta recorrer en bucle un atributo de matriz en el resultado, no devolverá ningún elemento.

Si desea gestionar los tiempos de espera o los errores de forma más correcta mostrando el contenido de reserva, puede comprobar si el resultado de la búsqueda está vacío y mostrar el contenido de reserva en ese caso.

Por ejemplo, puede mostrar un valor de reserva para un único atributo como este:

```
First video description: {%=result.videos[0].description ?: "none found" %}
```

o puede procesar condicionalmente un bloque entero de contenido como este:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
{%#if result%}
   ... do something with result ...
{%else%}
    ... return fallback content ...
{%/if%}
```

### Depuración

Para ayudar con la depuración, se incluyen detalles de tiempo de espera y error para búsquedas de datos externos en la vista de Edge Delivery en AEP Assurance. Si no ve los resultados esperados para un asistente externalDataLookup en una acción entrante, puede iniciar una sesión de Assurance, iniciar una llamada de [!DNL Journey Optimizer] desde una implementación web o móvil y utilizar la vista de Edge Delivery para buscar detalles de tiempo de espera o error.

Por ejemplo:

En la sección Edge Delivery del seguimiento de seguridad como parte de los detalles de ejecución, se ha agregado un nuevo bloque customActions con detalles de solicitud y respuesta similares al de abajo. La sección de errores debe ayudar con la depuración si hubo algún problema al ejecutar la acción personalizada

![](assets/external-data-troubleshoot.png "width=50%")

## Preguntas frecuentes

* ¿Cómo pasar un atributo contextual desde la solicitud como parámetro a una búsqueda de datos externa?

  Utilice el menú Atributos contextuales > Flujo de datos > Evento para examinar el esquema de Experience Event que está utilizando e insertar el atributo relevante como valor de parámetro como este:

  ```
  {{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}
  ```

* ¿Hace [!DNL Journey Optimizer] almacenamiento en caché de las respuestas de extremo externo?

  Actualmente no. Esta función será compatible en el futuro.
