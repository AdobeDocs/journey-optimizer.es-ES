---
solution: Journey Optimizer
product: journey optimizer
title: Diseño de contenido accesible
description: Aprenda a diseñar contenido accesible para sus correos electrónicos y páginas de aterrizaje en Journey Optimizer
feature: Email Design, Landing Pages
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: correo electrónico, diseño, accesibilidad
source-git-commit: 57890eede1d5a0de6002f31b9ce8807a903b84f7
workflow-type: tm+mt
source-wordcount: '1610'
ht-degree: 0%

---

# Diseño de contenido accesible {#accessible-content}

La [Ley Europea de Accesibilidad](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32019L0882){target="_blank"} es una directiva diseñada para mejorar el mercado interno de productos y servicios accesibles al eliminar las barreras causadas por las diferentes reglas nacionales en los Estados Miembros.

Esta regulación establece que todas las comunicaciones digitales, incluidos correos electrónicos, boletines informativos, PDF y contenido descargable, deben ser accesibles. Por lo tanto, al crear contenido para los destinatarios, se le exige que siga directrices específicas como el uso de fuentes accesibles, formatos legibles y proporcionar texto alternativo para las imágenes.

El [!DNL Journey Optimizer] [Designer de correo electrónico](content-from-scratch.md), que permite a los especialistas en marketing crear contenido para **correos electrónicos** y **páginas de aterrizaje**, le permite cumplir fácilmente con esta directiva, según las Directrices de accesibilidad del contenido web (WCAG) 2.1, nivel AA.

En línea con esto, las prácticas recomendadas para diseñar contenido accesible con [!DNL Journey Optimizer] se enumeran a continuación.

>[!NOTE]
>
>En esta página se trata de poner el contenido a disposición de todos los destinatarios para garantizar que las personas con discapacidades puedan leer, comprender e interactuar con los mensajes de correo electrónico y las páginas de aterrizaje diseñados con [!DNL Journey Optimizer].
>
>Por otro lado, la accesibilidad de la interfaz de [!DNL Journey Optimizer] se detalla en [esta sección](../start/accessibility.md).
> 
## Garantizar la legibilidad del texto {#text-readability}

