---
solution: Journey Optimizer
product: journey optimizer
title: Guía de entrega de calentamiento de IP
description: Conozca los aspectos básicos de la capacidad de entrega y las prácticas recomendadas para el calentamiento de IP
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, capacidad de envío, reputación, ISP, participación
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 5%

---

# Guía de entrega de calentamiento de IP {#ip-warmup-deliverability-guide}

Al lanzar campañas de correo electrónico con nuevas direcciones IP o dominios en Adobe Journey Optimizer, comprender los aspectos básicos de la capacidad de entrega es crucial para crear una sólida reputación de remitente. Esta guía cubre los conceptos clave, los pasos de preparación y las prácticas recomendadas para ayudarle a pasar de una reputación cero a una ubicación correcta en la bandeja de entrada.

➡️ Obtenga información acerca de los aspectos básicos de la capacidad de envío, la creación de reputación y las prácticas recomendadas para el calentamiento de IP en el vídeo de esta [publicación de blog de Adobe](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950){target="_blank"}.

>[!NOTE]
>
>Para obtener instrucciones paso a paso sobre cómo implementar planes de calentamiento de IP en Adobe Journey Optimizer, consulte [Introducción a los planes de calentamiento de IP](ip-warmup-gs.md).

## Por qué importan la IP y la reputación de dominio {#reputation-matters}

Los proveedores de buzones de correo (Gmail, Yahoo, Microsoft, Apple Mail y otros) evalúan cada remitente en función de cuatro pilares clave:

* **Quejas**: ¿Los destinatarios marcaron sus mensajes como correo no deseado?
* **Participación**: ¿Los destinatarios abren, hacen clic o responden a sus correos electrónicos?
* **Infraestructura**: ¿Su infraestructura de envío está autenticada, es estable y confiable?
* **Contenido**: ¿El contenido de su mensaje parece legítimo y valioso?

El calentamiento de la IP aborda principalmente los tres primeros pilares al demostrar gradualmente a los proveedores de buzones de correo que su nueva infraestructura es legítima y deseada antes de escalar al volumen de envío completo.

## Lista de comprobación previa al vuelo {#pre-flight-checklist}

Antes de empezar a calentar las direcciones IP, asegúrese de que todos los elementos básicos estén establecidos. La siguiente tabla describe las tareas esenciales que se deben completar antes de iniciar el plan de calentamiento de IP.

| Tarea | Por qué importa | Cómo se logra |
|------|----------------|-------------------|
| Reservar direcciones IP fijas y delegar subdominios en AJO | Toda la reputación futura se vincula a estos elementos de infraestructura. | Vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Subdominios]**. [Más información](delegate-subdomain.md) |
| Configuración de SPF y DKIM | Confirma que el servidor de envío es legítimo y está autorizado. | Adobe lo gestiona automáticamente después de [delegar subdominios](delegate-subdomain.md) y [crear la configuración de canal](channel-surfaces.md). |
| Asegúrese de que el registro de DMARC esté configurado (p=ninguno) | Habilita los informes de autenticación de correo electrónico y las futuras políticas de aplicación. | Compruebe que el registro de DMARC esté configurado para todos los subdominios delegados. Al delegar un nuevo subdominio, puede configurar DMARC directamente en la interfaz. [Más información](dmarc-record.md) |
| Configuración de la monitorización de listas semilla | Detecta problemas de colocación de la bandeja de entrada al principio del proceso de calentamiento. | Añada las direcciones semilla al crear la configuración de canal. [Más información](seed-lists.md) |
| Generar audiencia de alta participación de fase 1 | Aumenta las métricas de participación temprana con los destinatarios más activos. | Cree una audiencia de menos de 5000 contactos que hayan abierto o hecho clic en los últimos 30 días. [Más información](../audience/creating-a-segment-definition.md) |

>[!CAUTION]
>
>Los problemas de autenticación (SPF, DKIM, DMARC) no se pueden resolver mediante la ampliación de volumen. Asegúrese de que estén correctamente configuradas antes de empezar a enviar.

## Muestra de calendario de calentamiento de cuatro semanas {#warmup-calendar}

Este calendario de ejemplo proporciona una rampa de volumen progresiva basada en el porcentaje del volumen diario final (UDV). Ajuste estos números para adaptarlos a los requisitos de envío específicos y trabaje con su consultor del equipo de entrega para crear un plan personalizado.

| Days | % de UDV | Público destinatario | Recomendaciones de contenido |
|------|----------|-----------------|------------------------|
| 1-3 | 0,5 % | Sus destinatarios más comprometidos | Utilice un formato de texto sin formato corto con una call-to-action clara encima del pliegue. |
| 4-7 | 1 % | Usuarios comprometidos más compradores recientes | Añada una imagen a pantalla completa ligera y limite los vínculos a 3 o menos. |
| De 8 a 14 | 5 % | Lista de suscriptores activos más amplia | Introduzca su plantilla de correo electrónico estándar, pero evite contenido promocional pesado. |
| 15-21 | 25 % | Suscriptores activos más ligeramente inactivos | Utilice contenido de marketing normal mientras supervisa de cerca las tasas de quejas. |
| 22-28 | 50-100 % | Lista completa (respetando listas de supresión) | Transición a su cadencia de envío en estado estacionario. |

## Uso de la función planes de calentamiento de IP {#ajo-warmup-feature}

Adobe Journey Optimizer incluye una característica optimizada de [planes de calentamiento de IP](ip-warmup-gs.md) que elimina la necesidad de limitar el volumen manualmente mediante configuraciones de recorrido complejas. Esta funcionalidad garantiza un enfoque estandarizado para crear la reputación del remitente.

