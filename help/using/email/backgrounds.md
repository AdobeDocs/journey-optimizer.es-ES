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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebbid: c41e8697-e629-4c38-96b3-564faaa17acf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 7047a27a870c50f7a093ec7d98d8398948b78edb
workflow-type: tm+mt
source-wordcount: 887
ht-degree: 12%

---

# Personalice el fondo del correo electrónico {#backgrounds}

>[!BEGINSHADEBOX]

**En esta página:** aprenda a establecer colores e imágenes de fondo en los niveles de cuerpo, ventanilla, estructura y columna del correo electrónico en el diseñador de correo electrónico.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ac_edition_backgroundimage"
>title="Configuración de fondo"
>abstract="Puede personalizar el color o la imagen de fondo del contenido. Tenga en cuenta que la imagen de fondo no es compatible con todos los clientes de correo electrónico."

Los fondos le ayudan a reforzar su identidad de marca y a llamar la atención sobre las áreas clave de su correo electrónico. En el Designer de correo electrónico, puede establecer un color de fondo o una imagen en diferentes niveles del contenido, desde el cuerpo general hasta las estructuras y columnas individuales, lo que le proporciona un control preciso sobre cómo se representan los fondos en el correo electrónico.

Tenga en cuenta las siguientes prácticas recomendadas al configurar fondos en el Designer de correo electrónico:

* Aplique un color de fondo al cuerpo solo si el diseño lo requiere.
* Prefiera establecer colores de fondo en el nivel de columna siempre que sea posible.
* Evite utilizar colores de fondo en componentes de imagen o texto, ya que son más difíciles de administrar.
* Pruebe las imágenes de fondo en los clientes de correo electrónico reales antes de enviarlas, ya que el procesamiento puede diferir de la previsualización de Designer de correo electrónico.

La siguiente configuración permite aplicar un color de fondo o una imagen en cualquier nivel del contenido del correo electrónico, desde el cuerpo hasta las estructuras y columnas individuales.

