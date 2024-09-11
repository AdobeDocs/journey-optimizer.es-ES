---
solution: Journey Optimizer
product: journey optimizer
title: 'Introducción al asistente de IA en Journey Optimizer: acelerador de contenido '
description: 'Obtenga información sobre cómo acceder y trabajar con el asistente de IA en Journey Optimizer: acelerador de contenido '
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 616a9c30da4558d1e8b71733732dd4fd1f531ef8
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 42%

---

# Introducción al asistente de IA en Journey Optimizer: acelerador de contenido {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Asistente de IA en Journey Optimizer para la aceleración de contenido"
>abstract="Una vez que haya creado y personalizado su envío, puede utilizar el asistente de IA de Journey Optimizer para la aceleración de contenido a fin de mejorar su contenido. Esta función simplifica el proceso de personalización y mejora del contenido al permitirle refinarlo describiendo lo que desea generar."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Cargar recurso de marca"
>abstract="El menú Cargar recurso de marca le permite añadir cualquier recurso de marca que contenga contenido que pueda proporcionar un contexto adicional para el asistente de IA en Journey Optimizer para la aceleración de contenido o para seleccionar un recurso cargado anteriormente. Esta opción garantiza que el asistente de IA tenga acceso a todos los materiales necesarios para mejorar su funcionalidad y relevancia."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Términos de IA generativa de Adobe"
>abstract="El acceso a esta función está sujeto a su aceptación de las Directrices del usuario de IA generativa de Adobe Experience Cloud. Revise la exactitud de los resultados de esta función y asegurarse de que son adecuados para su caso de uso."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Directrices del usuario de IA generativa de Adobe"

>[!INFO]
>
>Sumérjase en una experiencia práctica con [nuestra demostración interactiva](https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"}, diseñada para que explore sus características de primera mano y comprenda plenamente sus capacidades.


El asistente de IA de Adobe Journey Optimizer para la aceleración de contenido, con tecnología Microsoft Azure OpenAI y Adobe Firefly, ofrece sugerencias proactivas de variación de contenido para texto e imágenes. Está disponible para canales de correo electrónico, push y SMS. Esta nueva funcionalidad proporciona una generación de texto e imágenes basada en solicitudes. La generación de imágenes se administra con Adobe Firefly.

Utilice el asistente de IA de Adobe Journey Optimizer para la aceleración de contenido a fin de optimizar el impacto de su mensaje mediante la experimentación con diferentes títulos e imágenes principales. Genere varias variantes y cree un experimento para compararlas. Con el Experimento de contenido de Journey Optimizer, puede definir varios tratamientos para los mensajes a fin de medir cuál ofrece el mejor rendimiento para su público destinatario. Puede elegir entre variar el contenido del envío o el asunto. El público del mensaje se asigna aleatoriamente a cada tratamiento para determinar cuál funciona mejor en términos de la métrica especificada. Obtenga más información sobre el Experimento de contenido en [esta sección](../content-management/content-experiment.md).

>[!IMPORTANT]
>
>* Antes de empezar a usar esta capacidad, lea [Protecciones y limitaciones](#generative-guardrails) relacionadas.
>
>
>* Debe aceptar un [acuerdo de usuario](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} para poder usar el Asistente de IA en Adobe Journey Optimizer para la aceleración de contenido. Para obtener más información, contacte con su representante de Adobe.

## Acceso al acelerador de contenido del asistente de IA {#generative-access}

Para acceder al asistente de IA en Adobe Journey Optimizer para la función de aceleración de contenido, los usuarios deben obtener el permiso **Generar contenido**. [Más información](../administration/permissions.md)

+++  Aprenda a asignar permisos relacionados con la generación de contenido

1. En el producto **Permisos**, vaya a la ficha **Roles** y seleccione el **Rol** que desee.

1. Haga clic en **Editar** para modificar los permisos.

1. Agregue el recurso **Asistente de IA** y, a continuación, seleccione **Generar contenido** en el menú desplegable.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. Haga clic en **Guardar** para aplicar los cambios.

   Los permisos de los usuarios que ya estén asignados a esta función se actualizarán automáticamente.

1. Para asignar esta función a nuevos usuarios, vaya a la pestaña **Usuarios** en el panel **Funciones** y haga clic en **Agregar usuario**.

1. Escriba el nombre del usuario, su dirección de correo electrónico o selecciónelo en la lista y, a continuación, haga clic en **Guardar**.

1. Si el usuario no se creó anteriormente, consulte [esta documentación](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users).

El usuario recibirá un correo electrónico con instrucciones para acceder a su instancia.

+++

## Mecanismos de protección y limitaciones {#generative-guardrails}

A continuación, se enumeran las directrices generales para utilizar el asistente de IA en Adobe Journey Optimizer para la aceleración de contenido para la generación de correo electrónico:

* La calidad del contenido generado depende en gran medida del objetivo de marketing o indicación que se defina. Utilice indicaciones bien definidas para que el modelo GenAI las interprete con precisión. 
* Cargue el recurso de marca para disponer de contenido preciso y acorde con el contenido de la marca. Si no, el contenido se basa en información pública. El contenido cargado puede estar en los siguientes formatos: archivos PDF, JPEG, PNG o ZIP (con formatos de archivo compatibles).
* El tamaño máximo del recurso de marca cargado es de 50 MB.Los archivos más grandes o muchas imágenes pueden funcionar, pero aumenta el tiempo de procesamiento.
* Utilice una plantilla específica de la marca o personalizada para crear el contenido de su correo electrónico con el asistente de IA en Adobe Journey Optimizer para la aceleración de contenido. Se recomiendan plantillas de correo electrónico con hasta 8-10 imágenes.
* Asegúrese de notificar cualquier salida problemática utilizando los iconos de pulgar hacia arriba, pulgar hacia abajo o bandera al seleccionar variantes.
* El uso que se haga del asistente de IA está sujeto a las Directrices del usuario de IA generativa de Adobe Experience Cloud. [Más información](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Como parte del compromiso de Adobe de fomentar la transparencia en el uso de herramientas de IA generativa en la creación de medios, Adobe aplicará Contentes credentials cuando se descargue o exporte contenido o un proyecto que incluya un recurso generado por el Firefly. [Más información](https://helpx.adobe.com/firefly/using/content-credentials.html)

Las siguientes limitaciones se aplican al asistente de IA en Adobe Journey Optimizer para la aceleración de contenido:

* El idioma admitido es solo inglés. Las entradas que no sean en inglés pueden producir resultados incoherentes o erróneos. En este momento no se abordarán ni mejorarán los problemas que surjan de las respuestas que no sean en inglés.
* Solo disponible para los canales de correo electrónico, push, web y SMS.
* El contenido de GenAI podría no ser siempre preciso: comparta sus comentarios para que nuestros ingenieros puedan perfeccionar los modelos.
* Puede cargar varios recursos de marca, pero solo puede utilizar uno para una generación específica.


## Funcionalidades de generación de contenido del asistente de IA {#generative-features}


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
<img alt="Generación web" src="assets/do-not-localize/web-genai.jpeg">
</a>
<div><a href="generative-web.md"><strong>Generación de página web</strong>
</div>
<p>
</td>
</tr></table>
