---
solution: Journey Optimizer
product: journey optimizer
title: Administrar marca
description: Aprenda a crear y administrar las directrices de marca
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: b1b7abbe-8600-4a8d-b0b5-0dbd49abc275
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '1451'
ht-degree: 21%

---

# Creación y administración de sus marcas {#brands}

>[!CONTEXTUALHELP]
>id="ajo_brand_overview"
>title="Introducción a las marcas"
>abstract="Cree y personalice sus propias marcas para definir su identidad visual y verbal única, al tiempo que facilita la generación de contenidos que coinciden con el estilo y la voz de su marca."

>[!CONTEXTUALHELP]
>id="ajo_brand_ai_menu"
>title="Seleccione su marca"
>abstract="Elija su marca para asegurarse de que todo el contenido generado por la IA se adapte a las especificaciones y directrices de su marca."

>[!CONTEXTUALHELP]
>id="ajo_brand_score_overview"
>title="Selección de la marca"
>abstract="Seleccione su marca para asegurarse de que el contenido se crea de acuerdo con sus directrices, estándares e identidad específicos, manteniendo la coherencia y la integridad de la marca."


Las directrices de marca son un conjunto detallado de reglas y estándares que establecen la identidad visual y verbal de una marca. Actúan como referencia para mantener una representación de marca coherente en todas las plataformas de marketing y comunicación.

En [!DNL Journey Optimizer], ahora tiene la opción de introducir y organizar manualmente los detalles de marca o cargar documentos de directrices de marca para la extracción automática de información.

>[!AVAILABILITY]
>
>Debe aceptar el [acuerdo de usuario](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} para poder usar el Asistente de IA en Adobe Journey Optimizer. Para obtener más información, contacte con su representante de Adobe.


## Acceso a marcas {#generative-access}

Para acceder al menú de **[!UICONTROL Marcas]** en [!DNL Adobe Journey Optimizer], los usuarios deben recibir los permisos de **[!UICONTROL Administrar kit de marca]** o **[!UICONTROL Habilitar el asistente de IA]**. [Más información](../administration/permissions.md)

+++  Aprenda a asignar permisos relacionados con la marca

Para asignar permisos para marcas, siga estos pasos:

1. En el producto **Permisos**, vaya a la pestaña **Funciones** y seleccione la **Función** que desee.

1. Haga clic en **Editar** para modificar los permisos.

1. Agregue el recurso **Asistente de IA** y, a continuación, seleccione **Administrar kit de marca** o **[!UICONTROL Habilitar el asistente de IA]** en el menú desplegable.

   Tenga en cuenta que el permiso **[!UICONTROL Habilitar el asistente de IA]** solo proporciona acceso de solo lectura al menú **[!UICONTROL Marcas]**.

   ![](assets/brands-permission.png){zoomable="yes"}

1. Haga clic en **Guardar** para aplicar los cambios.

   Los permisos de los usuarios que ya estén asignados a esta función se actualizarán automáticamente.

1. Para asignar esta función a nuevos usuarios, vaya a la pestaña **Usuarios** en el panel de control **Funciones** y haga clic en **Añadir usuario**.

1. Introduzca el nombre del usuario y su dirección de correo electrónico, o selecciónelo en la lista, y haga clic en **Guardar**.

