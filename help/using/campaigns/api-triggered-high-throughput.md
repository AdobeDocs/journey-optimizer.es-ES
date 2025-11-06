---
solution: Journey Optimizer
product: journey optimizer
title: Activación del modo de alto rendimiento para campañas activadas por API
description: Obtenga información sobre cómo activar el modo de alto rendimiento para campañas activadas por API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campañas, activadas por API, REST, optimizador, mensajes
source-git-commit: 4521990a02092365f996a81299ada55433639fb7
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 4%

---


# Activación del modo de alto rendimiento para campañas activadas por API {#high-throughput}

El modo de alto rendimiento está diseñado para organizaciones que necesitan **mensajes transaccionales en tiempo real a gran escala** (hasta 5000 transacciones por segundo). A diferencia de las campañas activadas por API normales, las campañas de alto rendimiento funcionan de forma independiente de los perfiles de Adobe y requieren un modelo de configuración diferente.

Esta página explica cómo las campañas de alto rendimiento difieren de las campañas activadas por API estándar, los requisitos de configuración y cuándo elegir cada modo.

## Mecanismos de protección y limitaciones

* **Acceso**: disponible solo en la región de EE. UU. para organizaciones con licencia con el complemento de mensajería transaccional de alto rendimiento.

* **Canales**: Actualmente solo está disponible para correo electrónico.

* **Personalization**:

   * Toda personalización debe incluirse en la carga útil de la API como **datos contextuales**. [Aprenda a personalizar el contenido mediante datos contextuales](../campaigns/api-triggered-campaign-action.md#contextual)
   * No se admite la personalización basada en perfiles. Si se utilizan variables de perfil, se producirán errores de validación.

* **Configuraciones de canal personalizadas**: las configuraciones de canal que usan la [personalización basada en perfiles](../email/surface-personalization.md) no se pueden usar con campañas de alto rendimiento. Solo se pueden utilizar superficies sin personalización de perfil.

* **Extremo de API**: las campañas de alto rendimiento utilizan un extremo diferente que las campañas estándar activadas por API. Para obtener más información, consulte [Ejecutar una campaña desencadenada por API](../campaigns/trigger-campaigns.md#trigger).

* **Exclusividad de la campaña**: las campañas de alto rendimiento no utilizan perfiles de Adobe. Los mensajes se envían independientemente de si existe o no un perfil.

  Además, una campaña no se puede usar en casos de uso con y sin perfil. Si necesita ambas, cree dos campañas independientes y asegúrese de que el sistema de llamada decida cuál almacenar en déclencheur en función del contexto.

* **Conjuntos de datos para comentarios y seguimiento**: los datos de comentarios y seguimiento de las campañas de alto rendimiento se almacenan en conjuntos de datos dedicados que no están habilitados para perfiles. Como resultado, estos eventos no se vinculan a perfiles, aunque exista un perfil coincidente.

  Los conjuntos de datos utilizados son:

   * **Conjunto De Datos De Evento De Comentarios De Mensajes De AJO - Sin Perfil**
   * **Conjunto de datos de evento de experiencia de seguimiento de correo electrónico de AJO - Sin perfil**

* **Asignación de rendimiento**: el rendimiento aprovisionado en el complemento Alto rendimiento está reservado exclusivamente para las campañas de alto rendimiento. No se comparte el rendimiento entre las campañas estándar y las activadas por la API de alto rendimiento.

## Elección entre campañas de rendimiento estándar y campañas de alto rendimiento

Utilice esta tabla para decidir qué tipo de campaña activada por API se adapta a su caso de uso:

| Función/requisito | Campaña activada por API estándar | Campaña de alto rendimiento |
|------------------------|---------------------------------|---------------------------|
| **Disponibilidad** | Incluido en la oferta base | Requiere un complemento de mensajería transaccional de alto rendimiento. |
| **Rendimiento** | Hasta 500 transacciones por segundo | Hasta 5000 transacciones por segundo |
| **Canales** | Correo electrónico, SMS, push | Correo electrónico |
| **Personalización** | Perfil + contextual en la carga útil de API | Solo contextual en la carga útil de API |
| **Perfil y vinculación** | Existe o se crea con eventos vinculados al perfil | Sin perfil |
| **Volumen de mensajes** | Paquetes de mensaje y asignación de derechos estándar | Volúmenes de mensajes por niveles independientes |
| **Infraestructura** | Estándar | Mejorado |
| **Tiempo de actividad** | 99,9 % | 99,99 % |
| **API de comprobación de estado** | Sí | Sí |

En otras palabras:

* Elija **API estándar desencadenada** campañas si:
   * No tiene contratado un alto rendimiento.
   * Sus necesidades de rendimiento son &lt;500 TPS.
   * Necesita una personalización basada en Perfiles de Adobe.
   * Desea vincular los datos de campaña a los perfiles para una futura segmentación.
   * Desea utilizar otro canal que no sea Correo electrónico.

* Elija **Alto rendimiento** campañas si:
   * Necesita rendimiento > 500 TPS.
   * No es necesario vincular perfiles.
   * Puede pasar toda la personalización en la carga útil de la API.
   * Desea utilizar el canal de correo electrónico.

## Directrices de configuración

Para configurar correctamente las campañas de alto rendimiento, siga estas directrices:

1. Cree un nuevo grupo de IP. [Aprenda a crear grupos de IP](../configuration/ip-pools.md)
1. Cree una nueva configuración de canal. [Aprenda a configurar las configuraciones de canal](../configuration/channel-surfaces.md)
1. Póngase en contacto con el Servicio de atención al cliente de Adobe para solicitar que la superficie activada se asigne a la capacidad Alto rendimiento. Proporcione la configuración del canal y los detalles del grupo de IP junto con su ID de organización.

>[!IMPORTANT]
>
>Las configuraciones de grupo de IP y canal designadas para los mensajes transaccionales de alto rendimiento deben utilizarse exclusivamente con ese fin y no con la mensajería transaccional estándar que utiliza campañas o recorridos activados por API.
