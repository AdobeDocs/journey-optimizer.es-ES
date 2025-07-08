---
solution: Journey Optimizer
product: journey optimizer
title: Bloquear contenido en plantillas de correo electrónico
description: Aprenda a bloquear contenido en las plantillas de correo electrónico.
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: f64fe1c4-3e30-4b74-80f8-b801a5f1d4c4
source-git-commit: a9f2eae6398f92a40accb62b1d4544bda031559c
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 30%

---

# Bloquear contenido en plantillas de correo electrónico {#lock-content-email-templates}

>[!CONTEXTUALHELP]
>id="ajo_locking_governance"
>title="Gobernanza"
>abstract="Active la gobernanza para bloquear contenido de la plantilla, ya sea bloqueando la plantilla completa o estructuras y componentes específicos. Esto le permite evitar ediciones o eliminaciones no intencionadas, lo que le proporciona un mayor control sobre la personalización de las plantillas y mejora la eficacia y fiabilidad de sus campañas de correo electrónico."

>[!CONTEXTUALHELP]
>id="ajo_locking_mode"
>title="Modo"
>abstract="Seleccione el modo de bloqueo que desee para la plantilla. **Bloqueo de contenido** le permite bloquear secciones específicas de contenido dentro de la plantilla. **Solo lectura** le permite bloquear todo el contenido de la plantilla, evitando así cualquier modificación."

>[!CONTEXTUALHELP]
>id="ajo_locking_content_addition"
>title="Habilitar adición de contenido"
>abstract="Active esta opción para definir con mayor precisión cómo pueden interactuar los usuarios con la plantilla. Seleccione **Permitir la adición de estructura y contenido** para permitir que los usuarios añadan estructuras entre las existentes y añadan componentes de contenido o fragmentos dentro de estructuras editables. **Permitir solo la adición de contenido** permite a los usuarios añadir componentes de contenido o fragmentos dentro de estructuras editables sin poder añadir ni duplicar estructuras."

>[!CONTEXTUALHELP]
>id="ajo_email_locking_activated"
>title="Gobernanza habilitada"
>abstract="El bloqueo de contenido está activado y evita modificaciones."

>[!CONTEXTUALHELP]
>id="ajo_email_locking_read_only"
>title="Solo lectura"
>abstract="Este contenido es de solo lectura y no se puede modificar."

Journey Optimizer permite bloquear el contenido en plantillas de correo electrónico, ya sea bloqueando toda la plantilla o estructuras y componentes específicos. Esto evita ediciones o eliminaciones involuntarias, lo que le proporciona un mayor control sobre la personalización de las plantillas y mejora la eficacia y fiabilidad de sus campañas de correo electrónico.

>[!IMPORTANT]
>
>El bloqueo de contenido es una función de nivel de editor para autores y no garantiza que el contenido permanezca sin editar cuando se importe o cree mediante API.

El bloqueo de contenido se puede aplicar en el nivel **structure** o en el nivel **component**. A continuación se muestran los principios principales que se aplican en el nivel de estructura y componente al bloquear contenido en la plantilla:

* Cuando una estructura está bloqueada:

   * Todo el contenido de esa estructura también está bloqueado de forma predeterminada.
   * No se puede añadir contenido a la estructura.
   * De forma predeterminada, no se puede eliminar la estructura. Puede anular esta restricción activando la opción Permitir eliminación.
   * Los componentes de contenido individuales dentro de la estructura bloqueada se pueden establecer como editables.

* Cuando una estructura es editable (estructura no bloqueada):

   * Los componentes de contenido individuales se pueden bloquear dentro de esa estructura.
   * De forma predeterminada, no se puede eliminar un componente si está bloqueado o si la opción &quot;Solo bloqueo de contenido editable&quot; está seleccionada. Puede anular esta restricción activando la opción Permitir eliminación.

