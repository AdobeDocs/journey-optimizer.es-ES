---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Enriquecimiento
description: Aprenda a utilizar la actividad Enriquecimiento
exl-id: 8a0aeae8-f4f2-4f1d-9b89-28ce573fadfd
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/Q7lT1NR61ALn475i9akX7z80pybh93kbx06Gc8TcCuI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 844
ht-degree: 64%

---

# Enriquecimiento {#enrichment}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment"
>title="Actividad de enriquecimiento"
>abstract="La actividad de **enriquecimiento** permite mejorar los datos de destino con información adicional de la base de datos. Normalmente, se utiliza en una campaña después de actividades de segmentación."

La actividad **[!UICONTROL Enriquecimiento]** es una actividad de **[!UICONTROL Segmentación]** que le permite mejorar sus datos de público con atributos adicionales.

Puede aprovechar esta información para segmentar el público de forma más precisa, en función de comportamientos, preferencias o necesidades, y para crear mensajes personalizados que se conecten mejor con cada perfil.

## Añadir una actividad Enriquecimiento {#enrichment-configuration}

>[!CONTEXTUALHELP]
>id="ajo_targetdata_personalization_enrichmentdata"
>title="Datos de enriquecimiento"
>abstract="Seleccione los datos que desee utilizar para enriquecer la campaña orquestada. Puede seleccionar dos tipos de datos de enriquecimiento: un único atributo de enriquecimiento de la dimensión de destino o un vínculo de recopilación, que es un vínculo con una cardinalidad 1-N entre las tablas."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_data"
>title="Actividad de enriquecimiento"
>abstract="Una vez añadidos los datos de enriquecimiento a la campaña de varios pasos, se pueden utilizar en las actividades añadidas después de la actividad Enriquecimiento para segmentar a los clientes en distintos grupos según sus comportamientos, preferencias y necesidades o bien para crear mensajes y campañas de marketing personalizados que tengan más probabilidades de conectar con el público destinatario."

Siga estos pasos para configurar la actividad **Enriquecimiento**:

1. Añada una actividad **Enriquecimiento**

