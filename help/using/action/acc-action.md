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
source-git-commit: d92c280e40419d2e3ec62a7ba85cd492a0867fde
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 14%

---

# Integración con las versiones 7 y 8 de Adobe Campaign {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Acciones de Adobe Campaign v7/v8"
>abstract="Esta integración está disponible para Adobe Campaign v7 y v8. Permite enviar correos electrónicos, notificaciones push y SMS mediante las funcionalidades de mensajería transaccional de Adobe Campaign. Adobe configura la conexión entre las instancias de Journey Optimizer y Campaign en el momento del aprovisionamiento."

Si tiene Adobe Campaign Classic v7 o Campaign v8, hay una acción personalizada específica disponible en sus recorridos para integrar Adobe Journey Optimizer y Adobe Campaign. Esta integración le permite enviar correos electrónicos, notificaciones push y SMS mediante las funciones de mensajería transaccional de Adobe Campaign. Obtenga más información en este [caso de uso completo](../building-journeys/ajo-ac.md).

Para cada acción configurada, hay una [actividad de acción de campaña](../building-journeys/using-adobe-campaign-v7-v8.md) disponible en la paleta del diseñador de recorridos.

## Activation {#access}

Cuando se solicita, Adobe configura la conexión entre los entornos de Journey Optimizer y Adobe Campaign en el momento del aprovisionamiento. Si no ha solicitado la conexión en el momento del aprovisionamiento, póngase en contacto con el soporte técnico de Adobe Journey Optimizer para solicitar la activación. Debe proporcionar los siguientes detalles:

>[!BEGINTABS]

>[!TAB Para Adobe Journey Optimizer]

* ID de organización (Adobe OrgID)

* Nombre de la zona protegida

>[!TAB Para Adobe Campaign]

* URL del servidor de Campaign

* URL del servidor en tiempo real

* Versión de la campaña

>[!ENDTABS]


## Mecanismos de protección y limitaciones {#important-notes}

* No se restringen los mensajes. El sistema limita el número de mensajes que se pueden enviar a 4000 cada 5 minutos, según la versión actual de Campaign SLA. Por este motivo, Journey Optimizer solo debe utilizarse en casos de uso unitarios (eventos individuales, no audiencias).

* Debe configurar una acción en el lienzo por plantilla para utilizar. Debe configurar una acción en Journey Optimizer para cada plantilla que desee utilizar desde Adobe Campaign.

* Le recomendamos que utilice una instancia específica del Centro de mensajes alojada o de Managed Services para esta integración con el fin de evitar afectar a otras operaciones de Campaign que pueda tener en marcha. El servidor de marketing puede estar alojado o ser local.<!--The build required is 21.1 Release Candidate or greater. -->

* No se ha validado que la carga útil o el mensaje de Campaign sean correctos.

* No puede utilizar una acción de Campaign con un evento de calificación de audiencia.

## Requisitos previos {#prerequisites}

En Adobe Campaign, debe crear y publicar un mensaje transaccional y su evento asociado. Consulte la [documentación de Adobe Campaign](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/send/real-time/transactional){target="_blank"}.

Puede crear la carga útil JSON correspondiente a cada mensaje siguiendo el patrón siguiente. Luego pegará esta carga útil al configurar la acción en Journey Optimizer (a continuación).

Vea el siguiente ejemplo:

```json
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
* **ctx**: variable basada en la personalización que tiene en el mensaje

## Configurar la acción {#configure-action}

En Journey Optimizer, debe configurar una acción por mensaje transaccional. Siga estos pasos:

1. Cree una nueva acción. [Más información sobre las acciones personalizadas](../action/action.md).
1. Introduzca un nombre y una descripción.
1. En el campo **Tipo de acción**, seleccione **Adobe Campaign Classic**.
1. Haga clic en el campo **Carga útil** y pegue un ejemplo de la carga útil JSON correspondiente al mensaje de Campaign. Póngase en contacto con Adobe para obtener esta carga útil.
1. Ajuste los distintos campos para que sean estáticos o variables, según si desea asignarlos en el lienzo de Recorrido. Algunos campos, como los parámetros de canal para la dirección de correo electrónico y los campos de personalización (ctx), probablemente desee definirlos como variables para su asignación en el contexto del recorrido.
1. Haga clic en **Guardar**.

![](assets/accintegration1.png)