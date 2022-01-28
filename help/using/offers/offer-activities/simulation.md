---
title: Creación de simulaciones
description: Aprenda a crear simulaciones
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: 39b52f39ec19c185d2cd95634a60e37f62a66f83
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 1%

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
   >De forma predeterminada, todos los indicadores de deduplicación están habilitados para la simulación, lo que significa que el motor de decisión permite duplicados y, por lo tanto, puede realizar la misma propuesta en múltiples decisiones/colocaciones. Obtenga más información sobre [!DNL Decisions] Propiedades de solicitud de API en [esta sección](../api-reference/decisions-api/deliver-offers.md).<!--Deduplication note TO REMOVE WHEN SIMULATIONS V2 is on PROD-->

<!--SIMULATIONS V2

## Define simulation settings {#define-simulation-settings}

To edit the default settings for your simulations, follow the steps below.

1. Click **[!UICONTROL Settings]**.

    ![](../../assets/offers_simulation-settings.png)

1. In the **[!UICONTROL Deduplication]** section, you can choose to allow duplicate offers accross decisions and/or placements. It means that multiple decisions/placements may get assigned the same offer.

    ![](../../assets/offers_simulation-settings-deduplication.png)

    >[!NOTE]
    >
    >By default, all Deduplication flags are enabled for simulation, which means that the decision engine allows duplicates and thus can make the same proposition accross multiple decisions/placements. Learn more on the [!DNL Decisions] API request properties in [this section](../api-reference/decisions-api/deliver-offers.md).

