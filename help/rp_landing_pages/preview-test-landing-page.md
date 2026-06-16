---
solution: Journey Optimizer
product: Journey Optimizer
title: Vista previa y prueba del contenido
description: Valide la precisión del mensaje antes del lanzamiento. Obtenga una vista previa del contenido personalizado con perfiles de prueba, envíe pruebas a las partes interesadas, compruebe el renderizado de los correos electrónicos entre los clientes, evalúe las puntuaciones de spam y pruebe varias variaciones de contenido de forma eficaz.
redpen-status: CREATED_||_2025-08-11_20-30-05
exl-id: bd78e0af-573b-4880-a9f1-44467c9db159
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 92%

---

# Vista previa y prueba del contenido{#section-overview}

>[!BEGINSHADEBOX]

**Propósito:** herramientas de validación previas al lanzamiento para campañas y recorridos\
**Usuarios principales:** administradores de campañas, especialistas en marketing por correo electrónico, creadores de contenido\
**Resultado clave:** detectar errores antes del envío del cliente

>[!ENDSHADEBOX]

Garantice un envío de mensajes impecable detectando los errores antes de que lleguen a los clientes. La vista previa del contenido valida la precisión de la personalización en diferentes perfiles de clientes, mientras que las herramientas de prueba revelan problemas de renderizado, riesgos de spam y variaciones de contenido que podrían afectar a la participación. Acceda a funciones completas para enviar pruebas a las partes interesadas, simular la personalización con datos de muestra, comprobar el renderizado de los correos electrónicos entre los clientes y evaluar las métricas de entregabilidad, todo ello antes de la activación. Domine estas técnicas de validación para proteger la reputación de la marca, maximizar la ubicación en la bandeja de entrada y ofrecer experiencias del cliente excelentes de forma consistente.

## Vista previa y prueba del contenido

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Cómo previsualizar y probar el contenido

Aprenda a utilizar perfiles de prueba y datos de entrada de muestra para previsualizar y probar el contenido, enviar pruebas y garantizar la precisión de la personalización.

[Introducción a la vista previa y prueba](../using/content-management/preview-test.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Cómo seleccionar perfiles de prueba

Descubra cómo seleccionar y administrar perfiles de prueba para previsualizar y probar contenido personalizado de forma eficaz.

[Más información sobre cómo seleccionar perfiles de prueba](../using/content-management/test-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Previsualizar el contenido mediante perfiles de prueba

Guía paso a paso para obtener una vista previa del contenido personalizado mediante perfiles de prueba y simular variaciones de contenido.

[Vista previa del contenido con perfiles de prueba](../using/content-management/preview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

Enviar pruebas mediante datos de perfil de prueba

Pruebe y valide sus mensajes de correo electrónico enviando pruebas utilizando datos de perfil de prueba para garantizar la precisión del contenido.

[Más información sobre cómo enviar pruebas](../using/content-management/proofs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/eye.svg)

Cómo probar el renderizado de correo electrónico con Litmus

Integre Litmus para obtener una vista previa de la representación de correo electrónico en clientes de correo electrónico populares y garantizar una visualización adecuada.

[Prueba de representación de correo electrónico con Litmus](../using/content-management/rendering.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Simulación y prueba de variaciones de contenido

Simule las variaciones de contenido utilizando datos de entrada de muestra o variantes generadas por IA para probar contenido personalizado y garantizar la precisión.

[Simulación de variaciones de contenido](../using/test-approve/simulate-sample-input.md)
:::

::::

## Guía rápida para la toma de decisiones

**Contexto:** esta tabla asigna los objetivos de prueba a herramientas específicas de Adobe Journey Optimizer.

Elija el método de prueba en función de su objetivo:

| **Si es necesario...** | **Use esta herramienta** |
|----------------------|-------------------|
| Verifique que la personalización se muestre correctamente | [Perfiles de prueba](../using/content-management/test-profiles.md) |
| Pruebe más de 10 variaciones de contenido rápidamente | [Datos de entrada de muestra](../using/test-approve/simulate-sample-input.md) |
| Obtenga la aprobación de las partes interesadas antes de enviar | [Envío de pruebas](../using/content-management/proofs.md) |
| Comprobar la visualización del correo electrónico en Gmail, Outlook y Apple Mail | [Renderizado de Litmus](../using/content-management/rendering.md) |
| Mejore la ubicación de bandeja de entrada | [Informe de correo no deseado](../using/content-management/spam-report.md) |
| Previsualice todas las variaciones a la vez | [Modo de vista previa](../using/content-management/preview.md) |

## Probar la lista de comprobación del flujo de trabajo

**Contexto:** se recomienda una secuencia de pruebas de 5 pasos aplicable a todos los canales (correo electrónico, SMS, push, web, en la aplicación).

Siga esta secuencia para realizar una validación completa:

1. **Vista previa**: utilice perfiles de prueba para comprobar correctamente los renderizados de personalización
2. **Variaciones de prueba**: cargue datos de muestra CSV/JSON para validar varios casos
3. **Compruebe la entregabilidad** (correo electrónico): ejecute el informe de correo no deseado y las pruebas de renderizado
4. **Envío de pruebas**: comparta con las partes interesadas para su revisión y aprobación
5. **Comprobación final**: compruebe que todos los vínculos, imágenes y CTA funcionan correctamente

**Sugerencia profesional:** realice una prueba con al menos 3 perfiles que representen diferentes segmentos de clientes (de alto valor, nuevos e inactivos) para detectar casos extremos.

## Casos comunes

**Contexto:** ejemplos del mundo real que muestran cómo aplicar herramientas de prueba en casos de uso habituales.

**Escenario 1: prueba de correos electrónicos personalizados para una campaña multisegmento**
→ Use [datos de entrada de muestra](../using/test-approve/simulate-sample-input.md) para probar hasta 30 variaciones sin crear perfiles de prueba individuales. Cargue un CSV con diferentes atributos del cliente, añada valores manualmente o genere variantes automáticamente con IA y previsualice todo a la vez.

**Escenario 2: validación de la representación de correo electrónico antes de un envío importante**
→ Ejecute las [pruebas Litmus](../using/content-management/rendering.md) para comprobar la visualización en los principales clientes de correo electrónico y, a continuación, compruebe el [informe de spam](../using/content-management/spam-report.md) para garantizar la ubicación en la bandeja de entrada.

**Escenario 3: obtención de la aprobación del responsable del departamento**
→ [Envíe pruebas](../using/content-management/proofs.md) a revisores internos con datos de perfil de prueba para que vean exactamente lo que los clientes recibirán.

## Principales conclusiones

- Los **perfiles de prueba** son esenciales para obtener una vista previa del contenido personalizado; use datos de entrada de muestra para probar más de 10 variaciones de forma eficaz
- Las **herramientas específicas para correo electrónico** incluyen pruebas de procesamiento (Litmus), informes de spam y pruebas
- **Secuencia recomendada:** Vista previa → Variaciones de prueba → Comprobar la capacidad de entregabilidad → Enviar pruebas → Comprobación final
- **Ahorro de tiempo:** cargue CSV/JSON con atributos del cliente en lugar de crear perfiles de prueba individuales

## Recursos adicionales

- **[Cómo usar el informe de correo no deseado](../using/content-management/spam-report.md)**: evalúe la puntuación de correo no deseado del contenido del correo electrónico mediante la función de informe de correo no deseado para mejorar la entregabilidad.

**Temas relacionados:** [Probar y aprobar la página de destino](test-landing-page.md) | [Flujos de trabajo de aprobación](approve-landing-page.md) | [Creación de perfiles de prueba](../using/audience/creating-test-profiles.md)
