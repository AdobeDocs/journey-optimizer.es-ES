---
title: Uso de identificadores suplementarios en recorridos
description: Aprenda a utilizar identificadores suplementarios en recorrido.
exl-id: f6ebd706-4402-448a-a538-e9a4c2cf0f8b
version: Journey Orchestration
source-git-commit: 62c0c1f46b5bd575102d9f27037cb6add1355ba2
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 4%

---

# Uso de identificadores suplementarios en recorridos {#supplemental-id}

>[!CONTEXTUALHELP]
>id="ajo_journey_parameters_supplemental_identifier"
>title="Usar identificador adicional"
>abstract="El identificador adicional es un identificador secundario que proporciona contexto adicional para la ejecución de un recorrido. Para definirlo, seleccione el campo que desea utilizar como identificador adicional y elija un espacio de nombres al que asociarlo."

<table style="border-collapse: collapse; width: 100%;">
  <tr>
    <td style="vertical-align: top; padding-right: 20px; border: none;">
      <p>De forma predeterminada, los recorridos se ejecutan en el contexto de un <b>ID de perfil</b>. Esto significa que, siempre y cuando el perfil esté activo en un recorrido determinado, no podrá volver a entrar en otro recorrido. Para evitarlo, Journey Optimizer le permite capturar un <b>identificador adicional</b>, como un identificador de pedido, un identificador de suscripción o un identificador de prescripción, además del identificador de perfil.  
      <p>En este ejemplo, hemos agregado un <b>ID de reserva</b> como identificador suplementario.</p>
      <p>Al hacerlo, los recorridos se ejecutan en el contexto del ID de perfil asociado al identificador suplementario (en este caso, el ID de reserva). Se ejecuta una instancia del recorrido para cada iteración del identificador suplementario. Esto permite varias entradas del mismo ID de perfil en recorridos si han realizado reservas diferentes.</p>
      <p>Además, Journey Optimizer le permite aprovechar los atributos del identificador suplementario (por ejemplo, número de reserva, fecha de renovación de la prescripción, tipo de producto) para la personalización de mensajes, lo que garantiza comunicaciones muy relevantes.</p>
    </td>
    <td style="vertical-align: top; border: none; text-align: center; width: 40%;">
      <img src="assets/event-supplemental-id.png" alt="Ejemplo de identificador suplementario" style="max-width:100%;" />
    </td>
  </tr>
