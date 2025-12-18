---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los conectores de fuentes en Journey Optimizer
description: Obtenga información sobre cómo introducir datos de fuentes externas en Adobe Journey Optimizer
feature: Integrations, Data Ingestion
role: User
level: Beginner
exl-id: 359ea3c6-7746-469e-8a24-624f9726f2d8
source-git-commit: 52b58d18cdbbff79f4dcb7af2817b178a4a0b429
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 11%

---

# Introducción a los conectores de fuentes {#sources-gs}

## ¿Qué es una fuente? {#what-is-source}

Un **origen** es un conector que lleva datos externos a Adobe Journey Optimizer. Las fuentes le permiten importar información de clientes desde sistemas que ya utiliza, como plataformas CRM, almacenamiento en la nube o bases de datos, y hacer que los datos estén disponibles para crear recorridos personalizados de clientes.

Considere las fuentes como puentes entre Journey Optimizer y sus sistemas de datos externos. Sincronizan los datos automáticamente para que siempre tenga información de clientes actualizada para impulsar sus campañas de marketing.

## Por qué importan las fuentes {#why-sources-matter}

Las fuentes son esenciales para crear experiencias de cliente personalizadas y basadas en datos en Journey Optimizer. He aquí la razón:

* **Vista unificada del cliente**: combine datos de varios sistemas para ver la imagen completa de cada cliente
* **Personalización en tiempo real**: use datos nuevos para enviar mensajes relevantes y oportunos en sus recorridos
* **Sincronización automática de datos**: mantenga actualizada la información del cliente sin importar manualmente los datos
* **Flujos de trabajo eficientes**: conéctese una vez y los datos fluirán automáticamente a sus recorridos

Por ejemplo, puede utilizar fuentes para importar el historial de compras desde su plataforma de comercio electrónico y, a continuación, crear recorridos que envíen recomendaciones de productos personalizadas basadas en lo que han comprado los clientes.

## Qué puede hacer con las fuentes {#sources-use-cases}

Los casos de uso comunes de las fuentes en Journey Optimizer incluyen:

* **Importar datos de clientes desde sistemas CRM** - Sincronizar información de contacto, preferencias e historial de participación desde plataformas como Salesforce o Microsoft Dynamics
* **Conectar datos de compra** - Incorporar el historial de pedidos y las preferencias de productos de las plataformas de comercio electrónico para personalizar las ofertas
* **Integrar datos del programa de fidelidad**: puntos de acceso e información de nivel para recompensar a los clientes más comprometidos
* **Sincronizar datos de comportamiento**: importe interacciones con sitios web y patrones de uso de aplicaciones para almacenar en déclencheur recorridos relevantes
* **Actualizar atributos de perfil**: mantenga los perfiles de los clientes actualizados con los datos del almacenamiento o las bases de datos en la nube

## Tipos de fuentes comunes {#source-types}

Journey Optimizer admite varios tipos de fuentes para conectarse con los sistemas existentes:

**aplicaciones de Adobe:**
* Adobe Analytics
* Adobe Audience Manager
* Adobe Campaign
* Adobe Commerce

**Almacenamiento en la nube:**
* Amazon S3
* Azure Blob Storage
* Almacenamiento en la nube de Google
* SFTP

**Bases de datos:**
* Amazon Redshift
* Google BigQuery
* Microsoft SQL Server
* MySQL
* PostgreSQL

**Automatización de marketing y CRM:**
* Microsoft Dynamics
* Salesforce
* Marketing Cloud de Salesforce

➡️ Ver la lista completa en el [catálogo de orígenes Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html#sources-catalog){target="_blank"}

## Antes de empezar {#prerequisites}

Antes de configurar las fuentes, asegúrese de lo siguiente:

* **Permisos adecuados** - Acceso para administrar orígenes en Adobe Experience Platform
* **Credenciales del sistema de Source**: detalles de autenticación del sistema externo al que desea conectarse
* **Comprensión de los datos**: Sepa qué campos de datos necesita y cómo se asignan a los perfiles de Journey Optimizer

➡️ Más información acerca de [control de acceso y permisos](../../administration/permissions.md)

## Cómo funcionan las fuentes {#how-sources-work}

Adobe Journey Optimizer utiliza el marco de trabajo de fuentes de Adobe Experience Platform. Este es el flujo de trabajo básico:

1. **Conectar**: configure la autenticación en su sistema de datos externo
2. **Seleccionar datos**: elija qué datos importar y con qué frecuencia sincronizar
3. **Asignar campos**: defina cómo se corresponden los campos de datos externos con los atributos de perfil de Journey Optimizer
4. **Programación** - Configurar intervalos de actualización automática de datos
5. **Supervisar**: efectúe el seguimiento del flujo de datos y resuelva los problemas de sincronización

Una vez configuradas, las fuentes se ejecutan automáticamente en segundo plano, lo que mantiene los datos de los clientes frescos y listos para usarlos en los recorridos.

## Más información {#learn-more}

![](assets/sources-home.png)

Vea este vídeo para comprender los conectores de origen y cómo configurarlos en Journey Optimizer:

>[!VIDEO](https://video.tv.adobe.com/v/335919?quality=12)

Para obtener información detallada sobre cómo configurar y administrar orígenes, consulte la [documentación de orígenes de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=es){target="_blank"}.

## Próximos pasos {#next-steps}

Ahora que comprende cuáles son las fuentes y por qué son importantes:

* Explore el [catálogo de fuentes](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html#sources-catalog){target="_blank"} para encontrar conectores para sus sistemas
* Aprenda a [crear una conexión de origen](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/overview.html){target="_blank"}
* Comprender la [asignación y transformación de datos](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/overview.html){target="_blank"}
* Ver cómo [usar datos importados en recorrido](../building-journeys/journey-gs.md)
