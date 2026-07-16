---
solution: Journey Optimizer
product: journey optimizer
title: Comprobación de contenido en el Designer de correo electrónico
description: Aprenda a utilizar las comprobaciones de contenido en el Designer de correo electrónico para detectar problemas de HTML y CSS antes de enviar correos electrónicos en Journey Optimizer.
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: correo electrónico, comprobación de contenido, HTML, CSS, validación, procesamiento, calidad
source-git-commit: 74bd6eeb380f433f08002024aba873906213aad4
workflow-type: tm+mt
source-wordcount: '1310'
ht-degree: 6%

---


# Comprobación de contenido en el diseñador de correo electrónico {#content-check}

>[!CONTEXTUALHELP]
>id="ajo_email_content_check"
>title="Validar el contenido del correo electrónico"
>abstract="Las comprobaciones de contenido detectan automáticamente los problemas de HTML y CSS en el correo electrónico antes de enviarlo. Indican etiquetas no admitidas, divs vacíos y límites de tamaño que pueden interrumpir el procesamiento en Gmail o Microsoft Outlook. Los problemas aparecen como errores, advertencias o avisos informativos, con detalles contextuales y correcciones con un solo clic cuando están disponibles."

[!DNL Journey Optimizer] incluye validación técnica automatizada directamente en el Designer de correo electrónico, lo que le ayuda a detectar problemas de HTML y CSS antes de enviarlos.

Los resultados aparecen como errores, advertencias o avisos informativos en el panel de creación, con detalles contextuales y correcciones con un solo clic cuando están disponibles, de modo que los problemas se pueden resolver sin salir del Designer de correo electrónico.

## Comprobación de contenido de acceso {#access-content-checks}

Las comprobaciones de contenido siempre están disponibles en el Designer de correo electrónico. Para verlos, haga clic en el icono Problemas en el carril derecho para abrir el panel **[!UICONTROL Comprobación de contenido]**, donde se enumeran todos los problemas detectados.

![Panel de verificación de contenido en el Designer de correo electrónico con problemas](assets/content-check.png)