1. Haga clic en **Añadir datos de enriquecimiento** y seleccione el atributo que utilizará para enriquecer los datos.

   Puede seleccionar dos tipos de datos de enriquecimiento: un atributo de enriquecimiento único desde la dimensión de público destinatario o un vínculo de colección. Cada uno de estos tipos se detalla en los ejemplos siguientes:

   * [Atributo de enriquecimiento único](#single-attribute)
   * [Vínculo de colección](#collection-link)

   ![](../assets/enrichment-1.png)

1. Haga clic en **[!UICONTROL Agregar vínculo]** para crear un vínculo entre los datos de la tabla de trabajo y Adobe Journey Optimizer. [Más información](#create-links)

   Por ejemplo, si se cargan datos de un archivo que contiene el nivel de lealtad del cliente y la fecha de la última compra, se debe crear un vínculo a la tabla de perfiles para enriquecer los registros de destinatario con estos atributos y utilizarlos para la personalización o el direccionamiento.

   ![](../assets/enrichment-1.png)

## Creación de vínculos entre tablas {#create-links}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_simplejoin"
>title="Definición de vínculo"
>abstract="Cree un vínculo entre los datos de la tabla de trabajo y la base de datos de Adobe Journey Optimizer. Por ejemplo, si carga datos de un archivo que contiene el número de cuenta, el país y el correo electrónico de los destinatarios, debe crear un vínculo con la tabla del país para poder actualizar esta información en sus perfiles."

Utilice la sección **[!UICONTROL Link definition]** para definir una relación entre la tabla de trabajo y otro origen de datos. Por ejemplo, si importa un archivo que contiene el nivel de lealtad del cliente y la fecha de la última compra, puede crear un vínculo a la tabla de perfiles para que esos atributos estén disponibles para la personalización y el direccionamiento.

Para crear un vínculo:

1. En la sección **[!UICONTROL Definición de vínculo]**, haga clic en **[!UICONTROL Agregar vínculo]**.

   ![](../assets/enrichment-1.png)

1. En el menú desplegable **[!UICONTROL Tipo de relación]**, seleccione el tipo de relación entre el conjunto principal y los datos vinculados:

   * **[!UICONTROL 1 vínculo simple de cardinalidad]**: Cada registro del conjunto principal se asigna exactamente a un registro de los datos vinculados.
   * **[!UICONTROL 0 o 1 vínculo simple de cardinalidad]**: Cada registro del conjunto principal se asigna a cero o a un registro de los datos vinculados.
   * **[!UICONTROL Vínculo de recopilación de cardinalidad N]**: Cada registro del conjunto principal puede asignarse a varios registros de los datos vinculados.

   ![](../assets/enrichment-8.png)

1. Seleccione el objetivo al que desea vincular el conjunto principal:

   * **[!UICONTROL Esquema de base de datos]**: vincule a una tabla existente en la base de datos. Seleccione la tabla del campo **[!UICONTROL Esquema de destino]**.
   * **[!UICONTROL Esquema temporal]**: vínculo a los datos que llegan desde una transición de entrada. Seleccione la transición correspondiente en la lista.

1. Defina las condiciones de unión utilizadas para hacer coincidir registros entre el conjunto principal y el esquema vinculado:

   * **[!UICONTROL Unión simple]**: Haga coincidir registros en un par de atributos específico. Haga clic en **[!UICONTROL Agregar unión]** y, a continuación, seleccione los atributos **[!UICONTROL Source]** y **[!UICONTROL Destination]** que se usarán como criterios coincidentes.
   * **[!UICONTROL Unión avanzada]**: cree una lógica de coincidencia personalizada con el generador de reglas. Haga clic en **[!UICONTROL Crear condición]** para comenzar.

## Ejemplos {#example}

### Atributo de enriquecimiento único {#single-attribute}

En este ejemplo, el público se enriquece con un solo atributo, como la fecha de nacimiento, de la dimensión de segmentación actual.

Para ello, haga lo siguiente:

1. Haga clic en **[!UICONTROL Añadir datos de enriquecimiento]**.

1. Seleccione un campo simple, como **[!UICONTROL Fecha de nacimiento]**, de la dimensión actual.

   ![](../assets/enrichment-2.png)

1. Haga clic en **[!UICONTROL Confirmar]**.

### Vínculo de colección {#collection-link}

Este caso de uso enriquece el público con datos de una tabla vinculada. Por ejemplo, desea recuperar las tres compras más recientes por debajo de 100 USD.

Para conseguirlo, configure el enriquecimiento de la siguiente manera:

* **Atributo de enriquecimiento**: **[!UICONTROL Precio]**

* **Número de registros que se van a recuperar**: 3

* **Filtro**: solo incluye compras donde el **[!UICONTROL Precio]** sea menor a 100 USD

#### Añadir el atributo {#add-attribute}

En primer lugar, seleccione el vínculo de colección que contiene los datos con los que desea enriquecer.

1. Haga clic en **[!UICONTROL Añadir datos de enriquecimiento]**.

1. En la tabla **[!UICONTROL Compras]**, seleccione el campo **[!UICONTROL Precio]**.

   ![](../assets/enrichment-2.png)

#### Definir la configuración de la colección{#collection-settings}

A continuación, configure cómo se deben recopilar los datos y cuántas entradas se deben incluir.

1. En el menú desplegable **[!UICONTROL Seleccionar cómo se recopilan los datos]**, elija **[!UICONTROL Recopilar datos]**.

   ![](../assets/enrichment-4.png)

1. En el campo **[!UICONTROL Líneas a recuperar (columnas a crear)]**, escriba `3`.

1. Para realizar una agregación (p. ej., importe promedio de compra), seleccione **[!UICONTROL Datos agregados]** y, a continuación, elija **[!UICONTROL Promedio]** en la lista desplegable **[!UICONTROL Función de agregado]**.

   ![](../assets/enrichment-5.png)

1. Utilice los campos **[!UICONTROL Etiqueta]** y **[!UICONTROL Alias]** para que los atributos enriquecidos sean más fáciles de identificar en actividades posteriores.

#### Definición de los filtros{#collection-filters}

Finalmente, aplique filtros para asegurarse de que solo se incluyen los registros relevantes:

1. Haga clic en **[!UICONTROL Crear filtros]**.

1. Añada estas dos condiciones:

   * **[!UICONTROL El precio]** existe (para excluir valores NULL)

   * **[!UICONTROL El precio]** es menor que 100

   ![](../assets/enrichment-6.png)

1. Haga clic en **[!UICONTROL Confirmar]**.


<!--
#### Define the sorting{#collection-sorting}

We now need to apply sorting in order to retrieve the three **latest** purchases.

1. Activate the **Enable sorting** option.
1. Click inside the **Attribute** field.
1. Select the **Order date** field.
1. Click **Confirm**. 
1. Select **Descending** from the **Sort** drop-down.

![](../assets/workflow-enrichment7bis.png)


## Data reconciliation {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_reconciliation"
>title="Reconciliation"
>abstract="The **Enrichment** activity can be used to reconcile data from the Journey Optimizer schema with data from another schema, or with data coming from a temporary schema such as data uploaded using a Load file activity. This type of link defines a reconciliation towards a unique record. Journey Optimizer creates a link to a target table by adding a foreign key in it for storing a reference to the unique record."

The **Enrichment** activity can be used to reconcile data from the the Campaign database schema with data from another schema, or with data coming from a temporary schema such as data uploaded using a Load file activity. This type of link defines a reconciliation towards a unique record. Journey Optimizer creates a link to a target table by adding a foreign key in it for storing a reference to the unique record.

For example, you can use this option to reconcile a profile's country, specified in an uploaded file, with one of the countries available in the dedicated table of the Campaign database. 

Follow the steps to configure an **Enrichment** activity with a reconciliation link: 

1. Click the **Add link** button in the **Reconciliation** section.
1. Identify the data you want to create a reconciliation link with.

    * To create a reconciliation link with data from the Campaign database, select **Database schema** and choose the schema where the target is stored. 
    * To create a reconciliation link with data coming from the input transition, select **Temporary schema** and choose the Orchestrated campaign transition where the target data is stored. 

1. The **Label** and **Name** fields are automatically populated based on the selected target schema. You can change their values if necessary.

1. In the **Reconciliation criteria** section, specify how you want to reconcile data from the source and destination tables:

    * **Simple join**: Reconcile a specific field from the source table with another field in the destination table. To do this, click the **Add join** button and specify the **Source** and **Destination** fields to use for the reconciliation.

        >[!NOTE]
        >
        >You can use one or more **Simple join** criteria, in which case they must all be verified so that the data can be linked together.

    * **Advanced join**: Use the rule builder to configure the reconciliation criteria. To do this, click the **Create condition** button then define your reconciliation criteria by building your own rule using AND and OR operations.

The example below shows an Orchestrated campaign configured to create a link between Journey Optimizer profiles table and a temporary table generated a **Load file** activity. In this example, the **Enrichment** activity reconciliates both tables using the email address as reconciliation criteria.

![](../assets/enrichment-reconciliation.png)

### Enrichment with linked data {#link-example}

The example below shows an Orchestrated campaign configured to create a link between two transitions. The first transitions targets profile data using a **Query** activity, while the second transition includes purchase data stored into a file loaded through a Load file activity.

![](../assets/enrichment-uc-link.png)

* The first **Enrichment** activity links the primary set (data from the **Query** activity) with the schema from the **Load file** activity. This allows us to match each profile targeted by the query with the corresponding purchase data.

    ![](../assets/enrichment-uc-link-purchases.png)

* A second **Enrichment** activity is added in order to enrich data from the Orchestrated campaign table with the purchase data coming from the **Load file** activity. This allows us to use those data in further activities, for example, to personalize messages sent to the customers with information on their purchase.

    ![](../assets/enrichment-uc-link-data.png)

## Add offers {#add-offers}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_offer_proposition"
>title="Offer proposition"
>abstract="The Enrichment activity allows you to add offers for each profile."

The **[!UICONTROL Enrichment]** activity allows you to add offers for each profile.

To do so, follow the steps to configure an **[!UICONTROL Enrichment]** activity with an offer: 

1. In the **[!UICONTROL Enrichment]** activity, at the **[!UICONTROL Offer proposition]** section, click on the **[!UICONTROL Add offer]** button

    ![](../assets/enrichment-addoffer.png)

1. You have two choices for the offer selection :

    * **[!UICONTROL Search for the best offer in category]** : check this option and specify the offer engine call parameters (offer space, category or theme(s), contact date, number of offers to keep). The engine will calculate the best offer(s) to add according to these parameters. We recommend completing either the Category or the Theme field, rather than both at the same time.

        ![](../assets/enrichment-bestoffer.png)

    * **[!UICONTROL A predefined offer]** : check this option and specify an offer space, a specific offer, and a contact date to directly configure the offer that you would like to add, without calling the offer engine.

        ![](../assets/enrichment-predefinedoffer.png)

1. After selecting your offer, click on **[!UICONTROL Confirm]** button.

You can now use the offer in the delivery activity.



### Using the offers from Enrichment activity

Within an Orchestrated campaign, if you want to use the offers you get from an enrichment activity in your delivery, follow the steps below:

1. Open the delivery activity and go in the content edition. Click on **[!UICONTROL Offers settings]** button and select in the drop-down list the **[!UICONTROL Offers space]** corresponding to your offer. 
If you want to to view only offers from the enrichment activity, set the number of **[!UICONTROL Propositions]** to 0, and save the modifications.

    ![](../assets/offers-settings.png) 

1. In the Email Designer, when adding a personalization with offers, click on the **[!UICONTROL Propositions]** icon, it will display the offer(s) you get from the **[!UICONTROL Enrichment]** activity. Open the offer you want to choose by clicking on it.

    ![](../assets/offers-propositions.png) 

    Go in **[!UICONTROL Rendering functions]** and choose **[!UICONTROL HTML rendering]** or **[!UICONTROL Text rendering]** according to your needs.

    ![](../assets/offers-rendering.png) 

>[!NOTE]
>
>If you choose to have more than one offer in the **[!UICONTROL Enrichment]** activity at the **[!UICONTROL Number of offers to keep]** option, all the offers are displayed when clicking on the **[!UICONTROL Propositions]** icon.
-->