---
solution: Journey Optimizer
product: journey optimizer
title: Conversión de imágenes en plantillas de HTML
description: Aprenda a utilizar el conversor de imágenes a HTML con tecnología de IA para convertir diseños de imagen en plantillas de correo electrónico editables de HTML
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
badge: label="Disponibilidad limitada" type="Informative"
keywords: correo electrónico, plantilla, imagen, HTML, IA, diseño, convertidor
exl-id: d13467b7-2f3c-4707-a7e0-9b46cb6cafb1
source-git-commit: e5b02fe84f00dec189d4002280e9a69b782cd91f
workflow-type: tm+mt
source-wordcount: '1659'
ht-degree: 4%

---

# Conversión de imágenes en plantillas de HTML {#image-to-html}

>[!AVAILABILITY]
>
>Esta funcionalidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

[!DNL Journey Optimizer] le ayuda a acelerar en gran medida la creación de correos electrónicos al convertir diseños de imagen estáticos en plantillas de contenido de correo electrónico modulares y totalmente personalizables de HTML.

Al aprovechar la tecnología de IA generativa, una herramienta integrada analiza el diseño, la tipografía, los colores y los elementos visuales de la imagen y genera código HTML limpio y modular que mantiene la fidelidad del diseño a la vez que garantiza la editabilidad completa con [Email Designer](../email/get-started-email-design.md).

Esta capacidad sin código permite a los especialistas en marketing transformar recursos visuales de diseñadores gráficos o herramientas de diseño en plantillas de correo electrónico interactivas y editables que se pueden guardar y reutilizar en varios recorridos y campañas, sin necesidad de conocimientos técnicos.

Los principales beneficios son los siguientes:

* **Más rápido que la codificación manual**: el convertidor convierte las imágenes en HTML editable en minutos, para que pueda omitir el lento flujo de trabajo manual de HTML.
* **No se necesitan habilidades técnicas**: los especialistas en mercadotecnia pueden producir y ajustar plantillas sin soporte de diseño o desarrollo.
* **Reutilizables en todas las campañas**: guarde las plantillas en la biblioteca y utilícelas en cualquier recorrido o campaña.
* **Se mantiene fiel al diseño**: la salida coincide con el diseño y el estilo, a la vez que es totalmente compatible con el Designer de correo electrónico.

<!--* **Design fidelity**: Maintain visual consistency with your original design while creating fully editable content
* **Email compatibility**: Generate HTML that works seamlessly with the Email Designer and across email clients-->

+++ Casos de uso comunes

El convertidor de imagen a HTML es ideal para:

* **Migración de la plataforma**: ¿Está migrando desde otra plataforma de marketing por correo electrónico? Convierta sus diseños de correo electrónico existentes en plantillas de HTML preparadas para [!DNL Journey Optimizer] sin tener que volver a compilar desde cero.
* **Conversión de maqueta de diseño**: transforme maquetas de diseño de herramientas como Photoshop, Figma u otro software de diseño en plantillas de correo electrónico funcionales.
* **Creación rápida de plantillas**: genere plantillas de correo electrónico rápidamente para campañas en las que el tiempo sea importante sin esperar los recursos para desarrolladores.
* **Creación de bibliotecas de plantillas**: cree una biblioteca completa de plantillas compatibles con la marca que los integrantes del equipo que no sean técnicos puedan personalizar e implementar.
* **Reducción de las dependencias técnicas**: permita que los especialistas en marketing creen plantillas de correo electrónico e iteren de forma independiente, lo que acelera la ejecución de la campaña.

+++

## Mecanismos de protección y recomendaciones {#limitations}

Tenga en cuenta las siguientes limitaciones al convertir imágenes a plantillas de contenido de HTML.

* **Interpretación de IA**: La IA genera HTML basándose en la interpretación visual de su imagen. Los diseños complejos o inusuales pueden requerir ajustes manuales después de la conversión.

* **Precisión del texto**: Mientras la IA intenta reconocer y reproducir el texto con precisión, compruebe siempre el contenido del texto y realice las correcciones necesarias.

* **Contenido dinámico**: el proceso de conversión crea HTML estático basado en la imagen. Después de la conversión, debe agregar manualmente la personalización, el contenido dinámico y el seguimiento.

* **Diseños complejos**: Es posible que los diseños muy complejos con capas complejas, formas inusuales o elementos no estándar no se conviertan a la perfección. Los diseños más simples generalmente arrojan mejores resultados.

* **Tiempo de procesamiento**: El proceso de conversión puede tardar hasta 5 minutos según la complejidad y el tamaño de la imagen. El procesamiento de IA se produce en segundo plano, lo que le permite trabajar en otras tareas sin mantener la pantalla abierta. La plantilla se guarda automáticamente como borrador una vez completada la conversión.

