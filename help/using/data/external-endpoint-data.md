---
solution: Journey Optimizer
product: journey optimizer
title: Personalización del contenido mediante datos de un extremo externo
description: Obtenga información sobre cómo recuperar dinámicamente datos de un extremo externo para personalizar el contenido entrante.
badge: label="Disponibilidad limitada" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor
source-git-commit: f5d1bc27afadbf875fe4dd3149ce090a8773e0f9
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 0%

---


# Personalización del contenido mediante datos de un extremo externo {#data-endpoint}

>[!AVAILABILITY]
>
>Esta capacidad solo está disponible para un conjunto de organizaciones (disponibilidad limitada).

Journey Optimizer permite aprovechar los datos de un extremo externo para personalizar el contenido en canales entrantes como la experiencia basada en código y los canales de mensajes web y en la aplicación.

Para ello, hay disponible una función de ayuda dedicada, `externalDataLookup`, en el editor de personalización. Para usar el asistente, primero debe definir una [!DNL Journey Optimizer] **Acción** en la que configure los detalles del extremo externo.

## Lectura obligatoria

### Ejecución en tiempo de ejecución

Cuando una acción entrante incluye un asistente externalDataLookup, se llama dinámicamente al extremo en el momento en que el Edge Network [!DNL Adobe Experience Platform] recibe y procesa la solicitud de personalización. Esto significa que el extremo externo debe poder gestionar al menos la misma carga y rendimiento simultáneos que el cliente envía para la superficie determinada a AEP Edge Network.

### Autenticación

El asistente externalDataLookup no admite actualmente las opciones de autenticación en la configuración de acción.
Mientras tanto, para la autenticación basada en claves de API u otras claves de autorización de texto sin formato, puede especificarlas como campos de encabezado en la configuración de acción.
SOLO para extremos internos de Adobe: póngase en contacto con el departamento de ingeniería de AJO para habilitar la autenticación basada en tokens de servicio para un extremo.

### Protecciones y limitaciones

Consulte también Acciones personalizadas en Canales entrantes de AJO Campañas y Recorridos #GuardrailsandGuidelines.

De forma predeterminada, AJO utiliza un tiempo de espera de 300 ms al llamar a un extremo externo. Póngase en contacto con el departamento de ingeniería de AJO para aumentar este tiempo de espera para un extremo.
En el Editor de Personalization, AJO no permite examinar el esquema de la respuesta del extremo al insertar expresiones y no valida referencias a atributos JSON de la respuesta utilizada en las expresiones.
Los tipos de datos admitidos para los parámetros de variable de carga útil que se sustituirán mediante el asistente externalDataLookup son String, Integer, Decimal, Boolean, listString, listInt, listInteger, listDecimal
Los cambios en una configuración de acción no se reflejan en las llamadas externas DataLookup correspondientes en campañas y recorridos activos. Para que se refleje un cambio, debe copiar o modificar cualquier campaña o recorrido activo que utilice la acción en un asistente de DataLookup externo.
Aún no se admite el uso de variables dentro de los parámetros de ayuda de búsqueda de datos externos.
Actualmente no se admite la ruta de URL dinámica.  - Mejoras en las acciones personalizadas entrantes#DynamicPathSegments

## Crear una acción

Cree una acción para configurar el extremo de la búsqueda. Esto solo debe hacerse una vez para cada punto de conexión y debe hacerlo un usuario técnico. Consulte esta página.

La misma acción se puede usar en una actividad **[!UICONTROL Custom Action]** para recuperar contenido en un recorrido y en una función de ayuda de `externalDataLookup` para recuperar datos en una acción entrante en un recorrido o una campaña.

Vaya al menú **[!UICONTROL Administración]** / **[!UICONTROL Configuraciones]**.

Observe el ID de acción y cópielo para utilizarlo en el paso 6.


## Personalice el contenido mediante los datos recuperados

### Añadir la función de ayuda al contenido

1. Cree una campaña o acción de recorrido entrante y edite su contenido.

1. Busque el contenido donde desea utilizar los datos recuperados del extremo externo y acceder al editor de personalización.

1. Seleccione el menú Funciones de ayuda y busque la función de ayuda `externalDataLookup`.

1. Seleccione para insertar la sintaxis asociada en el código y reemplazar los valores de parámetros `actionId` y `result` de la siguiente manera:

   * `actionId` : pegar la acción nID copiada al crear la acción.
   * `result`: establezca este parámetro en el nombre que elija. Utilizará esta variable de resultado para acceder al contenido recuperado.