>[!NOTE]
>
>Las comprobaciones se ejecutan automáticamente en el estado actual del correo electrónico y después de cada edición. [Más información](#recalculation)

Las comprobaciones aparecen con tres niveles de gravedad:

| Gravedad | Color | Descripción |
|---|---|---|
| **Error** | Rojo | Un problema crítico que provocará errores de entrega o procesamiento. Resolver antes de enviar. |
| **Advertencia** | Naranja | Un problema potencial que puede afectar al procesamiento en clientes de correo electrónico específicos. Recomendado para revisar y resolver. |
| **Información** | Azul | Aviso informativo sobre una condición que no bloquea el envío, pero que puede afectar a la capacidad de mantenimiento a largo plazo del contenido. |

Cuando no se detectan problemas, el panel muestra **No se detectaron problemas** y el icono correspondiente es de color verde.

![Panel de verificación de contenido en el Designer de correo electrónico sin problemas](assets/content-check-no-issues.png)

Según el problema, puede ver más contexto, aplicar una corrección de un solo clic o guardar el correo electrónico para actualizar un resultado de la comprobación.

* Para algunos problemas detectados, puede hacer clic en el botón **[!UICONTROL Mostrar detalles]** para ver más contexto. Haga clic en **[!UICONTROL Ocultar detalles]** para contraer.
  ![Panel de verificación de contenido en el Designer de correo electrónico con detalles](assets/content-check-details.png){width="80%"}
* Del mismo modo, puede hacer clic en el botón **[!UICONTROL Mostrar corrección]** y aplicar una corrección de un clic cuando esté disponible. Si la corrección no se puede aplicar automáticamente, se muestra un mensaje y debe resolver el problema manualmente.
  ![Panel de verificación de contenido en el Designer de correo electrónico con el botón Aplicar corrección](assets/content-check-fix.png){width="80%"}

### Recalculación de los cheques {#recalculation}

La mayoría de las comprobaciones, como los elementos HTML no compatibles, los divs vacíos y el tamaño de HTML, se vuelven a calcular cada vez que edita el correo electrónico, de modo que siempre reflejan el contenido actual.

Otras comprobaciones, como el tamaño de CSS, se calculan a partir del contenido serializado (la versión del correo electrónico tal y como se carga o guarda), no del estado de edición en directo en el Designer de correo electrónico. En este caso, el contenido guardado puede diferir ligeramente de lo que se ve al editar. Si realiza modificaciones sin guardar, aparecerá una etiqueta **[!UICONTROL Comprobación obsoleta]** para indicar que el resultado puede no ser más preciso. Guarde el correo electrónico para actualizar el cálculo.

![Panel de verificación de contenido en el Designer de correo electrónico con etiqueta de verificación obsoleta](assets/content-check-stale.png){width="100%"}

## Corrección de problemas detectados {#fix-issues}

En las tablas siguientes se enumeran todos los mensajes posibles y la acción recomendada para cada uno. Expanda la categoría que coincida con el mensaje que ve en el panel **[!UICONTROL Comprobación de contenido]**.

+++ Elementos de HTML no compatibles

| Mensaje | Gravedad | Qué hacer |
|---|---|---|
| El contenido contiene una etiqueta `<script>`, la cual no es compatible con ningún sistema de correo electrónico. Elimínelo para evitar problemas de envío y procesamiento. | Error | Busque y elimine todas las etiquetas `<script>` de su contenido de HTML. |
| El contenido contiene una etiqueta `<base>`, lo que puede causar problemas de resolución de vínculos y recursos en el Designer de correo electrónico. Para solucionarlo, debe eliminarlo. | Error | Quite la etiqueta `<base>` de su HTML. |
| El contenido contiene una metaetiqueta de HTML con actualización, que no se admite en el Designer de correo electrónico. Elimínelo para evitar comportamientos inesperados. | Advertencia | Elimine la etiqueta de actualización meta de su HTML. |
| El contenido contiene divs vacíos, lo que puede causar problemas de diseño en Microsoft Outlook (MSO). Para solucionarlo, elimine los divs vacíos y utilice el espaciado de los elementos del mismo nivel. | Advertencia | Elimine los elementos `<div>` vacíos y ajuste el relleno o el margen de los elementos adyacentes para mantener el espaciado. |

+++

+++ Problemas de CSS

| Mensaje | Gravedad | Qué hacer |
|---|---|---|
| El tamaño total de CSS supera el límite de 16 KB de Gmail y causará problemas de procesamiento en Gmail. | Error | Use **[!UICONTROL Aplicar corrección]** para eliminar automáticamente las reglas CSS que no se usen o simplificar manualmente los estilos. |
| El tamaño total de CSS está cerca del límite de 16 KB de Gmail y podría causar problemas de procesamiento si se añade más CSS. | Advertencia | Use **[!UICONTROL Aplicar corrección]** para eliminar las reglas CSS que no se usen o reducir los estilos antes de agregar más contenido. |
| El tamaño total de CSS para este fragmento supera los 3 KB. Combinar esto con otros fragmentos podría provocar que el CSS total del correo electrónico supere el límite de 16 KB de Gmail y causar problemas de procesamiento. | Advertencia | Simplifique el CSS en este fragmento para mantener el CSS de correo electrónico combinado por debajo de 16 KB. |
| El contenido contiene reglas CSS no utilizadas. Esto podría causar problemas de procesamiento en Gmail. | Advertencia | Use **[!UICONTROL Aplicar corrección]** para eliminar automáticamente las reglas CSS que hagan referencia a elementos que ya no están presentes en el correo electrónico. |

<!--
| Message | Severity | What to do |
|---|---|---|
| Your content has modifications to the system-generated default CSS. These changes may be overridden by future Email Designer updates. To preserve your styles, add them using the Custom CSS feature instead. | Info | Move your custom styles to [Custom CSS](custom-css.md) to ensure they are preserved across Email Designer updates. |
-->

+++

+++ Tamaño de HTML

| Mensaje | Gravedad | Qué hacer |
|---|---|---|
| El tamaño estimado de HTML supera el límite de 100 KB de Gmail y causará problemas de procesamiento en Gmail. El tamaño real de la HTML puede diferir en el momento del envío. | Error | Reduzca el contenido del correo electrónico: elimine los elementos innecesarios, simplifique la estructura o divida el contenido en varios envíos. |
| El tamaño estimado de HTML está cerca del límite de 100 KB de Gmail y podría causar problemas de procesamiento si se añade más HTML. El tamaño real de la HTML puede diferir en el momento del envío. | Advertencia | Simplifique el contenido antes de añadir más. Los correos electrónicos que superen el límite de Gmail se recortarán para los destinatarios. |
| El tamaño estimado de HTML para este fragmento supera los 20 KB. Si se combina esto con otros fragmentos, el total de correos electrónicos de HTML podría superar el límite de 100 KB de Gmail y causar problemas de procesamiento. El tamaño real de la HTML puede diferir en el momento del envío. | Advertencia | Reduzca la HTML en este fragmento para mantener el tamaño del correo electrónico combinado por debajo del límite de 100 KB de Gmail. |

+++

## Acerca del tamaño de HTML y CSS {#size-estimation}

Los valores de tamaño de HTML y CSS que se muestran en el Designer de correo electrónico son **estimaciones calculadas a la hora de crear**. Reflejan la carga útil procesada completa tal como existe en el editor en ese momento e incluyen:

* **Estructura de HTML**: todo el marcado, las etiquetas, los contenedores de diseño y los estilos en línea
* **CSS en línea**: envía por correo electrónico estilos en línea de Designer antes de calcular el tamaño, que es estándar para los clientes de correo electrónico, pero infla la cifra sin procesar en comparación con una hoja de estilos externa
* **Contenido de texto**: todos los tokens de copia y personalización, contados a la longitud de su marcador de posición (no su valor resuelto)
* **Fragmentos**: todos los fragmentos a los que se hace referencia se expanden en línea, por lo que cada fragmento aporta su peso total de HTML/CSS al total
* **Los bloques condicionales (if-else)** - **todas las ramas** se incluyen en la estimación de tamaño en el momento de la creación, porque las condiciones no se evalúan hasta el momento del envío
* **Imágenes**: solo se cuenta la referencia de imagen (URL src), no los datos de imagen binaria en sí

### Por qué la estimación puede diferir del tamaño entregado {#size-estimate-difference}

El tamaño mostrado es una estimación del límite superior en el peor de los casos, no el correo electrónico exacto que recibirá un destinatario. Puede diferir por las siguientes razones:

* **Contenido condicional**: a la hora de envío, solo se representa la rama que coincide con el perfil del destinatario. Una plantilla que muestre 120 KB en el editor puede generar un mensaje de correo electrónico de 60 KB para la mayoría de los destinatarios.
* **tokens de Personalization**: los tokens de marcador de posición se cuentan en su longitud de token sin procesar. Los valores resueltos suelen ser más cortos.
* **Optimización de tamaño de HTML**: si la opción **[!UICONTROL Optimizar tamaño de HTML]** está habilitada, los espacios en blanco, los comentarios y los caracteres redundantes se eliminan en el momento del envío, lo que reduce la carga útil final. [Más información](create-email.md#optimize-html-size)

### Significado de las advertencias de tamaño para los autores {#size-warnings}

Las advertencias de tamaño (por ejemplo, HTML que supera los 100 KB) son **señales proactivas** que le ayudarán a optimizar su correo electrónico antes de enviarlo; no son bloques duros y no reflejan el tamaño exacto que verán los destinatarios. Existen para ayudar a evitar:

* Cortes de correo electrónico recortados por Gmail, que recorta mensajes a aproximadamente 102 KB de HTML
* Representación lenta en dispositivos móviles o en conexiones de bajo ancho de banda
