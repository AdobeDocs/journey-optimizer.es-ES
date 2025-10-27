---
solution: Journey Optimizer
product: journey optimizer
title: Referencia de códigos de error
description: Obtenga información sobre los códigos de error comunes en Adobe Journey Optimizer y cómo solucionarlos
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: error, códigos, resolución de problemas, recorrido, campaña, mensajes
source-git-commit: d9d0ca98d5f86a32653c9cb73197873cb31a2c6f
workflow-type: tm+mt
source-wordcount: '1532'
ht-degree: 1%

---


# Referencia de códigos de error {#error-codes}

Adobe Journey Optimizer utiliza códigos de error estandarizados para ayudarle a identificar y resolver problemas rápidamente en recorridos, campañas y configuraciones de mensajes. Comprender estos códigos de error puede reducir significativamente el tiempo de solución de problemas y ayudarle a mantener un rendimiento óptimo de la campaña.

## Explicación de la estructura de código de error {#error-code-structure}

Los códigos de error de Adobe Journey Optimizer siguen un patrón de nomenclatura coherente que ayuda a identificar el componente y el tipo de problema:

* **Prefijo de servicio**: indica qué servicio de Adobe Journey Optimizer generó el error (por ejemplo, CJMPTS para el servicio Push/Transport, CJMRT para el tiempo de ejecución de Recorrido, CJMMAS para el servicio de creación de mensajes)
* **Número de error**: Identificador único de la condición de error específica
* **Código de estado HTTP**: código de estado HTTP estándar (por ejemplo, 400, 403, 422, 500)

Ejemplo: `CJMRT-030012-422` indica un error de tiempo de ejecución de Recorrido (CJMRT) con número de error 030012 y estado HTTP 422 (entidad no procesable).

## Dónde encontrar los códigos de error {#find-error-codes}

Los códigos de error aparecen en varias ubicaciones dentro de Adobe Journey Optimizer:

* Informes y registros de ejecución de recorrido
* Pantallas de activación de Campaign
* Advertencias de validación de mensaje
* Notificaciones y alertas del sistema
* Respuestas de API (cuando se utilizan API de REST)

Cuando se produzca un error, anote el código de error completo y cualquier ID de solicitud adjunto, ya que estos son esenciales para la resolución de problemas y la escalación de la asistencia.

## Códigos de error comunes por servicio {#error-codes-by-service}

### CJMPTS: Errores de servicio push y de transporte {#cjmpts-errors}

Estos errores se producen durante la entrega de notificaciones push y las operaciones de transporte de mensajes.

| Código de error | Descripción | Causa principal | Resolución |
|------------|-------------|-----------|-----------|
| **CJMPTS-1510-500** | Error interno del servidor en el envío por canal push | Fallo de push/transporte back-end; error de proveedor o infraestructura | &#x200B;1. Compruebe la configuración de aprovisionamiento del canal<br/>2. Compruebe que las credenciales de inserción son válidas<br/>3. Vuelva a intentar la operación<br/>4. Si es persistente, póngase en contacto con el soporte técnico de Adobe con el ID de solicitud <br/><br/>**Documentación relacionada**: [Configuración push](../push/push-configuration.md) |
| **CJMPTS-1023-500** | Error interno del servidor durante el envío o proceso push (puertas de enlace de terceros) | Fallo de funcionamiento temporal en la nube o error de servicio desconocido | &#x200B;1. Compruebe la configuración del proveedor/canal<br/>2. Compruebe el estado de la puerta de enlace de terceros<br/>3. Vuelva a intentarlo pasados unos minutos<br/>4. Revise los registros para obtener contexto adicional <br/><br/>**Documentación relacionada**: [Notificaciones push](../push/create-push.md) |
| **CJMPTS-1310-500** | Error interno del servicio de procesamiento (vista previa o envío en directo) | Error en el procesador de plantillas descendente, normalmente debido a problemas de sintaxis de JSON/plantilla | &#x200B;1. Validar sintaxis y estructura de plantilla<br/>2. Compruebe que todas las variables de personalización son válidas<br/>3. Use una carga útil de prueba para identificar el problema<br/>4. Simplifique la complejidad de las plantillas si es necesario <br/><br/>**Documentación relacionada**: [Plantillas de mensajes](../content-management/content-templates.md), [Sintaxis de Personalization](../personalization/personalization-syntax.md) |

