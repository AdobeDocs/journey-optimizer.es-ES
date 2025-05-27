---
solution: Journey Optimizer
product: journey optimizer
title: Integración con las versiones 7 y 8 de Adobe Campaign
description: Aprenda a integrar Journey Optimizer con Adobe Campaign v7/v8
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: campaign, acc, integration
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: ffce95a074c5827b637d081ad23f4cd3754515fe
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 17%

---

# Integración con las versiones 7 y 8 de Adobe Campaign {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Acciones de Adobe Campaign v7/v8"
>abstract="Esta integración está disponible para Adobe Campaign v7 y v8. Permite enviar correos electrónicos, notificaciones push y SMS mediante las funcionalidades de mensajería transaccional de Adobe Campaign. Adobe configura la conexión entre las instancias de Journey Optimizer y Campaign en el momento del aprovisionamiento."

Hay una acción personalizada específica disponible en sus recorridos para integrar Adobe Journey Optimizer y Adobe Campaign v7/v8.

Esta integración está disponible para las versiones 7 y 8 de Adobe Campaign a partir de la versión 7.1 y para la versión 8 de Adobe Campaign. Permite enviar correos electrónicos, notificaciones push y SMS mediante las funcionalidades de mensajería transaccional de Adobe Campaign.

Se presenta un caso de uso de extremo a extremo en esta [sección](../building-journeys/ajo-ac.md).

Para cada acción configurada, hay una actividad de acción disponible en la paleta del diseñador de recorridos. Consulte esta [sección](../building-journeys/using-adobe-campaign-v7-v8.md).

## Acceso {#access}

Adobe configura la conexión entre las instancias de Journey Optimizer y Campaign en el momento del aprovisionamiento si se solicita. Si no ha solicitado la conexión en el momento del aprovisionamiento, póngase en contacto con el servicio de asistencia de Adobe Journey Optimizer proporcionando los siguientes detalles para solicitar la habilitación:

Desde Adobe Journey Optimizer:

* ID de organización (Adobe OrgID)
* Zona protegida

Desde Adobe Campaign:

* URL de campaña
* URL de RT
* Versión de la campaña

## Notas importantes {#important-notes}

* No se restringen los mensajes. El sistema limita el número de mensajes que se pueden enviar a 4000 cada 5 minutos, según la versión actual de Campaign SLA. Por este motivo, Journey Optimizer solo debe utilizarse en casos de uso unitarios (eventos individuales, no audiencias).

* Debe configurar una acción en el lienzo por plantilla que desee utilizar. Debe configurar una acción en Journey Optimizer para cada plantilla que desee utilizar desde Adobe Campaign.

* Le recomendamos que utilice una instancia del Centro de mensajes dedicada que esté alojada para esta integración para evitar afectar a otras operaciones de Campaign que pueda tener en marcha. El servidor de marketing puede estar alojado o ser local. La versión requerida es 21.1 Release Candidate o superior.

* No se ha validado que la carga útil o el mensaje de Campaign sean correctos.

* No puede utilizar una acción de Campaign con un evento de calificación de audiencia.

## Requisitos previos {#prerequisites}

En Campaign, es necesario crear y publicar un mensaje transaccional y su evento asociado. Consulte la [documentación de Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target="_blank"}.

Puede crear la carga útil JSON correspondiente a cada mensaje siguiendo el patrón siguiente. A continuación, pegue esta carga útil al configurar la acción en Journey Optimizer (a continuación)

Vea el siguiente ejemplo:

```
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **canal**: el canal definido para su plantilla transaccional de Campaign
* **eventType**: el nombre interno del evento de Campaign
* **ctx**: variable basada en la personalización que tiene en el mensaje.

## Configuración de la acción {#configure-action}

En Journey Optimizer, debe configurar una acción por mensaje transaccional. Siga estos pasos:

1. Cree una nueva acción. Consulte esta [sección](../action/action.md).
1. Introduzca un nombre y una descripción.
1. En el campo **Tipo de acción**, seleccione **Adobe Campaign Classic**.
1. Haga clic en el campo **Carga útil** y pegue un ejemplo de la carga útil JSON correspondiente al mensaje de Campaign. Póngase en contacto con Adobe para obtener esta carga útil.
1. Ajuste los distintos campos para que sean estáticos o variables, según si desea asignarlos en el lienzo de Recorrido. Algunos campos, como los parámetros de canal para la dirección de correo electrónico y los campos de personalización (ctx), probablemente desee definirlos como variables para su asignación en el contexto del recorrido.
1. Haga clic en **Guardar**.

![](assets/accintegration1.png)