Aproveche la pestaña **[!UICONTROL Estilos]** del componente **[!UICONTROL Texto]** para asegurarse de que el texto sea legible, por ejemplo, usando un contraste de color adecuado y fuentes simples. [Más información](content-components.md#text)

![](assets/accessible-text-styles.png){width="80%"}

Para las fuentes y el texto, asegúrese de seguir las directrices siguientes:

**Selección de fuente**

* Utilice fuentes sans-serif como Arial, Verdana, Tahoma, Helvetica o Open Sans.
* Evite las fuentes seriadas, cursivas o decorativas en el contenido del cuerpo.
* Utilice un conjunto de fuentes limitado para mantener la coherencia y la reserva (por ejemplo: `font-family: Arial, Helvetica, sans-serif;`).

**Tamaño de fuente**

* Asegúrese de que el tamaño mínimo de la fuente sea de 16 píxeles para el texto del cuerpo.
* Utilice la jerarquía adecuada para los encabezados.

**Contraste de color**

* Mantenga una relación de contraste de al menos 4,5:1 entre el texto y el fondo.
* Para texto grande (≥24 px o negrita 18 px), asegúrese de que haya al menos un contraste de 3:1.
* Evite el texto gris claro o pastel sobre fondos blancos.
* No confíe solo en el color para transmitir significado, sino que utilice subrayados, iconos, etc.

**Accesibilidad de texto**

* Evite el texto en las imágenes.
* No utilice mayúsculas en el texto del cuerpo.
* Asegúrese de que el texto se pueda ampliar hasta un 200 % sin romper el diseño.

## Garantizar la accesibilidad visual {#visual-accessibility}

Para asegurarse de que el contenido es accesible visualmente, siga las prácticas recomendadas a continuación:

* Evite utilizar indicadores de solo color para la información importante.
* Utilice etiquetas de texto o iconos para garantizar la claridad.
* Optimice su diseño para diseños móviles y adaptables, asegurándose de que los botones sean grandes y estén correctamente espaciados.
* Realice pruebas con regularidad en todos los dispositivos y tamaños de pantalla para mantener la accesibilidad.

En [!DNL Journey Optimizer], el tamaño y el espaciado de los diferentes elementos del contenido se pueden refinar aún más mediante los parámetros y atributos de estilo del panel **[!UICONTROL Estilos]** de Designer de correo electrónico. [Más información](get-started-email-style.md)

Por ejemplo, puede actualizar el [fondo](backgrounds.md) o cambiar los márgenes, el relleno y la alineación para mejorar la accesibilidad visual del contenido. [Más información](alignment-and-padding.md)

![](assets/accessible-styles.png){width="80%"}

Además, [!DNL Journey Optimizer] Email Designer permite obtener una vista previa y optimizar el diseño para diferentes dispositivos y tamaños de pantalla. En cualquier momento puedes **[!UICONTROL Cambiar a la vista en vivo]** para comprobar cómo se puede presentar tu contenido en varios tamaños de dispositivo.

![](assets/accessible-live-view.png){width="80%"}

>[!CAUTION]
>
>La vista en directo es una previsualización genérica diseñada para comparar el aspecto que podría tener la renderización en varios tamaños de dispositivo. La renderización final puede variar según el cliente de correo electrónico del destinatario.

## Usar texto alternativo para imágenes {#alt-text}

Utilice el componente **[!UICONTROL Image]** para proporcionar texto alternativo para las imágenes. [Más información](content-components.md#image)

![](assets/accessible-alt-text.png){width="90%"}

Para obtener texto alternativo efectivo en productos digitales, siga las directrices siguientes:

* Describa el propósito de la imagen de forma concisa y contextual.
* Evite frases redundantes como &quot;Imagen de...&quot; y utilice texto alternativo vacío para imágenes decorativas.
* Para los iconos con significado, proporcione etiquetas significativas y, para las imágenes complejas, utilice un texto alternativo breve más una descripción más larga en otra parte.

## Usar formato legible {#readable-format}

Use la estructura relevante de Designer de correo electrónico y [componentes de contenido](content-components.md), así como las opciones del panel **[!UICONTROL Estilos]**, para organizar el contenido de una manera clara, lógica y concisa, accesible para todos.

![](assets/accessible-components.png){width="100%"}

* Utilice una HTML semántica estructurada con encabezados, párrafos, listas y tablas adecuados.
* Asegúrese de que el contenido sigue un flujo lógico de izquierda a derecha, de arriba a abajo.
* Utilice un lenguaje claro y conciso.
* Proporcionar formatos alternativos para PDF e infografías.
* Permita cambiar el tamaño y el reflujo del texto y asegúrese de que la tipografía sea legible con un contraste de color adecuado en todos los formatos.

## Garantizar la legibilidad del contenido {#readability}

Para ser legible, el contenido debe ser claro, bien estructurado y utilizable por todos, incluidas las personas con dificultades visuales, cognitivas o de lectura y las que utilizan tecnologías de asistencia. Algunos puntos a tener en cuenta al crear contenido accesible son:

* Mantener las frases en unas 20 palabras o menos.
* Edite la copia para que sea directa y directa.
* Utilice la voz activa para simplificar la estructura de la oración.
* Evite utilizar jergas, jergas o palabras regionales con las que algunas personas no estén familiarizadas.

Para evaluar la legibilidad del correo electrónico, puede usar la popular [prueba de facilidad de lectura de Flesch](https://support.microsoft.com/en-us/office/get-your-document-s-readability-and-level-statistics-85b4969e-e80a-4777-8dd3-f7fc3c8b3fd2){target="_blank"}, que se encuentra en Microsoft Word y calcula la facilidad de lectura del contenido en una escala del 0 al 100.

## Prueba del contenido {#test}

Para comprobar la accesibilidad del contenido, puede utilizar las funciones de prueba proporcionadas por [!DNL Journey Optimizer]. No están diseñadas específicamente para comprobar si el contenido es totalmente accesible, pero pueden proporcionar un primer nivel de verificación.

* Vista previa del contenido mediante perfiles de prueba. [Descubra cómo](../content-management/preview.md)

* Utilice la opción [Procesamiento de correo electrónico](../content-management/rendering.md) que aprovecha Litmus para simular los diseños en los principales clientes de correo electrónico (Apple Mail, Gmail, Outlook) y ver si el texto, los colores y las imágenes hacen que el contenido sea accesible. <!--Litmus includes accessibility testing-->

* Envíe pruebas para probar la renderización del contenido antes de enviarlo a su audiencia real. [Descubra cómo](../content-management/proofs.md)

![](assets/accessible-simulate.png){width="90%"}

Para comprobar de forma más coherente si el contenido es accesible de forma fiable, vaya a por herramientas externas específicas como:

* El verificador de contraste [WebAim](https://webaim.org/resources/contrastchecker/){target="_blank"} y la [herramienta de evaluación de accesibilidad web WAVE](https://wave.webaim.org/){target="_blank"} para evaluar el contraste y el cumplimiento;

* Tecnologías de asistencia como lectores de pantalla (por ejemplo: [NVDA](https://www.nvaccess.org/download/){target="_blank"} o [VoiceOver](https://support.apple.com/en-ie/guide/iphone/iph3e2e415f/ios){target="_blank"} en iPhone) para recibir correos electrónicos desde la perspectiva de los usuarios con problemas de visión.

## Usar modo oscuro {#dark-mode}

<!--TO PUBLISH WHEN DARK MODE IS RELEASED-->

El modo oscuro mejora la accesibilidad visual para los usuarios con sensibilidad a la luz o deficiencias visuales, para una experiencia de visualización mejorada.

![](assets/accessible-dark-mode.png){width="90%"}

Entre las prácticas recomendadas para diseñar contenido en modo oscuro, utilice archivos PNG o SVG transparentes, establezca etiquetas meta y CSS adecuadas y proporcione un estilo de reserva accesible si no se admite el modo oscuro. Finalmente, asegúrese de que los correos electrónicos se representan correctamente en el modo oscuro probando todo el contenido del correo electrónico y los elementos de la interfaz de usuario en los modos claro y oscuro.

Las prácticas recomendadas detalladas específicas del modo oscuro, incluidas las directrices para garantizar la accesibilidad, se enumeran en [esta sección](dark-mode.md#best-practices). <!--KEEP dark mode accessibility best practices IN ONE SINGLE LOCATION - for now listed on the Dark mode page.-->

## Utilizar atributos específicos para la accesibilidad {#attributes}

### Atributos de idioma {#language}

Al crear diseños, incluya los atributos `lang` (idioma) y `dir` (dirección del texto) en el cuerpo del contenido. Estos atributos ayudan a las tecnologías de asistencia, como los lectores de pantalla, a interpretar y presentar el contenido de una manera adecuada.

* El atributo `lang` indica el idioma del correo electrónico para las tecnologías de asistencia, lo que garantiza que las palabras se pronuncien correctamente.

  +++Ejemplos

  Ejemplo para inglés:

  ```
  <body lang="en">
  ```

  Ejemplo para francés:

  ```
  <body lang="fr">
  ```

  +++

* El atributo `dir` especifica la dirección del texto. La mayoría de los idiomas, incluidos el inglés y el francés, se leen de izquierda a derecha (ltr), mientras que idiomas como el árabe y el hebreo se leen de derecha a izquierda (rtl).

  +++Ejemplos

  Ejemplo para inglés (de izquierda a derecha):

  ```
  <body lang="en" dir="ltr">
  ```

  Ejemplo para árabe (de derecha a izquierda):

  ```
  <body lang="ar" dir="rtl">
  ```

  +++

Los lectores de pantalla dependen del atributo `lang` para aplicar las reglas de pronunciación correctas, mientras que la dirección del texto garantiza que el contenido fluya de forma natural para los idiomas de izquierda a derecha o de derecha a izquierda. Sin estos atributos, los usuarios pueden experimentar un orden de lectura confuso o una pronunciación incorrecta. En consecuencia, ajuste siempre el cuerpo del correo electrónico con los atributos adecuados de `lang` y `dir`.

>[!TIP]
>
>Si el correo electrónico contiene varios idiomas, asigne los atributos de idioma adecuados a secciones específicas (como bloques de `<table>` o `<td>`) para garantizar que cada parte se lea correctamente.

### Tablas {#tables}

En el contenido de HTML, las tablas suelen utilizarse para el diseño. De manera predeterminada, los lectores de pantalla tratan cada `<table>` como una tabla de datos, y anuncian filas, columnas y estructura. Esto puede resultar confuso si la tabla solo se utiliza para dar formato.

Agregue `role="presentation"` (o `role="none"`) a las tablas de diseño para garantizar que las tecnologías de asistencia omitan su estructura y se centren únicamente en el contenido real.

+++Ejemplo: Tabla de diseño (con `role="presentation"`)

```
<table role="presentation" border="0" cellpadding="0" cellspacing="0" width="100%"> 

  <tr> 

    <td align="center"> 

      <h1>Hello World</h1> 

      <p>Welcome to our newsletter</p> 

    </td> 

  </tr> 

</table>
```

Los lectores de pantalla dicen:
&quot;Hola Mundo. Bienvenido a nuestro boletín informativo&quot;. *(sin mención de filas, columnas ni tablas)*

+++

+++Ejemplo: tabla de datos (sin `role="presentation"`)

```
<table border="1" cellpadding="5" cellspacing="0"> 

  <tr> 

    <th scope="col">Name</th> 

    <th scope="col">Score</th> 

  </tr> 

  <tr> 

    <td>Alice</td> 

    <td>95</td> 

  </tr> 

  <tr> 

    <td>Bob</td> 

    <td>88</td> 

  </tr> 

</table> 
```

Los lectores de pantalla dicen:
&quot;Tabla con 2 columnas y 3 filas.&quot;

&quot;Nombre, Alice. Puntuación: 95&quot;.

&quot;Nombre, Bob. Puntuación: 88&quot;.

+++

>[!TIP]
>
>Usar `role="presentation"` exclusivamente para tablas de diseño. Para las tablas de datos, conserve la estructura semántica `<table>` de modo que los lectores de pantalla puedan anunciar correctamente los encabezados y las relaciones.

### Texto para vínculos {#links}

Los lectores de pantalla leen los vínculos usando su texto. Si un vínculo solo está etiquetado como &quot;Haga clic aquí&quot; o &quot;Más información&quot;, los usuarios de tecnologías de asistencia no sabrán el destino. Para garantizar la accesibilidad, necesitan un texto descriptivo que indique claramente el destinatario o la acción.

Use el Designer de correo electrónico para [agregar un vínculo](message-tracking.md#insert-links) al contenido y editarlo para que sea discernible (visible) y descriptivo (claro sobre el propósito). Evite etiquetas vagas como &quot;aquí&quot; o &quot;más&quot;.

![](assets/accessible-link.png){width="70%"}

+++Ejemplo: buen vínculo (descriptivo): 

```
<p>Learn more in the  

<a href="https://adobe.com/release-notes">August release notes</a>. 

</p>
```

Los lectores de pantalla dicen:
&quot;Vínculo, notas de la versión de agosto&quot;.

+++

+++Ejemplo: vínculo incorrecto (no descriptivo)

```
<p>Learn more about our new features.  

  <a href="https://adobe.com/release-notes">Click here</a>. 

</p>
```

Los lectores de pantalla dicen:
&quot;Link, haga clic aquí.&quot; *(no proporciona contexto fuera del orden de lectura)*

+++

<!--
>[!TIP]
>
>Always ensure link text is discernible (visible) and descriptive (clear about purpose). Avoid vague labels like 'here' or 'more'.-->

## Proporcionar compatibilidad de enfoque y navegación mediante el teclado {#keyboard}

<!--for landing pages-->

Proporcionar compatibilidad con la navegación mediante el teclado y el enfoque permite a las personas que no pueden utilizar un ratón acceder e interactuar con el contenido por completo. También mejora la capacidad de uso general al proporcionar a todos los usuarios una forma clara y coherente de desplazarse por la información.

* Enfoque mediante el teclado

   * Asegúrese de que todos los elementos interactivos (como botones, casillas de verificación y vínculos) tengan `tabindex="0"` para que se incluyan en el orden de tabulación natural.

   * Permita la navegación utilizando las teclas de tabulación y flecha (↑ ↓ ← →), que deben resaltar visiblemente el elemento centrado.

* Estilo de enfoque personalizado

   * Aplique estilos claros y distinguibles para centrarse en elementos procesables:

     +++Ejemplo (CSS)

     ```
     [tabindex="0"] : focus { 
     
     outline: 2px solid #00AEEF;  /* Cyan border */ 
     
     background-color: #20CEFF;   /* Optional background */ 
     
     }
     ```

     +++

   * Asegúrese de que los indicadores de enfoque cumplan los estándares de apariencia de enfoque WCAG 2.2, que incluyen:

      * Área mínima: contorno de grosor de 2 píxeles CSS.

      * Proporción de contraste: ≥ 3:1 entre el estado centrado y no centrado.

* Compatibilidad con activación de teclado

   * Asegúrese de que las casillas de verificación y los botones responden a las teclas Intro y Espacio.

   * Validar la interacción utilizando solo el teclado:

      * Intro o Espacio deben alternar las casillas de verificación.

      * Intro o espacio deben contener botones de déclencheur.