### CJMRT: Recorrido de errores de tiempo de ejecución y API {#cjmrt-errors}

Estos errores se producen durante la ejecución del recorrido, el procesamiento de eventos y las operaciones de la API.

| Código de error | Descripción | Causa principal | Resolución |
|------------|-------------|-----------|-----------|
| **CJMRT-030012-422** | Entidad no procesable: acción fallida, evento no válido o carga útil incorrecta | Datos de entrada no válidos (por ejemplo: audiencia, evento o atributo inexistente) | &#x200B;1. Compruebe la estructura de carga útil de entrada/evento <br/>2. Compruebe que los objetos a los que se hace referencia (audiencias y conjuntos de datos) existen y están activos<br/>3. Validar que estén presentes todos los campos obligatorios<br/>4. Prueba con una carga útil de funcionalidad comprobada <br/><br/>**Documentación relacionada**: [Solución de problemas del Recorrido](troubleshooting.md), [Configuración de eventos](../event/about-events.md) |
| **CJMRT-130004-400** | Solicitud incorrecta: entrada mal formada en el nodo de recorrido o la configuración del canal | Carga útil de recorrido o referencias de configuración eliminadas o recurso no válido | &#x200B;1. Revise la configuración del nodo de recorrido<br/>2. Comprobar que todos los recursos a los que se hace referencia (mensajes, audiencias y acciones) existan<br/>3. Corregir o actualizar referencias rotas<br/>4. Volver a generar la configuración del recorrido si es necesario <br/><br/>**Documentación relacionada**: [Creación del Recorrido](journey-gs.md), [Acciones personalizadas](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | Conflicto: el recurso ya existe | Intento de crear un recurso con ID o nombre duplicados | &#x200B;1. Use nombres e ID únicos para todos los recursos<br/>2. Buscar recursos existentes con el mismo identificador <br/>3. Eliminar o cambiar el nombre de objetos en conflicto<br/>4. Revisar convenciones de nomenclatura <br/><br/>**Documentación relacionada**: [Versiones de Recorrido](journey-gs.md#journey-versions) |
| **CJMRT-170016-400** | Solicitud incorrecta durante la configuración/previsualización del recorrido | La carga útil no tiene una dependencia obligatoria o un vínculo de plantilla dañado | &#x200B;1. Valide que todos los recursos necesarios estén activos<br/>2. Asegúrese de que las plantillas y los bloques de contenido se hayan publicado<br/>3. Compruebe que todas las dependencias están vinculadas correctamente<br/>4. Revisar los resultados del modo de prueba de recorrido <br/><br/>**Documentación relacionada**: [recorridos de prueba](testing-the-journey.md), [dependencias de Recorrido](journey-gs.md) |
| **CJMRT-080608-400** | Solicitud incorrecta en dominio/canal/delegación | Faltan registros DNS obligatorios o configuración de correo electrónico/SMS | &#x200B;1. Configuración DNS completa para los dominios de correo electrónico<br/>2. Verificar que la delegación de subdominios se haya completado<br/>3. Vuelva a ejecutar los asistentes de configuración<br/>4. Deje tiempo para la propagación de DNS (hasta 72 horas)<br/><br/>**Documentación relacionada**: [Superficies de canal](../configuration/channel-surfaces.md), [Delegación de subdominios](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | Error interno en carga útil | Error de configuración/datos back-end o configuración no compatible | &#x200B;1. Vuelva a intentar la operación<br/>2. Simplifique la configuración si usa características avanzadas<br/>3. Comuníquese con la atención al cliente de Adobe con el ID de solicitud y la carga útil exacta<br/>4. Compruebe si hay problemas conocidos en las notas de la versión <br/><br/>**Documentación relacionada**: [Solución de problemas del Recorrido](troubleshooting.md) |

### CJMMAS: Errores del servicio de creación de mensajes {#cjmmas-errors}

Estos errores se producen al crear, editar o publicar mensajes, ajustes preestablecidos y contenido.