>[!AVAILABILITY]
>
>Los usuarios con permisos para crear plantillas de contenido pueden activar el bloqueo de contenido.

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Bloquear una plantilla de correo electrónico {#define}

### Habilitar el bloqueo de contenido {#enable}

Puede activar el bloqueo de contenido para una plantilla de correo electrónico directamente en la Designer de correo electrónico, tanto si está creando una plantilla nueva como si está editando una existente. Siga estos pasos:

1. Abra o cree una plantilla de correo electrónico y acceda a la pantalla de edición de contenido en el Designer de correo electrónico.

1. En el panel **[!UICONTROL Cuerpo]** de la derecha, active la opción **[!UICONTROL Gobernanza]**.

1. En la lista desplegable **[!UICONTROL Modo]**, seleccione el modo de bloqueo que desee para la plantilla:

   * **[!UICONTROL Bloqueo de contenido]**: Bloquee secciones específicas de contenido dentro de la plantilla. De forma predeterminada, todas las estructuras y componentes se pueden editar. A continuación, puede bloquear selectivamente elementos individuales.
   * **[!UICONTROL Solo lectura]**: bloquee todo el contenido de la plantilla para evitar cualquier modificación.

   ![](assets/template-lock-enable.png)

1. Si seleccionó el modo **[!UICONTROL Bloqueo de contenido]**, puede definir con más detalle cómo los usuarios pueden interactuar con la plantilla. Active la opción **[!UICONTROL Habilitar edición de contenido]** y elija una de las siguientes opciones:

   * **[!UICONTROL Permitir la adición de estructura y contenido]**: los usuarios pueden agregar estructuras entre las existentes y agregar componentes de contenido o fragmentos dentro de estructuras editables.

   * **[!UICONTROL Permitir solo la adición de contenido]**: los usuarios pueden agregar componentes de contenido o fragmentos dentro de estructuras editables, pero no pueden agregar ni duplicar estructuras.

1. Después de seleccionar el modo de bloqueo, puede definir qué estructuras o componentes bloquear si ha seleccionado el modo **[!UICONTROL Bloqueo de contenido]**:

   * [Aprenda a bloquear estructuras](#lock-structures)
   * [Aprenda a bloquear componentes](#lock-components)

   Si eligió el modo **[!UICONTROL Solo lectura]**, complete y guarde la plantilla como de costumbre.

Puede ajustar la configuración de **[!UICONTROL Governance]** en cualquier momento al diseñar la plantilla seleccionando el cuerpo de la plantilla. Para ello, haga clic en el vínculo **[!UICONTROL Cuerpo]** en el carril de navegación ubicado en la parte superior del panel lateral derecho.

![](assets/template-lock-body.png)

### Bloqueo de estructuras {#lock-structures}

>[!CONTEXTUALHELP]
>id="ajo_locking_structure"
>title="Bloqueo de contenido en la estructura"
>abstract="Para bloquear la estructura de la plantilla, seleccione **Bloqueado** en el menú desplegable **Tipo de bloqueo**. De forma predeterminada, los usuarios no pueden eliminar las estructuras bloqueadas. Puede anular esta restricción habilitando la opción **[!UICONTROL Permitir eliminación]**."

Para bloquear una estructura dentro de la plantilla:

1. Seleccione la estructura que desee bloquear.

1. En la lista desplegable **[!UICONTROL Bloquear tipo]**, elija **[!UICONTROL Bloqueado]**.

   ![](assets/template-lock-structure.png)

   >[!NOTE]
   >
   >De forma predeterminada, los usuarios no pueden eliminar las estructuras bloqueadas. Puede anular esta restricción habilitando la opción **[!UICONTROL Permitir eliminación]**.

Después de bloquear una estructura, no se pueden duplicar ni agregar más componentes o fragmentos de contenido dentro de ella. Todos los componentes de una estructura bloqueada también están bloqueados de forma predeterminada. Para hacer que un componente se pueda editar dentro de una estructura bloqueada:

1. Seleccione el componente que desea desbloquear.

1. Active la opción **[!UICONTROL Usar bloqueo específico]**.

1. En la lista desplegable **[!UICONTROL Bloquear tipo]**, elija **[!UICONTROL Editable]**. Para permitir la edición de contenido al bloquear estilos, seleccione **[!UICONTROL Solo contenido editable]**. [Aprenda a bloquear componentes](#lock-components)

   ![](assets/template-lock-editable-component.png)

### Bloqueo de componentes {#lock-components}

>[!CONTEXTUALHELP]
>id="ajo_locking_component"
>title="Utilizar bloqueo específico en el componente"
>abstract="Para bloquear el componente de la plantilla, active la opción **Utilizar bloqueo específico**. En el menú desplegable **[!UICONTROL Bloquear tipo]**, seleccione la opción de bloqueo que prefiera: **Solo bloqueo de contenido editable** le permite bloquear los estilos del componente, pero permite editar contenido, mientras que **Bloqueado** bloquea completamente tanto el contenido como los estilos del componente."

Para bloquear un componente específico dentro de una estructura:

1. Seleccione el componente y habilite la opción **[!UICONTROL Usar bloqueo específico]** en el panel derecho.

1. En la lista desplegable **[!UICONTROL Tipo de bloqueo]**, seleccione la opción de bloqueo que prefiera:

   ![](assets/template-lock-component.png)

   * **[!UICONTROL Bloqueo de contenido editable solamente]**: Bloquee los estilos del componente pero permita la edición de contenido.
   * **[!UICONTROL Bloqueado]**: bloquea completamente el contenido y los estilos del componente.

   >[!NOTE]
   >
   >El tipo de bloqueo **[!UICONTROL Editable]** permite a los usuarios editar un componente, incluso dentro de una estructura bloqueada. [Aprenda a bloquear estructuras](#lock-structures)

1. De forma predeterminada, los usuarios no pueden eliminar los componentes bloqueados. Puede habilitar la eliminación activando la opción **[!UICONTROL Permitir eliminación]**.

### Identificar contenido bloqueado {#identify}

Para identificar fácilmente las estructuras y los componentes bloqueados dentro de la plantilla, use el **[!UICONTROL árbol de navegación]** ubicado en el menú del lado izquierdo. Este menú proporciona una visión general de todos los elementos de plantilla, resaltando los elementos bloqueados con un icono de candado y los elementos editables con un icono de lápiz.

En el ejemplo siguiente, el control está habilitado para el cuerpo de la plantilla. La *estructura 2* está bloqueada con *componente 1* editable, mientras que la *estructura 3* está bloqueada por completo.

![](assets/template-lock-navigation.png)

## Uso de plantillas con contenido bloqueado {#use}

>[!CONTEXTUALHELP]
>id="ajo_email_editable_areas"
>title="Resaltar áreas editables"
>abstract="Según el tipo de bloqueo aplicado a la plantilla, puede realizar diferentes acciones en las estructuras y componentes de la plantilla. Para identificar rápidamente todas las áreas editables dentro de la plantilla, active la opción **[!UICONTROL Resaltar áreas editables]**."

Cuando se usa una plantilla con contenido bloqueado, aparece el mensaje **[!UICONTROL Gobernanza habilitada]** en el panel derecho.

Según el tipo de bloqueo aplicado a la plantilla, puede realizar diferentes acciones en las estructuras y componentes de la plantilla. Para identificar rápidamente todas las áreas editables dentro de la plantilla, active la opción **[!UICONTROL Resaltar áreas editables]**.

Por ejemplo, en la plantilla siguiente, todas las áreas son editables, excepto la imagen superior, que se ha bloqueado, lo que significa que no puede editarla ni quitarla.

![](assets/template-lock-highlight.png)

Encontrará información detallada sobre los diferentes tipos de bloqueo que se pueden aplicar en estas secciones:

* [Bloqueo de estructuras](#lock-structures)
* [Bloqueo de componentes](#lock-components)

Estos son algunos ejemplos de ediciones de correo electrónico y de las configuraciones de bloqueo de contenido asociadas que se han configurado:

| Tipo de bloqueo de contenido | Configuración de plantilla | Edición por correo electrónico |
| ------- | ------- | ------- |
| Plantilla de contenido de solo lectura | ![](assets/locking-sample-read-only-conf.png){zoomable="yes"} | ![](assets/locking-sample-read-only.png){zoomable="yes"} |
| El contenido completo es editable, pero los usuarios no pueden agregar ninguna estructura ni componente | ![](assets/locking-sample-no-addition-conf.png){zoomable="yes"} | ![](assets/locking-sample-no-addition.png){zoomable="yes"} |
| Estructura bloqueada que no se puede eliminar | ![](assets/locking-sample-structure-locked-conf.png){zoomable="yes"} | ![](assets/locking-sample-structure-locked.png){zoomable="yes"} |
| Componente con estilos bloqueados y que no se puede eliminar. Los usuarios solo pueden modificar el contenido. | ![](assets/locking-sample-content-only-conf.png){zoomable="yes"} | ![](assets/locking-sample-content-only.png){zoomable="yes"} |
| Componente editable dentro de una estructura bloqueada. | ![](assets/locking-sample-editable-component-conf.png){zoomable="yes"} | ![](assets/locking-sample-editable-component.png){zoomable="yes"} |

## Vídeo práctico {#video}

Aprenda a bloquear contenido en plantillas de correo electrónico.

>[!VIDEO](https://video.tv.adobe.com/v/3451610?quality=12&captions=spa)