>[!TIP]
>
>Si se aplica una temática al correo electrónico, no puede anular directamente el color de fondo establecido por la temática para un componente determinado. Primero debe desbloquear ese estilo usando el icono dedicado en la ficha **[!UICONTROL Estilos]**. [Descubra cómo](apply-email-themes.md#unlocking-styles)

## Definir un color de fondo {#background-color}

1. **Color de fondo del cuerpo** - Establece un **[!UICONTROL color de fondo]** para todo el correo electrónico. Asegúrese de seleccionar **[!UICONTROL Cuerpo]** en el **[!UICONTROL árbol de navegación]** al que se puede acceder desde la paleta izquierda y utilice la opción dedicada de la pestaña **[!UICONTROL Estilos]** a la derecha.

   ![Designer de correo electrónico con el cuerpo seleccionado en el árbol de navegación y la opción Color de fondo resaltada en el panel Estilos](assets/background_1.png)

1. **Color de fondo de ventanilla** - Establezca un **[!UICONTROL color de ventanilla]** para aplicar el mismo color de fondo a todos los componentes de la estructura, independientemente del color de fondo del cuerpo.

   ![Panel de estilos de Designer de correo electrónico con la opción de color de ventanilla resaltada y un selector de color abierto para elegir el color de fondo aplicado a todas las estructuras](assets/background_2.png)

1. **Color de fondo de la estructura**: para aplicar un color de fondo a un solo componente de estructura, selecciónelo directamente en el lienzo o en la paleta izquierda y establezca un color específico para esa estructura.

   ![Panel Estilos de Designer de correo electrónico para una estructura seleccionada, con la opción Color de fondo resaltada](assets/background_3.png)

   >[!TIP]
   >
   >En ese caso, asegúrese de no establecer un color de fondo de ventanilla, ya que puede ocultar los colores de fondo de la estructura.

1. **Color de fondo de columna** - Establecer un color de fondo en el nivel de columna. De nuevo, asegúrese de seleccionar la columna deseada de la paleta izquierda y establecer un color específico para esa columna.

   ![Panel Estilos de Designer de correo electrónico para una columna seleccionada, con la opción Color de fondo resaltada](assets/background_5.png)

   >[!TIP]
   >
   >Este es el caso de uso más común y una práctica recomendada, ya que le ofrece más flexibilidad al editar el resto del contenido del correo electrónico.

## Establecer una imagen de fondo {#background-image}

También puede establecer una **[!UICONTROL imagen de fondo]** para el contenido de un componente de estructura o columna. Esto se utiliza generalmente en el nivel de estructura; es posible configurar uno en el nivel de columna, pero rara vez se utiliza.

>[!NOTE]
>
>Algunos programas de correo electrónico no admiten imágenes de fondo. Cuando no se admite, se utiliza el color de fondo de la fila. Asegúrese de seleccionar un color de fondo alternativo adecuado en caso de que la imagen no se pueda mostrar.

![Panel Estilos de Designer de correo electrónico con la imagen de fondo habilitada y la ubicación de la imagen establecida en Altura completa - Derecha, que muestra la imagen que rellena una columna](assets/background_4.png)

>[!TIP]
>
>Obtenga una vista previa de la imagen de fondo en los clientes de correo electrónico reales antes de enviarla, no solo en la vista previa de Designer de correo electrónico. La misma imagen y la misma ubicación pueden representarse correctamente en el editor, pero aparecen estiradas o recortadas de forma diferente en algunos clientes, como Outlook en iOS.

Una vez establecida una imagen de fondo, utilice la lista desplegable **[!UICONTROL Ubicación de la imagen]** para controlar cómo la imagen rellena la estructura o la columna. Las siguientes opciones están disponibles para seleccionarlas:

![Panel Estilos de Designer de correo electrónico que muestra el menú desplegable Ubicación de la imagen con varias opciones](assets/background_6.png){width=80%}

**Escala para rellenar, centrada:**

* **[!UICONTROL Ajustar]**: expande la imagen para llenar el contenedor en ambos ejes, sin conservar su proporción de aspecto.
* **[!UICONTROL Ancho completo]**: escala la imagen proporcionalmente a la anchura del contenedor y la centra verticalmente.
* **[!UICONTROL Altura completa]**: escala la imagen proporcionalmente a la altura del contenedor y la centra horizontalmente.

**Escalar para rellenar, anclado a un borde:**

* **[!UICONTROL Anchura completa - Superior]** - Igual que **[!UICONTROL Anchura completa]**, anclado en la parte superior del contenedor. El desbordamiento se recorta en la parte inferior.
* **[!UICONTROL Anchura completa - Inferior]** - Igual que **[!UICONTROL Anchura completa]**, anclado en la parte inferior del contenedor. El desbordamiento se recorta en la parte superior.
* **[!UICONTROL Altura completa - Izquierda]** - Igual que **[!UICONTROL Altura completa]**, anclado a la izquierda del contenedor. El desbordamiento se recorta a la derecha.
* **[!UICONTROL Altura completa - Derecha]** - Igual que **[!UICONTROL Altura completa]**, anclado a la derecha del contenedor. El desbordamiento se recorta a la izquierda.

**Mosaico:**

* **[!UICONTROL Repetir]** - Mosaica la imagen en su tamaño original para llenar el contenedor.

**Posición sin escala:**

* **[!UICONTROL Izquierda]**, **[!UICONTROL Derecha]**, **[!UICONTROL Centro]**, **[!UICONTROL Superior]**, **[!UICONTROL Inferior]**: coloca la imagen en su tamaño original, anclada al borde o centro correspondiente del contenedor.

>[!NOTE]
>
>Las opciones ancladas al borde le proporcionan más control sobre qué parte de la imagen permanece en la vista cuando no coincide con las proporciones de la estructura, en comparación con las opciones centradas anteriores.

{{$include /help/_includes/do-not-localize/email/ai-augmented-backgrounds.md}}