1. Agregue cualquier valor de parámetro de variable que se vaya a pasar como parte de la llamada al extremo. Por ejemplo, así es como se puede pasar un parámetro de idioma y un parámetro de elementos máximos.

### Personalización mediante datos recuperados

Para acceder a los datos recuperados de una llamada de búsqueda de extremo externa, puede hacer referencia a los campos definidos en la carga útil de respuesta en la definición de acción mediante expresiones de personalización y funciones de ayuda.

Utilice la variable `result` para acceder a los datos recuperados e insertarlos en el contenido para la acción entrante. Por ejemplo, así es como podría devolver una matriz JSON de elementos recuperados del extremo.

Veamos el ejemplo siguiente, donde la carga útil de respuesta en la acción se ha configurado de la siguiente manera:

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

Ejemplo 1 de Personalization: mostrar la descripción del primer vídeo en una acción de Experience HTML basada en código:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Ejemplo 2 de Personalization: Devolver una matriz de elementos en una acción JSON de experiencia basada en código:

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

## Tiempos de espera y gestión de errores

AJO utiliza un tiempo de espera estricto al llamar al extremo externo para mantener características de rendimiento de alto rendimiento y baja latencia para AEP Edge Network.

Si se agota el tiempo de espera del extremo o hay algún otro tipo de error que llegue al extremo, la variable de resultado estará vacía. Cualquier referencia a atributos dentro de la variable de resultado en este caso también estará vacía. Si simplemente muestra el atributo en el contenido, se mostrará en blanco. Si intenta recorrer en bucle un atributo de matriz en el resultado, no devolverá ningún elemento.

Si desea gestionar los tiempos de espera o los errores de forma más correcta mostrando el contenido de reserva, puede comprobar si el resultado de la búsqueda está vacío y mostrar el contenido de reserva en ese caso.

Por ejemplo, puede mostrar un valor de reserva para un único atributo como este:

Descripción del primer vídeo: {%=result.videos[0].description ?: &quot;ninguno encontrado&quot; %}


o puede procesar condicionalmente un bloque entero de contenido como este:

{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}

{%#if result%}
... hacer algo con el resultado ...
{%else%}
... devolver contenido de reserva...
{%/if%}
Depuración
Para ayudar con la depuración, se incluyen detalles de tiempo de espera y error para búsquedas de datos externos en la vista de Edge Delivery en AEP Assurance. Si no ve los resultados esperados para un asistente externo de DataLookup en una acción entrante, puede iniciar una sesión de Assurance, iniciar una llamada de AJO desde una implementación web o móvil y utilizar la vista de Edge Delivery para comprobar si hay detalles de tiempo de espera o error.

Por ejemplo:

En la sección Edge Delivery del seguimiento de seguridad como parte de los detalles de ejecución, se ha añadido un nuevo bloque customActions con

detalles de solicitud y respuesta similares al de abajo. La sección de errores debe ayudar con la depuración si hubo algún problema al ejecutar la acción personalizada

## Preguntas frecuentes

+++¿Cómo pasar un atributo contextual desde la solicitud como parámetro a una búsqueda de datos externa?

Utilice el menú Atributos contextuales > Flujo de datos > Evento para examinar el esquema de Experience Event que está utilizando e insertar el atributo relevante como valor de parámetro como este:

`{{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}`

+++

+++¿AJO almacena en caché las respuestas de extremos externos?

Actualmente no. Esta función será compatible en el futuro.

+++









Sintaxis
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}



Pasar parámetros
Cuando se llama al extremo externo, todos los valores de encabezado constante, parámetros de consulta y valor de carga útil de solicitud definidos en la acción se envían con los valores proporcionados en la configuración de acción.

Para cualquier valor de encabezado de variable, parámetro de consulta/ruta o valor de carga útil de solicitud, puede pasar valores dinámicamente mediante parámetros al asistente externalDataLookup.

Nombres de parámetros:

Parámetros de encabezado: encabezado.&lt;parameter-name>
Query parameters: query.&lt;parameter-name>
Parámetros de carga útil: carga útil.&lt;parameter-name>
Parámetros de ruta: dynamic_path.&lt;parameter-name>
Por ejemplo:

{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}
Los valores de parámetro pueden ser valores fijos o pueden personalizarse haciendo referencia a campos de perfil u otros atributos contextuales, por ejemplo:

{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
Los parámetros de carga útil se pueden proporcionar utilizando la notación de puntos para hacer referencia a atributos JSON anidados, por ejemplo:

{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}