* **Disponibilidad limitada**: como característica de disponibilidad limitada, el conversor de imagen a HTML se mejora continuamente. La funcionalidad y la precisión pueden variar, y los comentarios ayudan a mejorar la función.

>[!NOTE]
>
>El conversor de imagen a HTML está diseñado para proporcionar un punto de partida sólido para la creación de correos electrónicos. La HTML generada debe revisarse y refinarse usando la Designer de correo electrónico para asegurarse de que cumple con sus requisitos exactos.

## Conversión de una imagen en una plantilla de HTML {#convert-image}

Para convertir un diseño de imagen en una plantilla de correo electrónico de HTML totalmente personalizable, siga los pasos a continuación.

1. Asegúrese de tener un archivo de imagen en formato JPEG o PNG que contenga su diseño de correo electrónico.

   >[!NOTE]
   >
   >Para obtener los mejores resultados, utilice imágenes de alta calidad con elementos visuales claros y texto legible. Lo ideal es que las imágenes tengan entre 600 y 800 píxeles de ancho para coincidir con las dimensiones de correo electrónico estándar.

1. Para acceder a la lista de plantillas de contenido, seleccione **[!UICONTROL Administración de contenido]** > **[!UICONTROL Plantillas de contenido]** en el menú de la izquierda.

1. Haga clic en **[!UICONTROL Crear plantilla]**.

1. Complete los detalles de la plantilla, seleccione **[!UICONTROL Correo electrónico]** como canal y haga clic en **[!UICONTROL Crear]**.

1. En la sección **[!UICONTROL Convertir imagen en plantilla]**, realice los siguientes pasos:

   * (Opcional) Si su organización tiene temas de marca definidos en Journey Optimizer, puede seleccionar un tema como entrada para que el HTML generado tenga un estilo acorde con los parámetros del tema de la marca. [Más información sobre los temas](../email/apply-email-themes.md)

     El estilo, como el color de fondo, el color del botón, las fuentes, el interlineado, los márgenes y el relleno, se aplicará a la plantilla generada, lo que reducirá el trabajo de diseño adicional y producirá una plantilla lista para usar con ediciones mínimas.

   * Para poder cargar una imagen, asegúrese de que no contenga información de identificación personal (PII) u otros datos confidenciales y marque la opción correspondiente para confirmar que ha revisado el archivo.

   * Haga clic en el botón **[!UICONTROL Cargar imagen]** para seleccionar el archivo de imagen.

     ![](../email/assets/email_designer_convert_img.png)

     >[!CAUTION]
     >
     >Al cargar una imagen para su conversión, todo el contenido añadido actualmente en el correo electrónico se eliminará y se reemplazará por la plantilla generada.


1. Después de seleccionar la imagen, haz clic en **[!UICONTROL Abrir]** para iniciar el proceso de conversión con tecnología de IA.

   >[!NOTE]
   >
   >El proceso de generación puede tardar hasta 5 minutos en función de la complejidad y el tamaño del diseño de la imagen. Puede salir de esta pantalla y trabajar en otras tareas mientras la conversión está en curso.

1. Una vez completada la conversión, la plantilla de contenido se guarda automáticamente como borrador.

   ![](../email/assets/email_designer_converted_img.png)

1. Haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]**. La plantilla convertida se abre en [Email Designer](../email/get-started-email-design.md) con funciones de edición completas. Ahora puede:

   * Revisar, editar contenido de texto y aplicar personalización
   * Modificación de imágenes y adición de vínculos
   * Ajuste de colores, fuentes y estilo
   * Agregar, quitar o reorganizar componentes de contenido
   * Aproveche todas las funciones de Email Designer como con cualquier otra plantilla

   ![](../email/assets/email_designer_html_components.png)

1. Realice los ajustes necesarios para perfeccionar la plantilla y adaptarla a las directrices de marca.

1. Cuando esté satisfecho con la plantilla, haga clic en **[!UICONTROL Guardar]**.

La plantilla ya está disponible en la biblioteca de plantillas de contenido y se puede utilizar al crear correos electrónicos en recorridos o campañas. [Aprenda a utilizar las plantillas de contenido](../email/use-email-templates.md)

## Prácticas recomendadas {#best-practices}

Para obtener resultados óptimos al convertir imágenes a plantillas de contenido de HTML, siga estas recomendaciones.

+++Antes de comenzar

* **Guardar contenido existente**: al convertir una imagen a HTML, se reemplazará todo el contenido existente en el correo electrónico. Guarde siempre el trabajo actual antes de utilizar esta función.
* **Planifique el flujo de trabajo**: use el convertidor de imagen a HTML al principio del proceso de creación del correo electrónico o asegúrese de que está listo para reemplazar todo el contenido actual.

