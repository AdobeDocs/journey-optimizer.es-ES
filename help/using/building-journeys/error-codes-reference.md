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
source-git-commit: 405c87f9ca138e4e92438704b5051ce89c73d726
workflow-type: tm+mt
source-wordcount: '2392'
ht-degree: 1%

---


# Referencia de códigos de error {#error-codes}

Adobe Journey Optimizer utiliza códigos de error estandarizados para ayudarle a identificar y resolver problemas rápidamente en recorridos, campañas y configuraciones de mensajes. Comprender estos códigos de error puede reducir significativamente el tiempo de solución de problemas y ayudarle a mantener un rendimiento óptimo de la campaña.

## Explicación de la estructura de código de error {#error-code-structure}

Los códigos de error de Adobe Journey Optimizer siguen un patrón de nomenclatura coherente que ayuda a identificar el componente y el tipo de problema:

* **Prefijo de servicio**: indica qué servicio de Adobe Journey Optimizer generó el error (por ejemplo, CJMPTS para el servicio Push/Transport, CJMRT para el tiempo de ejecución de Recorrido, CJMMAS para el servicio de creación de mensajes, CJMCMP para Campaign, CJMTL para la capa de transporte, CJMRPS para el servicio de informes/aprovisionamiento)
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
| **CJMPTS-1410-500** | Error interno del servidor al realizar la acción de envío push/canal | Interrupción del back-end del canal, credenciales caducadas, configuración incorrecta o error del proveedor | &#x200B;1. Reintentar tras retraso<br/>2. Compruebe las configuraciones y cuotas del proveedor<br/>3. Compruebe que las credenciales de inserción son válidas<br/>4. Probar con un canal alternativo <br/>5. Si es persistente, póngase en contacto con el soporte técnico de Adobe con el ID de solicitud <br/><br/>**Documentación relacionada**: [Configuración push](../push/push-configuration.md) |
| **CJMPTS-1006-404** | Push/SMS produce el error &quot;no se encontró el recurso&quot; | El proveedor o canal al que se hace referencia no existe, está mal escrito o se ha desaprovisionado | &#x200B;1. Revise y corrija las referencias e ID de proveedor/canal<br/>2. Auditar configuración de organización/zona protegida<br/>3. Verifique que las configuraciones de canal estén activas<br/>4. Vuelva a crear la configuración de canal si es necesario <br/><br/>**Documentación relacionada**: [Superficies de canal](../configuration/channel-surfaces.md) |
| **CJMPTS-1510-500** | Error interno del servidor en el envío por canal push | Fallo de push/transporte back-end; error de proveedor o infraestructura | &#x200B;1. Compruebe la configuración de aprovisionamiento del canal<br/>2. Compruebe que las credenciales de inserción son válidas<br/>3. Vuelva a intentar la operación<br/>4. Si es persistente, póngase en contacto con el soporte técnico de Adobe con el ID de solicitud <br/><br/>**Documentación relacionada**: [Configuración push](../push/push-configuration.md) |
| **CJMPTS-1023-500** | Error interno del servidor durante el envío o proceso push (puertas de enlace de terceros) | Fallo de funcionamiento temporal en la nube o error de servicio desconocido | &#x200B;1. Compruebe la configuración del proveedor/canal<br/>2. Compruebe el estado de la puerta de enlace de terceros<br/>3. Vuelva a intentarlo pasados unos minutos<br/>4. Revise los registros para obtener contexto adicional <br/><br/>**Documentación relacionada**: [Notificaciones push](../push/create-push.md) |
| **CJMPTS-1310-500** | Error interno del servicio de procesamiento (vista previa o envío en directo) | Error en el procesador de plantillas descendente, normalmente debido a problemas de sintaxis de JSON/plantilla | &#x200B;1. Validar sintaxis y estructura de plantilla<br/>2. Compruebe que todas las variables de personalización son válidas<br/>3. Use una carga útil de prueba para identificar el problema<br/>4. Simplifique la complejidad de las plantillas si es necesario <br/><br/>**Documentación relacionada**: [Plantillas de mensajes](../content-management/content-templates.md), [Sintaxis de Personalization](../personalization/personalization-syntax.md) |

### CJMRT: Recorrido de errores de tiempo de ejecución y API {#cjmrt-errors}

Estos errores se producen durante la ejecución del recorrido, el procesamiento de eventos y las operaciones de la API.

