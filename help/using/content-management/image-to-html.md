---
solution: Journey Optimizer
product: journey optimizer
title: Conversión de imágenes en plantillas de contenido de correo electrónico
description: Aprenda a utilizar el conversor de imágenes a HTML con tecnología de IA para convertir diseños de imagen en plantillas de contenido de correo electrónico editables
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
keywords: correo electrónico, plantilla, imagen, HTML, IA, diseño, convertidor
exl-id: d13467b7-2f3c-4707-a7e0-9b46cb6cafb1
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '2043'
ht-degree: 2%

---

# Conversión de imágenes en plantillas de contenido de correo electrónico {#image-to-html}

[!DNL Journey Optimizer] le ayuda a acelerar en gran medida la creación de correo electrónico al convertir diseños de imagen estáticos en plantillas de contenido de correo electrónico modulares y totalmente personalizables.

>[!AVAILABILITY]
>
>Para usar esta característica, su organización debe haber firmado el anexo [!DNL Generative AI] con Adobe. Si no está seguro, póngase en contacto con su representante de Adobe.
>
>Esta funcionalidad solo está disponible para el canal de correo electrónico.

Al aprovechar la tecnología de IA generativa, una herramienta integrada analiza el diseño, la tipografía, los colores y los elementos visuales de la imagen y genera contenido modular y limpio de HTML que mantiene la fidelidad del diseño, a la vez que garantiza la editabilidad completa con [Email Designer](../email/get-started-email-design.md).

Esta capacidad sin código permite a los especialistas en marketing transformar recursos visuales de diseñadores gráficos o herramientas de diseño en plantillas de correo electrónico interactivas y editables que se pueden guardar y reutilizar en varios recorridos y campañas, sin necesidad de conocimientos técnicos.

