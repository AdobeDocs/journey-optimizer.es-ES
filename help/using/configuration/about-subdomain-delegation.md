---
title: Delegación de subdominios
description: Obtenga información sobre cómo delegar subdominios
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: da995c56b59fb191934788c7aea9048123a2fe6d
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 43%

---


# Introducción a la delegación de subdominios

## Aísle las marcas para proteger su reputación

Un subdominio es una división de su dominio que puede utilizarse para aislar sus marcas o varios tipos de tráfico (mensajes transaccionales, información de marketing, etc.).
Veamos el ejemplo del dominio &quot;mybrand.com&quot;, que se utiliza para enviar comunicaciones transaccionales y de marketing. En este caso, puede configurar dos subdominios:

* subdominio &quot;info.mybrand.com&quot; para comunicaciones transaccionales (confirmación de compras, restablecimiento de contraseña, etc.),
* Subdominio &quot;marketing.mybrand.com&quot; para correos electrónicos de prospección.

Al hacerlo, ayudará a preservar la reputación de su dominio y otros subdominios. Por ejemplo: si los subdominios &quot;marketing.mybrand.com&quot; terminan en la lista de bloqueados de los proveedores de servicios de Internet debido a la mala capacidad de entrega, esto impedirá que todo el dominio &quot;mybrand.com&quot; y el subdominio &quot;info.mybrand.com&quot; terminen en la lista de bloqueados.

## Mantenga las direcciones URL de los recursos transparentes para los clientes

Al implementar una solución, existen requisitos para componentes externos: estas incluyen la configuración de vínculos y páginas web para rastrear, la visualización de páginas espejo, etc.

Aunque estos requisitos se administran a través de componentes alojados tanto por Adobe como por el cliente, incluyen direcciones URL que pueden ver los destinatarios de los correos electrónicos. Para evitar tener direcciones URL que indiquen la solución técnica subyacente o el proveedor de alojamiento, se pueden configurar subdominios para que esto sea transparente para los destinatarios de los correos electrónicos. [Obtenga más información sobre la Delegación de dominios](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=es).

## Delegación de subdominios en Journey Optimizer

Journey Optimizer proporciona varias funciones que le ayudan a administrar subdominios:

* [Delegar los ](delegate-subdomain.md) subdominios directamente desde la interfaz,
* [Agregue ](google-txt.md) registros TXT de Google a sus subdominios para garantizar el envío correcto de correos electrónicos a las direcciones de Gmail.
* [Acceda a los ](ptr-records.md) registros PTR generados para los subdominios, lo que permite que se verifiquen enviando servidores de correo.
