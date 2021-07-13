---
title: Delegar subdominios
description: Obtenga información sobre cómo delegar subdominios
internal: n
snippet: y
feature: Configuración de la aplicación
topic: Administración
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 27%

---


# Delegación de subdominios en [!DNL Journey Optimizer]

La creación de un subdominio para campañas de correo electrónico permite a las marcas aislar distintos tipos de tráfico (marketing frente a empresa, por ejemplo) en grupos de IP específicos y con dominios específicos, lo que acelera el proceso de calentamiento de IP y mejora la capacidad de envío en general. Si comparte un dominio y este se bloquea o añade a la lista de bloqueados, podría afectar a la entrega de correo empresarial. Sin embargo, los problemas de reputación o los bloques de un dominio específico de las comunicaciones de marketing por correo electrónico solo afectarán a ese flujo de correo electrónico. El uso del dominio principal como remitente o dirección &quot;De&quot; para varios flujos de correo también podría dañar la autenticación por correo electrónico, lo que bloquearía los mensajes o colocarlos en la carpeta de correo no deseado.

Un subdominio es una división de su dominio que puede utilizarse para aislar sus marcas o varios tipos de tráfico, por ejemplo, mensajes transaccionales y comunicaciones de marketing.

Veamos el ejemplo del dominio &quot;mybrand.com&quot;, que se utiliza para enviar comunicaciones transaccionales y de marketing. En este caso, puede configurar dos subdominios:

* subdominio &quot;info.mybrand.com&quot; para comunicaciones transaccionales (confirmación de compras, restablecimiento de contraseña, etc.),
* Subdominio &quot;marketing.mybrand.com&quot; para correos electrónicos de prospección.

Al hacerlo, ayudará a preservar la reputación de su dominio y otros subdominios. Por ejemplo: si los subdominios &quot;marketing.mybrand.com&quot; terminan en la lista de bloqueados de los proveedores de servicios de Internet debido a la mala capacidad de entrega, esto impedirá que todo el dominio &quot;mybrand.com&quot; y el subdominio &quot;info.mybrand.com&quot; terminen en la lista de bloqueados.

Al implementar una solución, existen requisitos para componentes externos: estas incluyen la configuración de vínculos y páginas web para rastrear, la visualización de páginas espejo, etc.

Aunque estos requisitos se administran a través de componentes alojados tanto por Adobe como por el cliente, incluyen direcciones URL que pueden ver los destinatarios de los correos electrónicos. Para evitar tener direcciones URL que indiquen la solución técnica subyacente o el proveedor de alojamiento, se pueden configurar subdominios para que esto sea transparente para los destinatarios de los correos electrónicos.

**Más información**

* Obtenga información sobre cómo [delegar sus subdominios](delegate-subdomain.md) directamente desde la interfaz
* Obtenga información sobre cómo [añadir registros TXT de Google](google-txt.md) a los subdominios para garantizar el envío correcto de correos electrónicos a las direcciones de Gmail
* Obtenga información sobre cómo [acceder a los registros PTR](ptr-records.md) generados para los subdominios, lo que permite que los servidores de correo los verifiquen