>[!IMPORTANT]
>
>Antes de empezar a usar esta característica, lea [Protecciones y recomendaciones](#limitations) relacionadas.

Los principales beneficios son los siguientes:

* **Más rápido que la codificación manual**: el conversor convierte las imágenes en contenido editable en minutos, por lo que puede omitir el lento flujo de trabajo manual de maquetas para HTML.
* **No se necesitan habilidades técnicas**: los especialistas en mercadotecnia pueden producir y ajustar plantillas sin soporte de diseño o desarrollo.
* **Reutilizables en todas las campañas**: guarde las plantillas en la biblioteca y utilícelas en cualquier recorrido o campaña.
* **Se mantiene fiel al diseño**: la salida coincide con el diseño y el estilo, a la vez que es totalmente compatible con el Designer de correo electrónico.

<!--
* **Design fidelity**: Maintain visual consistency with your original design while creating fully editable content
* **Email compatibility**: Generate HTML that works seamlessly with the Email Designer and across email clients
-->

+++ Casos de uso comunes

El convertidor de imagen a HTML es ideal para:

* **Migración de la plataforma**: ¿Está migrando desde otra plataforma de marketing por correo electrónico? Convierta sus diseños de correo electrónico existentes en plantillas de HTML preparadas para [!DNL Journey Optimizer] sin tener que volver a compilar desde cero.
* **Conversión de maqueta de diseño**: transforme maquetas de diseño de herramientas como Photoshop, Figma u otro software de diseño en plantillas de correo electrónico funcionales.
* **Creación rápida de plantillas**: genere plantillas de correo electrónico rápidamente para campañas en las que el tiempo sea importante sin esperar los recursos para desarrolladores.
* **Creación de bibliotecas de plantillas**: cree una biblioteca completa de plantillas compatibles con la marca que los integrantes del equipo que no sean técnicos puedan personalizar e implementar.
* **Reducción de las dependencias técnicas**: permita que los especialistas en marketing creen plantillas de correo electrónico e iteren de forma independiente, lo que acelera la ejecución de la campaña.

+++

## Acceso al conversor de imágenes a HTML {#access-image-to-html}

**Anexo con Adobe**

Para tener acceso a esta característica, su organización debe haber firmado el anexo [!DNL Generative AI] con Adobe. Si no está seguro, póngase en contacto con su representante de Adobe.

**Permisos**

* Para acceder y crear plantillas, su función debe incluir el permiso **[!UICONTROL Administrar plantillas de contenido]** (en el recurso **Administración de contenido**). [Más información sobre los permisos](../administration/permissions.md)

* Para usar el convertidor de imagen a HTML, se le debe otorgar el permiso **Generar contenido**. Aprenda a asignar permisos relacionados con la generación de contenido en [esta sección](../content-management/gs-generative.md#generative-access).

**Acuerdo**

Antes de poder aprovechar esta característica, debe aceptar un acuerdo de usuario que se muestre la primera vez que utilice IA generativa en [!DNL Journey Optimizer]. Para obtener más información, lea las [Directrices de usuario de IA generativa de Adobe Experience Cloud](https://www.adobe.com/es/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

## Mecanismos de protección y recomendaciones {#limitations}

Tenga en cuenta las siguientes limitaciones y recomendaciones al convertir imágenes en plantillas de contenido de correo electrónico.

**Adecuación**

* **Interpretación de IA**: La IA genera contenido HTML estático basado en la interpretación visual de su imagen. Proporciona un buen punto de partida para la creación de correos electrónicos, pero debe revisarse y refinarse con Email Designer para garantizar que cumpla con sus requisitos exactos. Si es necesario, debe agregar manualmente la personalización, el contenido dinámico y el seguimiento después de la conversión.

* **Precisión del texto**: Mientras la IA intenta reconocer y reproducir el texto con precisión, compruebe siempre el contenido del texto y realice las correcciones necesarias. Consulte las [Directrices de usuario de IA generativa de Adobe](https://www.adobe.com/es/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

**Selección de imagen**

* **PII y datos confidenciales**: Asegúrese de seleccionar una imagen que no contenga información personal identificable (PII) u otros datos confidenciales.

* **Tamaño de imagen**: no se pueden cargar imágenes de más de 10 MB.

* **Imágenes de alta calidad**: Para obtener los mejores resultados, use imágenes claras y de alta calidad: imágenes nítidas, texto legible y elementos de diseño bien definidos. Las imágenes borrosas, oscuras o desordenadas reducen la calidad de conversión. Lo ideal es que las imágenes tengan entre 600 y 800 píxeles de ancho para coincidir con las dimensiones de correo electrónico estándar.

* **Diseños simples**: Es posible que los diseños muy complejos con capas intrincadas, formas inusuales o elementos no estándar no se conviertan perfectamente. Los diseños más simples generalmente arrojan mejores resultados.

**Procesando**

* **Actualizar la página**: el resultado no se mostrará automáticamente hasta que lo actualice.

* **Tiempo de procesamiento**: la conversión suele finalizar en **unos 5 minutos**, según la complejidad y el tamaño de la imagen. Las imágenes muy grandes o complejas a veces pueden tardar hasta 10 minutos; espere en consecuencia y actualice para ver el resultado.

<!--
* **Background processing**: The AI processing happens in the background, so you can work on other tasks without keeping the screen open. The template is automatically saved as a draft once the conversion is complete.

**Feedback is welcome!** Use the dedicated section to share your thoughts and suggestions with Adobe to help us improve the feature.
-->

## Conversión de una imagen en una plantilla de HTML {#convert-image}

Para convertir un diseño de imagen en una plantilla de contenido de correo electrónico totalmente personalizable, siga los pasos a continuación.

1. Asegúrese de tener un archivo de imagen en formato JPEG o PNG que contenga su diseño de correo electrónico.

   >[!IMPORTANT]
   >
   >El tamaño de la imagen no puede exceder de **10MB**. Para obtener mejores resultados, usa una **imagen clara y de alta calidad** con imágenes nítidas, texto legible y elementos de diseño bien definidos.

1. Para acceder a la lista de plantillas de contenido, seleccione **[!UICONTROL Administración de contenido]** > **[!UICONTROL Plantillas de contenido]** en el menú de la izquierda.

1. Haga clic en **[!UICONTROL Crear plantilla]**.

1. Complete los detalles de la plantilla, seleccione **[!UICONTROL Correo electrónico]** como canal y haga clic en **[!UICONTROL Crear]**.

1. En la sección **[!UICONTROL Convertir imagen en plantilla]**, realice los siguientes pasos:

   * (Opcional) Si su organización tiene temas de marca definidos en Journey Optimizer, puede seleccionar un tema como entrada para que el HTML generado tenga un estilo acorde con los parámetros del tema de la marca. [Más información sobre los temas](../email/apply-email-themes.md)

     El estilo, como el color de fondo, el color del botón, las fuentes, el interlineado, los márgenes y el relleno, se aplicará a la plantilla generada, lo que reducirá el trabajo de diseño adicional y producirá una plantilla lista para usar con ediciones mínimas.

   * Para poder cargar una imagen, asegúrese de que no contenga información de identificación personal (PII) u otros datos confidenciales. Marque la opción correspondiente para confirmar que ha revisado el archivo.

   * Haga clic en el botón **[!UICONTROL Cargar imagen]** para seleccionar el archivo de imagen.

     ![Editor de plantillas de contenido de correo electrónico de Journey Optimizer con la sección Convertir imagen en plantilla](../email/assets/email_designer_convert_img.png){width=80%}

     >[!CAUTION]
     >
     >Al cargar una imagen para su conversión, todo el contenido añadido actualmente en el correo electrónico se eliminará y se reemplazará por la plantilla generada.

1. Si es la primera vez que usa IA generativa en [!DNL Journey Optimizer], se le pedirá que acepte el contrato de usuario. Para obtener más información, consulte las [Directrices de usuario de IA generativa de Adobe](https://www.adobe.com/es/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

   ![Cuadro de diálogo de acuerdo de usuario de inteligencia artificial generativa en Journey Optimizer](../email/assets/email_designer_convert_agreement.png){width=50%}

   Haga clic en **[!UICONTROL Aceptar]** para continuar.

1. Después de seleccionar la imagen, haga clic en **[!UICONTROL Abrir]** para iniciar el proceso de conversión con tecnología de IA, que a menudo se completa en **unos 5 minutos**, según la complejidad y el tamaño del diseño de la imagen.

   >[!NOTE]
   >
   >Las imágenes muy grandes pueden tardar hasta 10 minutos en algunos casos. Puede salir de esta pantalla y trabajar en otras tareas mientras la conversión está en curso.

1. **Actualice la página** para ver el resultado. Una vez finalizada la conversión, el contenido generado se muestra y se guarda automáticamente como borrador.

   >[!IMPORTANT]
   >
   >El resultado no se muestra automáticamente hasta que se actualiza.

   ![Plantilla de contenido de correo electrónico que muestra el borrador generado a partir de la conversión de imágenes](../email/assets/email_designer_converted_img.png){width=90%}

1. Use la sección **[!UICONTROL Comentarios sobre el conversor de imágenes a plantillas]** para compartir sus ideas y sugerencias con Adobe y ayudarnos a mejorar la función.
   ![Sección de comentarios en Journey Optimizer con un área de texto para compartir tus ideas y sugerencias](../email/assets/email_designer_converter_feedback.png){width=70%}

1. Haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]**. La plantilla convertida se abre en [Email Designer](../email/get-started-email-design.md) con funciones de edición completas. Ahora puede:

   * Revisar, editar contenido de texto y aplicar personalización
   * Modificación de imágenes y adición de vínculos
   * Ajuste de colores, fuentes y estilo
   * Agregar, quitar o reorganizar componentes de contenido
   * Aproveche todas las funciones de Email Designer como con cualquier otra plantilla

   ![Designer de correo electrónico en Journey Optimizer que muestra la plantilla convertida como componentes de contenido modulares para editar](../email/assets/email_designer_html_components.png)

   Realice los ajustes necesarios para perfeccionar la plantilla y adaptarla a las directrices de marca.

1. Cuando esté satisfecho con la plantilla, haga clic en **[!UICONTROL Guardar]**.

La plantilla ya está disponible en la biblioteca de plantillas de contenido y se puede utilizar al crear correos electrónicos en recorridos o campañas. [Aprenda a utilizar las plantillas de contenido](../email/use-email-templates.md)

## Prácticas recomendadas {#best-practices}

Para lograr resultados óptimos al convertir imágenes en plantillas de contenido de correo electrónico, siga estas recomendaciones.

+++Antes de comenzar

* **Guardar contenido existente**: al convertir una imagen, se reemplaza todo el contenido existente en la plantilla de correo electrónico. Guarde siempre el trabajo actual antes de utilizar esta función.
* **Planifique el flujo de trabajo**: use esta característica al principio del proceso de creación de correo electrónico o asegúrese de que está listo para reemplazar todo el contenido actual.

+++

+++Preparación de imágenes

* **Resolución**: utilice imágenes de alta resolución para un mejor reconocimiento de texto y detección de elementos.
* **Claridad**: usa una imagen clara; el texto debe ser fácil de leer y los elementos visuales deben estar bien definidos; evita archivos de origen borrosos, con poco contraste o ruidosos.
* **Anchura**: Diseñe imágenes con anchuras de correo electrónico estándar (600-800 px) para que coincidan con los requisitos habituales de los clientes de correo electrónico.
* **Formato de archivo**: use el formato JPEG o PNG para evitar imágenes comprimidas o de baja calidad.
* **Diseño completo**: incluya el diseño de correo electrónico completo en una sola imagen, desde el encabezado hasta el pie de página.

+++

+++Consideraciones de diseño

* **Diseños simples**: los diseños más simples y bien estructurados se convierten con mayor precisión que los diseños muy complejos.
* **Elementos estándar**: utilice patrones de diseño de correo electrónico comunes (encabezado, secciones de cuerpo, CTA, pie de página).
* **Legibilidad del texto**: Asegúrese de que haya suficiente contraste entre el texto y los fondos.
* **Fuentes seguras para la Web**: Los diseños que usan fuentes seguras para la Web comunes tendrán una mejor fidelidad.
* **Evite elementos superpuestos**: Mantenga los elementos de diseño claramente separados para un mejor reconocimiento de la estructura.

+++

+++Después de la conversión

* **Actualice para ver los resultados**: Después de unos 5 minutos (o hasta 10 minutos para imágenes muy grandes), actualice la página para que aparezca la conversión completada.
* **Revise el borrador**: una vez completada la conversión, la plantilla se guardará automáticamente como borrador. Tómese tiempo para revisar cuidadosamente el contenido generado y comprobar su precisión.
* **Realizar pruebas exhaustivas**: probar el correo electrónico en distintos clientes y dispositivos de correo electrónico. [Obtenga información sobre cómo obtener una vista previa y probar contenido](preview-test.md).
* **Refinar manualmente**: realice los ajustes necesarios utilizando las funciones de edición completas de [Email Designer](../email/get-started-email-design.md).
* **Alineación de marca**: compruebe que los colores, las fuentes y el estilo coinciden con las directrices de marca mediante temas, si están disponibles. [Más información sobre los temas de correo electrónico](../email/apply-email-themes.md).
* **Personalization**: agregue contenido dinámico y tokens de personalización según sea necesario. [Más información sobre personalización](../personalization/personalize.md).
* **Accesibilidad**: revise y mejore las características de accesibilidad si es necesario. [Más información sobre el contenido de correo electrónico accesible](../email/accessible-content.md).

+++

+++Los comentarios son bienvenidos.

Utilice la sección dedicada para compartir sus ideas y sugerencias con Adobe para ayudarnos a mejorar la función.

+++






## Preguntas frecuentes {#faq}

+++¿Qué sucede con el contenido del correo electrónico existente cuando convierto una imagen en una plantilla de contenido?

Todo el contenido existente en su correo electrónico se eliminará y se reemplazará por la plantilla recién generada al cargar una imagen para su conversión. Asegúrese de guardar cualquier contenido importante antes de utilizar esta función. Es mejor utilizar esta capacidad al principio del proceso de creación de correo electrónico.

+++

+++¿Qué formatos de archivo se admiten?

El conversor admite los formatos de imagen JPEG (.jpg, .jpeg) y PNG (.png).

+++

+++¿Cuánto tiempo tarda el proceso de conversión?

La conversión suele finalizar en unos 5 minutos, según la complejidad y el tamaño del diseño de la imagen. Las imágenes muy grandes pueden tardar a veces hasta 10 minutos; deje tiempo adicional y, a continuación, actualice. El procesamiento de IA se produce en segundo plano, por lo que puede desplazarse y trabajar en otras tareas; no es necesario mantener la pantalla abierta. Una vez completada la conversión, el archivo se guarda automáticamente como borrador para que lo revise y edite.

+++

+++¿Puedo editar la plantilla generada?

¡Sí! La plantilla de contenido generada se abre en el Designer de correo electrónico con funciones de edición completas. Puede modificar todos los aspectos de la plantilla, incluidos el texto, las imágenes, el estilo, el diseño y la estructura.

+++

+++¿Qué sucede si la conversión no coincide exactamente con mi diseño?

La IA hace todo lo posible para interpretar con precisión su diseño, pero puede ser necesario un poco de refinamiento manual. Utilice la Designer de correo electrónico para ajustar cualquier elemento que necesite ajustes.

+++

+++¿Puedo utilizar esta función para páginas de aterrizaje u otros tipos de contenido?

El convertidor de imagen a HTML está diseñado actualmente específicamente para plantillas de contenido de correo electrónico. Para otros tipos de contenido, utilice las opciones de diseño e importación estándar disponibles en el Designer de correo electrónico.

+++

+++¿Necesito permisos especiales para utilizar esta función?

Esta capacidad está disponible para todos los clientes que han firmado el anexo [!DNL Gen AI] con Adobe. Si no está seguro de si su organización ha firmado el anexo, póngase en contacto con su representante de Adobe.

+++

+++¿Puedo reutilizar plantillas convertidas en varias campañas?

¡Sí! Las plantillas creadas con el convertidor de imagen a HTML se guardan automáticamente en la biblioteca de plantillas de contenido. Puede acceder a ellas y reutilizarlas en cualquier mensaje de correo electrónico de sus recorridos y campañas. [Más información](content-templates.md)

+++

+++¿Puedo utilizarlo para la migración de plataformas?

¡Sí! El conversor de imagen a HTML es ideal para migrar desde otras plataformas de marketing por correo electrónico. Solo tiene que exportar o capturar la pantalla de sus diseños de correo electrónico existentes de la plataforma anterior y convertirlos en plantillas de HTML preparadas para AJO sin necesidad de reconstruirlos desde cero.

+++

## Temas relacionados {#related-topics}

* [Introducción a las plantillas de contenido](content-templates.md)
* [Creación de plantillas de contenido](create-content-templates.md)
* [Uso de plantillas de correo electrónico](../email/use-email-templates.md)
* [Aprovechar los temas de correo electrónico](../email/apply-email-themes.md)
* [Introducción al diseño de correo electrónico](../email/get-started-email-design.md)