1. Si el usuario no estaba ya creado, consulte [esta documentación](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Creación y administración de la marca {#create-brand-kit}

>[!CONTEXTUALHELP]
>id="ajo_brands_create"
>title="Cree su marca"
>abstract="Introduzca el nombre de su marca y cargue el archivo de directrices de la marca. La herramienta extraerá automáticamente los detalles clave, lo que facilita el mantenimiento de la identidad de su marca."

Para crear y administrar las directrices de marca, puede introducir los detalles usted mismo o cargar el documento de directrices de marca para que la información se extraiga automáticamente:

1. En el menú **[!UICONTROL Marcas]**, haga clic en **[!UICONTROL Crear marca]**.

   ![](assets/brands-1.png)

1. Escriba un **[!UICONTROL Nombre]** para su marca.

1. Arrastre y suelte o seleccione el archivo para cargar las directrices de marca y extraer automáticamente la información de marca relevante. Haga clic en **[!UICONTROL Crear marca]**.

   Ahora comienza el proceso de extracción de información. Tenga en cuenta que puede tardar varios minutos en completarse.

   ![](assets/brands-2.png)

1. Los estándares de creación visual y de contenido ahora se rellenan automáticamente. Examine las diferentes pestañas para adaptar la información según sea necesario. [Más información](#personalize)

1. Desde el menú avanzado de cada sección o categoría, puede añadir referencias para extraer automáticamente información de marca relevante.

   Para quitar el contenido existente, usa las opciones **[!UICONTROL Borrar sección]** o **[!UICONTROL Borrar categoría]**.

   ![](assets/brands-15.png)

1. Una vez configurada, haz clic en **[!UICONTROL Guardar]** y luego en **[!UICONTROL Publicar]** para que la guía de marca esté disponible en el Asistente de IA.

1. Para hacer modificaciones a tu marca publicada, haz clic en **[!UICONTROL Editar marca]**.

   >[!NOTE]
   >
   >Esto crea una copia temporal en el modo de edición y reemplaza la versión activa una vez publicada.

   ![](assets/brands-8.png)

1. En el panel **[!UICONTROL Marcas]**, abra el menú avanzado haciendo clic en el icono ![](assets/do-not-localize/Smock_More_18_N.svg) para:

   * Ver marca
   * Editar
   * Duplicar
   * Publicación
   * Cancelar publicación
   * Eliminar

   ![](assets/brands-6.png)

Ahora se puede acceder a las directrices de marca desde la lista desplegable **[!UICONTROL Marca]** del menú Asistente de IA, lo que le permite generar contenido y recursos alineados con las especificaciones. [Más información sobre el Asistente de IA](gs-generative.md)

![](assets/brands-7.png)

### Establecer una marca predeterminada {#default-brand}

Puede designar una marca predeterminada para que se aplique automáticamente al generar contenido y calcular las puntuaciones de alineación durante la creación de la campaña.

Para establecer una marca predeterminada, ve a tu panel **[!UICONTROL Marcas]**. Abra el menú avanzado haciendo clic en el icono ![](assets/do-not-localize/Smock_More_18_N.svg) y seleccione **[!UICONTROL Marcar como marca predeterminada]**.

![](assets/brands-9.png)

## Personalice su marca {#personalize}

### Acerca de la marca {#about-brand}

Use la ficha **[!UICONTROL Acerca de la marca]** para establecer la identidad central de su marca, y delinear su propósito, personalidad, eslogan y otros atributos que la definen.

1. Comience por rellenar la información fundamental de su marca en la categoría **[!UICONTROL Detalles clave]**:

   * **[!UICONTROL Nombre del kit de marca]**: Escriba el nombre del kit de marca.

   * **[!UICONTROL Cuándo se debe usar]**: especifique los escenarios o contextos a los que se debe aplicar este kit de marca.

   * **[!UICONTROL Nombre de marca]**: escriba el nombre oficial de la marca.

   * **[!UICONTROL Descripción de la marca]**: proporcione una descripción general de lo que representa esta marca.

   * **[!UICONTROL Línea de etiquetas predeterminada]**: Agregue el lema principal asociado con la marca.

     ![](assets/brands-about-1.png)

1. En la categoría **[!UICONTROL Principios rectores]**, aclare la dirección y filosofía básicas de su marca:

   * **[!UICONTROL Misión]**: detalla el propósito de tu marca.

   * **[!UICONTROL Visión]**: describe tu objetivo a largo plazo o el estado futuro deseado.

   * **[!UICONTROL Posicionamiento en el mercado]**: explica cómo se posiciona tu marca en el mercado.

     ![](assets/brands-about-2.png)

1. En la categoría **[!UICONTROL Valores principales de marca]**, haga clic en ![Texto alternativo de la imagen de buceo](assets/do-not-localize/Smock_Add_18_N.svg "Agregar icono") para agregar los valores principales de la marca y rellenar los detalles:

   * **[!UICONTROL Valor]**: Asigne un nombre al valor de marca principal.

   * **[!UICONTROL Descripción]**: explica qué significa este valor para tu marca.

   * **[!UICONTROL Comportamientos]**: describe las acciones o actitudes que reflejan este valor en la práctica.

   * **[!UICONTROL Manifestaciones]**: dé ejemplos de cómo se expresa este valor en la promoción de marca en el mundo real.

     ![](assets/brands-12.png)

1. Si es necesario, haz clic en el icono ![Dive image alt text](assets/do-not-localize/Smock_Edit_18_N.svg "Editar")para actualizar o eliminar uno de los valores principales de tu marca.

   ![](assets/brands-10.png)

Ahora puedes personalizar aún más tu marca o [publicar tu marca](#create-brand-kit).

### Estilo de escritura {#writing-style}

>[!CONTEXTUALHELP]
>id="ajo_brand_writing_style"
>title="Puntuación del estilo de escritura"
>abstract="La sección Estilo de escritura define los estándares de lenguaje, formato y estructura para garantizar un contenido claro y coherente. La puntuación de alineación, clasificada de alta a baja, muestra en qué medida el contenido sigue estas directrices y resalta las áreas de mejora."

La sección **[!UICONTROL Estilo de escritura]** describe los estándares para escribir contenido, y detalla cómo se debe usar el idioma, el formato y la estructura para mantener la claridad, la coherencia y la consistencia en todos los materiales.

+++ Categorías y ejemplos disponibles

<table>
  <thead>
    <tr>
      <th>Categoría</th>
      <th>Subcategoría</th>
      <th>Ejemplo de directrices</th>
      <th>Ejemplo de exclusiones</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4">Estándares de creación de contenido</td>
      <td>Estándares de mensajería de marca</td>
      <td>Resalte la innovación y la mensajería basada en el cliente.</td>
      <td>No prometa excesivamente las capacidades del producto.</td>
    </tr>
    <tr>
      <td>Uso de lema</td>
      <td>Coloque el lema debajo del logotipo en todos los recursos de marketing digital.</td>
      <td>No modifique ni traduzca el lema.</td>
    </tr>
    <tr>
      <td>Mensajería principal</td>
      <td>Enfatice la declaración de beneficios clave, como la mejora de la productividad.</td>
      <td>No utilice propuestas de valores no relacionadas.</td>
    </tr>
    <tr>
      <td>Estándares de nomenclatura</td>
      <td>Utilice nombres descriptivos sencillos como "ProScheduler".</td>
      <td>No utilice términos complejos ni caracteres especiales.</td>
    </tr>
    <tr>
      <td rowspan="5">Estilo de comunicación de marca</td>
      <td>Características de personalidad de marca</td>
      <td>Amable y accesible.</td>
      <td>No seas derrotista.</td>
    </tr>
    <tr>
      <td>Mecánica de escritura</td>
      <td>Utilice frases cortas e impactantes.</td>
      <td>No use jerga excesiva.</td>
    </tr>
    <tr>
      <td>Tono situacional</td>
      <td>Mantener un tono profesional en las comunicaciones de crisis.</td>
      <td>No sea desdeñoso en las comunicaciones de soporte.</td>
    </tr>
    <tr>
      <td>Directrices de opción de Word</td>
      <td>Utilice palabras como "innovador" e "inteligente".</td>
      <td>Evite palabras como "barato" o "hackear".</td>
    </tr>
    <tr>
      <td>Estándares de idioma</td>
      <td>Sigue las convenciones del inglés americano.</td>
      <td>No mezcle ortografía británica y estadounidense.</td>
    </tr>
    <tr>
      <td rowspan="3">Normas de cumplimiento legal</td>
      <td>Normas de marcas</td>
      <td>Utilice siempre el símbolo ™ o ®.</td>
      <td>No omita los símbolos legales cuando sea necesario.</td>
    </tr>
    <tr>
      <td>Estándares de copyright</td>
      <td>Incluir avisos de copyright en los materiales de marketing.</td>
      <td>No utilice contenido de terceros sin permiso.</td>
    </tr>
    <tr>
      <td>Normas de exención de responsabilidad</td>
      <td>Muestre de forma legible las exenciones de responsabilidad en los recursos digitales.</td>
      <td>No oculte las exenciones de responsabilidad en áreas no visibles.</td>
    </tr>
</table>

+++

</br>

Para personalizar tu **[!UICONTROL estilo de escritura]**:

1. En la ficha **[!UICONTROL Estilo de escritura]**, haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar una directriz, excepción o exclusión.

1. Escriba la directriz, excepción o exclusión y haga clic en **[!UICONTROL Agregar]**.

   ![](assets/brands-3.png)

1. Seleccione una de las directrices o exclusiones para actualizar o eliminar.

1. Haga clic en el ![texto alternativo de la imagen de buceo](assets/do-not-localize/Smock_Edit_18_N.svg "Editar") para editar el ejemplo o en el ![Texto alternativo de la imagen de buceo](assets/do-not-localize/Smock_Delete_18_N.svg "Eliminar")icono para eliminarlo.

   ![](assets/brands-11.png)

Ahora puedes personalizar aún más tu marca o [publicar tu marca](#create-brand-kit).

### Contenido visual {#visual-content}

>[!CONTEXTUALHELP]
>id="ajo_brand_imagery"
>title="Puntuación de alineación del contenido visual"
>abstract="La puntuación de alineación de contenido visual indica la adecuación del contenido a las directrices de marca configuradas. Puntuado de alto a bajo, le ayuda a evaluar la alineación de un vistazo. Explore las diferentes categorías para identificar las áreas de mejora y localizar elementos que puedan estar fuera de la marca."

La sección **[!UICONTROL Contenido visual]** define los estándares para imágenes y diseño, detallando las especificaciones necesarias para mantener un aspecto de marca unificado y coherente.

+++ Categorías y ejemplos disponibles

<table>
  <thead>
    <tr>
      <th>Categoría</th>
      <th>Ejemplo de directrices</th>
      <th>Ejemplo de exclusiones</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Normas de fotografía</td>
      <td>Utilice la iluminación natural para las tomas al aire libre.</td>
      <td>Evite las imágenes sobreeditadas o pixeladas.</td>
    </tr>
    <tr>
      <td>Estándares de ilustración</td>
      <td>Utilice estilos limpios y minimalistas.</td>
      <td>Evite los problemas excesivamente complejos.</td>
    </tr>
    <tr>
      <td>Estándares de icono</td>
      <td>Utilice un sistema de cuadrícula coherente de 24 píxeles.</td>
      <td>No mezcle dimensiones de icono, utilice grosores de trazo incoherentes ni se desvíe de las reglas de cuadrícula.</td>
    </tr>
    <tr>
      <td>Directrices de uso</td>
      <td>Elija imágenes de estilo de vida que reflejen el uso que hacen los clientes reales del producto en entornos profesionales.</td>
      <td>No utilice imágenes que contradigan el tono de la marca o que aparezcan fuera de contexto.</td>
    </tr>
</table>

+++

</br>

Para personalizar tu **[!UICONTROL contenido visual]**:

1. En la ficha **[!UICONTROL Contenido visual]**, haga clic en ![](assets/do-not-localize/Smock_Add_18_N.svg) para agregar una directriz, una exclusión o un ejemplo.

1. Escriba la directriz, exclusión o ejemplo y haga clic en **[!UICONTROL Agregar]**.

   ![](assets/brands-4.png)

1. Para agregar una imagen que muestre el uso correcto, seleccione **[!UICONTROL Ejemplo]** y haga clic en **[!UICONTROL Seleccionar imagen]**. También puede añadir una imagen que muestre un uso incorrecto como ejemplo de exclusión.

   ![](assets/brands-13.png)

1. Seleccione una de las directrices o exclusiones para actualizar o eliminar.

1. Seleccione una de las directrices o exclusiones para actualizarla. Haga clic en el icono ![Dive image alt text](assets/do-not-localize/Smock_Delete_18_N.svg "Delete")para eliminarlo.

   ![](assets/brands-14.png)

Ahora puedes personalizar aún más tu marca o [publicar tu marca](#create-brand-kit).
