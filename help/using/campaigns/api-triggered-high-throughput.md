---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 2%

---
El archivo no existe en el repositorio de canalización; es un archivo de documentación proporcionado como contexto. Escribiré el Markdown actualizado completo directamente como se indica (solo el archivo de salida, sin explicaciones).

---

solución: Journey Optimizer
producto: optimizador de recorrido
title: Activar el modo de alto rendimiento para campañas activadas por API
description: Aprenda a activar el modo de alto rendimiento para campañas activadas por API.
Función: Campañas, API
Tema: Administración de contenido
función: Desarrollador
level: Con experiencia
palabras clave: campañas, activadas por API, REST, optimizador, mensajes
exl-id: 2b3e87dc-097a-4d05-873c-f421d11338c3
TQID: https://experienceleague.adobe.com/SwmK1epuhZUf4EWnaLRHTBH-eE1hEV02Z8nqXGtMb6U
product_v2:
- id: cb954087-f4fc-4456-afb9-e939cabcdc79
internal-label: Journey Optimizer
feature_v2:
- id: d556b755-390a-43f0-be32-a08cf6236126
internal-label: Configuración
- id: a653cc2e-bc85-4353-a306-399e5b247978
internal-label: campañas de Journey Optimizer
subfeature_v2:
- id: f7479fa1-474b-479d-8c98-f6cee5865a38
internal-label: campañas activadas por API
- id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
internal-label: Administración de campañas
role_v2:
- id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label: Desarrollador
topic_v2:
- id: e0eb8757-182f-49f3-94a4-1587d16f5094
internal-label: Personalization
---
# Activación del modo de alto rendimiento para campañas activadas por API {#high-throughput}

>[!BEGINSHADEBOX]

**En esta página:** Active el modo de alto rendimiento para campañas activadas por API de modo que pueda enviar mensajes transaccionales en tiempo real a gran escala con un máximo de 5000 transacciones por segundo (correo electrónico) o hasta 1500 transacciones por segundo (push) sin depender de perfiles.

>[!ENDSHADEBOX]

El modo de alto rendimiento está diseñado para organizaciones que necesitan **mensajes transaccionales en tiempo real a gran escala**. A diferencia de las campañas activadas por API normales, las campañas de alto rendimiento funcionan de forma independiente de los perfiles de Adobe y requieren un modelo de configuración diferente.

Esta página explica cómo las campañas de alto rendimiento difieren de las campañas activadas por API estándar, los requisitos de configuración y cuándo elegir cada modo.

## Protecciones y limitaciones

* **Acceso**: disponible solo en la región de EE. UU. para organizaciones con licencia con el complemento de mensajería transaccional de alto rendimiento.

* **Canales**: disponibles para notificaciones push y por correo electrónico.

* **Rendimiento**:

   * **Correo electrónico**: hasta 5000 transacciones por segundo.
   * **Push**: hasta 1500 transacciones por segundo. Los siguientes niveles de rendimiento por niveles están disponibles: 500 TPS (base), 1000 TPS y 1500 TPS. Los niveles más altos requieren el derecho de complemento adecuado.

* **Personalization**:

   * Toda personalización debe incluirse en la carga útil de la API como **datos contextuales**. [Aprenda a personalizar el contenido mediante datos contextuales](../campaigns/api-triggered-campaign-content.md#contextual)
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
| **Rendimiento** | Hasta 500 transacciones por segundo | Hasta 5000 TPS (correo electrónico); hasta 1500 TPS (push) |
| **Canales** | Correo electrónico, SMS, push | Correo electrónico, push |
| **Personalización** | Perfil + contextual en la carga útil de API | Solo contextual en la carga útil de API |
| **Perfil y vinculación** | Existe o se crea con eventos vinculados al perfil | Sin perfil |
| **Volumen de mensajes** | Paquetes de mensaje y asignación de derechos estándar | Volúmenes de mensajes por niveles independientes |
| **Infraestructura** | Estándar | Mejorado |
| **Tiempo de actividad** | 99,9% | 99,99% |
| **API de comprobación de estado** | Sí | Sí |

En otras palabras:

* Elija **API estándar desencadenada** campañas si:
   * No tiene contratado un rendimiento alto.
   * Sus necesidades de rendimiento son ≤500 TPS.
   * Necesita una personalización basada en Perfiles de Adobe.
   * Desea vincular los datos de campaña a los perfiles para una futura segmentación.
   * Necesitas mensajes SMS.

* Elija **Alto rendimiento** campañas si:
   * Necesita rendimiento > 500 TPS.
   * No es necesario vincular perfiles.
   * Puede pasar toda la personalización en la carga útil de la API.
   * Desea utilizar el canal de correo electrónico o push.

## Directrices de configuración

Para configurar correctamente las campañas de alto rendimiento, siga estas directrices:

1. **Solo para correo electrónico con alto rendimiento** - Cree un nuevo grupo de IP. [Aprenda a crear grupos de IP](../configuration/ip-pools.md)
1. Cree una nueva configuración de canal. [Aprenda a configurar las configuraciones de canal](../configuration/channel-surfaces.md)
1. Póngase en contacto con el Servicio de atención al cliente de Adobe para solicitar que la superficie activada se asigne a la capacidad Alto rendimiento. Proporcione la configuración del canal y los detalles del grupo de IP (para correo electrónico) junto con su ID de organización.

>[!IMPORTANT]
>
>Las configuraciones de canal designadas para los mensajes transaccionales de alto rendimiento deben utilizarse exclusivamente con ese fin y no con la mensajería transaccional estándar que utiliza campañas o recorridos activados por API. Para el alto rendimiento del correo electrónico, el grupo de IP designado para este fin también debe utilizarse exclusivamente para el envío de alto rendimiento.