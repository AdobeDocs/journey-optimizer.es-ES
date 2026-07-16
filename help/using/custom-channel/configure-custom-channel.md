---
title: 'Configuración de un canal personalizado: información general'
description: Conozca los pasos que debe seguir un administrador para configurar un canal personalizado en Adobe Journey Optimizer, desde la creación del canal hasta la configuración de un canal.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 4556e8b50fe71cf9d703d034a3c5772b8fea9d33
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 9%

---


# Configuración de un canal personalizado {#custom-channel-configuration}

>[!AVAILABILITY]
>
>Esta funcionalidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

La configuración de un canal personalizado es una tarea del administrador que se produce una vez por canal. Una vez configurado el canal, los especialistas en marketing pueden seleccionarlo inmediatamente en campañas, recorridos y campañas orquestadas, igual que cualquier canal [!DNL Journey Optimizer] nativo.

El proceso de configuración cubre cuatro pasos: definir el canal en sí (punto de conexión, autenticación, carga útil), administrar las credenciales de API utilizadas para autenticar solicitudes, delegar opcionalmente un subdominio para el seguimiento de vínculos y, finalmente, crear una configuración de canal que los especialistas en marketing seleccionarán en el momento de la creación.

>[!NOTE]
>
>Antes de empezar, revise los requisitos previos y las protecciones de los canales personalizados, incluidos los permisos necesarios y los métodos de autenticación admitidos.

## Pasos de configuración {#steps}

El proceso de configuración de un canal personalizado consta de cuatro pasos. Cada paso se describe en detalle en los artículos vinculados a continuación.

| Paso | Lo que haces | Por qué importa | Vínculo |
| --- | --- | --- | --- |
| **1. Crear el canal personalizado** | Defina la URL del punto de conexión, los encabezados, la política de regulación, el tipo de autenticación y la estructura de carga útil de mensajes en el Generador de canales. | Esta es la definición principal del canal. Indica a [!DNL Journey Optimizer] cómo enviar un mensaje y cómo se ve ese mensaje. | [Más información](create-custom-channel.md) |
| **2. Administrar credenciales de API** | Cree y administre los conjuntos de credenciales utilizadas para autenticar solicitudes en el extremo. | Varios conjuntos de credenciales le permiten reutilizar la misma definición de canal en diferentes marcas o entornos sin duplicar el canal. | [Más información](custom-channel-api-credentials.md) |
| **3. Delegar un subdominio** *(opcional)* | Delegue un subdominio específicamente para su canal personalizado. | Solo es necesario si la carga útil del mensaje contiene vínculos a los que se puede realizar un seguimiento. Sin un subdominio delegado, el seguimiento de vínculos no está disponible para este canal. | [Más información](custom-channel-subdomains.md) |
| **4. Crear una configuración de canal** | Cree un ajuste preestablecido con nombre que vincule el canal personalizado a un conjunto específico de credenciales, un subdominio y valores predeterminados de carga útil opcionales. | Al crear campañas o recorridos, los especialistas en marketing seleccionan un canal personalizado y una configuración de canal asociada. Puede crear varias configuraciones para el mismo canal (por ejemplo, una por marca o región). | [Más información](custom-channel-configuration.md) |

<!--
## Get started {#get-started}

1. [Create the custom channel](create-custom-channel.md) by defining its endpoint, authentication method, and message payload structure in the Channel Builder.
1. [Set up API credentials](custom-channel-api-credentials.md) to authenticate requests sent to your endpoint — required for all authentication types other than **None**.
1. [Delegate a subdomain](custom-channel-subdomains.md) if your message payload includes trackable links and you want them served from a branded domain.
1. [Create a channel configuration](custom-channel-configuration.md) to produce the named preset that marketers will select when building campaigns and journeys.


-->