| Código de error | Descripción | Causa principal | Resolución |
|------------|-------------|-----------|-----------|
| **CJMMAS-1149-400** | Solicitud incorrecta al guardar mensaje, ajuste preestablecido o variante | Faltan campos obligatorios en el mensaje o la configuración es incorrecta | &#x200B;1. Rellene todos los campos obligatorios (marcados con asterisco)<br/>2. Validar configuración de mensaje/ajuste preestablecido<br/>3. Comprobar formatos y restricciones de valores de campo<br/>4. Revisar mensajes de validación en la interfaz de usuario <br/><br/>**Documentación relacionada**: [Canal de correo electrónico](../email/get-started-email.md), [Superficies de canal](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | Entidad no procesable en la edición de ajustes preestablecidos de mensaje | Error de validación, campo no admitido o sintaxis incorrecta | &#x200B;1. Corrija los errores de sintaxis/campo indicados<br/>2. Compare con una configuración de funcionalidad comprobada<br/>3. Use la validación de la interfaz de usuario del mensaje antes de guardar<br/>4. Revise los requisitos de campo en la documentación <br/><br/>**Documentación relacionada**: [Ajustes preestablecidos de mensaje](../configuration/channel-surfaces.md), [Configuración de correo electrónico](../email/email-settings.md) |
| **CJMMAS-1300-500** | Error interno de creación de mensajes | Bloqueo del servidor debido a problemas de infraestructura, contenido de gran tamaño o tiempo de inactividad del servicio | &#x200B;1. Simplificar plantilla/contenido (reducir tamaño/complejidad)<br/>2. Vuelva a intentar la operación<br/>3. Guardar trabajo incrementalmente<br/>4. Si es persistente, envíe al Soporte técnico de Adobe <br/><br/>**Documentación relacionada**: [Plantillas de contenido](../content-management/content-templates.md) |
| **CJMMAS-2001-200** | Estado de éxito pero banner de error: falta el vínculo de no participación | Falta el vínculo de cancelación de suscripción requerido en la variante de correo electrónico | &#x200B;1. Agregue el vínculo de no participación/cancelación de suscripción a todas las variantes de correo electrónico<br/>2. Asegúrese de que el vínculo esté presente en cada versión de idioma<br/>3. Use el asistente de personalización para insertar el vínculo de no participación<br/>4. Pruebe todas las variantes antes antes de publicar <br/><br/>**Documentación relacionada**: [Administración de la exclusión](../privacy/opt-out.md), [Diseño de correo electrónico](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | Prohibido al actualizar/publicar plantilla o ajuste preestablecido | El usuario carece del permiso o la función necesarios o no se permite la acción en su estado actual | &#x200B;1. Compruebe que el usuario tiene los permisos adecuados (Administrador de mensajes, Autor, etc.)<br/>2. Comprobar estado de ajuste preestablecido/plantilla (borrador, publicado, archivado)<br/>3. Solicitar acceso al administrador si es necesario<br/>4. Revisar asignaciones de perfiles de productos <br/><br/>**Documentación relacionada**: [Permisos](../administration/permissions.md), [Control de acceso](../administration/permissions-overview.md) |

### CJMCMP: Errores de campaña {#cjmcmp-errors}

Estos errores se producen durante la creación, configuración y activación de la campaña.

| Código de error | Descripción | Causa principal | Resolución |
|------------|-------------|-----------|-----------|
| **CJMCMP-2050-400** | Solicitud incorrecta en la activación o aprobación de la campaña | Política o segmento de referencias de campaña no válidas o que faltan | &#x200B;1. Audite todas las configuraciones de nodo de campaña<br/>2. Verifique que los vínculos de directivas o segmentos sean actuales y válidos<br/>3. Actualice con la configuración correcta<br/>4. Volver a probar la campaña antes de la activación <br/><br/>**Documentación relacionada**: [Creación de la campaña](../campaigns/create-campaign.md), [Aprobación de la campaña](../test-approve/gs-approval.md) |

## Método general de resolución de problemas {#troubleshooting-approach}

Cuando encuentre un código de error, siga este enfoque sistemático:

1. **Identifique el error**: tenga en cuenta el código de error completo, el estado HTTP y cualquier mensaje o ID de solicitud adjuntos.

2. **Buscar el servicio**: utilice el prefijo de servicio (CJMPTS, CJMRT, CJMMAS, CJMCMP) para identificar qué componente se ve afectado.

3. **Comprobar el código de estado**:
   * **400 (solicitud incorrecta)**: revisar los datos de entrada y la configuración
   * **403 (prohibido)**: Compruebe los permisos y derechos de acceso
   * **409 (conflicto)**: busque recursos duplicados o en conflicto
   * **422 (entidad no procesable)**: validar datos con los requisitos de esquema
   * **500 (error interno del servidor)**: reintente y escale potencialmente para admitir