</table>

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Mecanismos de protección y limitaciones {#guardrails}

* **recorridos admitidos**: se admiten identificadores adicionales para los recorridos **activados por eventos** y **Leer audiencia**. No son **compatibles** con los recorridos de calificación de audiencia (es decir, recorridos que comiencen con una actividad de calificación de audiencia).

* **Límites de instancias simultáneas**: los perfiles no pueden tener más de 10 instancias de recorrido simultáneas.

* **Reglas de frecuencia**: Cada instancia de recorrido creada a partir del uso de identificadores suplementarios se contabiliza en la restricción de frecuencia, incluso si el uso de identificadores suplementarios resulta en varias instancias de recorrido.

* **Tipo de datos y estructura de esquema**: el identificador suplementario debe ser del tipo `string`. Puede ser un atributo de cadena independiente o puede ser un atributo de cadena dentro de una matriz de objetos. El atributo de cadena independiente generará una única instancia de recorrido, mientras que el atributo de cadena dentro de una matriz de objetos generará una instancia de recorrido única por iteración de la matriz de objetos. No se admiten matrices de cadenas ni mapas.

* **reentrada al Recorrido**

  El recorrido del comportamiento de reentrada con identificadores suplementarios sigue la política de reentrada existente:

   * Si el recorrido no es de reentrada, la misma combinación de ID de perfil + ID suplementario no puede volver a entrar en el recorrido.
   * Si el recorrido es de reentrada con una ventana de tiempo, la misma combinación de ID de perfil + ID suplementario puede volver a introducirse después de la ventana de tiempo definida.

* **Etiquetado y aplicación del uso de datos (Data Use Labeling and Enforcement, DULE)**: no se realizan comprobaciones de validación DULE en el ID suplementario. Esto significa que este atributo no se tendrá en cuenta cuando el recorrido busque infracciones de directivas de gobernanza de datos.

* **Configuración de eventos descendentes**

  Si está utilizando otro evento descendente en la recorrido, debe utilizar el mismo ID suplementario y tener el mismo área de nombres de ID.

* **Leer recorridos de audiencia**

   * El ID suplementario se desactiva si se utiliza un evento empresarial.
   * El ID suplementario debe ser un campo del perfil (es decir, no un campo de evento/contexto).
   * Para recorridos de audiencia de lectura que utilizan ID suplementarios, la tasa de lectura de la actividad de audiencia de lectura para cada instancia de recorrido está limitada a un máximo de 500 perfiles por segundo.
   * Solo se admiten audiencias del servicio de perfil unificado al usar recorridos de audiencia de lectura con ID suplementarios.

## Comportamiento de criterios de salida con ID suplementarios {#exit-criteria}

Condición previa: Recorrido habilitado para ID suplementario (a través de actividades de evento unitario o lectura de audiencia)

En la tabla siguiente se explica el comportamiento de los perfiles en un recorrido suplementario habilitado para ID cuando se configuran los criterios de salida:

| Configuración de criterios de salida | Comportamiento cuando se cumplen los criterios de salida |
| ---------------------------- | ---------------------------------- |
| Basado en un evento de ID no suplementario | Se abandonan todas las instancias del perfil correspondiente en ese recorrido. |
| Basado en un evento de ID suplementario <br/>*Nota: el área de nombres de ID suplementario debe coincidir con el del nodo inicial.* | Solo se sale del perfil coincidente + instancia de ID suplementario. |
| Basado en una audiencia | Se abandonan todas las instancias del perfil correspondiente en ese recorrido. |

## Añadir un identificador suplementario y aprovecharlo en un recorrido {#add}

>[!BEGINTABS]

>[!TAB recorrido activado por eventos]

Para utilizar un identificador suplementario en un recorrido activado por evento, siga estos pasos:

1. **Marcar el atributo como identificador en el esquema de eventos**

   1. Acceda al esquema de eventos y busque el atributo que desee utilizar como identificador suplementario (por ejemplo, ID de reserva, ID de suscripción) y márquelo como ID. [Aprenda a trabajar con esquemas](../data/get-started-schemas.md)

   1. Marca el identificador como **[!UICONTROL identidad]**.

      ![](assets/supplemental-ID-schema.png)

      >[!IMPORTANT]
      >
      >Asegúrese de no marcar el atributo como **Identidad principal**.

   1. Seleccione el área de nombres que se asociará al ID suplementario. Debe ser un área de nombres de identificador de persona.

      Después de aplicar el área de nombres de identidad no personal a un esquema, debe crear un nuevo evento para utilizar el identificador suplementario. Las entidades existentes no se pueden actualizar para reconocer el nuevo identificador.

1. **Agregar el identificador suplementario al evento**

   1. Cree o edite el evento deseado. [Aprenda a configurar un evento unitario](../event/about-creating.md)

   1. En la pantalla de configuración del evento, marque la opción **[!UICONTROL Usar identificador suplementario]**.

      ![](assets/supplemental-ID-event.png)

   1. Utilice el editor de expresiones para seleccionar el atributo marcado como ID suplementario.

      >[!NOTE]
      >
      >Asegúrese de utilizar el editor de expresiones en **[!UICONTROL Modo avanzado]** para seleccionar el atributo.

   1. Después de seleccionar el ID suplementario, el área de nombres asociado se muestra en la pantalla de configuración de evento como de solo lectura.

1. **Agregar el evento al recorrido**

   Arrastre el evento configurado al lienzo de recorrido. Almacenará en déclencheur la entrada de recorrido en función tanto del ID de perfil como del ID suplementario.

   ![](assets/supplemental-ID-journey.png)

>[!TAB Leer recorrido de audiencia]

Para utilizar un identificador suplementario en un recorrido Leer audiencia, siga estos pasos:

1. **Marcar el atributo como identificador en el esquema de unión/perfil**

   1. Acceda al esquema de unión/perfil y busque el atributo que desea utilizar como identificador suplementario (por ejemplo, ID de reserva, ID de suscripción) y márquelo como ID. [Aprenda a trabajar con esquemas](../data/get-started-schemas.md)

   1. Marca el identificador como **[!UICONTROL identidad]**.

      ![](assets/supplemental-ID-schema-profile.png)

      >[!IMPORTANT]
      >
      >Asegúrese de no marcar el atributo como **Identidad principal**.

   1. Seleccione el área de nombres que se asociará al ID suplementario. Debe ser un área de nombres de identificador de persona.

      Después de aplicar el área de nombres de identidad no personal a un esquema, debe crear un nuevo grupo de campos para utilizar el identificador suplementario. Las entidades existentes no se pueden actualizar para reconocer el nuevo identificador.

<!--1. **Add the supplemental ID field to the data source**

    1. Navigate to the **[!UICONTROL Configuration]** / **[!UICONTROL Data Sources]** menu, then locate the "ExperiencePlatformDataSource" data source.

        ![](assets/supplemental-ID-data-source.png)

    1. Open the field selector then select the attribute you want to use as a supplemental identifier (e.g., booking ID, subscription ID).-->

1. **Agregar y configurar una actividad Leer audiencia en el recorrido**

   1. Arrastre una actividad **[!UICONTROL Leer audiencia]** a su recorrido.

   1. En el panel de propiedades de la actividad, active la opción **[!UICONTROL Usar identificador suplementario]**.

      ![](assets/supplemental-ID-read-audience.png)

   1. En el campo **[!UICONTROL Identificador de suplemento]**, use el editor de expresiones para seleccionar el atributo que marcó como identificador suplementario.

      >[!NOTE]
      >
      >Asegúrese de utilizar el editor de expresiones en **[!UICONTROL Modo avanzado]** para seleccionar el atributo.

   1. Después de seleccionar el identificador suplementario, el área de nombres asociado se muestra en el campo **[!UICONTROL Área de nombres suplementaria]** como de sólo lectura.

>[!ENDTABS]

## Aprovechamiento de atributos de ID suplementarios

Utilice el editor de expresiones y el editor de personalización para hacer referencia a los atributos del identificador suplementario para la personalización o la lógica condicional. Se puede acceder a los atributos desde el menú **[!UICONTROL Atributos contextuales]**.

![](assets/supplemental-ID-perso.png)

Para los recorridos activados por eventos si trabaja con matrices (por ejemplo, varias prescripciones o directivas), utilice una fórmula para extraer elementos específicos.

+++ Ver ejemplos

En una matriz de objetos con el Id. suplementario como `bookingNum` y un atributo en el mismo nivel denominado `bookingCountry`, el recorrido se iterará a través del objeto de matriz basado en bookingNum y creará una instancia de recorrido para cada objeto.

* La siguiente expresión en la actividad de condición iterará a través de la matriz de objetos y comprobará si el valor de `bookingCountry` es igual a &quot;FR&quot;:

  ```
  @event{<event_name>.<object_path>.<object_array_name>.all(currentEventField.<attribute_path>.bookingNum==${supplementalId}).at(0).<attribute_path>.bookingCountry}=="FR"
  ```

* La siguiente expresión en el editor de personalización de correo electrónico se iterará a través de la matriz de objetos, extraerá el `bookingCountry` aplicable a la instancia de recorrido actual y lo mostrará en el contenido:

  ```
  {{#each context.journey.events.<event_ID>.<object_path>.<object_array_name> as |l|}} 
  
  {%#if l.<attribute_path>.bookingNum = context.journey.technicalProperties.supplementalId%} {{l.<attribute_path>.bookingCountry}}  {%/if%}
  
  {{/each}}
  ```

* Ejemplo del evento utilizado para almacenar en déclencheur el recorrido:

  ```
  "bookingList": [
        {
            "bookingInfo": {
                "bookingNum": "x1",
                      "bookingCountry": "US"
            }
        },
        {
            "bookingInfo": {
                "bookingNum": "x2",
                "bookingCountry": "FR"
            }
        }
    ]
  ```

+++

## Casos de uso de ejemplo

### **Notificaciones de renovación de directivas**

* **Escenario**: un proveedor de seguros envía recordatorios de renovación por cada póliza activa que posea un cliente.
* **Ejecución**:
   * Perfil: &quot;John&quot;.
   * Identificadores suplementarios: `"AutoPolicy123", "HomePolicy456"`.
   * El recorrido se ejecuta por separado para cada póliza, con fechas de renovación personalizadas, detalles de cobertura e información sobre primas.

### **Administración de suscripciones**

* **Escenario**: un servicio de suscripción envía mensajes personalizados para cada suscripción cuando se activa un evento para esa suscripción.
* **Ejecución**:
   * Perfil: &quot;Jane&quot;.
   * Identificadores suplementarios: `"Luma Yoga Program ", "Luma Fitness Program"`.
   * Cada evento incluye un ID de suscripción y detalles sobre dicha suscripción. El recorrido se ejecuta por separado para cada evento/suscripción, lo que permite ofertas de renovación personalizadas por suscripción.

### **Recomendaciones de productos**

* **Escenario**: una plataforma de comercio electrónico envía recomendaciones basadas en productos específicos comprados por un cliente.
* **Ejecución**:
   * Perfil: &quot;Alex&quot;.
   * Identificadores suplementarios: `"productID1234", "productID5678"`.
   * El recorrido se ejecuta por separado para cada producto, con oportunidades de ampliación de venta personalizadas.

## Vídeo práctico {#video}

Obtenga información sobre cómo habilitar y aplicar un identificador suplementario en [!DNL Adobe Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3464795?captions=spa&quality=12)
