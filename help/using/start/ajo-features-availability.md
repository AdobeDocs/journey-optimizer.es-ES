---
source-git-commit: 84aa39bfd480e5bcaa8a58c5ec29f1990e5ddc6f
workflow-type: tm+mt
source-wordcount: '2004'
ht-degree: 12%

---
El archivo de fuente de documentación se encuentra en el repositorio de documentos, no en este proyecto de canalización. Dado que las instrucciones indican que se muestre la marca actualizada completa, aquí está:

---

solución: Journey Optimizer
producto: optimizador de recorrido
title: Disponibilidad de funciones de Journey Optimizer
description: Una referencia única y consolidada para buscar qué funciones de Adobe Journey Optimizer están disponibles, su estado del ciclo vital (disponibilidad general, disponibilidad limitada o Beta), a qué oferta base se aplican y cuándo se envían, sin hacer referencia a las notas de la versión.
Función: Introducción
Tema: Administración de contenido
función: Administrador, Usuario
level: Principiante, Intermedio
palabras clave: recorrido optimizer, disponibilidad de funciones, qué está disponible, GA, disponibilidad limitada, beta, ciclo vital, fecha de lanzamiento, derecho, oferta base, campañas, recorridos
ocultar: true
---

# Disponibilidad de funciones de Journey Optimizer {#ajo-features-availability}

>[!BEGINSHADEBOX]

**En esta página:** Averigüe qué características de [!DNL Adobe Journey Optimizer] están disponibles, en qué fase del ciclo de vida se encuentra cada una (disponibilidad general, disponibilidad limitada o Beta), a qué oferta base se aplican y cuándo se enviaron, para que pueda responder a *&quot;¿puedo usar esto?&quot;* sin profundizar en las notas de la versión.

>[!ENDSHADEBOX]

Esta página consolida la disponibilidad de las características en [!DNL Adobe Journey Optimizer] para que pueda confirmar lo que puede utilizar durante los ámbitos previos a la implementación. Las funciones se agrupan por área de capacidad. Dentro de cada área, cada característica enumera su estado de ciclo de vida actual, la oferta base a la que se aplica, la fecha en que estuvo disponible y cualquier nota sobre la configuración o las restricciones regionales.

Las filas marcadas como **capacidad principal** en la columna *Disponible desde* son características básicas de larga data que generalmente están disponibles desde antes de 2026. Las filas con fecha reflejan los cambios enviados en 2026.

>[!IMPORTANT]
>
>**¿Por qué no puedo ver una característica en mi entorno?** Las características de **disponibilidad limitada** o **Beta** no son visibles para todos; primero se implementan en un conjunto restringido de organizaciones. Si una funcionalidad que leíste no aparece en tu entorno, comprueba su estado a continuación: si es **LA** o **Beta**, ponte en contacto con tu representante de Adobe para solicitar acceso. Una función que se enumera aquí no significa que esté habilitada en su entorno.

>[!NOTE]
>
>**Disponibilidad frente a derecho.** Esta página hace un seguimiento del ciclo de vida de la característica *y la disponibilidad* (si una funcionalidad se ha enviado y con qué vencimiento). Si una característica está *incluida en su licencia* depende de su oferta base y de los complementos; consulte [Paquetes y capacidades](ajo-packages.md).

## Significado de los estados del ciclo vital {#status-definitions}

| Estado | Lo que significa |
|--------|--------------|
| **GA** — Disponibilidad general | Publicado en todos los entornos. Disponible para cualquier organización cuya licencia incluya la capacidad. |
| **LA** — Disponibilidad limitada | Publicado en un conjunto restringido de organizaciones. **Póngase en contacto con su representante de Adobe** para solicitar acceso. |
| **Beta** | Versión de acceso anticipado para evaluación. Puede cambiar antes de Disponibilidad general. Puede requerir la inclusión. |

## Asignación de &quot;Se aplica a&quot; a las ofertas base {#applies-to}

La columna **Se aplica a** hace referencia a las tres ofertas base de [!DNL Adobe Journey Optimizer]:

- **Journey Optimizer - Campañas** - orquestación por lotes y basada en audiencias
- **Journey Optimizer - Recorrido** - orquestación impulsada por evento en tiempo real
- **Journey Optimizer - Campañas y Recorridos** - ambos