1. In the **[!UICONTROL Response format]** section, you can choose to include metadata in the code view. Check the corresponding option, and select the metadata of your choice. They will be displayed in the request and response payloads when selecting **[!UICONTROL View code]**. Learn more in the [View simulation results](#simulation-results) section.

    ![](../../assets/offers_simulation-settings-response-format.png)

    >[!NOTE]
    >
    >When turning on the option, all items are selected by default.

1. Click **[!UICONTROL Save]**.-->

<!--NOT FOR SIMULATIONS V2

In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context Data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## Ver resultados de simulación {#simulation-results}

Una vez agregado el ámbito de decisión y seleccionado un perfil de prueba, puede ver los resultados.

1. Haga clic en **[!UICONTROL View results]**.

   ![](../../assets/offers_simulation-view-results.png)

1. Las mejores ofertas disponibles se muestran según el perfil seleccionado para cada decisión.

   Seleccione una oferta para mostrar sus detalles.

   ![](../../assets/offers_simulation-offer-details.png)

   <!--
    SIMULATIONS V2
    1. Click **[!UICONTROL View code]** to display the request and response payloads. [Learn more](#view-code)-->

1. Seleccione otro perfil de la lista para mostrar los resultados de las decisiones de oferta para un perfil de prueba diferente.

1. Puede agregar, quitar o actualizar los ámbitos de decisión tantas veces como sea necesario.

>[!NOTE]
>
>Cada vez que cambia perfiles o actualiza los ámbitos de decisión, debe actualizar los resultados utilizando la variable **[!UICONTROL View results]** botón.

<!--
SIMULATIONS V2

## View code {#view-code}

To use the request payload outside of [!DNL Journey Optimizer] - for troubleshooting purpose for example, you can copy it by clicking the corresponding button on top of the code view.
    
>[!NOTE]
>
>You cannot copy the response payload.

Below is an example of code view:

    ```
    curl -X POST \
    'https://platform.adobe.io/data/core/ode/{CONTAINER_ID}/decisions' \
    -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
    -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
    -H 'Authorization: Bearer eyJhbGciOiJSUzI1NiIsIng1dSI6Imltc19uYTEtc3RnMS1rZXktMS5jZXIifQ.eyJpZCI6IjE2NDMxMzg3NDMxODlfOTIzY2ZjZjgtOWVkYy00MjE1LWJjODgtYmEyYTY2ZGIyYmMyX3VlMSIsInR5cGUiOiJhY2Nlc3NfdG9rZW4iLCJjbGllbnRfaWQiOiJhY3BfdWlfcGxhdGZvcm0iLCJ1c2VyX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJzdGF0ZSI6IntcInNlc3Npb25cIjpcImh0dHBzOi8vaW1zLW5hMS1zdGcxLmFkb2JlbG9naW4uY29tL2ltcy9zZXNzaW9uL3YxL1l6azNNakE0TXpNdFpXVTVaUzAwTVdOaExUZ3pNamd0TmpFM1pqZ3lOak5qTmpSakxTMDBPRVExTnpRM1FUWXdOemMyUkVSRk1FRTBPVFF3TVVSQVFXUnZZbVZKUkFcIn0iLCJhcyI6Imltcy1uYTEtc3RnMSIsImFhX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJjdHAiOjAsImZnIjoiV0VQQTNUSUY0UjRaQTZEWlBDUk1BMklBQ1U9PT09PT0iLCJzaWQiOiIxNjQzMDYwMDg0NzI2XzYzNGJkNDEzLWMwYTktNDA0NS1iNTM3LWRmMzgzYzU5ZGIxY191ZTEiLCJydGlkIjoiMTY0MzEzODc0MzE4OV9lYWMxOWY5Yi00ZjhhLTQ1NWMtOWVmMi1mNjYwNmQ0ODY4N2ZfdWUxIiwibW9pIjoiYmVjOTQzYzIiLCJwYmEiOiIiLCJvYyI6InJlbmdhKm5hMXItc3RnMSoxN2U5MmIzNzYzNCo2MEJEVjBGUlhOMFlRMkdHSkRON0E5Tk1HOCIsInJ0ZWEiOiIxNjQ0MzQ4MzQzMTg5IiwiZXhwaXJlc19pbiI6Ijg2NDAwMDAwIiwic2NvcGUiOiJvcGVuaWQsc2Vzc2lvbixyZWFkX29yZ2FuaXphdGlvbnMsYWRkaXRpb25hbF9pbmZvLnByb2plY3RlZFByb2R1Y3RDb250ZXh0LGFkZGl0aW9uYWxfaW5mby5yb2xlcyxhdWRpZW5jZW1hbmFnZXJfYXBpLEFkb2JlSUQiLCJjcmVhdGVkX2F0IjoiMTY0MzEzODc0MzE4OSJ9.TgZ998KHA4Zeoyq7b_NbPv8aPHb2cs9GgP3uJKrTbzosylKKRYqLpj_8HkloI-bFVQFCBCOWbCwtJtkcRIvFlQFruTr5bpMatPV8izEUVutO6smkYBFoGFYyEGuN5Xe97uOJZEHzFSWguGZtgttSrNhXr-j0hFloofjXDJXPB_911dzXALp5s15sd3HLH9XWTwwlqF_a5SMNDXaSj1800RxsB9bJ8_YL0x4pqQwjYJxRGMhiy7Y9IOpwogSBEiqCQitlKYgaO7yaJzFwhfyisnqM7_MWX2ETn-kGFEOoBHxXDTx9P2OPojzb8ChWQgmGf7Expyvtc1ke3nJkppzrxg' \
    -H 'x-api-key: {API_KEY}' \
    -H 'x-gw-ims-org-id: 5D1328435BF324E90A49402A@AdobeOrg' \
    -H 'x-sandbox-name: prod' \
    -D '{
      "xdm:propositionRequests": [
            {
                  "xdm:placementId": "xcore:offer-placement:1416f4109d9d292c",
                  "xdm:activityId": "xcore:offer-activity:1416f4aad9fd99d7",
                  "xdm:itemCount": 2
            }
      ],
      "xdm:profiles": [
            {
                  "xdm:identityMap": {
                        "email": [
                              {
                                    "xdm:id": "poyfair@adobe.com"
                              }
                        ]
                  }
            }
      ],
      "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
      },
      "xdm:responseFormat": {
            "xdm:includeMetadata": {
                  "xdm:activity": [],
                  "xdm:option": [],
                  "xdm:placement": []
            }
      }
    }'
    ```

>[!NOTE]
>
>When copying the request payload into your own code, make sure you replace CONTAINER_ID and API_KEY with your own values.-->

