---
solution: Journey Optimizer
product: journey optimizer
title: Preguntas frecuentes sobre las integraciones
description: Preguntas frecuentes sobre las integraciones de Journey Optimizer para datos externos y contenido de mensajes.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: integración, preguntas frecuentes, datos externos, personalización
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 6dbdae6edd95d97e039565ed5c6e3cab9f4a19d8
workflow-type: tm+mt
source-wordcount: 877
ht-degree: 1%

---

# Preguntas frecuentes sobre las integraciones {#vendor-integration-faq}

>[!BEGINSHADEBOX]

**En esta página:** Encuentre respuestas a las preguntas más frecuentes acerca de Integraciones en Adobe Journey Optimizer, que abarcan configuración, autenticación, canales y formatos admitidos, permisos y solución de problemas.

>[!ENDSHADEBOX]

A continuación se muestran las preguntas más frecuentes sobre **integraciones** en Adobe Journey Optimizer.


## Introducción

+++ ¿Qué hacen las integraciones en Journey Optimizer?

Conecta fuentes de datos externas a Journey Optimizer para que pueda extraer contenido y datos de sistemas de terceros para incluirlos en campañas y recorridos, y personalizar mensajes con esos datos.

➡️ [Más información sobre la descripción general de las integraciones](integrations.md)

+++

+++ ¿Quién configura las integraciones y quién las utiliza en el contenido?

Los administradores crean y activan la configuración técnica (**[!UICONTROL Configuraciones]** > **[!UICONTROL Integraciones]** > **[!UICONTROL Administrar]** > **[!UICONTROL Crear integración]**). Los especialistas en marketing usan **[!UICONTROL Agregar personalización]** en los componentes Texto o HTML, abren **[!UICONTROL Integraciones]**, eligen una integración activa y asignan atributos.

➡️ [Más información sobre los flujos de trabajo de administradores y especialistas en marketing](integrations.md)

+++

+++ ¿Dónde se crean o administran integraciones en la interfaz de usuario como administrador?

Vaya a la sección **[!UICONTROL Configuraciones]** en el menú de la izquierda, abra **[!UICONTROL Administrar]** desde la tarjeta **[!UICONTROL Integraciones]** y, a continuación, seleccione **[!UICONTROL Crear integración]**.