### Funcionamiento

1. **Crear campañas de calentamiento de IP**: Cree una o más campañas con la opción **[!UICONTROL activación del plan de calentamiento de IP]** habilitada. [Más información](ip-warmup-campaign.md)

1. **Configure su plan**: Acceda a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Planes de calentamiento de IP]** y cargue su plantilla de calentamiento por fases preparada con su consultor de capacidad de envío. [Más información](ip-warmup-plan.md)

1. **Ejecutar fases**: Seleccione una campaña para cada fase y active las ejecuciones correspondientes. El sistema excluye automáticamente los perfiles de ejecuciones anteriores para evitar ponerse en contacto en exceso. [Más información](ip-warmup-execution.md)

1. **Supervisar y ajustar**: Use el tablero de informes consolidados para seguir el progreso, supervisar los estados de ejecución y modificar el plan si surgen problemas. [Más información](ip-warmup-execution.md#monitor-plan)

## Monitorización en tiempo real y métricas clave {#monitoring}

Adobe Journey Optimizer proporciona funciones de sistema de informes integradas para realizar un seguimiento del rendimiento de calentamiento de la IP:

* **Informes en vivo**: Acceda a la medición y visualización en tiempo real de sus campañas desde la pestaña **[!UICONTROL Últimas 24 horas]**. [Más información](../reports/campaign-live-report.md#email-live)

* **Informes de todo tiempo**: para obtener perspectivas más detalladas, aproveche Customer Journey Analytics para analizar datos de Adobe Experience Platform y crear visualizaciones personalizadas. [Más información](../reports/report-gs-cja.md)

### Métricas de Target

Monitorice estos indicadores de rendimiento clave durante el calentamiento:

| Métrica | Umbral de destino | Acción correctiva |
|--------|-----------------|-------------------|
| Tasa de quejas | ≤ 0,1 % | Si se supera, audite el segmento y elimine a los denunciantes crónicos. |
| Tasa de salida hacia otro sitio dura | ≤ 2 % | Si se excede, revise las prácticas de calidad e higiene de la lista. |
| Tasa de apertura | ≥ 10 % | Si es demasiado bajo, compruebe que está segmentando las audiencias que interactúan. |

## Guía de resolución de problemas {#troubleshooting}

Utilice esta matriz de decisión para abordar problemas comunes durante el calentamiento:

| Síntoma | Causa probable | Acción recomendada |
|---------|--------------|-------------------|
| Errores temporales de Yahoo (421 errores) | El volumen ha aumentado demasiado rápido | Pausar el envío durante 24 horas y luego reiniciar en el nivel anterior. |
| Tasa de apertura inferior al 2 % en las cuentas semilla | INCLUSIÓN EN LA LISTA DE BLOQUEADOS IP | Compruebe [Google Postmaster Tools](https://postmaster.google.com/) y [Microsoft SNDS](https://sendersupport.olc.protection.outlook.com/snds/); abra un ticket de envío si es necesario. |
| La tasa de quejas supera el 0,3% | Audiencia mal dirigida o antigua | Audite las definiciones de segmentos y excluya a los denunciantes crónicos de su [lista de supresión](manage-suppression-list.md). |

>[!IMPORTANT]
>
>Es mejor ralentizar el calentamiento que intentar reparar una reputación de remitente dañada más adelante. Priorice siempre el mantenimiento de métricas saludables sobre las rampas de volumen agresivas.

## Prácticas recomendadas posteriores al calentamiento {#post-warmup}

Una vez completado el plan de calentamiento, las métricas se han estabilizado:

* **Mantener consistencia**: Mantenga los aumentos de volumen diarios por debajo del 30% una semana tras otra para preservar su reputación establecida.

* **Supervisar continuamente**: Programe comprobaciones de estado de reputación trimestrales para identificar y abordar los problemas de forma proactiva.

* **Respetar señales de participación**: siga dando prioridad a los destinatarios comprometidos e implemente campañas de renovación de participación para suscriptores inactivos.

* **Mantener la autenticación actualizada**: compruebe periódicamente que los registros de SPF, DKIM y DMARC permanecen correctamente configurados.

## Puntos clave {#key-takeaways}

* El calentamiento de la **IP es esencial**: omitir el proceso de calentamiento cuesta más tiempo y reputación que el esfuerzo necesario para hacerlo correctamente.

* **Decisiones basadas en datos**: Rastree diariamente las tasas de quejas, rechazos y participación y ajuste su estrategia antes de que los ISP lo penalicen.

* **Autenticación primero, volumen segundo**: Resuelva todos los problemas de SPF, DKIM y DMARC antes de comenzar a aumentar el volumen.

* **La coherencia importa**: los proveedores de buzones de correo prefieren patrones de envío predecibles; evite picos de volumen repentinos o programaciones de envío irregulares.

<!--
>[!NOTE]
>
>For more guidance, explore the [Adobe Journey Optimizer Deliverability Guide blog post](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950).-->

## Temas relacionados {#related-topics}

* [Introducción a los planes de calentamiento de IP](ip-warmup-gs.md)
* [Creación de campañas de calentamiento de IP](ip-warmup-campaign.md)
* [Creación de un plan de calentamiento de IP](ip-warmup-plan.md)
* [Ejecución del plan de calentamiento de IP](ip-warmup-execution.md)
* [Creación de configuraciones de canal](channel-surfaces.md)
* [Delegar subdominios](delegate-subdomain.md)
* [Administrar lista de supresión](manage-suppression-list.md)
* [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=es)