+++

+++Preparación de imágenes

* **Resolución**: Use imágenes de alta resolución (al menos 1200 px de ancho) para un mejor reconocimiento de texto y detección de elementos
* **Claridad**: Asegúrese de que el texto sea claramente legible y de que los elementos visuales estén bien definidos
* **Anchura**: diseñe imágenes con anchuras de correo electrónico estándar (600-800 px) para que coincidan con los requisitos habituales de los clientes de correo electrónico
* **Formato de archivo**: use el formato JPEG o PNG para evitar imágenes comprimidas o de baja calidad
* **Diseño completo**: incluya el diseño de correo electrónico completo en una sola imagen, de encabezado a pie de página

+++

+++Consideraciones de diseño

* **Diseños simples**: los diseños más simples y bien estructurados se convierten con mayor precisión que los diseños muy complejos
* **Elementos estándar**: utilice patrones de diseño de correo electrónico comunes (encabezado, secciones de cuerpo, CTA, pie de página).
* **Legibilidad del texto**: Asegúrese de que haya suficiente contraste entre el texto y los fondos
* **Fuentes seguras para la Web**: Los diseños que usan fuentes seguras para la Web comunes tendrán una mejor fidelidad
* **Evite elementos superpuestos**: Mantenga los elementos de diseño claramente separados para un mejor reconocimiento de la estructura

+++

+++Después de la conversión

* **Revise el borrador**: una vez completada la conversión, la plantilla se guardará automáticamente como borrador. Tómese tiempo para revisar cuidadosamente la HTML generada para comprobar su precisión
* **Realizar pruebas exhaustivas**: probar el correo electrónico en distintos clientes y dispositivos de correo electrónico
* **Refinar manualmente**: realice los ajustes necesarios mediante las funciones de edición completas de Designer de correo electrónico
* **Alineación de marca**: compruebe que los colores, las fuentes y el estilo coinciden con las directrices de marca
* **Personalization**: agregue contenido dinámico y tokens de personalización según sea necesario
* **Accesibilidad**: revise y mejore las características de accesibilidad si es necesario

+++

## Preguntas frecuentes {#faq}

+++¿Qué sucede con el contenido del correo electrónico existente cuando utilizo el convertidor de imagen a HTML?

Todo el contenido existente en su correo electrónico se eliminará y se reemplazará por la plantilla recién generada al cargar una imagen para su conversión. Asegúrese de guardar cualquier contenido importante antes de utilizar esta función. Es mejor utilizar el conversor de imagen a HTML al principio del proceso de creación del correo electrónico.

+++

+++¿Qué formatos de archivo se admiten?

El convertidor de imagen a HTML es compatible con los formatos de imagen JPEG (.jpg, .jpeg) y PNG (.png).

+++

+++¿Cuánto tiempo tarda el proceso de conversión?

La conversión puede tardar hasta 5 minutos, según la complejidad y el tamaño del diseño de la imagen. El procesamiento de IA se realiza en segundo plano, por lo que puede desplazarse y trabajar en otras tareas; no es necesario que mantenga la pantalla abierta. Una vez completada la conversión, el archivo se guardará automáticamente como borrador para que lo revise y edite.

+++

+++¿Puedo editar la plantilla generada?

¡Sí! La plantilla de HTML generada se abre en el Designer de correo electrónico con funciones de edición completas. Puede modificar todos los aspectos de la plantilla, incluidos el texto, las imágenes, el estilo, el diseño y la estructura.

+++

+++¿Qué sucede si la conversión no coincide exactamente con mi diseño?

La IA hace todo lo posible para interpretar con precisión su diseño, pero puede ser necesario un poco de refinamiento manual. Utilice la Designer de correo electrónico para ajustar cualquier elemento que necesite ajustes.

+++

+++¿Puedo utilizar esta función para páginas de aterrizaje u otros tipos de contenido?

El convertidor de imagen a HTML está diseñado actualmente específicamente para plantillas de correo electrónico. Para otros tipos de contenido, utilice las opciones de diseño e importación estándar disponibles en el Designer de correo electrónico.

+++

+++¿Necesito permisos especiales para utilizar esta función?

El convertidor de imagen a HTML está disponible en disponibilidad limitada. Necesita acceso de disponibilidad limitado (póngase en contacto con su representante de Adobe para obtener acceso) y permisos estándar de Designer de correo electrónico para utilizar esta función.

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
* [Importar el contenido del correo electrónico](../email/existing-content.md)
* [Diseño de contenido desde cero](../email/content-from-scratch.md)
