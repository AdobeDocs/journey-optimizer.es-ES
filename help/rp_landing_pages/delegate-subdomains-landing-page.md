---
solution: Journey Optimizer
product: Journey Optimizer
title: Delegar subdominios de correo electrónico
description: Delegar subdominios de correo electrónico
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: bb50d06e86f9399dfd295b8091aa637abcaea4a8
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 41%

---

# Delegar subdominios de correo electrónico{#section-overview}

La delegación de subdominios de correo electrónico es un paso central en la [configuración del canal](../using/configuration/get-started-configuration.md), necesario para poder enviar correos electrónicos desde Journey Optimizer. Los subdominios le permiten aislar los tipos de tráfico (por ejemplo, de marketing o transaccional), proteger la reputación de su dominio principal y acelerar el calentamiento de la IP [1. &#x200B;](../using/configuration/ip-warmup-gs.md) Funcionan junto con la [configuración del canal de correo electrónico](../using/email/get-started-email-config.md) y la [monitorización de la capacidad de envío](../using/reports/deliverability.md) para garantizar que los mensajes lleguen a las bandejas de entrada.

Puede elegir entre varios métodos de configuración: **delegación completa** (Adobe administra DNS), **configuración CNAME** o **delegación personalizada** (tiene certificados y DNS). Si empieza con CNAME, más adelante [puede migrar a la delegación personalizada](../using/configuration/custom-subdomain-migration.md) para una seguridad más estricta. Esta sección también trata los registros de DMARC y PTR, los registros TXT de Google para Gmail y los grupos de IP. Para obtener instrucciones más amplias sobre la capacidad de entrega, consulte [Introducción a la capacidad de entrega](../using/reports/deliverability.md) y [Supervisión de las direcciones de correo electrónico](monitor-reputation-landing-page.md).

## Delegar subdominios de correo electrónico

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Introducción a la delegación de subdominios

Conozca las ventajas, los métodos de configuración y las consideraciones para delegar subdominios en Adobe Journey Optimizer.

[Iniciar la delegación de subdominios](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

Delegar un subdominio

Instrucciones paso a paso para delegar subdominios a Adobe, incluyendo la delegación completa y la configuración de CNAME.

[Más información sobre cómo delegar](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/screwdriver-wrench.svg)

Configuración de un subdominio personalizado

Tome la propiedad total de sus subdominios con delegación personalizada: cargue sus propios certificados SSL y mantenga un control total sobre la configuración del dominio.

[Configuración de un subdominio personalizado](../using/configuration/delegate-custom-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

Migrar de CNAME a delegación personalizada

Migre los subdominios configurados con CNAME existentes a la delegación personalizada para cumplir con las directivas de seguridad y obtener un control total sobre los certificados.

[Migración del subdominio](../using/configuration/custom-subdomain-migration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

Configurar registros DMARC

Configure los registros de DMARC para mejorar la seguridad del correo electrónico y la entregabilidad de los subdominios delegados.

[Configurar DMARC ahora mismo](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Añadir un registro TXT de Google

Compruebe los subdominios para la entregabilidad de Gmail añadiendo registros TXT de Google en Adobe Journey Optimizer.

[Añadir registros TXT de Google](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Acceso y edición de registros PTR

Administre los registros PTR para subdominios delegados, incluyendo la edición y el conocimiento de los estados de actualización.

[Editar registros PTR](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Crear grupos de IP

Agrupe direcciones IP para mejorar la entregabilidad del correo electrónico y administrar la reputación de los subdominios de forma eficaz.

[Crear grupos de IP](../using/configuration/ip-pools.md)
:::

::::

## Recursos adicionales

- **[Configurar subdominios de página de aterrizaje](../using/landing-pages/lp-subdomains.md)**: configure subdominios para páginas de aterrizaje y formularios de suscripción.
- **[Configurar subdominios web](../using/web/web-delegated-subdomains.md)**: delegue subdominios para experiencias web y seguimiento.
- **[Introducción a la configuración de canales](../using/configuration/get-started-configuration.md)**: Información general sobre todos los pasos de configuración de canales, incluida la delegación de subdominios.
