---
solution: Journey Optimizer
product: journey optimizer
title: Publicación del recorrido
description: Obtenga información sobre cómo publicar un recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, recorrido, en directo, validez, comprobar
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
version: Journey Orchestration
source-git-commit: 3866cedf2c264d94e981a43b649073aa1bdcd4f2
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 34%

---

# Publicación del recorrido {#publishing-the-journey}

Debe publicar un recorrido para activarlo y hacer que esté disponible para que los nuevos perfiles entren en el recorrido. Antes de publicar el recorrido, compruebe que es válido y que no hay errores. No se puede publicar un recorrido con errores.

>[!NOTE]
>
>Al guardar o publicar un recorrido, Journey Optimizer valida el tamaño total de la carga útil del recorrido y puede advertir o bloquear la publicación si se aproxima o supera el límite. Obtenga más información en [validación del tamaño de la carga útil de Recorrido](../start/guardrails.md#journey-payload-size).

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Proceso de publicación {#journey-publication}

Los pasos para publicar un recorrido se detallan a continuación:

1. Antes de publicar el recorrido, compruebe que es válido y que no hay errores. No se puede publicar un recorrido con errores.

   * Aprenda a probar su recorrido en [esta página](testing-the-journey.md).
   * Aprenda a solucionar los errores de recorrido en [esta sección](../building-journeys/troubleshooting.md#activity-errors).

1. Para publicar el recorrido, haga clic en la opción **[!UICONTROL Publicar]**, que se encuentra en el menú desplegable superior derecho.

   >[!NOTE]
   >
   > Si el recorrido está sujeto a una directiva de aprobación, debe solicitar la aprobación para publicar el recorrido. [Más información](../test-approve/gs-approval.md)

   ![Botón Publicar en la barra de herramientas de recorrido para activar el recorrido](assets/journeyuc1_18.png)

Cuando se publica el recorrido, está en modo **solo lectura**. En el modo de solo lectura, solo puede modificar las etiquetas y las descripciones de la actividad, el nombre del recorrido y la descripción del recorrido. Si necesita hacer más modificaciones en un recorrido publicado, cree [una nueva versión](journey-ui.md#journey-filter) del recorrido.

Cuando se detiene un recorrido, se detiene permanentemente. Todos los individuos que fluyen a través del recorrido se detienen permanentemente, y el recorrido deja de permitir nuevas entradas. Si necesita volver a ejecutar el recorrido, duplíquelo y publique el nuevo recorrido.

>[!IMPORTANT]
>
>* Si se realizan cambios en una decisión de oferta utilizada en un mensaje de recorrido, se debe cancelar la publicación del recorrido y volver a publicarlo. Esto garantiza que los cambios se incorporen al mensaje del recorrido y que el mensaje sea coherente con las últimas actualizaciones.
>
>* Se puede acceder a las imágenes o Assets en el contenido enviado durante un máximo de 2 años (730 días) desde su primera publicación en cualquier fragmento o mensaje en línea. Se requiere volver a publicar después de este período de caducidad (en cualquier momento después de 730 días) para mantenerlos accesibles durante otros 2 años. Cualquier republicación realizada dentro de los 730 días posteriores a la primera publicación no extenderá la caducidad de los activos/imágenes a los próximos 730 días.

## Versiones de recorridos {#journey-versions}

En la lista de recorridos, todas las versiones del recorrido se muestran con el número de versión. Cuando busca un recorrido, las versiones más recientes aparecen en la parte superior de la lista la primera vez que se abre la aplicación. A continuación, puede definir la clasificación que desee y la aplicación la mantendrá como preferencia del usuario. La versión del recorrido también se muestra en la parte superior de la interfaz de la edición de recorrido, encima del lienzo.

![Lista de versiones de Recorrido que muestra las versiones publicadas y en borrador](assets/journeyversions1.png)

>[!NOTE]
>
>Normalmente, un perfil no puede estar presente varias veces en el mismo recorrido y al mismo tiempo para todas las versiones activas del recorrido. Si la reentrada está habilitada, un perfil puede volver a entrar en un recorrido, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido. [Más información](entry-management.md).

### Crear una nueva versión de un recorrido {#journey-create-new-version}

Si necesita modificar a un recorrido activo, cree una nueva versión del recorrido. Para crear una nueva versión de un recorrido existente, siga los pasos a continuación:

1. Abra la última versión del recorrido activo, haga clic en **[!UICONTROL Crear una nueva versión]** y confirme.

   ![Cuadro de diálogo Crear nueva versión para duplicar el recorrido](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Solo puede crear una nueva versión a partir de la última versión de un recorrido.

1. Realice las modificaciones necesarias, haga clic en **[!UICONTROL Publicar]** y confirme.

Desde el momento en que se publique el recorrido, las personas empezarán a fluir hacia la última versión del recorrido. Las personas que ya han accedido a una versión anterior permanecerán en ella hasta que finalicen el recorrido. Si más tarde vuelven a entrar en el mismo recorrido, accederán a la versión más reciente.

Las versiones de recorrido se pueden detener individualmente. Todas las versiones de los recorridos tienen el mismo nombre.

Cuando se publica una nueva versión de un recorrido, la versión anterior finaliza automáticamente y cambia al estado **Cerrado.**. No puede haber ninguna entrada en el recorrido. Aunque detenga la versión más reciente, la versión anterior permanecerá cerrada.


>[!NOTE]
>
>Se aplican limitaciones y protecciones específicas al control de versiones de los recorridos. Obtenga más información en [esta página](../start/guardrails.md#journey-versions-g).


## Vídeo práctico {#video}

Obtenga información sobre cómo publicar un recorrido en este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3427933?captions=spa&quality=12)