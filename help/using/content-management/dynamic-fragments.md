---
solution: Journey Optimizer
product: journey optimizer
title: Uso de fragmentos dinámicos
description: Aprenda a utilizar la resolución dinámica de fragmentos en Adobe Journey Optimizer para seleccionar e insertar fragmentos en tiempo de ejecución en función de atributos de perfil, búsquedas de conjuntos de datos o datos de contexto.
feature: Fragments
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: dinámico, fragmento, expresión, personalización, tiempo de ejecución
source-git-commit: b4affc5b905236419928a65cd173173b49058827
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 2%

---

# Uso de fragmentos dinámicos {#dynamic-fragments}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar la resolución dinámica de fragmentos en Adobe Journey Optimizer para seleccionar qué fragmento publicado se inserta en un mensaje en tiempo de ejecución, en función de atributos de perfil, búsquedas de conjuntos de datos o datos de contexto pasados en el momento de envío.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] admite **resolución dinámica de fragmentos** durante la ejecución, lo que le permite seleccionar qué fragmento publicado se inserta en un mensaje en función de atributos de perfil, búsquedas de conjuntos de datos o datos de contexto pasados en el momento del envío. Esto permite contenido altamente personalizado sin duplicar la lógica de campaña o de recorrido.

## Información general {#overview}

**Los fragmentos estáticos** están incrustados en un mensaje en tiempo de diseño; se utiliza el mismo fragmento para cada destinatario. **Los fragmentos dinámicos** resuelven el ID de fragmento en tiempo de ejecución por destinatario, lo que significa que distintos perfiles pueden recibir bloques de contenido totalmente diferentes dentro de la misma campaña o recorrido.

Los ID de fragmento dinámicos pueden proceder de tres fuentes:

* Una **búsqueda de conjuntos de datos**; por ejemplo, un conjunto de datos de Recommendations escrito por estilo o producto
* Un **atributo de perfil** almacenado en Adobe Experience Platform
* **Datos de contexto** pasados directamente en la solicitud de API en el momento del envío

>[!NOTE]
>
>El uso de la función de ayuda `datasetLookup` en fragmentos de expresiones está disponible actualmente para un conjunto limitado de clientes. Para obtener acceso, póngase en contacto con su representante de Adobe.

## Requisitos previos {#prerequisites}

Antes de usar fragmentos dinámicos, asegúrese de que lo siguiente esté configurado:

