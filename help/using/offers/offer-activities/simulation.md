---
title: Creación de simulaciones
description: Aprenda a crear simulaciones
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: null
source-git-commit: bad206b6c9b48241dbbd7758a331d602fac466b4
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# Creación de simulaciones

## Acerca de la simulación

Para validar la lógica de decisiones, puede simular qué ofertas se enviarán a un perfil de prueba para una ubicación determinada.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Esto permite probar y perfeccionar varias versiones de las ofertas sin afectar a los destinatarios objetivo.

>[!NOTE]
>
>Esta capacidad simula una sola solicitud al [!DNL Decisions] API. Más información sobre [Enviar ofertas mediante la API de decisiones](../api-reference/decisions-api/deliver-offers.md).

Para acceder a esta función, seleccione la opción **[!UICONTROL Simulation]** en la ficha **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** para abrir el Navegador.

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## Seleccionar perfiles de prueba

Primero debe seleccionar los perfiles de prueba que va a utilizar para la simulación.

1. Haga clic en **[!UICONTROL Manage profile]**.

   ![](../../assets/offers_simulation-manage-profile.png)

1. Seleccione el área de nombres de identidad que desea utilizar para identificar los perfiles de prueba. En este ejemplo, utilizaremos la variable **Correo electrónico** espacio de nombres.

   >[!NOTE]
   >
   >Un área de nombres de identidad define el contexto de un identificador, como una dirección de correo electrónico o un ID de CRM. Obtenga más información sobre las áreas de nombres de identidad de Adobe Experience Platform [en esta sección](../../get-started-identity.md){target=&quot;_blank&quot;}.

1. Introduzca el valor de identidad y haga clic en **[!UICONTROL View]** para enumerar los perfiles disponibles.

   ![](../../assets/offers_simulation-add-profile.png)

1. Añada otros perfiles si desea probar diferentes datos de perfil y guarde la selección.

   ![](../../assets/offers_simulation-save-profiles.png)

1. Una vez añadidos, todos los perfiles se enumeran en la lista desplegable debajo de **[!UICONTROL Test profile]**. Puede cambiar entre los perfiles de prueba guardados para mostrar los resultados de cada perfil seleccionado.

   ![](../../assets/offers_simulation-saved-profiles.png)

1. Puede hacer clic en el botón **[!UICONTROL Profile details]** vínculo para mostrar los datos de perfil seleccionados.

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## Agregar ámbitos de decisión

Ahora, seleccione las decisiones de oferta que desee simular en los perfiles de prueba.

1. Seleccione **[!UICONTROL Add decision scope]**.

   ![](../../assets/offers_simulation-add-decision.png)

1. Seleccione una colocación de la lista.

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. Se muestran las decisiones disponibles.

   * Puede utilizar el campo de búsqueda para restringir la selección.
   * Puede hacer clic en el botón **[!UICONTROL Open offer decisions]** para abrir la lista de todas las decisiones que ha creado. Más información sobre [decisiones](create-offer-activities.md).

   Seleccione la decisión que desee y haga clic en **[!UICONTROL Add]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. El ámbito de decisión que acaba de definir se muestra en el espacio de trabajo principal.

   Puede ajustar el número de ofertas que desea solicitar. Por ejemplo, si selecciona 2, se mostrarán las dos mejores ofertas para este ámbito de decisión.

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Puede solicitar hasta 30 ofertas.

1. Repita los pasos anteriores para agregar tantas decisiones como necesite.

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Aunque defina varios ámbitos de decisión, solo se simula una solicitud de API.
   >
   >Todos los indicadores de deduplicación están habilitados de forma predeterminada para la simulación, lo que significa que el motor de decisión permite duplicados y, por lo tanto, puede realizar la misma propuesta en varias decisiones. Obtenga más información sobre [!DNL Decisions] Propiedades de solicitud de API en [esta sección](../api-reference/decisions-api/deliver-offers.md).

## Ver resultados de simulación

Una vez agregado el ámbito de decisión y seleccionado un perfil de prueba, puede ver los resultados.

1. Haga clic en **[!UICONTROL View results]**.

   ![](../../assets/offers_simulation-view-results.png)

1. Las mejores ofertas disponibles se muestran según el perfil seleccionado para cada decisión.

   Seleccione una oferta para mostrar sus detalles.

   ![](../../assets/offers_simulation-offer-details.png)

1. Seleccione otro perfil de la lista para mostrar los resultados de las decisiones de oferta para un perfil de prueba diferente.

1. Puede agregar, quitar o actualizar los ámbitos de decisión tantas veces como sea necesario.

>[!NOTE]
>
>Cada vez que cambia perfiles o actualiza los ámbitos de decisión, debe actualizar los resultados utilizando la variable **[!UICONTROL View results]** botón.

<!--Questions

* Is it recommended to first select profiles or first add decision scopes?
* What does Request offer changes?
* Nothing displays when I click View results? Can't see any score...
* What's the typical example? i.e. how many decisions do you select, and how do you compare scores?
* What do you learn from simulation? i.e. if I selected 2 decisions and I compare the scores, which one is better or should I use for my customers?
* Is there a way to create relevant test profiles?
* Error on Profile details link.
* Is there a tutorial planned to be released?
* Why still a big red frame when no profile is found?

## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
-->