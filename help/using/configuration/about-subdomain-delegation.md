---
solution: Journey Optimizer
product: journey optimizer
title: Delegación de subdominios en  [!DNL Journey Optimizer]
description: Obtenga información sobre cómo delegar los subdominios
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: subdominio, optimizador, delegación
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: 7854de133ebcd3b29ca59b747aa89fae242f2ea5
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 32%

---

# Delegación de subdominios en [!DNL Journey Optimizer] {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="Aquí se muestran sus subdominios delegados."
>abstract="Delegue su primer subdominio. Una vez completada la delegación, se crean registros PTR y se habilitarán los canales de correo electrónico."

La creación de un subdominio para campañas de correo electrónico permite a las marcas aislar distintos tipos de tráfico (marketing o corporativo, por ejemplo) en grupos de IP específicos y con dominios específicos, lo que acelera el proceso de calentamiento de IP y mejora la capacidad de entrega en general.

Si comparte un dominio y se bloquea o se agrega a la lista de bloqueados, podría afectar a su envío de correo corporativo. Sin embargo, los problemas de reputación o los bloqueos en un dominio específico de las comunicaciones de marketing por correo electrónico afectarán solo a ese flujo de correo electrónico. El uso del dominio principal como remitente o de la dirección &quot;De&quot; para varias secuencias de correo electrónico también podría interrumpir la autenticación del correo electrónico, lo que provocaría que los mensajes se bloquearan o se colocaran en la carpeta de correo no deseado.

>[!CAUTION]
>
>No puede usar el mismo dominio de envío para enviar mensajes desde [!DNL Adobe Journey Optimizer] y desde otro producto, como [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage].

## ¿Por qué configurar subdominios?  {#why-set-up-subdomains}

Un subdominio es una división de su dominio que puede utilizarse para aislar sus marcas o varios tipos de tráfico, por ejemplo, mensajes transaccionales y comunicaciones de marketing.

Veamos el ejemplo del dominio &quot;mybrand.com&quot;, que se utiliza para enviar comunicaciones transaccionales y de marketing. En este caso, puede configurar dos subdominios:

* subdominio &quot;info.mybrand.com&quot; para comunicaciones transaccionales (confirmación de compras, restablecimiento de contraseña, etc.),
* Subdominio &quot;marketing.mybrand.com&quot; para correos electrónicos de prospección.

Al hacerlo, ayudará a preservar la reputación de su dominio y otros subdominios. Por ejemplo: si los subdominios &quot;marketing.mybrand.com&quot; terminan en la lista de bloqueados de los proveedores de servicios de Internet debido a la mala capacidad de entrega, esto impedirá que todo el dominio &quot;mybrand.com&quot; y el subdominio &quot;info.mybrand.com&quot; terminen en la lista de bloqueados.

Al implementar una solución, existen requisitos para los componentes externos, como configurar vínculos y páginas web para rastrear, mostrar páginas espejo, etc.

Aunque estos requisitos se administran mediante componentes alojados por Adobe y el cliente, incluyen direcciones URL que pueden ver los destinatarios de los correos electrónicos. Para evitar tener direcciones URL que indiquen la solución técnica subyacente o el proveedor de alojamiento, se pueden configurar subdominios para que esto sea transparente para los destinatarios de los correos electrónicos.

**Más información**

* Aprenda a [delegar sus subdominios](delegate-subdomain.md) directamente desde la interfaz
* Aprenda a [añadir registros TXT de Google](google-txt.md) a sus subdominios para garantizar el envío correcto de correos electrónicos a las direcciones de Gmail
* Obtenga información sobre cómo [acceder a los registros PTR](ptr-records.md) generados para sus subdominios, lo que permite verificarlos enviando servidores de correo

## Métodos de configuración de subdominios {#subdomain-delegation-methods}

La configuración de subdominios le permite configurar una subsección de su dominio (técnicamente, una &quot;zona DNS&quot;) para utilizarla con Adobe Campaign.

Los métodos de configuración disponibles son los siguientes.

