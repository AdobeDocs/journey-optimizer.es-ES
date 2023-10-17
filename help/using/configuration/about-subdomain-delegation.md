---
solution: Journey Optimizer
product: journey optimizer
title: Delegación de subdominios en [!DNL Journey Optimizer]
description: Obtenga información sobre cómo delegar los subdominios
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: subdominio, optimizador, delegación
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: c4b8a74541a3fb9fea054bd1145592d75c62b165
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 26%

---

# Delegación de subdominios en [!DNL Journey Optimizer] {#subdomain-delegation}

La creación de un subdominio para campañas de correo electrónico permite a las marcas aislar distintos tipos de tráfico (marketing o corporativo, por ejemplo) en grupos de IP específicos y con dominios específicos, lo que acelera el proceso de calentamiento de IP y mejora la capacidad de entrega en general. Si comparte un dominio y se bloquea o se agrega a la lista de bloqueados, podría afectar a su envío de correo corporativo. Sin embargo, los problemas de reputación o los bloqueos en un dominio específico de las comunicaciones de marketing por correo electrónico afectarán solo a ese flujo de correo electrónico. El uso del dominio principal como remitente o de la dirección &quot;De&quot; para varias secuencias de correo electrónico también podría interrumpir la autenticación del correo electrónico, lo que provocaría que los mensajes se bloquearan o se colocaran en la carpeta de correo no deseado.

>[!NOTE]
>
>No puede utilizar el mismo dominio de envío para enviar mensajes desde [!DNL Adobe Journey Optimizer] y de otro producto, como [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage].

## ¿Por qué configurar subdominios? {#why-set-up-subdomains}

Un subdominio es una división de su dominio que puede utilizarse para aislar sus marcas o varios tipos de tráfico, por ejemplo, mensajes transaccionales y comunicaciones de marketing.

Veamos el ejemplo del dominio &quot;mybrand.com&quot;, que se utiliza para enviar comunicaciones transaccionales y de marketing. En este caso, puede configurar dos subdominios:

* subdominio &quot;info.mybrand.com&quot; para comunicaciones transaccionales (confirmación de compras, restablecimiento de contraseña, etc.),
* Subdominio &quot;marketing.mybrand.com&quot; para correos electrónicos de prospección.

Al hacerlo, ayudará a preservar la reputación de su dominio y otros subdominios. Por ejemplo: si los subdominios &quot;marketing.mybrand.com&quot; terminan en la lista de bloqueados de los proveedores de servicios de Internet debido a la mala capacidad de entrega, esto impedirá que todo el dominio &quot;mybrand.com&quot; y el subdominio &quot;info.mybrand.com&quot; terminen en la lista de bloqueados.

Al implementar una solución, existen requisitos para los componentes externos, como configurar vínculos y páginas web para rastrear, mostrar páginas espejo, etc.

Aunque estos requisitos se administran mediante componentes alojados por el Adobe y el cliente, incluyen direcciones URL que pueden ver los destinatarios de los correos electrónicos. Para evitar tener direcciones URL que indiquen la solución técnica subyacente o el proveedor de alojamiento, se pueden configurar subdominios para que esto sea transparente para los destinatarios de los correos electrónicos.

**Más información**

* Obtenga información sobre cómo [delegar los subdominios](delegate-subdomain.md) directamente desde la interfaz de
* Obtenga información sobre cómo [añadir registros TXT de Google](google-txt.md) a sus subdominios para garantizar el envío correcto de correos electrónicos a las direcciones de Gmail
* Obtenga información sobre cómo [acceso a los registros PTR](ptr-records.md) generados para sus subdominios, lo que permite verificarlos enviando servidores de correo

## Métodos de configuración de subdominios {#subdomain-delegation-methods}

La configuración de subdominios le permite configurar una subsección de su dominio (técnicamente, una &quot;zona DNS&quot;) para utilizarla con Adobe Campaign. Los métodos de configuración disponibles son estos:

* **Delegación de subdominios completa en Adobe** (recomendado): el subdominio se delega completamente a Adobe. El Adobe puede controlar y mantener todos los aspectos de DNS necesarios para enviar, procesar y rastrear mensajes. [Más información sobre la delegación de subdominios completa](delegate-subdomain.md#full-subdomain-delegation)

* **Uso de CNAME**: Cree un subdominio y utilice CNAME para señalar registros específicos del Adobe. Con esta configuración, tanto usted como Adobe comparten la responsabilidad de mantener DNS. [Obtenga más información sobre la delegación de subdominios CNAME](delegate-subdomain.md#cname-subdomain-delegation)

>[!CAUTION]
>
>* La delegación completa de subdominios es el método preferido.
>
>* Se recomienda el método CNAME si las políticas de su organización restringen el método de delegación de subdominios completo. Este enfoque requiere que mantenga y administre los registros DNS por su cuenta. El Adobe no podrá ayudarle a cambiar, mantener o administrar DNS para un subdominio configurado mediante el método CNAME.

En el cuadro que figura a continuación se ofrece un resumen del funcionamiento de estos métodos, así como el nivel de esfuerzo que suponen:

| Método de configuración | Funcionamiento | Nivel de esfuerzo |
|---|---|---|
| **Delegación completa** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe configurará todos los registros DNS necesarios para Adobe Campaign.<br/><br/>En esta configuración, Adobe es totalmente responsable de administrar el subdominio y todos los registros DNS. | Bajo |
| **CNAME, método personalizado** | Cree el subdominio y el registro de área de nombres. A continuación, Adobe proporcionará los registros que se van a colocar en los servidores DNS y configurará los valores correspondientes en los servidores DNS de Adobe Campaign.<br/><br/>En esta configuración, tanto usted como Adobe comparten la responsabilidad de mantener DNS. | Alto |

Encontrará información adicional sobre la configuración de dominios en [esta documentación](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

Si tiene alguna pregunta acerca de los métodos de configuración de subdominios, póngase en contacto con el Adobe de o, finalmente, póngase en contacto con el Servicio de atención al cliente para solicitar consultoría de capacidad de entrega.

## Acceder a subdominios delegados {#access-delegated-subdomains}

Todos los subdominios delegados se muestran en la **[!UICONTROL Administration]** > **[!UICONTROL Canales]** > **[!UICONTROL Subdominios]** menú. Los filtros están disponibles para ayudarle a refinar la lista (fecha de delegación, usuario o estado).

![](assets/subdomain-list.png)

El **[!UICONTROL Estado]** proporciona información sobre el proceso de delegación de subdominios:

* **[!UICONTROL Borrador]**: la delegación de subdominios se ha guardado como borrador. Haga clic en el nombre del subdominio para reanudar el proceso de delegación.
* **[!UICONTROL Procesando]**: el subdominio está pasando por varias comprobaciones de configuración antes de poder utilizarse,
* **[!UICONTROL Correcto]**: el subdominio ha pasado por las comprobaciones correctamente y puede utilizarse para enviar mensajes,
* **[!UICONTROL Error]**: una o varias comprobaciones han fallado después de enviar la delegación de subdominios.

Para acceder a información detallada sobre un subdominio con **[!UICONTROL Correcto]** estado, ábralo desde la lista.

![](assets/subdomain-delegated.png)

Puede hacer lo siguiente:

* Recupere el nombre de subdominio (solo lectura) configurado durante el proceso de delegación, así como las direcciones URL generadas (recursos, páginas espejo y direcciones URL de seguimiento).

* Agregue un registro TXT de verificación del sitio de Google al subdominio para asegurarse de que se verifica (consulte ). [Adición de un registro TXT de Google a un subdominio](google-txt.md)).


>[!CAUTION]
>
>La configuración de subdominios es común a todos los entornos. Por lo tanto, cualquier modificación en un subdominio también afectará a las zonas protegidas de producción.