* Tiene los permisos necesarios para crear y publicar fragmentos en [!DNL Journey Optimizer]. [Más información](../administration/ootb-product-profiles.md#content-library-manager)
* El fragmento al que desea hacer referencia es **publicado** (estado: **Activo**). Los fragmentos de borrador no se pueden resolver durante la ejecución.
* Si se resuelve el ID del fragmento de un conjunto de datos, el esquema del conjunto de datos incluye un campo que almacena el ID del fragmento y el conjunto de datos está [habilitado para la búsqueda](../data/lookup-aep-data.md).
* Todos los atributos de perfil a los que hace referencia el propio fragmento dinámico se incluyen en la ruta de exportación del mensaje o están disponibles en el perfil en el momento de la entrega.

>[!CAUTION]
>
>Las validaciones relacionadas con fragmentos se omiten en el flujo de fragmentos dinámico. Los ID de fragmento no válidos aparecen como errores de entrega en tiempo de ejecución en lugar de errores de validación iniciales. Compruebe siempre que los ID de fragmento a los que se hace referencia son válidos y se publican antes de activar una campaña.

## Paso 1: Crear y publicar el fragmento {#create-fragment}

Antes de hacer referencia a un fragmento de forma dinámica, debe publicarse en [!DNL Journey Optimizer].

1. En [!DNL Journey Optimizer], vaya a **[!UICONTROL Administración de contenido]** > **[!UICONTROL Fragmentos]**.

1. Seleccione **[!UICONTROL Crear fragmento]** y cree el contenido. [Aprenda a crear fragmentos](create-fragments.md)

1. Cuando el contenido esté listo, haga clic en **[!UICONTROL Publicar]**. La publicación es asíncrona y puede tardar unos segundos. Confirme que el estado del fragmento cambia a **Activo** antes de continuar.

1. Observe el **ID de fragmento** desde la vista de detalles del fragmento o desde la respuesta de la API de fragmentos. En el mensaje hará referencia a este ID.

>[!NOTE]
>
>Puede recuperar todos los ID de fragmento publicados mediante programación usando la API `GET /fragments`. Consulte la [documentación de las API de Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"} para obtener más información.

## Paso 2: Crear el mensaje con una referencia de fragmento dinámico {#author-message}

En el editor de personalización, inserte el marcador de posición del fragmento dinámico con la siguiente sintaxis:

```handlebars
{{fragment id=dynamic_fragment_id}}
```

El identificador `dynamic_fragment_id` es un nombre de variable. Su valor debe resolverse antes de que se produzca la búsqueda de fragmentos. La resolución se realiza mediante una expresión de búsqueda del conjunto de datos, un atributo de perfil o datos de contexto.

### Resolver a partir de una búsqueda de conjuntos de datos {#resolve-from-dataset}

Si el ID de fragmento está almacenado en un conjunto de datos de AEP (por ejemplo, una tabla de asignación de estilo a fragmento), utilice la función de ayuda `datasetLookup` para resolverlo:

```handlebars
{{
  {datasetLookup datasetId="<your-dataset-id>" key=profile.style attribute="fragmentId"}
}}

{{fragment id=dynamic_fragment_id}}
```

En este ejemplo, el conjunto de datos contiene filas marcadas por un valor de estilo (como `style1`). Para un perfil determinado, la búsqueda recupera el valor de columna `fragmentId` correspondiente y lo asigna a `dynamic_fragment_id`, que luego se utiliza para resolver el fragmento.

>[!NOTE]
>
>El uso de la función de ayuda `datasetLookup` en fragmentos de expresiones está disponible actualmente para un conjunto limitado de clientes. Para obtener acceso, póngase en contacto con su representante de Adobe. Para obtener más información sobre las búsquedas de conjuntos de datos en la personalización, consulte [Usar datos de Adobe Experience Platform](../data/lookup-aep-data.md).

### Resolver a partir de datos de contexto {#resolve-from-context}

Si el ID de fragmento se proporciona en el momento de envío como parte del contexto de solicitud de API, haga referencia a él mediante el área de nombres `context`:

```handlebars
{{fragment id=context.audiencePayload.fragmentId}}
```

La ruta de acceso `context.audiencePayload` es el prefijo necesario para todos los atributos procedentes de un archivo de audiencia CSV o pasados a través del contexto de solicitud de API. El nombre de columna del CSV (por ejemplo, `fragmentId`) sigue el prefijo.

### Resolución a partir de un atributo de perfil {#resolve-from-profile}

Si el ID de fragmento se almacena como un atributo de perfil en Adobe Experience Platform, haga referencia a él directamente:

```handlebars
{{fragment id=profile.mi.fragmentId}}
```

## Paso 3: Configurar el conjunto de datos para el enfoque de búsqueda {#configure-dataset}

Si utiliza el método de búsqueda de conjuntos de datos, actualice el esquema y los datos del conjunto de datos para que lleven el ID de fragmento.

1. En el conjunto de datos de asignaciones o recomendaciones, agregue una columna (por ejemplo, `fragmentId`) que almacene el ID de fragmento de AJO publicado para cada fila.

1. Para cada estilo o variante (por ejemplo, `style1`, `style2`), rellene la columna `fragmentId` con el ID de fragmento correspondiente.

1. Asegúrese de ingerir el conjunto de datos en Adobe Experience Platform y de que [esté habilitado para la búsqueda](../data/lookup-aep-data.md).

1. Confirme que todos los atributos de perfil a los que se hace referencia dentro del fragmento dinámico se capturan en el mensaje o en un fragmento estático para evitar que la representación esté vacía en el momento de la exportación.

**Ejemplo de estructura del conjunto de datos:**

| Columna | Valor de ejemplo |
|---|---|
| estilo | style1 |
| fragmentId | &lt;fragment-id-1> |
| estilo | style2 |
| fragmentId | &lt;fragment-id-2> |

## Paso 4: Pasar datos de contexto en el momento del envío {#pass-context-data}

Si está resolviendo el ID de fragmento a partir de datos de contexto (por ejemplo, desde un archivo de recomendación de audiencia CSV), pase el ID de fragmento en la solicitud de API bajo el prefijo de contexto requerido.

Cuando utilice la API de revisión de campaña, incluya el ID de fragmento en el objeto `context`:

```json
{
  "recipients": [
    {
      "userId": "<profile-email>",
      "namespace": "email"
    }
  ],
  "inChannelData": {
    "channel": "email",
    "emailAddresses": ["<delivery-address>"]
  },
  "context": {
    "audiencePayload": {
      "fragmentId": "<published-fragment-id>",
      "systemSource": "<optional-system-value>"
    }
  }
}
```

El prefijo `context.audiencePayload` es obligatorio. Los atributos anidados en esta clave se asignan directamente a las columnas del archivo de audiencia CSV cuando se ejecuta la campaña en directo.

## Paso 5: Prueba y validación {#proof-validate}

Antes de activar la campaña, utilice la API de prueba de campaña para comprobar que el fragmento dinámico se resuelve correctamente y que el resultado del correo electrónico procesado es el esperado.

1. Almacenar en déclencheur un trabajo de revisión mediante el extremo `POST /campaigns/{id}/proofs`. En la solicitud de revisión, apruebe el ID de fragmento que desee probar en `context.audiencePayload.fragmentId`.

1. Encuesta el estado del trabajo de revisión usando el extremo `GET /campaigns/{id}/proofs/{proofId}` hasta que el estado sea `Submitted` o `Failed`.

1. Compruebe el correo electrónico enviado para verificar que se representa el contenido de fragmento correcto.

1. Si falta el contenido del fragmento o es incorrecto, compruebe que el ID del fragmento es válido, que se publica y que están presentes todos los atributos de perfil requeridos.

Para obtener más información sobre la API de campaña, consulte la [documentación de las API de Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"}.

## Mecanismos de protección y limitaciones {#guardrails}

>[!CAUTION]
>
>OLAC (Control de acceso de nivel de objeto) no se aplica a los fragmentos del modelo de fragmentos dinámico. Asegúrese de que los requisitos de control de acceso se tienen en cuenta en el nivel de campaña y audiencia.

Al utilizar fragmentos dinámicos, se aplican las siguientes limitaciones:

* **Cobertura de atributo de perfil en el momento de la exportación**: el fragmento se elige en tiempo de ejecución por perfil. Los atributos de perfil requeridos por el fragmento dinámico no se conocen de antemano. Si el fragmento dinámico se basa en un atributo de perfil que no estaba presente en el mensaje original ni en ningún fragmento estático al que se haga referencia en el mensaje, ese campo puede quedar vacío en la ruta de exportación.

* **Sin validación de fragmentos iniciales**: las validaciones relacionadas con fragmentos se omiten en este flujo. Los ID de fragmento incorrectos o sin publicar aparecen como errores de entrega en tiempo de ejecución en lugar de errores de validación mostrados en la interfaz de usuario.

* **Cambio de esquema necesario para el enfoque del conjunto de datos**: el uso de la ruta de acceso de búsqueda por ID requiere la actualización del esquema del conjunto de datos para almacenar y pasar el ID del fragmento, además de la canalización necesaria para alimentarlo en la canalización de mensajes.

* **Captura de atributos para la exportación**: Asegúrese de que todos los atributos utilizados dentro del fragmento dinámico se capturan en el mensaje o en fragmentos estáticos para evitar que se represente en blanco en la ruta de exportación.

Hay más protecciones aplicables a los fragmentos disponibles en [esta sección](../start/guardrails.md#fragments-guardrails).

## Control de errores {#error-handling}

Si un fragmento dinámico no se puede resolver durante la ejecución, se genera un evento de exclusión para el perfil afectado. Actualmente, todos los errores de procesamiento de fragmentos se clasifican como un solo tipo de error general.

Para depurar errores de resolución de fragmentos:

1. Consulte los informes de entrega de campañas para ver los eventos de exclusión.
1. Compruebe que el ID de fragmento pasado en tiempo de ejecución coincida con un fragmento publicado.
1. Confirme que todos los atributos de perfil requeridos por el fragmento están presentes en el perfil en el momento del envío.
1. Use la [API de revisión](#proof-validate) para probar los identificadores de fragmento específicos antes de activar la campaña.
