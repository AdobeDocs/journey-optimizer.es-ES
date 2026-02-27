---
solution: Journey Optimizer
product: journey optimizer
title: Medios dinámicos
description: Uso de Dynamic Media con Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 1b0b2b5aa8c5b4ea0a101583ee1132574996bd98
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 1%

---

# Insertar temporizador de cuenta atrás {#countdown}

Cree conversiones urgentes y maximice las conversiones con los temporizadores de cuenta atrás de Dynamic Media que se actualizan en tiempo real cuando los destinatarios abren sus correos electrónicos. Esta función es ideal para ventas flash, ofertas por tiempo limitado y promociones con distinción de tiempo.

Por ejemplo, como experto en marketing de una marca minorista, realiza una venta flash de 48 horas. Usando el temporizador de cuenta atrás en sus correos electrónicos promocionales:

* Los destinatarios que abren inmediatamente ven &quot;Quedan 47 horas&quot;
* Los destinatarios que abren 24 horas después ven &quot;Quedan 23 horas&quot;
* Los destinatarios que abran después de que finalice la venta verán &quot;La venta ha finalizado&quot;

Para obtener más información sobre cómo crear Dynamic Media en Adobe Experience Manager, consulte [este documento](assets/do-not-localize/Dynamic%20Media%20Templates.pdf).


1. En **[!DNL Adobe Experience Manager]**, cree una plantilla de Dynamic Media y agréguele un componente de temporizador de cuenta atrás.

   ![](assets/timer-1.png)

1. En **[!DNL Journey Optimizer]**, cree una nueva campaña o abra una existente y luego acceda al Designer de correo electrónico.

1. Arrastre y suelte un **[!UICONTROL componente de HTML]** en el contenido del correo electrónico.

1. Seleccione **[!UICONTROL Mostrar el código fuente]** para editar el HTML directamente.

   ![](assets/timer-2.png)

1. En el menú **[!UICONTROL Editar HTML]**, vaya a **[!UICONTROL Assets]** y haga clic en **[!UICONTROL Abrir selector de recursos]** para examinar y seleccionar la plantilla publicada de Dynamic Media.

   ![](assets/timer-3.png)

1. En el menú **[!UICONTROL Atributos personalizados]**, configure los parámetros personalizables de URL que sean necesarios para la plantilla.

   Haga clic en **[!UICONTROL Guardar]** cuando termine.

   ![](assets/timer-4.png)

1. Seleccione el recurso en el Designer de correo electrónico y, a continuación, acceda al menú **[!UICONTROL Estilos]**.

   Configure los siguientes ajustes:
   * **Texto del titular**: El texto mostrado con el temporizador
   * **Hora de finalización**: La fecha y hora en que caduca la cuenta atrás. Introduzca la hora solo en GMT (hora del meridiano de Greenwich). El sistema no acepta otras zonas horarias.
   * **Texto alternativo**: El mensaje que aparece después de que finalice el temporizador

   ![](assets/timer-5.png)

1. Haga clic en **[!UICONTROL Vista previa]** para ver el temporizador con actualizaciones de cuenta atrás en tiempo real y verificar la configuración.

Cuando los destinatarios abren el correo electrónico, ven el tiempo preciso que queda para la venta flash. Si vuelve a abrir el correo electrónico más tarde, la cuenta atrás se actualiza automáticamente para reflejar el tiempo restante actual. Después de la fecha de finalización, aparece automáticamente el mensaje predeterminado.

