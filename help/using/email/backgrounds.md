---
solution: Journey Optimizer
product: journey optimizer
title: Personalice el fondo del correo electrónico
description: Obtenga información sobre cómo personalizar el fondo del correo electrónico
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: fondo, correo electrónico, color, editor
exl-id: 09a2e892-8c6f-460d-8b12-5026582c6ed0
TQID: https://experienceleague.adobe.com/8kFppIm3Q-zHDqalE0Vt0CK5Z1ts9fGspVu476TapSk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
    internal-label: Email
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
    internal-label: Email design
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
    internal-label: Publish
  - id: c41e8697-e629-4c38-96b3-564faaa17acf
    internal-label: Dynamic content
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 7047a27a870c50f7a093ec7d98d8398948b78edb
workflow-type: ht
source-wordcount: '887'
ht-degree: 100%
---
# Personalice el fondo del correo electrónico {#backgrounds}

>[!BEGINSHADEBOX]

**En esta página:** aprenda a establecer colores e imágenes de fondo en los niveles de cuerpo, ventanilla, estructura y columna del correo electrónico en el diseñador de correo electrónico.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ac_edition_backgroundimage"
>title="Configuración de fondo"
>abstract="Puede personalizar el color o la imagen de fondo del contenido. Tenga en cuenta que la imagen de fondo no es compatible con todos los clientes de correo electrónico."

Los fondos le ayudan a reforzar su identidad de marca y a llamar la atención sobre las áreas clave de su correo electrónico. En el Diseñador de correo electrónico, puede establecer un color de fondo o una imagen en diferentes niveles de su contenido, desde el cuerpo general hasta las estructuras y columnas individuales, lo que le proporciona un control preciso sobre cómo se representan los fondos en el correo electrónico.

Tenga en cuenta las siguientes prácticas recomendadas a la hora de establecer fondos en el Diseñador de correo electrónico:

* Aplique un color de fondo al cuerpo solo si el diseño lo requiere.
* Siempre que sea posible, es preferible establecer colores de fondo a nivel de columna.
* Evite utilizar colores de fondo en componentes de imagen o texto, ya que son más difíciles de administrar.
* Pruebe las imágenes de fondo en los clientes de correo electrónico reales antes de enviarlas, ya que la representación puede diferir de la vista previa del Diseñador de correo electrónico.

La siguiente configuración permite aplicar un color de fondo o una imagen a cualquier nivel del contenido del correo electrónico, desde el cuerpo hasta las estructuras y columnas individuales.

