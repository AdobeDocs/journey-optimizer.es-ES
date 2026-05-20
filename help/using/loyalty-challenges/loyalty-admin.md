---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del programa de fidelización
description: Aprenda a configurar proveedores de recompensas, definiciones de eventos y configuraciones de organización para su programa de fidelidad en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: e66628ab1d9df497226ab625947aa18a2a3b6f48
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 2%

---

# Configuración del programa de fidelización {#loyalty-admin}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](get-started.md)
* [Acceder y administrar desafíos y tareas](access-loyalty-challenges.md)
* [Crear desafíos](create-challenges.md)
* [Creación de tareas](create-tasks.md)
* [Monitorización del rendimiento del desafío de fidelidad](loyalty-reporting.md)
* **Configurar el programa de fidelización** ◀︎ **Usted está aquí**
* [Referencia de API de retos de fidelización](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta privada**. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](../rn/releases.md).

En la sección **[!UICONTROL Administrador de fidelidad]**, los administradores configuran cómo se conecta Journey Optimizer al servidor del programa de fidelidad. Los especialistas en marketing utilizan **[!UICONTROL Desafíos de fidelidad (Beta)]** para diseñar desafíos, tareas, contenido y mensajería. El administrador de fidelidad es una configuración única e independiente para el cumplimiento de recompensas y la asignación de eventos.

Cuando un cliente completa un desafío (o alcanza un hito de recompensa), Journey Optimizer llama al proveedor de recompensas que configuró aquí para entregar puntos u otras recompensas. La configuración del desafío **[!UICONTROL Contenido]**, **[!UICONTROL Mensajería]** y **[!UICONTROL Audiencia]** no se ve afectada por la configuración de la administración de fidelización.

## Acceso a administrador de fidelización {#access-loyalty-admin}

Para abrir Administración de fidelización, inicia sesión en Journey Optimizer y selecciona **[!UICONTROL Administración de fidelización]** en el panel de navegación izquierdo.

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

La interfaz de administración está organizada en pestañas. Según su organización, es posible que vea **[!UICONTROL Configuración global]**, **[!UICONTROL Proveedores de recompensas]**, **[!UICONTROL Definiciones de eventos]** y **[!UICONTROL Inventario de productos]**.

## Configuración global {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Configuración global"
>abstract="Seleccione el área de nombres de identidad de Adobe Experience Platform para su programa de fidelidad y copie su ID de configuración. Esta configuración a nivel de organización es necesaria para que los proveedores de recompensas puedan entregar las recompensas correctamente."

Use **[!UICONTROL Configuración global]** para configurar las opciones de toda la organización para los Desafíos de fidelidad.

1. Abra la ficha **[!UICONTROL Configuración global]**.

1. En la lista desplegable **[!UICONTROL Área de nombres]**, seleccione el [área de nombres de identidad](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces) de Adobe Experience Platform que utiliza su programa de fidelidad. Seleccione **[!UICONTROL Guardar]** para actualizar el área de nombres en la configuración de Retos de fidelidad de su organización.

1. Copie el **[!UICONTROL ID de configuración]** si necesita compartirlo con su equipo de implementación o sistemas externos.

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## Proveedores de recompensa {#reward-providers}

Un **proveedor de recompensas** le dice a Journey Optimizer dónde enviar llamadas de cumplimiento cuando se registra el progreso del desafío o se completa un desafío; por ejemplo, una API que acredita puntos de lealtad o estrellas a una cuenta de miembro.

Un proveedor de recompensas incluye:

* Detalles básicos de conexión (nombre, descripción, dirección URL de la API, encabezados)
* **[!UICONTROL Definiciones de recompensa]**: tipos de recompensa que este proveedor puede emitir (por ejemplo, estrellas o millas)
* **[!UICONTROL Proxies de recompensa]** (opcional): enrute las llamadas a través de un proxy en lugar de directamente al extremo
* **[!UICONTROL Generadores de tokens de autenticación]**: cómo obtiene Journey Optimizer los tokens de acceso antes de llamar a su API