| Código de error | Descripción | Causa principal | Resolución |
|------------|-------------|-----------|-----------|
| **CJMRT-110001-500** | Se ha superado el máximo de ejecuciones para el paso del flujo de trabajo (por ejemplo, se agota el tiempo de espera del aprovisionamiento de afinidad IP) | El trabajo de flujo de trabajo/aprovisionamiento no se completó dentro de los reintentos/tiempo permitido, a menudo debido a un retraso de la infraestructura/servicio o a un problema temporal del servidor | &#x200B;1. Inténtelo de nuevo más tarde<br/>2. Comprobar [estado de Adobe](https://status.adobe.com/es) para detectar interrupciones<br/>3. Comuníquese con la Asistencia de Adobe con los detalles de flujo de trabajo/trabajo/organización<br/>4. Proporcione registros y capturas de red si están disponibles <br/><br/>**Documentación relacionada**: [Solución de problemas del Recorrido](troubleshooting.md) |
| **CJMRT-000071-400** | Solicitud incorrecta durante el evento de recorrido/prueba o llamada de API | Faltan parámetros o la carga útil está mal formada; la entrada hace referencia a un recurso inexistente o inactivo | &#x200B;1. Revise el cuerpo de la solicitud para obtener detalles del error<br/>2. Referencia/parámetro correcto<br/>3. Quitar la configuración avanzada y reintentar<br/>4. Vuelva a agregar características una por una para identificar el problema <br/><br/>**Documentación relacionada**: [Solución de problemas del Recorrido](troubleshooting.md), [Configuración de eventos](../event/about-events.md) |
| **CJMRT-000013-401** | Error no autorizado durante la operación/evento de API de tiempo de ejecución del mensaje | Error de autenticación: el token ha caducado, faltan permisos o el usuario/integración ha perdido el acceso al entorno | &#x200B;1. Compruebe los permisos y funciones<br/>2. Actualizar token de autenticación<br/>3. Use una cuenta de usuario/servicio válida conocida<br/>4. Revisar asignaciones de perfiles de productos <br/><br/>**Documentación relacionada**: [Permisos](../administration/permissions.md) |
| **CJMRT-080605-400** | Solicitud incorrecta desde el tiempo de ejecución de la recorrido (por ejemplo, déclencheur de nodo, acción, etc.) | La configuración hace referencia a una función, plantilla o canal desactualizados o eliminados o con un nombre cambiado | &#x200B;1. Validar todas las referencias de recursos<br/>2. Auditar la configuración del recorrido y los indicadores de características<br/>3. Actualizar referencias rotas<br/>4. Revise las actualizaciones y migraciones recientes del sistema <br/><br/>**Documentación relacionada**: [Creación de Recorridos](journey-gs.md) |
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
| **CJMMAS-1732-500** | La prueba ha fallado: todos los recursos no se publican al enviar la prueba o la prueba con el recurso de AEM | El recurso publicado recientemente aún no está en AJO; ID de recurso no coincide; uso de varios repositorios; retraso de sincronización de AEM | &#x200B;1. Use solamente los ID de recurso publicados del repositorio o entorno correcto<br/>2. Deje tiempo para la sincronización entre AEM y AJO<br/>3. Vuelva a intentarlo con un recurso de funcionalidad comprobada<br/>4. Verificar el estado de publicación de recursos en AEM <br/><br/>**Documentación relacionada**: [Integración de Assets](../content-management/assets.md) |
| **CJMMAS-1069-500** | Error interno al guardar o publicar la plantilla de mensaje | Excepción back-end (error de infraestructura/servicio o problema de contenido); marcado o función no compatible | &#x200B;1. Simplifique o reduzca la complejidad de la plantilla<br/>2. Vuelva a agregar contenido en pasos incrementales para identificar el problema<br/>3. Comprueba la [página de estado de Adobe](https://status.adobe.com/es)<br/>4. Quitar características o marcas no compatibles <br/><br/>**Documentación relacionada**: [Plantillas de contenido](../content-management/content-templates.md) |
| **CJMMAS-1149-400** | Solicitud incorrecta al guardar mensaje, ajuste preestablecido o variante | Faltan campos obligatorios en el mensaje o la configuración es incorrecta | &#x200B;1. Rellene todos los campos obligatorios (marcados con asterisco)<br/>2. Validar configuración de mensaje/ajuste preestablecido<br/>3. Comprobar formatos y restricciones de valores de campo<br/>4. Revisar mensajes de validación en la interfaz de usuario <br/><br/>**Documentación relacionada**: [Canal de correo electrónico](../email/get-started-email.md), [Superficies de canal](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | Entidad no procesable en la edición de ajustes preestablecidos de mensaje | Error de validación, campo no admitido o sintaxis incorrecta | &#x200B;1. Corrija los errores de sintaxis/campo indicados<br/>2. Compare con una configuración de funcionalidad comprobada<br/>3. Use la validación de la interfaz de usuario del mensaje antes de guardar<br/>4. Revise los requisitos de campo en la documentación <br/><br/>**Documentación relacionada**: [Ajustes preestablecidos de mensaje](../configuration/channel-surfaces.md), [Configuración de correo electrónico](../email/email-settings.md) |
| **CJMMAS-1300-500** | Error interno de creación de mensajes | Bloqueo del servidor debido a problemas de infraestructura, contenido de gran tamaño o tiempo de inactividad del servicio | &#x200B;1. Simplificar plantilla/contenido (reducir tamaño/complejidad)<br/>2. Vuelva a intentar la operación<br/>3. Guardar trabajo incrementalmente<br/>4. Si es persistente, envíe al Soporte técnico de Adobe <br/><br/>**Documentación relacionada**: [Plantillas de contenido](../content-management/content-templates.md) |
| **CJMMAS-2001-200** | Estado de éxito pero banner de error: falta el vínculo de no participación | Falta el vínculo de cancelación de suscripción requerido en la variante de correo electrónico | &#x200B;1. Agregue el vínculo de no participación/cancelación de suscripción a todas las variantes de correo electrónico<br/>2. Asegúrese de que el vínculo esté presente en cada versión de idioma<br/>3. Use el asistente de personalización para insertar el vínculo de no participación<br/>4. Pruebe todas las variantes antes antes de publicar <br/><br/>**Documentación relacionada**: [Administración de la exclusión](../privacy/opt-out.md), [Diseño de correo electrónico](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | Prohibido al actualizar/publicar plantilla o ajuste preestablecido | El usuario carece del permiso o la función necesarios o no se permite la acción en su estado actual | &#x200B;1. Compruebe que el usuario tiene los permisos adecuados (Administrador de mensajes, Autor, etc.)<br/>2. Comprobar estado de ajuste preestablecido/plantilla (borrador, publicado, archivado)<br/>3. Solicitar acceso al administrador si es necesario<br/>4. Revisar asignaciones de perfiles de productos <br/><br/>**Documentación relacionada**: [Permisos](../administration/permissions.md), [Control de acceso](../administration/permissions-overview.md) |

