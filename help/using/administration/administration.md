---
title: Configuración técnica
description: Conozca las directrices de administración y configuración
hidefromtoc: true
hide: true
feature: Configuración de la aplicación
topic: Administración
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 8%

---

# Configuración técnica

![](../assets/do-not-localize/badge.png)

## Configurar parámetros de marca{#cjm-branding}

Cada compañía tiene directrices técnicas y visuales de marca. Puede definir un conjunto de especificaciones para presentar una marca coherente a sus clientes, desde logotipos hasta aspectos técnicos, como el remitente del correo electrónico, el dominio de la URL de las páginas espejo o la configuración del seguimiento de mensajes.
Los usuarios finales no pueden crear ni modificar marcas: esta configuración se administra mediante Adobe.

Para configurar parámetros de marca para su instancia [!DNL Journey Optimizer], debe ponerse en contacto con Adobe y compartir los siguientes detalles:

* Nombre de la empresa

* Dirección de correo electrónico del remitente (de)

* Nombre del remitente (de)

* Dirección de respuesta

Una vez configurados los parámetros de marca, podrá seleccionarlos al crear mensajes.

Una vez configurados los parámetros de marca, podrá seleccionarlos al crear mensajes desde la lista **[!UICONTROL Presets]**. [Obtenga más información sobre la creación](../create-message.md) de contenido.

## Configuración del canal de notificaciones push

Aprenda a configurar el canal push en esta [sección](../create-push.md).

## Delegación de subdominios

Para que cualquier nuevo subdominio se utilice en [!DNL Journey Optimizer], el primer paso será delegarlo. Debe ponerse en contacto con el contacto técnico de su Adobe.

Al implementar una solución, existen requisitos para componentes externos: estas incluyen la configuración de vínculos y páginas web para rastrear, la visualización de páginas espejo, etc.

Aunque estos requisitos se administran a través de componentes alojados tanto por Adobe como por el cliente, incluyen direcciones URL que pueden ver los destinatarios de los correos electrónicos.  Para evitar tener direcciones URL que indiquen la solución técnica subyacente o el proveedor de alojamiento, se pueden configurar subdominios para que esto sea transparente para los destinatarios de los correos electrónicos.

A continuación de estas delegaciones, la infraestructura establecida por Adobe garantiza que se realicen los siguientes servicios para cada dominio de envío delegado o autorizado por CNAME:

* Creación de las bandejas de entrada de postmaster@ y abuse@

* Configuración de los bucles de comentarios para el dominio delegado

* Configuración básica del registro DMARC

Los parámetros establecidos por Adobe sólo son válidos desde el momento en que la delegación se completó y luego se verificó por Adobe, y siguen funcionando.

[Obtenga más información sobre la Delegación de dominios](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=es).


## Crear fuentes de datos, eventos y acciones

Utilice la sección **[!UICONTROL Admin]** para administrar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** y **[!UICONTROL Actions]**.

![](../assets/admin-menu.png)

### Fuentes de datos

La configuración de la fuente de datos permite definir una conexión con un sistema para recuperar información adicional que se utilizará en los recorridos.

Obtenga más información sobre las fuentes de datos en esta [sección](../datasource/about-data-sources.md)

### Eventos

Los eventos le permiten almacenar en déclencheur sus recorridos de forma unitaria para enviar mensajes, en tiempo real, al individuo que entra en el recorrido.

En la configuración de eventos, se configuran los eventos esperados en los recorridos. Los datos entrantes de los eventos se normalizan siguiendo el modelo de datos de Adobe Experience (XDM). Los eventos provienen de las API de ingesta de transmisión para eventos autenticados y no autenticados (como eventos del SDK de Adobe Mobile).

Obtenga más información sobre los eventos en esta [sección](../event/about-events.md)

### Acciones

[!DNL Journey Optimizer] las funciones de mensajes están integradas: solo necesita diseñar el contenido y publicar el mensaje. Si utiliza un sistema de terceros para enviar mensajes, puede crear una acción personalizada.

Obtenga más información sobre las acciones en esta [sección](../action/action.md)
