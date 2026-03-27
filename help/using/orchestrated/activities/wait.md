---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Espera en campañas orquestadas
description: Aprenda a utilizar la actividad Espera en campañas orquestadas
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
version: Campaign Orchestration
source-git-commit: c783d638bd2a64298ff587067c29639636da0c54
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 65%

---


# Esperar {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Actividad Esperar"
>abstract="La actividad **Esperar** se utiliza para retrasar la transición de una actividad a otra."

La actividad **[!UICONTROL Wait]** es un componente **[!UICONTROL Flow control]** que se usa para producir un retraso entre dos actividades en una campaña orquestada. Esto le ayuda a garantizar que las actividades de seguimiento estén mejor sincronizadas y sean más relevantes para la participación del usuario.

Por ejemplo, puede esperar unos días después de un envío de correo electrónico para rastrear aperturas y clics antes de enviar un mensaje de seguimiento.

## Configuración{#wait-configuration}

>[!IMPORTANT]
>
>Los datos de las tablas temporales no se conservan después de **5 días**. Cuando use **[!UICONTROL Duración]** o **[!UICONTROL Tiempo fijo]** esperas, asegúrese de que el tiempo transcurrido hasta que la siguiente actividad se complete dentro de ese límite para que los datos intermedios permanezcan disponibles.

Siga estos pasos para configurar la actividad **[!UICONTROL Esperar]**:

1. Agregue una actividad **[!UICONTROL Wait]** a su campaña orquestada.

1. Seleccione el tipo de espera que mejor se adapte a sus necesidades:

   * **[!UICONTROL Duración]**: especifique un retraso en segundos, minutos, horas o días antes de continuar con la siguiente actividad.

   * **[!UICONTROL Tiempo fijo]**: establezca una fecha y hora específicas después de la cual comienza la siguiente actividad.

   ![](../assets/wait_activity.png)

## Ejemplo{#wait-example}

El siguiente ejemplo ilustra la actividad **[!UICONTROL Esperar]** en un caso de uso típico.  Se envía un correo electrónico con un código promocional a los perfiles que celebran su cumpleaños. Después de 2 días, se envía un SMS al mismo grupo como recordatorio de que el código de promoción de cumpleaños está a punto de caducar.

![](../assets/wait-example.png)