### Delegar completamente un subdominio a Adobe (recomendado) {#full-subdomain-delegation}

[!DNL Journey Optimizer] le permite delegar completamente sus subdominios a Adobe directamente desde la interfaz del producto. Al hacerlo, Adobe podrá entregar mensajes como servicio administrado controlando y manteniendo todos los aspectos de DNS necesarios para entregar, procesar y rastrear campañas de correo electrónico.

<!--The subdomain is fully delegated to Adobe. Adobe is able to control and maintain all aspects of DNS that are required for delivering, rendering and tracking messages.-->

Puede confiar en Adobe para mantener la infraestructura DNS necesaria para satisfacer los requisitos de capacidad de entrega estándar del sector para sus dominios de envío de marketing por correo electrónico, a la vez que mantiene y controla el DNS para sus dominios de correo electrónico internos.

>[!IMPORTANT]
>
>La delegación completa de subdominios es el método preferido.

Aprenda a delegar completamente un subdominio a Adobe en [esta sección](delegate-subdomain.md#set-up-subdomain).

### Configurar un subdominio con CNAME {#cname-subdomain-setup}

Si tiene políticas de restricción específicas del dominio y desea que Adobe tenga solo un control parcial sobre DNS, puede elegir llevar a cabo todas las actividades relacionadas con DNS de su parte.

La configuración del subdominio CNAME le permite crear un subdominio y utilizar CNAME para señalar registros específicos de Adobe. Con esta configuración, tanto usted como Adobe comparten la responsabilidad de mantener DNS para configurar el entorno de envío, procesamiento y seguimiento de correos electrónicos.

>[!CAUTION]
>
>Se recomienda el método CNAME si las políticas de su organización restringen el método de delegación de subdominios completo. Este enfoque requiere que mantenga y administre los registros DNS por su cuenta.
>
>Adobe no podrá ayudarle a cambiar, mantener o administrar DNS para un subdominio configurado mediante el método CNAME.

Aprenda a crear un subdominio con CNAME para que apunte a registros específicos de Adobe en [esta sección](delegate-subdomain.md#cname-subdomain-setup).

## Comparación de los métodos de configuración

En el cuadro que figura a continuación se ofrece un resumen del funcionamiento de estos métodos, así como el nivel de esfuerzo que suponen:

| Método de configuración | Funcionamiento | Nivel de esfuerzo |
|---|---|---|
| **Delegación completa** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe configurará todos los registros DNS necesarios para Adobe Campaign.<br/><br/>En esta configuración, Adobe es totalmente responsable de administrar el subdominio y todos los registros DNS. | Bajo |
| **método CNAME** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe proporcionará los registros que se van a colocar en los servidores DNS y configurará los valores correspondientes en los servidores DNS de Adobe Campaign.<br/><br/>En esta configuración, tanto usted como Adobe comparten la responsabilidad de mantener DNS. | Alto |

<!--
| Configuration method | How it works | Level of effort |
|---|---|---|
| **Full delegation** | Create the subdomain and namespace record. Adobe will then configure all DNS records required for Adobe Campaign.<br/><br/>In this setup, Adobe is fully responsible for managing the subdomain and all the DNS records. | Low |
| **CNAME method** |  Create the subdomain and namespace record. Adobe will then provide the records to be placed in your DNS servers and will configure the corresponding values in Adobe Campaign DNS servers.<br/><br/>In this setup, both you and Adobe share responsibility for maintaining DNS. | High |
| **Custom delegation method** |  Create the subdomain and namespace record - Adobe will then provide the records to be placed in your DNS servers. Upload the SSL Certificate obtained from the Certificate Authority and complete the Feedback Loop steps by verifying domain ownership and reporting email address.<br/><br/>In this setup, you have full responsibility for maintaining DNS. | Very high |-->

Encontrará más información sobre la configuración de dominios en [esta documentación](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=es){target="_blank"}.

Si tiene alguna pregunta acerca de los métodos de configuración de subdominios, póngase en contacto con Adobe o con el Servicio de atención al cliente para solicitar consultoría de capacidad de entrega.