➡️ [Más información sobre cómo crear una integración](integrations.md#configure)

+++

+++ ¿Cuáles son los casos de uso más comunes de las integraciones?

Algunos ejemplos son puntos de recompensa de sistemas de fidelidad, información sobre el precio de los productos, recomendaciones de motores de recomendación y actualizaciones logísticas como el estado de entrega.

➡️ [Más información sobre datos de ejemplo de sistemas de terceros](integrations.md)

➡️ [Más información sobre ejemplos de integración de proveedores](vendor-integration.md)

+++

## Configuración

+++ ¿Cómo configuro una integración de alto nivel como administrador?

Proporcione un nombre y una descripción, una dirección URL de extremo de API (opcionalmente con variables de ruta de acceso), valores de plantilla de ruta de acceso, **[!UICONTROL GET]** o **[!UICONTROL POST]**, encabezados y parámetros de consulta opcionales, un método de autenticación, configuración de directiva (como tiempo de espera y caché opcional o reintento), una respuesta JSON de ejemplo a los campos de asignación y, a continuación, ejecute **[!UICONTROL Enviar conexión de prueba]** y **[!UICONTROL Activar]** cuando sea válida.

➡️ [Más información sobre la configuración de la integración](integrations.md#configure)

+++

+++ ¿Qué tipos de autenticación se admiten?

Estos tipos de autenticación están disponibles: **[!UICONTROL Sin autenticación]**, **[!UICONTROL clave de API]**, **[!UICONTROL autenticación básica]** y **[!UICONTROL OAuth 2.0]** (con configuración de carga útil para OAuth cuando corresponda).

➡️ [Más información sobre los tipos de autenticación](integrations.md#configure)

+++

+++ ¿Para qué se utiliza el paso de carga útil de respuesta?

Pegue una respuesta JSON de muestra para que el sistema pueda detectar tipos de datos y pueda elegir qué campos se exponen para su personalización en los mensajes. Puede limitar qué campos están disponibles para los especialistas en marketing durante la creación.

➡️ [Más información sobre la asignación de carga útil de respuesta](integrations.md#configure)

+++

+++ ¿Cómo añaden los especialistas en marketing una integración a un mensaje?

En el contenido de la campaña o del recorrido, usa **[!UICONTROL Agregar personalización]** en un componente de texto o HTML, ve a **[!UICONTROL Integraciones]**, selecciona una integración y guarda. Con el modo Píldoras en el editor de personalización, puede asignar valores a variables de la configuración (como parámetros de encabezado o consulta o variables de ruta en la dirección URL).

➡️ [Más información sobre personalización con integraciones](integrations.md#personalization)

+++

## Capacidades y casos de uso

+++ ¿Puedo usar Integraciones en recorridos y campañas?

Sí. La característica está disponible tanto para recorridos como para campañas de **canales salientes** (por ejemplo, correo electrónico, SMS y push), dentro de los límites actuales del producto.

➡️ [Más información sobre recorridos y campañas](integrations.md#limitations)

+++

+++ ¿Puedo utilizar integraciones en fragmentos reutilizables?

La función Integraciones es compatible con Fragmentos.

➡️ [Más información sobre los fragmentos](aem-fragments-gs.md)

+++

## Limitaciones

+++ ¿Qué canales admiten integraciones?

Se admiten **canales salientes** (por ejemplo, correo electrónico, SMS y push).

➡️ [Más información sobre los canales admitidos](integrations.md#limitations)

+++

+++ ¿Qué formatos de respuesta de API son compatibles?

Para las respuestas de llamada de API, **JSON** y **HTML** son compatibles con la asignación de campos. La salida de imagen binaria sin procesar y los formatos que no son JSON no están disponibles para este flujo de trabajo.

➡️ [Más información sobre los formatos JSON y de respuesta](integrations.md#limitations)

+++

+++ ¿A qué patrones de API puedo conectarme?

Se admiten las API **Retrieval** destinadas a contenido específico. Las API **Listing** (lista amplia o patrones de paginación) no son compatibles con este modelo de integración.

➡️ [Más información sobre la recuperación en comparación con las API de listado](integrations.md#limitations)

+++

## Permisos y funciones relacionadas

+++ ¿Qué permisos necesito para configurar las integraciones?

Para empezar a usar integraciones, los usuarios deben tener los permisos **[!UICONTROL Administrar configuración de integración de AJO]** y **[!UICONTROL Ver configuración de integración de AJO]**.

➡️ [Más información sobre los permisos de las integraciones](integrations.md#overview)

+++

+++ ¿Las integraciones reemplazan los conectores de Adobe Journey Optimizer a las fuentes de Experience Platform?

No. **Las integraciones** son para campos de personalización en el contenido de mensajes que conduces desde las API. **Sources** y otras capacidades de ingesta de datos tienen diferentes propósitos (por ejemplo, ingesta de datos por lotes y enriquecimiento de perfiles). Utilice cada capacidad para el ámbito deseado.

➡️ [Más información sobre las integraciones para](integrations.md)

➡️ [Más información sobre orígenes de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=es){target="_blank"}

+++

## Solución de problemas

+++ ¿Por qué falla la conexión de prueba o permanece inválida?

Compruebe la dirección URL del extremo, el método HTTP, las plantillas de ruta, los encabezados y los parámetros de consulta, la autenticación y el tiempo de espera de la directiva. Use **[!UICONTROL Enviar conexión de prueba]** después de los ajustes. Para problemas de carga útil, asegúrese de que el ejemplo refleje un JSON válido y de que los campos seleccionados coincidan con lo que devuelve la API.

➡️ [Más información sobre la validación de la carga útil y la conexión de prueba](integrations.md#configure)

+++

+++ ¿Por qué los especialistas en marketing no ven mi integración en el selector?

Las integraciones deben **activarse** después de una prueba con éxito. Solo aparecen integraciones activas cuando los especialistas en marketing abren **[!UICONTROL Integraciones]**. Si la integración sigue siendo de borrador o está inactiva, complete primero la activación.

➡️ [Más información sobre la activación y la conexión de prueba](integrations.md#configure)

+++

## Proveedores externos

+++ ¿Qué ejemplos de proveedores están disponibles y quién protege la API?

Se puede integrar con cualquier plataforma de terceros que exponga un extremo de API compatible. Los patrones de proveedor **Illustrative** y los ejemplos de configuración pueden ayudarle a modelar API compatibles. La responsabilidad de garantizar los puntos finales recae en la plataforma de terceros y en su equipo.

➡️ [Más información sobre los procedimientos de integración de proveedores](vendor-integration.md)

+++