### Crear un proveedor de recompensas {#create-reward-provider}

Siga estos pasos para registrar un nuevo proveedor de recompensas y sus recursos relacionados.

1. Abra la pestaña **[!UICONTROL Proveedores de recompensas]** y empiece a crear un proveedor.

1. Escriba **[!UICONTROL Name]** y **[!UICONTROL Description]**, y después la **[!UICONTROL URL de API]** a la que se enviarán las solicitudes de cumplimiento.

1. Agregue **[!UICONTROL encabezados]** según sea necesario para su API (por ejemplo, claves de API o tipos de contenido). Puede agregar o quitar filas de encabezado en la interfaz de usuario.

1. Configurar **[!UICONTROL definiciones de recompensa]**:

   * Defina cada tipo de recompensa que admite su proveedor (por ejemplo, puntos de programa o estrellas).
   * Opcionalmente, marque una definición como **default** para ese proveedor.
   * Especifique la **carga útil** enviada con las llamadas de cumplimiento para cada definición.

1. Si lo desea, configure un **[!UICONTROL proxy de recompensa]**:

   * **[!UICONTROL Host]**, **[!UICONTROL Puerto]** y credenciales
   * **[!UICONTROL Nombre]**, **[!UICONTROL Descripción]** y si el proxy está **habilitado**

1. Configure un **[!UICONTROL generador de tokens de autenticación]** si su API requiere un token antes de cada llamada:

   * URL de extremo de token y método HTTP (por ejemplo, **POST** para flujos de estilo OAuth)
   * **[!UICONTROL Clave de token]** en la respuesta (por ejemplo, `access_token`)
   * Encabezados requeridos por el extremo del token

   Journey Optimizer solicita un token de esta configuración antes de llamar a su API de recompensa, de modo que las llamadas utilizan una credencial actual.

1. Seleccione **[!UICONTROL Crear proveedor de recompensas]**. El proveedor y sus recursos secundarios (definiciones, proxy y generador de tokens) se crean juntos.

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

