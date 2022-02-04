---
title: Delegación de subdominios en [!DNL Journey Optimizer]
description: Obtenga información sobre cómo delegar subdominios
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: e5ebf038565329fdaa7b01a12042c2c4bba79f37
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 35%

---

# Delegación de subdominios en [!DNL Journey Optimizer] {#subdomain-delegation}

La creación de un subdominio para campañas de correo electrónico permite a las marcas aislar distintos tipos de tráfico (marketing frente a empresa, por ejemplo) en grupos de IP específicos y con dominios específicos, lo que acelera el proceso de calentamiento de IP y mejora la capacidad de envío en general. Si comparte un dominio y este se bloquea o añade a la lista de bloqueados, podría afectar a la entrega de correo empresarial. Sin embargo, los problemas de reputación o los bloques de un dominio específico de las comunicaciones de marketing por correo electrónico solo afectarán a ese flujo de correo electrónico. El uso del dominio principal como remitente o dirección &quot;De&quot; para varios flujos de correo también podría dañar la autenticación por correo electrónico, lo que bloquearía los mensajes o colocarlos en la carpeta de correo no deseado.

>[!NOTE]
>
>No puede utilizar el mismo dominio de envío para enviar mensajes desde [!DNL Adobe Journey Optimizer] y de otro producto, como [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage].

## ¿Por qué configurar subdominios?  {#why-setting-up-subdomains}

Un subdominio es una división de su dominio que puede utilizarse para aislar sus marcas o varios tipos de tráfico, por ejemplo, mensajes transaccionales y comunicaciones de marketing.

Veamos el ejemplo del dominio &quot;mybrand.com&quot;, que se utiliza para enviar comunicaciones transaccionales y de marketing. En este caso, puede configurar dos subdominios:

* subdominio &quot;info.mybrand.com&quot; para comunicaciones transaccionales (confirmación de compras, restablecimiento de contraseña, etc.),
* Subdominio &quot;marketing.mybrand.com&quot; para correos electrónicos de prospección.

Al hacerlo, ayudará a preservar la reputación de su dominio y otros subdominios. Por ejemplo: si los subdominios &quot;marketing.mybrand.com&quot; terminan en la lista de bloqueados de los proveedores de servicios de Internet debido a la mala capacidad de entrega, esto impedirá que todo el dominio &quot;mybrand.com&quot; y el subdominio &quot;info.mybrand.com&quot; terminen en la lista de bloqueados.

Al implementar una solución, existen requisitos para componentes externos: estas incluyen la configuración de vínculos y páginas web para rastrear, la visualización de páginas espejo, etc.

Aunque estos requisitos se administran a través de componentes alojados tanto por Adobe como por el cliente, incluyen direcciones URL que pueden ver los destinatarios de los correos electrónicos. Para evitar tener direcciones URL que indiquen la solución técnica subyacente o el proveedor de alojamiento, se pueden configurar subdominios para que esto sea transparente para los destinatarios de los correos electrónicos.

**Más información**

* Obtenga información sobre cómo [delegar subdominios](delegate-subdomain.md) directamente desde la interfaz
* Obtenga información sobre cómo [añadir registros TXT de Google](google-txt.md) a los subdominios para garantizar el envío correcto de correos electrónicos a las direcciones de Gmail
* Obtenga información sobre cómo [acceder a los registros PTR](ptr-records.md) generado para los subdominios, lo que permite que se verifiquen enviando servidores de correo

## Métodos de configuración de subdominios {#subdomain-delegation-methods}

La configuración del subdominio le permite configurar una subsección de su dominio (técnicamente, una &quot;zona DNS&quot;) para usarla con Adobe Campaign. Los métodos de configuración disponibles son estos:

* **Delegación de subdominios completa en Adobe** (recomendado): el subdominio se delega completamente a Adobe. Adobe puede controlar y mantener todos los aspectos de DNS necesarios para enviar, procesar y rastrear mensajes. [Más información sobre la delegación de subdominios completa](delegate-subdomain.md#full-subdomain-delegation)

* **Uso de CNAME**: Cree un subdominio y utilice CNAME para señalar registros específicos de Adobe. Con esta configuración, tanto usted como el Adobe comparten la responsabilidad de mantener DNS. [Más información sobre la delegación de subdominios CNAME](delegate-subdomain.md#cname-subdomain-delegation)

En el cuadro que figura a continuación se ofrece un resumen del funcionamiento de estos métodos, así como el nivel de esfuerzo que suponen:

| Método de configuración | Funcionamiento | Nivel de esfuerzo |
|---|---|---|
| **Delegación completa** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe configurará todos los registros DNS necesarios para Adobe Campaign.<br/><br/>En esta configuración, Adobe es totalmente responsable de administrar el subdominio y todos los registros DNS. | Bajo |
| **CNAME, método personalizado** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe proporcionará los registros que se van a colocar en los servidores DNS y configurará los valores correspondientes en los servidores DNS de Adobe Campaign.<br/><br/>En esta configuración, tanto usted como Adobe comparten la responsabilidad de mantener DNS. | Alto |

Encontrará información adicional sobre la configuración de dominios en [esta documentación](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

Si tiene alguna pregunta sobre los métodos de configuración de subdominios, póngase en contacto con el Adobe o póngase en contacto con el Servicio de atención al cliente para solicitar consultoría de entregas.
