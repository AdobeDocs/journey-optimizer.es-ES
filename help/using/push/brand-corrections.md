---
solution: Journey Optimizer
product: journey optimizer
title: Correcciones de marca con tecnología de IA
description: Aprenda a configurar y utilizar correcciones de marca impulsadas por IA en Adobe Journey Optimizer.
feature: Brand Validation
topic: Content Management
role: User
level: Intermediate
exl-id: dd4fde0e-86c8-4a57-86ba-202e3be2c41f
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: 993
ht-degree: 1%

---


# Correcciones de marca con tecnología de IA {#brand-corrections}

>[!AVAILABILITY]
>
>Esta funcionalidad está disponible para Adobe Journey Optimizer y se aplica a los canales push, SMS y de contenido web.

## Información general {#overview}

Cuando el contenido se marca durante el control de calidad de la marca, Adobe Journey Optimizer puede generar automáticamente alternativas de texto corregidas o mejoradas mediante IA generativa. En lugar de volver a escribir manualmente las copias marcadas, recibirá sugerencias en línea que se ajustan a las directrices de marca, que puede revisar, previsualizar y aplicar con un solo clic.

Esto convierte el paso de control de calidad de la marca de una puerta de revisión de bloqueos en una **experiencia de corrección sobre la marcha**, lo que reduce el tiempo empleado en las correcciones manuales y acelera la producción de contenido en todos los canales.

Esta función está diseñada para especialistas en marketing de contenido, redactores de textos y operadores de campañas que necesiten mantener la conformidad de la marca en campañas de gran volumen y multicanal sin ralentizar los flujos de trabajo de producción.

## Funcionamiento {#how-it-works}

El control de calidad de la marca en Adobe Journey Optimizer evalúa el contenido en función de las directrices de marca de su organización, incluido el tono de voz, la terminología, los estándares de mensajería y las reglas editoriales. Cuando se detecta una infracción o un problema de calidad, el sistema marca el elemento de contenido afectado y, cuando se admite, genera automáticamente un reemplazo recomendado mediante el motor de IA generativa de Adobe.

El flujo de extremo a extremo es el siguiente:

1. **Examen de control de calidad de la marca**: al ejecutar una comprobación de marca en el contenido (cuerpo de notificación push, texto de mensaje SMS o bloque de contenido web), el sistema evalúa cada elemento comparándolo con las reglas de marca activas.
2. **Detección de infracciones**: los elementos que no cumplen uno o más criterios de marca se marcan con un indicador de gravedad (por ejemplo, crítico, advertencia o sugerencia).
3. **Generación de sugerencias de IA**: Por cada elemento marcado, el sistema genera automáticamente una o más alternativas de texto corregidas. Las sugerencias las produce el motor de IA generativa de Adobe, que conoce tanto el motivo de la infracción como el contexto de las directrices de su marca.
4. **Vista previa en línea**: el texto de reemplazo sugerido aparece en línea, directamente junto al original marcado. Puede comparar las versiones originales y sugeridas una al lado de la otra antes de realizar cualquier cambio.
5. **Aplicación con un solo clic**: si la sugerencia satisface sus necesidades, seleccione **Aplicar** para reemplazar el texto marcado con la versión generada por IA. El editor de contenido se actualiza inmediatamente y se borra el indicador de marca.
6. **Anulación manual**: nunca estará bloqueado en la sugerencia de IA. Puede editar la sugerencia antes de aplicarla, descartarla y escribir su propia corrección, o ignorar el indicador por completo si el contexto justifica una excepción.

>[!NOTE]
>
>Las sugerencias generadas por IA solo son recomendaciones. Su equipo retiene el control editorial completo. Revise siempre las sugerencias en el contexto de la campaña antes de aplicarlas.

## Requisitos previos {#prerequisites}

Antes de usar correcciones de marca con tecnología de IA, asegúrese de que se cumplan las siguientes condiciones:

- **Directrices de marca configuradas**: su organización debe tener al menos un perfil de marca activo configurado en Adobe Journey Optimizer. Los perfiles de marca definen las reglas con las que se evalúa el contenido. Póngase en contacto con el administrador de Adobe o con el administrador de marca para comprobar que los perfiles de marca se han publicado y asociado con los entornos limitados.
- **Funciones de inteligencia artificial aplicada al contenido habilitadas**: la asistencia de contenido con tecnología de IA debe habilitarse para su organización y su zona protegida. Esto se administra en el nivel de perfil de producto en Adobe Admin Console. Si las sugerencias de IA no aparecen después de un análisis de marca, confirme con su administrador que la asignación de derechos de generación de contenido de IA está activa.
- **Tipo de contenido admitido**: las correcciones de marca con sugerencias de IA se admiten para los siguientes tipos de contenido: título y cuerpo de la notificación push, texto del mensaje SMS y bloques de contenido web editados mediante Journey Optimizer Web Designer. Los recursos de medios enriquecidos (imágenes y vídeo) se evalúan por separado para determinar la conformidad con la marca y no entran en el ámbito de las correcciones de IA de nivel de texto.
- **Permisos de edición**: debe tener acceso de edición al recorrido, la campaña o la plantilla de contenido en la que reside el contenido marcado.

## Configurar {#configure}

No se requiere ninguna configuración adicional para habilitar las correcciones de marca con tecnología de IA si su organización ya utiliza el control de calidad de la marca. La capa de sugerencias de IA se activa automáticamente cuando se detectan violaciones de marca en tipos de contenido admitidos.

Para ejecutar una comprobación de marca y acceder a las sugerencias de IA:

1. Abra la campaña o el recorrido en Adobe Journey Optimizer.
2. Vaya al paso de contenido del canal correspondiente (push, SMS o web).
3. Seleccione **Comprobar la alineación de la marca** (o abra el panel **Control de calidad de la marca** desde la barra de herramientas del editor de contenido).
4. Espere a que finalice el análisis. Los elementos marcados se resaltan en el lienzo y se enumeran en el panel **Problemas de marca** de la derecha.
5. Para cada elemento marcado, expanda la fila de problema para ver el motivo de la infracción y la sugerencia generada por IA.
6. Use **Vista previa** para ver el texto sugerido en el lienzo de contenido.
7. Seleccione **Aplicar sugerencia** para reemplazar el texto marcado o seleccione **Editar** para modificar la sugerencia antes de aplicar.
8. Una vez resueltos o reconocidos todos los problemas, vuelva a ejecutar la comprobación de marca para confirmar el cumplimiento.

>[!NOTE]
>
>Al aplicar una sugerencia, se actualiza el contenido activo en el editor, pero no se publica ni activa automáticamente la campaña. Debe completar los pasos de configuración y activación de la campaña restantes como es habitual.

### Trabajo con varias sugerencias {#multiple-suggestions}

En el caso de algunas infracciones, el motor de IA puede generar más de una alternativa. En estos casos, el panel **Problemas de marca** muestra una lista numerada de opciones. Utilice las flechas hacia delante y hacia atrás para recorrer las alternativas antes de seleccionar la que mejor se ajuste a sus intenciones. Cada alternativa se genera con un enfoque estilístico diferente; por ejemplo, uno puede priorizar la concisión mientras que otro enfatiza la alineación de tonos.

### Correcciones masivas {#bulk-corrections}

Si se marcan varios elementos en el mismo fragmento de contenido, puede aplicar sugerencias individualmente o usar la acción **Aplicar todas las sugerencias** en la parte superior del panel **Problemas de marca** para aceptar todos los reemplazos generados por IA en un solo paso. Revise la lista cuidadosamente antes de utilizar la aplicación masiva, ya que esta acción reemplaza todo el texto marcado simultáneamente.

>[!NOTE]
>
>La aplicación masiva solo está disponible cuando todos los elementos marcados tienen una sugerencia de IA asociada. Los elementos sin sugerencia disponible (por ejemplo, los indicadores de compatibilidad con imágenes) se omiten y permanecen marcados para su revisión manual.

## Temas relacionados {#related-topics}

- [Información general sobre directrices de marca](../content-management/brands.md)
- [Ejecute una comprobación de marca en el contenido](../content-management/brand-score.md)
- [Asistente de IA para la generación de contenido](../content-management/gs-generative.md)
- [Crear una notificación push](create-push.md)
- [Creación de un mensaje SMS](../sms/create-sms.md)
- [Edición de contenido web con Journey Optimizer](../web/edit-web-content.md)