Después de la creación, el proveedor aparece en la lista de proveedores de recompensas. Los especialistas en marketing seleccionan este proveedor al [configurar las recompensas por desafío](create-challenges.md#rewards).

### Editar un proveedor de recompensas {#edit-reward-provider}

1. Abra la pestaña **[!UICONTROL Proveedores de recompensas]** y seleccione un proveedor.

1. Actualice el nombre, la descripción, la dirección URL o los encabezados del proveedor según sea necesario.

1. Para cambiar **[!UICONTROL definiciones de recompensa]**, **[!UICONTROL proxies de recompensa]** o **[!UICONTROL generadores de tokens de autenticación]**, abra la sección correspondiente y edite los campos. Los cambios en estos recursos secundarios se guardan al actualizarlos.

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>Para los desafíos de **[!UICONTROL Trae tus propios datos]** donde las tareas y las recompensas provienen por completo de tu integración de datos, es posible que los proveedores de recompensas configurados aquí no apliquen. [Más información sobre los desafíos que plantea el incorporar tus propios datos](create-challenges.md#create-the-challenge).

## Definiciones de eventos {#event-definitions}

**[!UICONTROL Definiciones de eventos]** asigna eventos de experiencia entrantes en el formato de tu marca a actividades que los Desafíos de fidelidad pueden usar, especialmente las tareas de **[!UICONTROL Evento personalizado]**. Cuando llegan los datos de sus canales, Journey Optimizer utiliza estas definiciones para decidir si un evento es relevante y cómo interpretarlo. Los eventos que no coinciden con ninguna definición se omiten.

### Creación de una definición de evento {#create-event-definition}

1. Abra la ficha **[!UICONTROL Definiciones de eventos]** y cree una nueva definición.

1. Escriba un **[!UICONTROL Nombre]** para el evento (por ejemplo, `Coffee purchase`). Este nombre es lo que los especialistas en marketing seleccionan cuando configuran una tarea de **[!UICONTROL Custom event]**.

1. Especifique cómo identificar el evento en las cargas útiles entrantes:

   * **[!UICONTROL Ruta de identificador]** — Ruta de acceso JSON al campo que identifica el evento o miembro (por ejemplo, `data.memberId`)
   * **[!UICONTROL Valores de identificador]**: valores que deben estar presentes para que esta definición coincida

1. Opcionalmente, especifique un ID de esquema **[!UICONTROL XDM]** o use los campos **[!UICONTROL Esquema]** y **[!UICONTROL Transformador]** para pegar las cadenas de esquema y transformación que su equipo usa para analizar y validar el JSON entrante antes de procesarlo.

   Puede proporcionar un ID de esquema XDM, una ruta de identificador o ambos, según la estructura de los eventos.

1. Guarde la definición del evento.

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

La mayoría de las organizaciones crean varias definiciones de eventos, una por cada actividad que desean rastrear (por ejemplo, compras, registros o visitas al sitio). [Aprenda a utilizar tareas de eventos personalizados en desafíos](create-tasks.md#choose-activity).

## Inventario de productos {#product-inventory}

La pestaña **[!UICONTROL Inventario de productos]** le permite cargar un archivo CSV para asignar identificadores de productos o artículos (por ejemplo, ID de MPG) a grupos de productos utilizados en la elegibilidad de tareas. Esto es compatible con escenarios en los que las tareas hacen referencia a productos agrupados en lugar de SKU individuales escritas manualmente.

1. Abra la ficha **[!UICONTROL Inventario de productos]**.

1. Cargue el archivo de asignación arrastrándolo al área de carga o explorando para seleccionarlo.

1. Revise las asignaciones importadas en la lista de inventario. Seleccione un grupo de productos para ver todos los elementos de ese grupo. Utilice la búsqueda para buscar elementos por nombre o ID.

1. Use **[!UICONTROL Historial de cargas]** para ver las cargas anteriores.

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>**[!UICONTROL Exclusiones globales]** para el inventario de productos está planificado para una versión futura y no está documentado aquí.

## Relación entre el administrador de fidelización y los desafíos {#how-admin-relates-to-challenges}

| Área | Configurado en la administración de fidelización | Configurado en retos de fidelización |
|------|----------------------------|----------------------------------|
| API de satisfacción de recompensas | Sí, proveedores de recompensas | No: seleccionar proveedor e importes solamente |
| Asignación de eventos para actividades personalizadas | Sí: definiciones de eventos | No: seleccionar el nombre del evento en las tareas de eventos personalizados |
| Asignaciones de grupos de productos | Sí: inventario de productos | No: utilizar grupos al crear tareas de compra/gasto |
| Estructura, contenido y audiencia del desafío | No | Sí |

Orden de configuración típico:

1. Configure **[!UICONTROL Configuración global]** y al menos un **[!UICONTROL Proveedor de recompensas]** en la administración de fidelidad.
1. Opcionalmente, puede agregar **[!UICONTROL definiciones de eventos]** e **[!UICONTROL inventario de productos]** si su programa utiliza eventos personalizados o grupos de productos basados en CSV.
1. Cree [tareas](create-tasks.md) y [desafíos](create-challenges.md) en **[!UICONTROL Desafíos de fidelidad (Beta)]**, seleccionando el proveedor de recompensas y las definiciones que configuró.

Adobe Journey Optimizer envía llamadas de cumplimiento a su proveedor cuando los clientes obtienen recompensas; su plataforma de fidelidad es la propietaria del abono en la cuenta del miembro.

## Requisitos previos {#prerequisites}

El administrador de fidelización está diseñado para un pequeño conjunto de administradores de su organización. Además de los permisos necesarios para [Desafíos de fidelidad](get-started.md#prerequisites), necesita acceso para configurar los ajustes de fidelidad en el nivel de organización.

Póngase en contacto con el administrador si **[!UICONTROL Administrador de fidelización]** no aparece en la navegación izquierda o si no puede guardar la configuración global o los proveedores de recompensas.