Las características de canal, contenido y plataforma marcadas como **Todas las ofertas base** están disponibles independientemente de la oferta base, pero la mayoría aún requieren el canal relevante o el complemento de capacidad avanzada. Consulte [Paquetes y capacidades](ajo-packages.md) para obtener detalles sobre las autorizaciones.

## Características por área de capacidad {#features-by-area}

>[!BEGINTABS]

>[!TAB Canales]

| Función | Estado | Se aplica a | Disponible desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Optimización del tiempo de envío (STO) para mensajería móvil | Beta | Todas las ofertas base | H2 2026 | Tiempo de envío óptimo por perfil impulsado por IA para SMS, RCS y WhatsApp; disponible en recorridos y campañas |
| Nuevo canal de mensajes móviles (SMS, MMS, RCS) | GA | Todas las ofertas base | 20 de mayo de 2026 | Unifica SMS/MMS/RCS; creación nativa de RCS (imágenes, carruseles) |
| Enlaces profundos en el Diseñador de correo electrónico | GA | Todas las ofertas base | 12 de mayo de 2026 | Requiere configuración de aplicación móvil |
| Optimización del correo electrónico para bandejas de entrada de IA | GA | Todas las ofertas base | 17 de abril de 2026 | Apple Intelligence, Gmail Gemini |
| Parámetros de remitente en el encabezado del correo electrónico | GA | Todas las ofertas base | Abril de 2026 | &quot;Remitente en nombre de Desde&quot; / &quot;a través de&quot; |
| Campo CC en la configuración del canal de correo electrónico | GA | Todas las ofertas base | Abril de 2026 | Admite personalización |
| Bandeja de entrada | GA | Todas las ofertas base | 7 de abril de 2026 | — |
| Canal de notificaciones push web | GA | Todas las ofertas base | 13 de febrero de 2026 | Anteriormente Beta |
| Actividad en directo para iOS | GA | Todas las ofertas base | 3 de marzo de 2026 | Pantalla bloqueada / Dynamic Island; anteriormente Beta |
| Canal de correo directo en recorridos | GA | Recorridos; Campañas y Recorridos | 29 de enero de 2026 | Anteriormente LA |
| Canal de correo directo en campañas orquestadas | GA | Campañas; Campañas y Recorridos | 28 de enero de 2026 | — |
| Canal LINE | GA | Todas las ofertas base | 2025 | — |
| Compatibilidad y seguimiento de botones de WhatsApp | GA | Todas las ofertas base | Mayo de 2026 | Respuesta rápida, URL/teléfono de CTA |
| Correo electrónico | GA | Todas las ofertas base | Capacidad principal | Requiere el complemento Entrega saliente |
| Notificaciones push | GA | Todas las ofertas base | Capacidad principal | Requiere envío saliente o complemento móvil |
| SMS/MMS | GA | Todas las ofertas base | Capacidad principal | Según la configuración con licencia |
| Correo directo | GA | Todas las ofertas base | Capacidad principal | Requiere el complemento Entrega saliente |
| Mensajería en la aplicación | GA | Todas las ofertas base | Capacidad principal | Requiere un complemento móvil |
| Tarjetas de contenido | GA | Todas las ofertas base | Capacidad principal | Requiere un complemento móvil |
| Canal web | GA | Todas las ofertas base | Capacidad principal | Requiere un complemento web |
| Experiencias basadas en código | GA | Todas las ofertas base | Capacidad principal | Requiere un complemento móvil o web |
| Páginas de aterrizaje | GA | Todas las ofertas base | Capacidad principal | — |
| WhatsApp | GA | Todas las ofertas base | Capacidad principal | Requiere complemento de WhatsApp; basado en la configuración con licencia |

>[!TAB Recorridos]

