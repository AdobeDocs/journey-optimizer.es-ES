---
solution: Journey Optimizer
product: journey optimizer
title: Publicación del recorrido
description: Obtenga información sobre cómo publicar un recorrido en Adobe Journey Optimizer, crear nuevas versiones, administrar los estados de recorrido y comprender los requisitos de republicación.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, recorrido, en directo, validez, comprobar
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Hhvwpfq0phAjvzIGgv-NMnnhWhYJ-PpLOL0F4Q-CnqA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 0bbbbf94550d4cb762ecca300932620c8d3da50e
workflow-type: tm+mt
source-wordcount: 1823
ht-degree: 14%

---

# Publicación del recorrido {#publishing-the-journey}

>[!BEGINSHADEBOX]

**En esta página:** Obtenga información sobre cómo publicar un recorrido para activarlo, incluidos los requisitos previos, el proceso de publicación, la administración de versiones y los requisitos para volver a publicar.

>[!ENDSHADEBOX]

La publicación de un recorrido lo activa: pasa al estado **[!UICONTROL Activo]**, pasa a estar disponible para que entren nuevos perfiles y cambia al modo de solo lectura. No puede publicar un recorrido que contenga errores.

>[!NOTE]
>
>Al guardar o publicar un recorrido, Journey Optimizer valida el tamaño total de la carga útil del recorrido y puede advertir o bloquear la publicación si se aproxima o supera el límite. Obtenga más información en [validación del tamaño de la carga útil de Recorrido](../start/guardrails.md#journey-payload-size).

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Antes de publicar {#before-you-publish}

Antes de publicar, asegúrese de que el recorrido cumpla los siguientes requisitos previos:

* **Sin errores de validación**: no puede publicar un recorrido que contenga errores. [Pruebe primero su recorrido](testing-the-journey.md) y [solucione los errores de actividad](../building-journeys/troubleshooting.md#activity-errors).
* **Permiso de publicación** — La publicación requiere el permiso de alto nivel **[!DNL Publish journeys]**. Más información sobre [administrar derechos de acceso](../administration/permissions-overview.md).
* **Carga útil dentro del límite**: la carga útil de recorrido debe estar dentro del límite configurado (4 MB de forma predeterminada). Ver [validación del tamaño de carga útil de Recorrido](../start/guardrails.md#journey-payload-size).
* **Aprobación obtenida**: si su recorrido está sujeto a una directiva de aprobación, solicite y obtenga la aprobación antes de publicarlo. [Más información](../test-approve/gs-approval.md).

>[!TIP]
>
>Antes de publicar, valide el recorrido con una de las opciones de prueba disponibles:
>
>* [Simulación](simulate-journey-gs.md): prueba con usuarios simulados, sin usar perfiles de prueba persistentes en Adobe Experience Platform.
>* [Modo de prueba](testing-the-journey.md): prueba con perfiles persistentes marcados como perfiles de prueba en Adobe Experience Platform.
>* [Ejecución en seco](journey-dry-run.md): prueba con datos de producción reales, sin contactar con perfiles.

## Proceso de publicación {#journey-publication}

Los pasos para publicar un recorrido se detallan a continuación:

1. Compruebe que la recorrido es válida y no contiene errores, y que cumple los [requisitos previos anteriores](#before-you-publish).

1. Para publicar el recorrido, haga clic en la opción **[!UICONTROL Publicar]**, que se encuentra en el menú desplegable superior derecho.

   >[!NOTE]
   >
   > Si el recorrido está sujeto a una directiva de aprobación, debe solicitar la aprobación para publicar el recorrido. [Más información](../test-approve/gs-approval.md)

   ![Botón Publicar en la barra de herramientas de recorrido para activar el recorrido](assets/journeyuc1_18.png)

Cuando se publica el recorrido, está en modo **solo lectura**. En el modo de solo lectura, solo puede modificar las etiquetas y las descripciones de la actividad, el nombre del recorrido y la descripción del recorrido. Si necesita hacer más modificaciones en un recorrido publicado, cree [una nueva versión](journey-ui.md#journey-filter) del recorrido.

### estados de recorrido {#journey-statuses}

Después de la publicación, un recorrido se desplaza por varios estados:

* **[!UICONTROL Activo]**: el recorrido se ha publicado y los perfiles pueden entrar en él.
* **[!UICONTROL Cerrado]**: una versión anterior que finalizó automáticamente cuando se publicó una nueva versión. No puede pasar ninguna entrada.
* **[!UICONTROL Finalizado]**: el recorrido se ha completado según sus criterios finales. Para ver la definición exacta de cuándo se considera que ha finalizado un recorrido, consulte [Cómo finalizan los recorridos](end-journey.md#journey-finished-definition).

### Detener un recorrido {#stop-journey}

Cuando se detiene un recorrido, se detiene permanentemente. Todos los individuos que fluyen a través del recorrido se detienen permanentemente, y el recorrido deja de permitir nuevas entradas. Si necesita volver a ejecutar el recorrido, duplíquelo y publique el nuevo recorrido. Para obtener más información sobre cómo finalizan los recorridos, consulte [Cómo finalizan los recorridos](end-journey.md).

### Requisitos de republicación {#republishing}

En algunos casos, debe volver a publicar un recorrido para que los cambios o los recursos sigan en vigor:

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


## Preguntas frecuentes {#faq}

**¿Por qué no puedo publicar mi recorrido?**

El motivo más común es que el recorrido contiene errores de validación: no se puede publicar un recorrido con errores. Otros bloqueadores incluyen el exceso de [límite de tamaño de carga útil](../start/guardrails.md#journey-payload-size), la falta del permiso **[!DNL Publish journeys]** o una [aprobación pendiente](../test-approve/gs-approval.md). Consulte [Antes de publicar](#before-you-publish) y [solucionar errores de actividad](../building-journeys/troubleshooting.md#activity-errors).

**¿Puedo editar un recorrido después de publicarlo?**

Un recorrido publicado está en modo de solo lectura. Solo puede cambiar las etiquetas y descripciones de las actividades, el nombre del recorrido y la descripción del recorrido. Para cualquier otro cambio, [cree una nueva versión](#journey-create-new-version) del recorrido.

**¿Qué les sucede a los perfiles que ya están en la recorrido cuando publico una nueva versión?**

Los nuevos perfiles fluyen a la versión más reciente. Los perfiles que ya están en una versión anterior permanecen allí hasta que finalizan; si más adelante vuelven a entrar, pasan a la versión más reciente. La versión anterior cambia automáticamente a **[!UICONTROL Cerrado]** y no acepta nuevas entradas. Ver [versiones de Recorrido](#journey-versions).

**¿Cómo puedo volver a ejecutar un recorrido detenido?**

Detener un recorrido es permanente. Para volver a ejecutarlo, duplíquelo y publique el nuevo recorrido. Ver [Detener un recorrido](#stop-journey).

**¿Debo volver a publicar después de cambiar una decisión de oferta o actualizar recursos?**

Sí. Si cambia una decisión de oferta utilizada en el mensaje de un recorrido, cancele la publicación del recorrido y vuelva a publicarlo para que se aplique el cambio. Assets e imágenes caducan 730 días después de la primera publicación; vuelva a publicar después de ese periodo para mantenerlas accesibles. Consulte [Requisitos para volver a publicar](#republishing).

**¿Puedo publicar un recorrido que requiera aprobación?**

Si el recorrido está sujeto a una directiva de aprobación, debe solicitar la aprobación antes de publicar. [Más información sobre la aprobación](../test-approve/gs-approval.md).

## Temas relacionados {#related-topics}

* [Pruebe su recorrido](testing-the-journey.md) - Valide su recorrido con perfiles de prueba antes de publicar
* [simulación de Recorrido](simulate-journey-gs.md): valide su recorrido con usuarios simulados antes de publicar
* [Ejecución en seco de Recorrido](journey-dry-run.md): prueba con datos de producción reales sin contactar con perfiles
* [Solución de problemas](../building-journeys/troubleshooting.md#activity-errors) - Resolver errores de actividad y publicación
* [Cómo terminan los recorridos](end-journey.md#journey-finished-definition) - Comprender la finalización y los estados de los recorridos
* [Administración de entrada de perfiles](entry-management.md): configure el modo en que los perfiles escriben y vuelven a introducir recorridos
* [limitaciones y protecciones de Recorrido](../start/guardrails.md#journeys-guardrails-journeys): revise las protecciones de publicación y versiones

## Vídeo práctico {#video}

Obtenga información sobre cómo publicar un recorrido en este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3424998?quality=12)

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo publicar un recorrido de Adobe Journey Optimizer, administrar versiones de recorrido y comprender las restricciones que se aplican una vez que un recorrido está activo.

**Intenciones:**
* Publicar un recorrido para que esté activo y disponible para la entrada de perfiles
* Compruebe la validez de la recorrido y resuelva los errores antes de publicar
* Cree una nueva versión de un recorrido activo para realizar modificaciones
* Comprender las restricciones de solo lectura que se aplican después de publicar un recorrido
* Detener un recorrido de forma permanente o administrar las transiciones entre versiones

**Glosario:**
* **Versión de Recorrido**: Una iteración numerada de un recorrido; se crean nuevas versiones para modificar un recorrido activo sin interrumpir los perfiles en curso *(específico del producto)*
* **Estado cerrado**: El estado en el que entra automáticamente una versión anterior del recorrido cuando se publica una nueva versión; ningún perfil nuevo puede entrar en un recorrido cerrado *(específico del producto)*
* **Directiva de aprobación**: Un flujo de trabajo de administración opcional que requiere aprobación explícita antes de que se pueda publicar un recorrido *(específico del producto)*

**Protecciones:**
* No se puede publicar un recorrido con errores.
* Journey Optimizer valida el tamaño total de la carga útil de los recorridos en el momento de guardar y publicar; la publicación puede bloquearse si se supera el límite.
* Después de la publicación, un recorrido se encuentra en modo de solo lectura; solo se pueden editar etiquetas, descripciones y el nombre del recorrido.
* Solo se puede crear una nueva versión a partir de la última versión de un recorrido.
* Cuando se detiene un recorrido, se detiene permanentemente; debe duplicarse para volver a ejecutarse.
* Se puede acceder a Assets e imágenes en el contenido enviado durante un máximo de 730 días desde la primera publicación; se requiere volver a publicar después de ese periodo.
* Si cambia la decisión de oferta utilizada en un mensaje de recorrido, se debe cancelar la publicación del recorrido y volver a publicarlo.
* Se aplican protecciones específicas al control de versiones de recorrido (consulte la página de protecciones).

**Terminología:**
* Nombre canónico: Publicar Recorrido — Acrónimo: none — variantes: activar recorrido, activar
* Sinónimos: &quot;Publish&quot; = &quot;activate&quot; = &quot;go live&quot;
* No confundir: Detener (parada de emergencia de todos los perfiles) ≠ Cerca de nuevas entradas (cierre correcto manual; perfiles existentes terminan) ≠ Estado cerrado (automático cuando se publica una nueva versión o después de cerrar manualmente las nuevas entradas)

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Puedo editar un recorrido después de publicarlo?** — Sólo se pueden cambiar las etiquetas, las descripciones y el nombre del recorrido. Para realizar otras modificaciones, cree una nueva versión del recorrido.
* **Q: ¿Qué les sucede a los perfiles de una versión de recorrido anterior cuando se publica una nueva versión?** : los perfiles que ya están en la versión anterior permanecen allí hasta que finalizan; los nuevos perfiles introducen la versión más reciente.
* **Q: ¿Puedo volver a publicar una versión de recorrido cerrado?** — No. Una vez que una versión anterior está Cerrada, permanece cerrada incluso si se detiene la última versión.
* **Q: ¿Qué debo hacer si cambia una decisión de oferta usada en el recorrido?** — Cancele la publicación del recorrido y vuelva a publicarlo para incorporar la decisión de oferta actualizada.
* **Q: ¿Se requiere aprobación antes de publicar?** — Solo si su recorrido está sujeto a una directiva de aprobación; en ese caso, primero debe solicitar la aprobación.

+++