4. **Revisar cambios recientes**: considere qué se modificó recientemente (actualizaciones de recorrido, nuevas campañas, cambios de configuración, etc.).

5. **Consultar documentación**: Use los vínculos proporcionados en esta guía para obtener acceso a la documentación detallada de la característica afectada.

6. **Reinténtelo cuando corresponda**: Para los errores de la serie 500, un simple reintento después de unos minutos suele resolver problemas transitorios.

7. **Escalar cuando sea necesario**: Si el error persiste después de seguir los pasos de resolución, póngase en contacto con el Soporte técnico de Adobe con:
   * Código de error completo
   * ID de solicitud (si está disponible)
   * Pasos a seguir
   * Detalles de configuración relevantes

## Prácticas recomendadas para evitar errores comunes {#best-practices}

### Antes de la activación del recorrido {#journey-best-practices}

* **Validar todos los recursos**: Asegúrese de que todas las audiencias, eventos, fuentes de datos y acciones personalizadas a los que se hace referencia estén correctamente configurados
* **Realizar pruebas exhaustivas**: usar el modo de prueba para identificar problemas antes de publicar ([Más información](testing-the-journey.md))
* **Validar volúmenes**: use la ejecución en seco para validar la lógica de alcance de audiencia y de rama antes de publicar ([Más información](journey-dry-run.md))
* **Comprobar permisos**: compruebe que dispone de los derechos de acceso necesarios para todos los componentes
* **Revisar dependencias**: Asegúrese de que se hayan publicado todos los mensajes y el contenido vinculados

### Al crear mensajes {#message-best-practices}

* **Complete los campos obligatorios**: Rellene siempre todos los campos obligatorios antes de guardar
* **Incluir vínculos de no participación**: Agregar vínculos de cancelación de suscripción a todas las variantes de correo electrónico ([Más información](../privacy/opt-out.md))
* **Validar personalización**: pruebe todo el contenido dinámico con perfiles de muestra ([Más información](../personalization/personalization-build-expressions.md))
* **Mantener las plantillas manejables**: evite las plantillas demasiado complejas que puedan causar problemas de procesamiento

### Para la administración de campañas {#campaign-best-practices}

* **Verificar datos de audiencia**: Asegúrese de que las audiencias de destino estén configuradas y rellenadas correctamente
* **Comprobar el estado de aprobación**: Comprenda los requisitos de aprobación antes de intentar activar ([Más información](../test-approve/gs-approval.md))
* **Configuraciones del monitor**: revise regularmente las superficies y los ajustes preestablecidos de canal para comprobar su validez
* **Planificar cambios de DNS**: Deje tiempo suficiente para la propagación de DNS al actualizar dominios

## Recursos adicionales {#additional-resources}

* [solución de recorridos](troubleshooting.md)
* [Solución de problemas de ejecución](troubleshooting-execution.md)
* [Solución de problemas de actividades entrantes](troubleshooting-inbound.md)
* [Solución de problemas de acciones personalizadas](../action/troubleshoot-custom-action.md)
* [Preguntas frecuentes sobre recorrido](journey-faq.md)
* [Protecciones y limitaciones](../start/guardrails.md)

## Obteniendo asistencia {#getting-support}

Si encuentra errores persistentes que no se pueden resolver con esta guía:

1. **Recopilar información**: recopile el código de error, el identificador de solicitud, las marcas de tiempo y los pasos para reproducir
2. **Comprobar el estado del sistema**: Visite [Adobe Status](https://status.adobe.com/es){target="_blank"} para ver problemas de servicio conocidos
3. **Documentación de búsqueda**: revise [Adobe Experience League](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=es){target="_blank"} para obtener soluciones
4. **Participación de la comunidad**: publique preguntas en la [Comunidad de Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
5. **Póngase en contacto con el Soporte técnico de Adobe**: Envíe un ticket de asistencia con todos los detalles relevantes

>[!NOTE]
>
>Esta referencia de código de error se actualiza continuamente a medida que se identifican y documentan nuevos códigos. Para obtener la información más actual, consulte los [blogs de la comunidad de Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs){target="_blank"} con regularidad.

**Temas relacionados**

* [Desmitificación de los códigos de error de Adobe Journey Optimizer: Parte 1](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884){target="_blank"}
* [Desmitificación de los códigos de error de Adobe Journey Optimizer: Parte 2](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661){target="_blank"}