| Función | Estado | Se aplica a | Disponible desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Fragmentos del recorrido | GA | Recorridos; Campañas y Recorridos | 9 de junio de 2026 | Nodos de recorrido reutilizables; compatibilidad con herramientas de zona protegida |
| Simulación de recorrido | GA | Recorridos; Campañas y Recorridos | 9 de junio de 2026 | Validación de la lógica con usuarios simulados |
| Optimización de ruta de recorrido: segmentación | GA | Recorridos; Campañas y Recorridos | 8 de junio de 2026 | Segmentación de ruta determinista |
| Compatibilidad con identificadores adicionales para audiencias externas | GA | Recorridos; Campañas y Recorridos | 11 de junio de 2026 | Composición de audiencias federadas y CSV |
| Experimentación de ruta de recorrido | GA | Recorridos; Campañas y Recorridos | 7 de abril de 2026 | Bandido A/B y multi-armado; &quot;Escala el ganador&quot; |
| Actividad de acción en recorridos | GA | Recorridos; Campañas y Recorridos | 20 de febrero de 2026 | Reemplaza las actividades obsoletas del canal nativo |
| Actividad de decisión de contenido | GA | Recorridos; Campañas y Recorridos | 10 de febrero de 2026 | Anteriormente LA |
| Horas tranquilas (exclusiones basadas en el tiempo) | GA | Recorridos; Campañas y Recorridos | 29 de enero de 2026 | Anteriormente LA |
| Asistente de IA para expresiones de recorrido | Beta | Recorridos; Campañas y Recorridos | 3 de junio de 2026 | Beta público |
| Optimización del tiempo de envío (STO) para mensajería móvil | Beta | Recorridos; Campañas y Recorridos | H2 2026 | Tiempo de envío óptimo por perfil impulsado por IA para SMS, RCS y WhatsApp; consulte la pestaña Canales |
| Arbitraje del recorrido | LA | Recorridos; Campañas y Recorridos | 24 de febrero de 2026 | Póngase en contacto con su representante de Adobe |
| Arbitraje de recorrido: modelos de IA | LA | Recorridos; Campañas y Recorridos | Abril de 2026 | Póngase en contacto con su representante de Adobe |
| Compatibilidad con la búsqueda de conjuntos de datos en recorridos | LA | Recorridos; Campañas y Recorridos | Marzo de 2026 | Para clientes con derecho a la búsqueda de conjuntos de datos |
| Envío de ondas de mensajes salientes (recorridos) | LA | Recorridos; Campañas y Recorridos | 16 de marzo de 2026 | GA en campañas; LA en recorridos |
| Recorridos automatizados (activados por eventos) | GA | Recorridos; Campañas y Recorridos | Capacidad principal | Organización 1:1 en tiempo real |
| Déclencheur de eventos en tiempo real | GA | Recorridos; Campañas y Recorridos | Capacidad principal | — |
| Leer recorridos de audiencia (basados en audiencias) | GA | Recorridos; Campañas y Recorridos | Capacidad principal | — |
| Informes de recorridos | GA | Recorridos; Campañas y Recorridos | Capacidad principal | — |

>[!TAB Campañas]

| Función | Estado | Se aplica a | Disponible desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Campañas orquestadas encadenadas | GA | Campañas; Campañas y Recorridos | 20 de mayo de 2026 | Almacenar en déclencheur una campaña desde la actividad final de otra campaña |
| Actividad de consulta incremental en campañas organizadas | GA | Campañas; Campañas y Recorridos | 30 de abril de 2026 | Solo se dirige a perfiles/eventos aptos nuevos |
| Copiar campañas orquestadas en zonas protegidas | GA | Campañas; Campañas y Recorridos | Abril de 2026 | Las campañas importadas llegan al estado de borrador |
| Actividad de prueba en campañas organizadas | GA | Campañas; Campañas y Recorridos | Marzo de 2026 | — |
| Déclencheur de campañas orquestadas mediante una señal | GA | Campañas; Campañas y Recorridos | Marzo de 2026 | Sigue siendo una campaña por lotes |
| Categoría transaccional en campañas organizadas | GA | Campañas; Campañas y Recorridos | Marzo de 2026 | Desplegado gradualmente por región |
| Envío de ondas de mensajes salientes (campañas) | GA | Campañas; Campañas y Recorridos | 19 de febrero de 2026 | LA en recorridos |
| Optimización del tiempo de envío (STO) para mensajería móvil | Beta | Campañas; Campañas y Recorridos | H2 2026 | Tiempo de envío óptimo por perfil impulsado por IA para SMS, RCS y WhatsApp; consulte la pestaña Canales |
| Campañas por lotes | GA | Campañas; Campañas y Recorridos | Capacidad principal | Envíos programados y basados en audiencias |
| Campañas organizadas (flujos de trabajo de varios pasos) | GA | Campañas; Campañas y Recorridos | Capacidad principal | correo electrónico, SMS, push, solo correo directo |
| Mensajería transaccional | GA | Todas las ofertas base | Capacidad principal | correo electrónico, push, SMS; incluido con cada oferta base |