### CJMCMP: Errores de campaña {#cjmcmp-errors}

Estos errores se producen durante la creación, configuración y activación de la campaña.

| Código de error | Descripción | Causa principal | Resolución |
|------------|-------------|-----------|-----------|
| **CJMCMP-6003-400** | &quot;Hay al menos una campaña incorrecta&quot; al publicar/probar el recorrido/mensaje del modo | El nodo hace referencia a una campaña que falta, que no se ha publicado o que no es válida; el recorrido heredado o clonado no crea inlines | &#x200B;1. Abra cada nodo de mensaje y compruebe la configuración<br/>2. Volver a vincular o agregar nodos de mensajes<br/>3. Activar el modo de prueba para forzar la creación de campañas en línea<br/>4. Pasarse al nuevo asistente de recorrido si el problema es frecuente <br/><br/>**Documentación relacionada**: [Creación de Recorrido](journey-gs.md), [recorridos de prueba](testing-the-journey.md) |
| **CJMCMP-2003-400** | Titular de la interfaz de usuario: &quot;El experimento es incorrecto&quot; en el correo electrónico de Designer | Experimento o proveedor de datos obsoleto o ausente; limpieza del experimento fallida, discrepancia de esquema o error de validación de la interfaz de usuario | &#x200B;1. Quite los campos de experimento no utilizados<br/>2. Validar conexiones de esquema y proveedor de datos<br/>3. Vuelva a cargar la interfaz de usuario y borre la caché del explorador<br/>4. Volver a crear nodo/correo electrónico si el problema no se ha resuelto <br/><br/>**Documentación relacionada**: [Experimentos de contenido](../content-management/content-experiment.md) |
| **CJMCMP-3001-400** | Simulación/previsualización &quot;filtro de tipo de superficie incorrecto&quot; | El nodo creado con la estructura heredada envía type=surfaceId, el back-end espera brandingPresetId | &#x200B;1. Elimine y vuelva a crear el nodo afectado<br/>2. Usar la nueva versión o plantilla de recorrido<br/>3. Use el modo de prueba para borrar la configuración<br/>4. Volver a crear nodos de forma masiva si el problema está generalizado <br/><br/>**Documentación relacionada**: [Superficies de canal](../configuration/channel-surfaces.md), [Simulación de mensaje](../content-management/preview.md) |
| **CJMCMP-2050-400** | Solicitud incorrecta en la activación o aprobación de la campaña | Política o segmento de referencias de campaña no válidas o que faltan | &#x200B;1. Audite todas las configuraciones de nodo de campaña<br/>2. Verifique que los vínculos de directivas o segmentos sean actuales y válidos<br/>3. Actualice con la configuración correcta<br/>4. Volver a probar la campaña antes de la activación <br/><br/>**Documentación relacionada**: [Creación de la campaña](../campaigns/create-campaign.md), [Aprobación de la campaña](../test-approve/gs-approval.md) |