>[!TIP]
>
>Si se aplica una temática al correo electrónico, no podrá anular directamente el color de fondo establecido por la temática para un componente determinado. Primero debe desbloquear ese estilo usando el icono dedicado en la pestaña **[!UICONTROL Estilos]**. [Descubra cómo](apply-email-themes.md#unlocking-styles)

## Establecimiento de un color de fondo {#background-color}

1. **Color de fondo del cuerpo**: defina un **[!UICONTROL color de fondo]** para todo el correo electrónico. Asegúrese de seleccionar **[!UICONTROL Cuerpo]** en el **[!UICONTROL Árbol de navegación]** accesible desde la paleta izquierda y utilice la opción dedicada en la pestaña **[!UICONTROL Estilos]** situada a la derecha.

   ![Diseñador de correo electrónico con el cuerpo seleccionado en el árbol de navegación y la opción Color de fondo resaltada en el panel Estilos](assets/background_1.png)

1. **Color de fondo de la ventanilla**: defina un **[!UICONTROL Color de ventanilla]** para aplicar el mismo color de fondo a todos los componentes de la estructura, independientemente del color de fondo del cuerpo.

   ![Panel de estilos del Diseñador de correo electrónico con la opción Color de ventanilla resaltada y un selector de color abierto para elegir el color de fondo aplicado a todas las estructuras](assets/background_2.png)

1. **Color de fondo de la estructura**: para aplicar un color de fondo a un solo componente de la estructura, selecciónelo directamente en el lienzo o en la paleta izquierda y establezca un color específico para esa estructura.

   ![Panel Estilos del Diseñador de correo electrónico para una estructura seleccionada, con la opción Color de fondo resaltada](assets/background_3.png)

   >[!TIP]
   >
   >En ese caso, asegúrese de no establecer un color de fondo de ventanilla, ya que podría ocultar los colores de fondo de la estructura.

1. **Color de fondo de la columna**: defina un color de fondo a nivel de la columna. De nuevo, asegúrese de seleccionar la columna deseada en la paleta izquierda y establezca un color específico para esa columna.

   ![Panel Estilos del Diseñador de correo electrónico para una columna seleccionada, con la opción Color de fondo resaltada](assets/background_5.png)

   >[!TIP]
   >
   >Este es el caso de uso más común y una práctica recomendada, ya que le ofrece más flexibilidad a la hora de editar el resto del contenido del correo electrónico.

## Establecimiento de una imagen de fondo {#background-image}

También puede establecer una **[!UICONTROL Imagen de fondo]** para el contenido de un componente de estructura o columna. Se suele utilizar a nivel de la estructura, aunque es posible establecerlo a nivel de columna, pero muy pocas veces se utiliza.

>[!NOTE]
>
>Algunos programas de correo electrónico no admiten imágenes de fondo. Cuando no se admite, se utiliza el color de fondo de la fila. Asegúrese de seleccionar un color de fondo alternativo adecuado en caso de que la imagen no se pueda mostrar.

![Panel Estilos del Diseñador de correo electrónico con la opción Imagen de fondo activada y Ubicación de imágenes establecida en Altura completa: derecha, que muestra la imagen que rellena una columna](assets/background_4.png)

>[!TIP]
>
>Obtenga una vista previa de la imagen de fondo en los clientes de correo electrónico reales antes de enviarla, no solo en la vista previa del Diseñador de correo electrónico. La misma imagen y la misma ubicación pueden representarse correctamente en el editor, pero aparecen estiradas o recortadas de forma diferente en algunos clientes, como Outlook en iOS.

Una vez establecida una imagen de fondo, utilice el menú desplegable **[!UICONTROL Ubicación de imágenes]** para controlar cómo la imagen rellena la estructura o la columna. Las siguientes opciones están disponibles para su selección:

![Panel Estilos del Diseñador de correo electrónico que muestra el menú desplegable Ubicación de imágenes con varias opciones](assets/background_6.png){width=80%}

**Escalar para rellenar, centrado:**

* **[!UICONTROL Ajustar]**: expande la imagen para llenar el contenedor en ambos ejes, sin conservar su relación de aspecto.
* **[!UICONTROL Anchura completa]**: escala la imagen proporcionalmente a la anchura del contenedor y la centra verticalmente.
* **[!UICONTROL Altura completa]**: escala la imagen proporcionalmente a la altura del contenedor y la centra horizontalmente.

**Escalar para rellenar, anclado a un borde:**

* **[!UICONTROL Anchura completa: arriba]**: igual que **[!UICONTROL Anchura completa]**, anclada a la parte superior del contenedor. La parte que desborda se recorta por abajo.
* **[!UICONTROL Anchura completa: abajo]**: igual que **[!UICONTROL Anchura completa]**, anclada en la parte inferior del contenedor. La parte que desborda se recorta por arriba.
* **[!UICONTROL Altura completa: izquierda]**: igual que **[!UICONTROL Altura completa]**, anclada a la izquierda del contenedor. La parte que desborda se recorta por la derecha.
* **[!UICONTROL Altura completa: derecha]**: igual que **[!UICONTROL Altura completa]**, anclada a la derecha del contenedor. La parte que desborda se recorta por la izquierda.

**Mosaico:**

* **[!UICONTROL Repetir]**: muestra la imagen en mosaico a su tamaño original para que ocupe todo el contenedor.

**Posición sin escala:**

* **[!UICONTROL Izquierda]**, **[!UICONTROL Derecha]**, **[!UICONTROL Centro]**, **[!UICONTROL Arriba]**, **[!UICONTROL Abajo]**: coloca la imagen en su tamaño original, anclada al borde o al centro correspondiente del contenedor.

>[!NOTE]
>
>Las opciones ancladas al borde le proporcionan más control sobre qué parte de la imagen permanece en la vista cuando no coincide con las proporciones de la estructura, en comparación con las opciones centradas anteriores.

{{$include /help/_includes/do-not-localize/email/ai-augmented-backgrounds.md}}