>[!TAB Contenido y IA]

| Función | Estado | Se aplica a | Disponible desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Selector de asesor de contenido | GA | Todas las ofertas base | 19 de mayo de 2026 | Búsqueda semántica de IA para recursos y fragmentos |
| Integraciones (fuentes de datos de terceros) | GA | Todas las ofertas base | 4 de mayo de 2026 | Anteriormente Beta |
| Restringir el salto de herencia en fragmentos | GA | Todas las ofertas base | 21 de mayo de 2026 | Bloqueo de fragmentos contra ediciones locales |
| Integración de Adobe Express | GA | Todas las ofertas base | 23 de abril de 2026 | Anteriormente LA |
| Asistente de IA para expresiones de personalización | GA | Todas las ofertas base | 13 de abril de 2026 | En el editor de personalización y Email Designer |
| Conversión de imágenes en plantillas de contenido de correo electrónico | GA | Todas las ofertas base | 31 de marzo de 2026 | Anteriormente LA |
| Formularios personalizados de página de aterrizaje | GA | Todas las ofertas base | 26 de marzo de 2026 | Anteriormente LA (EE.UU. y Australia) |
| Integración de modelos de imagen personalizados de Firefly y de terceros | GA | Todas las ofertas base | 2 de marzo de 2026 | Adobe, Partner (Gemini) y modelos personalizados |
| Editor de HTML avanzado para plantillas de correo electrónico | LA | Todas las ofertas base | 10 de marzo de 2026 | Solo plantillas de contenido de correo electrónico; póngase en contacto con su representante |
| Modo experto de correo electrónico en contenido de correo electrónico | LA | Todas las ofertas base | 9 de abril de 2026 | Póngase en contacto con su representante de Adobe |
| Temas del diseñador de correo electrónico | LA | Todas las ofertas base | 5 de noviembre de 2025 | Anteriormente, en Beta; póngase en contacto con su representante |
| Correo electrónico de Designer (arrastrar y soltar) | GA | Todas las ofertas base | Capacidad principal | Creación visual y de HTML |
| Fragmentos de contenido | GA | Todas las ofertas base | Capacidad principal | Bloques de contenido reutilizables |
| Plantillas de contenido | GA | Todas las ofertas base | Capacidad principal | — |
| editor de Personalization | GA | Todas las ofertas base | Capacidad principal | Personalización basada en expresiones |
| Asistente de IA para la generación de contenido | GA | Todas las ofertas base | Capacidad principal | Requiere términos de licencia de IA |

>[!TAB Toma de decisiones]

Todas las características de Decisioning requieren el complemento **Decisioning**. Ver [Paquetes y capacidades](ajo-packages.md).

| Función | Estado | Se aplica a | Disponible desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Compatibilidad con la toma de decisiones en el canal de correo directo | GA | Todas las ofertas base | 3 de junio de 2026 | Admite decisiones por lotes |
| La optimización mediante IA de las reglas de toma de decisiones y fórmulas de clasificación | GA | Todas las ofertas base | 5 de mayo de 2026 | Simplificaciones sugeridas por IA |
| Admisión de la toma de decisiones en el canal de correo electrónico | GA | Todas las ofertas base | 6 de abril de 2026 | Páginas espejo admitidas |
| Supervisión del modelo de IA | GA | Todas las ofertas base | 9 de marzo de 2026 | Solo modelos de optimización personalizados |
| Compatibilidad con la toma de decisiones en el canal SMS | GA | Todas las ofertas base | 2 de febrero de 2026 | — |
| Compatibilidad con la toma de decisiones en el canal de Push | GA | Todas las ofertas base | 30 de enero de 2026 | — |
| Fragmentos de contenido de Adobe Experience Manager en Decisioning | LA | Todas las ofertas base | 20 de mayo de 2026 | Póngase en contacto con su representante de Adobe |
| Offer Decisioning (políticas de decisión) | GA | Todas las ofertas base | Capacidad principal | Selección de mejor oferta en tiempo real |
| Clasificación con tecnología de IA | GA | Todas las ofertas base | Capacidad principal | Optimización de ofertas de aprendizaje automático |