### CJMTL: Errores de capa de transporte {#cjmtl-errors}

Estos errores se producen durante el transporte de mensajes y las operaciones de envío.

| Código de error | Descripción | Causa principal | Resolución |
|------------|-------------|-----------|-----------|
| **CJMTL-010018-422** | &quot;No se permite Personalization en el nombre de dominio&quot; al guardar o enviar contenido | La validación demasiado estricta interrumpió temporalmente la personalización del dominio href dinámico | &#x200B;1. Refactorice los vínculos si usa variables de dominio<br/>2. Compruebe que la última versión de AJO esté en uso<br/>3. Vuelva a intentar la operación<br/>4. Use dominios estáticos si el problema persiste <br/><br/>**Documentación relacionada**: [Sintaxis de Personalization](../personalization/personalization-syntax.md), [Diseño de correo electrónico](../email/content-from-scratch.md) |
| **CJMTL-010011-422** | Entidad no procesable: el envío push/SMS/correo electrónico falla, dice &quot;campo no válido&quot; | Faltan datos de carga útil o de destinatario/contacto o no son válidos | &#x200B;1. Inspeccione los registros para detectar errores de campo específicos<br/>2. Se corrigió la información de perfil/contacto<br/>3. Validar con perfil de prueba<br/>4. Refactorice el formato de carga útil según sea necesario <br/><br/>**Documentación relacionada**: [Administración de perfiles](../audience/get-started-profiles.md), [Perfiles de prueba](../audience/creating-test-profiles.md) |

### CJMRPS: Errores del servicio de creación de informes y aprovisionamiento {#cjmrps-errors}

Estos errores se producen durante las operaciones de configuración de informes y aprovisionamiento de conjuntos de datos.

| Código de error | Descripción | Causa principal | Resolución |
|------------|-------------|-----------|-----------|
| **CJMRPS-1047-409** | &quot;Conflicto. El conjunto de datos ya se ha agregado al agregar un conjunto de datos de informes | Intentando agregar un conjunto de datos que ya está aprovisionado | &#x200B;1. Revise la configuración del conjunto de datos en la configuración de informes<br/>2. No vuelva a agregar los conjuntos de datos ya presentes<br/>3. Usar listas de comprobación de migración oficiales para informar sobre la migración<br/>4. Quitar referencias duplicadas de conjuntos de datos <br/><br/>**Documentación relacionada**: [Informes globales](../reports/global-report.md), [Informes en vivo](../reports/live-report.md) |

## Método general de resolución de problemas {#troubleshooting-approach}

Cuando encuentre un código de error, siga este enfoque sistemático:

1. **Identifique el error**: tenga en cuenta el código de error completo, el estado HTTP y cualquier mensaje o ID de solicitud adjuntos.

2. **Buscar el servicio**: utilice el prefijo de servicio (CJMPTS, CJMRT, CJMMAS, CJMCMP, CJMTL, CJMRPS) para identificar qué componente se ve afectado.

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
* [Mecanismos de protección y limitaciones](../start/guardrails.md)

## Obteniendo asistencia {#getting-support}

Si encuentra errores persistentes que no se pueden resolver con esta guía:

1. **Recopilar información**: recopile el código de error, el identificador de solicitud, las marcas de tiempo y los pasos para reproducir
2. **Comprobar el estado del sistema**: Visite [Adobe Status](https://status.adobe.com/es){target="_blank"} para ver problemas de servicio conocidos
3. **Documentación de búsqueda**: revise [Adobe Experience League](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=es){target="_blank"} para obtener soluciones
4. **Participación de la comunidad**: publique preguntas en la [Comunidad de Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=es){target="_blank"}
5. **Póngase en contacto con el Soporte técnico de Adobe**: Envíe un ticket de asistencia con todos los detalles relevantes

>[!NOTE]
>
>Esta referencia de código de error se actualiza continuamente a medida que se identifican y documentan nuevos códigos. Para obtener la información más actual, consulte los [blogs de la comunidad de Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs?profile.language=es){target="_blank"} con regularidad.

**Temas relacionados**

* [Desmitificación de los códigos de error de Adobe Journey Optimizer: Parte 1](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884?profile.language=es){target="_blank"}
* [Desmitificación de los códigos de error de Adobe Journey Optimizer: Parte 2](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661?profile.language=es){target="_blank"}

