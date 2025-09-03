---
solution: Journey Optimizer
product: journey optimizer
title: Introducción al Asistente de IA en Journey Optimizer
description: Obtenga información sobre cómo acceder y trabajar con el Asistente de IA en Journey Optimizer
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: f755275d183e8ebc7bfb7ad3d3bac38da762ee9f
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 93%

---

# Introducción al Asistente de IA {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Asistente de IA en Journey Optimizer"
>abstract="Cuando haya creado y personalizado su envío, puede utilizar el Asistente de IA de Journey Optimizer para mejorar el contenido. Esta función simplifica el proceso de personalización y mejora del contenido al permitirle refinarlo, describiendo lo que desea generar."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Cargar recurso de marca"
>abstract="El menú Cargar recurso de marca le permite añadir cualquier recurso de marca que incluya contenido que pueda proporcionar un contexto adicional para el Asistente de IA en Journey Optimizer, o seleccionar un recurso cargado anteriormente. Esta opción garantiza que el Asistente de IA tenga acceso a todos los materiales necesarios para mejorar su funcionalidad y relevancia."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Términos de IA generativa de Adobe"
>abstract="El acceso a esta función está sujeto a su aceptación de las Directrices del usuario de IA generativa de Adobe Experience Cloud. Revise la exactitud de los resultados de esta función y asegúrese de que son adecuados para su caso de uso."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Directrices del usuario de IA generativa de Adobe"

>[!INFO]
>
>Sumérjase en una experiencia práctica con [nuestra vista previa de funciones en directo](https://experienceleague.adobe.com/es/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"}, diseñada para permitirle explorar sus funciones en primera persona y comprender plenamente sus posibilidades.


El Asistente de IA en Adobe Journey Optimizer, impulsado por Microsoft Azure OpenAI y Adobe Firefly, aporta sugerencias proactivas de variación de contenido para texto e imágenes. Esta nueva funcionalidad proporciona **texto basado en mensajes y generación de imágenes**. La generación de imágenes se administra con Adobe Firefly.

El Asistente de IA admite la generación **en varios idiomas**, lo que le permite llegar a diversas audiencias globales y participar en ellas. El asistente de IA está disponible en los siguientes idiomas:

<table style="table-layout:auto; margin-top: 0px; margin-bottom: 0px;">
  <tbody>
    <tr style="border: 0;background-color: #FFFFFF;">
      <td>
        <ul>
          <li>Francés</li>
          <li>Español</li>
          <li>Alemán</li>
          <li>Italiano</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Japonés</li>
          <li>Sueco</li>
          <li>Neerlandés</li>
          <li>Noruego</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

Ahora puede utilizar el Asistente de IA en Adobe Journey Optimizer para optimizar el impacto del mensaje experimentando con diferentes títulos e imágenes principales. Genere varias variantes y cree un experimento para compararlas. Aprovechando **Experimento con contenido de Journey Optimizer**, puede definir varios tratamientos para los mensajes a fin de medir cuál ofrece el mejor rendimiento para la audiencia objetivo. Puede elegir entre variar el contenido del envío o el asunto. El público del mensaje se asigna aleatoriamente a cada tratamiento para determinar cuál funciona mejor en términos de la métrica especificada. Obtenga más información sobre el Experimento de contenido en [esta sección](../content-management/content-experiment.md).

>[!IMPORTANT]
>
>* Antes de empezar a usar esta capacidad, lea las [Mecanismos de protecciones y limitaciones](#generative-guardrails) relacionadas.
>
>
>* Debe aceptar un [acuerdo de usuario](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} para poder utilizar el Asistente de IA de Adobe Journey Optimizer. Para obtener más información, contacte con su representante de Adobe.

## Acceso al Asistente de IA {#generative-access}

Para acceder a la función del Asistente de IA de Adobe Journey Optimizer, los usuarios deben tener concedido el permiso **Generar contenido**. [Más información](../administration/permissions.md)

+++  Más información sobre la asignación de permisos relacionados con la generación de contenido

1. En el producto **Permisos**, vaya a la pestaña **Funciones** y seleccione la **Función** que desee.

1. Haga clic en **Editar** para modificar los permisos.

1. Añada el recurso **Asistente de IA** y, a continuación, seleccione **Generar contenido** en el menú desplegable.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. Haga clic en **Guardar** para aplicar los cambios.

   Los permisos de los usuarios que ya estén asignados a esta función se actualizarán automáticamente.

1. Para asignar esta función a nuevos usuarios, vaya a la pestaña **Usuarios** en el panel de control **Funciones** y haga clic en **Añadir usuario**.

1. Introduzca el nombre del usuario y su dirección de correo electrónico, o selecciónelo en la lista, y haga clic en **Guardar**.

1. Si el usuario no estaba ya creado, consulte [esta documentación](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/users).

El usuario recibirá un correo electrónico con instrucciones para acceder a su instancia.

+++

## Mecanismos de protección y limitaciones {#generative-guardrails}

A continuación, se indican las directrices generales para utilizar el Asistente de IA de Adobe Journey Optimizer para la generación de correos electrónicos:

* La calidad del contenido generado depende en gran medida del objetivo de marketing o indicación que defina. Utilice indicaciones bien definidas para que el modelo GenAI las interprete con precisión. 
* Cargue el recurso de marca para disponer de contenido preciso y acorde con el contenido de la marca. Si no, el contenido se basa en información pública. El contenido cargado puede estar en los siguientes formatos: archivos PDF, JPEG, PNG o ZIP (con formatos de archivo compatibles).
* El tamaño máximo del recurso de marca cargado es de 50 MB.Los archivos más grandes o muchas imágenes pueden funcionar, pero aumenta el tiempo de procesamiento.
* Utilice plantillas específicas de la marca o personalizadas para crear el contenido de sus correos electrónicos utilizando el Asistente de IA en Adobe Journey Optimizer. Se recomiendan plantillas de correo electrónico con un máximo de 8 a 10 imágenes.
* Asegúrese de notificar cualquier salida problemática utilizando los iconos de pulgar hacia arriba, pulgar hacia abajo o bandera al seleccionar variantes.
* El uso que haga del asistente de IA está sujeto a las directrices del usuario de IA generativa de Adobe Experience Cloud. [Más información](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Como parte del compromiso de Adobe de fomentar la transparencia en el uso de herramientas de IA generativa en la creación de medios, Adobe aplicará Content Credentials cuando se descargue o exporte contenido o un proyecto que incluya un recurso generado por Firefly. [Más información](https://helpx.adobe.com/es/firefly/using/content-credentials.html)

Las siguientes limitaciones se aplican al asistente de IA en Adobe Journey Optimizer:

* Solo está disponible para los canales de correo electrónico, push, web y SMS.
* El contenido de GenAI podría no ser siempre preciso: comparta sus comentarios para que nuestros ingenieros puedan perfeccionar los modelos.
* Puede cargar varios recursos de marca, pero solo puede utilizar uno para una generación específica.


## Capacidades de generación de contenido del Asistente de IA {#generative-features}


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="Generación de correo electrónico" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong>Generación de correo electrónico</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="Generación de SMS" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong>Generación de SMS</strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="Generación de push" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>Generación de notificaciones push</strong></a>
</div>
<p></td>
<td>
<a href="generative-web.md">
<img alt="Generación de web" src="assets/do-not-localize/web-genai.jpeg">
</a>
<div><a href="generative-web.md"><strong>Generación de páginas web</strong>
</div>
<p>
</td>
</tr></table>