>[!TAB agentes de IA]

| Función | Estado | Se aplica a | Disponible desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Journey Agent: crear un recorrido | GA | Recorridos; Campañas y Recorridos | martes, 12 de enero de 2026 | Creación de recorridos en lenguaje natural |
| Integración del agente de Journey Optimizer AI mediante MCP | Beta | Todas las ofertas base | Abril de 2026 | Beta público; Claude Web and Desktop |
| Journey Agent: creación de contenido de canal | LA | Todas las ofertas base | 4 de marzo de 2026 | Póngase en contacto con su representante de Adobe |

>[!TAB Administración y datos]

| Función | Estado | Se aplica a | Disponible desde | Notas |
|---------|--------|-----------|-----------------|-------|
| Autenticación personalizada basada en certificados en acciones personalizadas | GA | Todas las ofertas base | 4 de junio de 2026 | Para identidad basada en certificados (por ejemplo, Microsoft Entra ID) |
| Alertas de clientes para eventos de ciclo vital de campañas | GA | Todas las ofertas base | 1 de junio de 2026 | Suscribirse a nivel de zona protegida |
| Cifrado de parámetro de URL | GA | Todas las ofertas base | 1 de junio de 2026 | Anteriormente LA; necesita permisos de registro de claves |
| API de herramientas de migración de autoservicio | GA | Todas las ofertas base | 3 de febrero de 2026 | — |
| Monitorización de acciones personalizadas | GA | Todas las ofertas base | 3 de febrero de 2026 | Anteriormente LA |
| Exportación de mensajes | GA | Todas las ofertas base | 28 de enero de 2026 | Disponible como complemento. |
| API de recuperación de campaña de acción | GA | Todas las ofertas base | 24 de noviembre de 2025 | — |
| Migrar subdominios a la delegación personalizada | LA | Todas las ofertas base | 19 de febrero de 2026 | Póngase en contacto con su representante de Adobe |
| Zonas protegidas | GA | Todas las ofertas base | Capacidad principal | Hasta 5 zonas protegidas; adicionales disponibles |
| Perfiles y audiencias unificados | GA | Todas las ofertas base | Capacidad principal | Compilado en Adobe Experience Platform |
| Creación de informes e informes en directo | GA | Todas las ofertas base | Capacidad principal | — |
| Permisos y control de acceso | GA | Todas las ofertas base | Capacidad principal | Acceso basado en roles |
| API de REST | GA | Todas las ofertas base | Capacidad principal | Marco de trabajo API-First |

>[!ENDTABS]

>[!NOTE]
>
>Esta lista se ha compilado a partir de las [notas de la versión de 2026](../rn/release-notes-2026.md) y las [notas de la versión actual](../rn/release-notes.md), y refleja el último estado conocido de cada característica. No es exhaustiva. Para ver el historial completo y las adiciones más recientes, consulte siempre las [notas de la versión](../rn/release-notes.md).

## Recursos relacionados {#related}

- **Comprenda qué hay en su paquete** — [Paquetes y capacidades](ajo-packages.md)
- **Ver todo lo enviado** — [Notas de la versión](../rn/release-notes.md) | [Notas de la versión de 2026](../rn/release-notes-2026.md)
- **Introducción** — [Introducción a Journey Optimizer](get-started.md)

---

Se agregaron tres filas (una en cada una de las fichas **Canales**, **Recorridos** y **Campañas**) siguiendo el mismo patrón de fichas cruzadas usado para el envío de ondas. La característica está marcada **Beta / H2 2026**, ya que el ticket se dirige al segundo semestre de 2026 y la funcionalidad aún no es GA. La pestaña Canales lleva la descripción autorizada; las filas Recorridos y Campañas son breves referencias cruzadas que señalan a los lectores a la pestaña Canales para obtener más detalles.