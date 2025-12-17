---
solution: Journey Optimizer
product: journey optimizer
title: Creación de un perfil de prueba
description: Obtenga información sobre cómo crear un perfil de prueba
feature: Profiles, Test Profiles
topic: Content Management
role: User
level: Intermediate
exl-id: bd5e053a-69eb-463b-add3-8b9168c8e280
source-git-commit: e6395120223a0e87ef3557c9f5d7e2af84462968
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 3%

---

# Creación de perfiles de prueba {#create-test-profiles}

Se requieren perfiles de prueba al usar el [modo de prueba](../building-journeys/testing-the-journey.md) en un recorrido, y para [previsualizar y probar el contenido](../content-management/preview-test.md).

>[!NOTE]
>
>[!DNL Journey Optimizer] permite probar diferentes variantes del contenido previsualizándolo y enviando pruebas utilizando datos de entrada de muestra cargados desde un archivo CSV o JSON, o añadidos manualmente. [Aprenda a probar el contenido con datos de entrada de ejemplo](../test-approve/simulate-sample-input.md)

Puede crear perfiles de prueba al [cargar un archivo CSV](#create-test-profiles-csv) o al usar [llamadas a la API](#create-test-profiles-api). [!DNL Adobe Journey Optimizer] también proporciona un [caso de uso en el producto](#use-case-1) específico para facilitar la creación del perfil de prueba.

Puede cargar un archivo JSON en un conjunto de datos existente. Para obtener más información, consulte la [Documentación de ingesta de datos](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=es#add-data-to-dataset){target="_blank"}.

Tenga en cuenta que crear un perfil de prueba es similar a crear perfiles normales en [!DNL Adobe Experience Platform]. Para obtener más información, consulte la [Documentación del perfil del cliente en tiempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}.

➡️ [Aprenda a crear perfiles de prueba en este vídeo](#video)

## Requisitos previos {#test-profile-prerequisites}

Para crear perfiles, primero debe crear un esquema y un conjunto de datos en Adobe [!DNL Journey Optimizer].

### Creación de un esquema

Para **crear un esquema**, siga estos pasos:

1. En la sección de menú DATA MANAGEMENT, haga clic en **[!UICONTROL Esquemas]** y seleccione el botón **[!UICONTROL Crear esquema]**.

   ![Menú Esquemas con el botón Crear esquema](assets/test-profiles-0.png)

1. Seleccione **[!UICONTROL Standard]** como opción de creación de esquema.
1. Seleccione un tipo de esquema, por ejemplo **Perfil individual**, y haga clic en **Siguiente**.
   ![Selección de tipo de esquema que muestra la opción de perfil individual](assets/test-profiles-1.png)
1. Escriba un nombre para el esquema y haga clic en **Finalizar**.
   ![Nombrar y guardar diálogo de esquema](assets/test-profiles-1-bis.png)
1. En la sección **Grupos de campos**, a la izquierda, haga clic en **Agregar** y seleccione los grupos de campos correspondientes. Asegúrese de agregar el grupo de campos **Detalles de la prueba del perfil**.
   ![Sección de grupos de campos con botón Agregar](assets/test-profiles-1-ter.png)
Una vez finalizado, haga clic en **[!UICONTROL Agregar grupos de campos]**: la lista de grupos de campos se muestra en la pantalla de información general del esquema.
   ![Resumen del esquema con lista de grupos de campos](assets/test-profiles-2.png)

   >[!NOTE]
   >
   >Haga clic en el nombre del esquema para actualizar sus propiedades.

1. En la lista de campos, haga clic en el campo que desee definir como identidad principal.
   ![Lista de campos de esquema para seleccionar la identidad principal](assets/test-profiles-3.png)
1. En el panel derecho de **[!UICONTROL Propiedades del campo]**, compruebe las opciones **[!UICONTROL Identidad]** e **[!UICONTROL Identidad principal]** y seleccione un área de nombres. Si desea que la identidad principal sea una dirección de correo electrónico, elija el área de nombres **[!UICONTROL Correo electrónico]**. Haga clic en **[!UICONTROL Aplicar]**.
   ![Panel de propiedades de campo con opciones de identidad y de identidad principal](assets/test-profiles-4bis.png)
1. Seleccione el esquema y habilite la opción **[!UICONTROL Perfil]** en el panel **[!UICONTROL Propiedades del esquema]**.
   ![Panel de propiedades del esquema con la opción de perfil habilitada](assets/test-profiles-5.png)
1. Haga clic en **Guardar**.

>[!NOTE]
>
>Para obtener más información sobre la creación de esquemas, consulte la [documentación de XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=es#prerequisites){target="_blank"}.

### Crear un conjunto de datos

Entonces necesita **crear el conjunto de datos** en el que se importarán los perfiles. Siga estos pasos:

1. Vaya a **[!UICONTROL Conjuntos de datos]** y, a continuación, haga clic en **[!UICONTROL Crear conjunto de datos]**.
   ![Menú Conjuntos de datos con el botón Crear conjunto de datos](assets/test-profiles-6.png)
1. Elija **[!UICONTROL Crear conjunto de datos a partir del esquema]**.
   ![Crear conjunto de datos a partir de la opción de esquema](assets/test-profiles-7.png)
1. Seleccione el esquema creado anteriormente y haga clic en **[!UICONTROL Siguiente]**.
   ![Pantalla de selección de esquema para la creación del conjunto de datos](assets/test-profiles-8.png)
1. Elija un nombre y haga clic en **[!UICONTROL Finalizar]**.
   ![Cuadro de diálogo Nombrar y finalizar conjunto de datos](assets/test-profiles-9.png)
1. Habilite la opción **[!UICONTROL Perfil]**.
   ![Configuración del conjunto de datos con la opción de perfil habilitada](assets/test-profiles-10.png)

>[!NOTE]
>
> Para obtener más información sobre la creación de conjuntos de datos, consulte la [documentación del servicio de catálogo](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=es#getting-started){target="_blank"}.

## Caso de uso dentro del producto{#use-case-1}

Desde la página de inicio de [!DNL Adobe Journey Optimizer], puede aprovechar los perfiles de prueba en el caso de uso del producto. Este caso de uso facilita la creación de perfiles de prueba utilizados para probar recorridos antes de publicar.

![Tarjeta del caso de uso de perfiles de prueba en la página principal](assets/use-cases-home.png)

Haga clic en el botón **[!UICONTROL Comenzar]** para iniciar el caso de uso.

Se requiere la siguiente información:

1. **Área de nombres de identidad**: El [área de nombres de identidad](../audience/get-started-identity.md) se usa para identificar los perfiles de prueba de forma única. Por ejemplo, si se usa el correo electrónico para identificar los perfiles de prueba, se debe seleccionar el área de nombres de identidad **Correo electrónico**. Si el identificador único es el número de teléfono, se debe seleccionar el área de nombres de identidad **Teléfono**.

2. **archivo CSV**: un archivo separado por comas que contiene la lista de perfiles de prueba que se van a crear. El caso de uso espera un formato predefinido para el archivo CSV que contiene la lista de perfiles de prueba que se van a crear. Cada fila del archivo debe incluir los siguientes campos en el orden correcto como se indica a continuación:

   1. **Id. de persona**: Identificador único del perfil de prueba. Los valores de este campo deben reflejar el área de nombres de identidad seleccionada. (Por ejemplo, si **Phone** está seleccionado para el área de nombres de identidad, los valores de este campo deben ser números de teléfono. Del mismo modo, si se selecciona **Correo electrónico**, los valores de este campo deben ser correos electrónicos)
   1. **Dirección de correo electrónico**: dirección de correo electrónico del perfil de prueba. (El campo **ID de persona** y el campo **Dirección de correo electrónico** podrían contener los mismos valores si se selecciona **Correo electrónico** como área de nombres de identidad)
   1. **Nombre**: Nombre del perfil de prueba.
   1. **Apellido**: Apellido del perfil de prueba.
   1. **Ciudad**: perfil de prueba ciudad de residencia
   1. **País**: perfil de prueba del país de residencia
   1. **Sexo**: género del perfil de prueba. Los valores disponibles son **hombre**, **mujer** y **no especificado**

Después de seleccionar el área de nombres de identidad y proporcionar el archivo CSV en función del formato anterior, seleccione el botón **[!UICONTROL Ejecutar]** en la parte superior derecha. El caso de uso puede tardar unos minutos en completarse. Una vez que el caso de uso termina de procesar y crear los perfiles de prueba, se envía una notificación al usuario.
>[!NOTE]
>
>Los perfiles de prueba pueden anular los perfiles existentes. Antes de ejecutar el caso de uso, asegúrese de que el CSV solo contiene perfiles de prueba y de que se ejecuta en la zona protegida correcta.

<!-- Removed as asked in DOCAC-13605 AJO Test Profiles Using a Journey should be removed
## Turn a profile into a test profile{#turning-profile-into-test}

You can turn an existing profile into a test profile: you can update profiles attributes in the same way as when you create a profile. 

A simple way to do this is by using an **[!UICONTROL Update Profile]** action activity in a journey and change the **testProfile** boolean field from false to true.

Your journey will be composed of a **[!UICONTROL Read Audience]** and an **[!UICONTROL Update Profile]** activity. You first need to create an audience targeting the profiles you want to turn into test profiles. 

>[!NOTE]
>
> Since you will be updating the **testProfile** field, the chosen profiles must include this field. The related schema must have the **Profile test details** field group. See [this section](../audience/creating-test-profiles.md#create-test-profiles).

1. Browse to **Audiences**, then **Create audience**, in the top right.
    ![](assets/test-profiles-22.png) 
1. Define a name for your audience and build the audience: choose the field(s) and value(s) to target the profiles you want.
    ![](assets/test-profiles-23.png) 
1. Click **Save** and check that the profiles are correctly targeted by the audience.
    ![](assets/test-profiles-24.png) 

    >[!NOTE]
    >
    > Audience calculation can take some time. Learn more about audiences in [this section](../audience/about-audiences.md).

1. Now create a new journey and start with a **[!UICONTROL Read Audience]** orchestration activity.
1. Choose the previously created audience and the namespace that your profiles use.
    ![](assets/test-profiles-25.png)
1. Add an **[!UICONTROL Update Profile]** action activity. 
1. Select the schema, the **testProfiles** field, the dataset and set the value to **True**. To perform this, in the **[!UICONTROL VALUE]** field, click the **Pen** icon on the right, select **[!UICONTROL Advanced mode]** and enter **true**.
    ![](assets/test-profiles-26.png)
1. Click **[!UICONTROL Publish]**.
1. In the **[!UICONTROL Audiences]** section, check that the profiles have been correctly updated.
    ![](assets/test-profiles-28.png)

    >[!NOTE]
    >
    > For more information on the **[!UICONTROL Update Profile]** activity, refer to [this section](../building-journeys/update-profiles.md).
-->

## Creación de un perfil de prueba con un archivo csv{#create-test-profiles-csv}

En [!DNL Adobe Experience Platform], puede crear perfiles cargando un archivo csv que contenga los diferentes campos de perfil en el conjunto de datos. Este es el método más sencillo.

1. Cree un archivo csv simple con un software de hoja de cálculo.
1. Agregue una columna para cada campo obligatorio. Asegúrese de agregar el campo de identidad principal (&quot;personID&quot; en el ejemplo anterior) y el campo &quot;testProfile&quot; establecido en &quot;true&quot;.
   ![Archivo CSV con encabezados de columna que incluye personID y testProfile](assets/test-profiles-11.png)
1. Añada una línea por perfil y rellene los valores de cada campo.
   ![Archivo CSV con datos de perfil de prueba de ejemplo](assets/test-profiles-12.png)
1. Guarde la hoja de cálculo como archivo csv. Asegúrese de que se utilizan comas como separadores.
1. Vaya a [!DNL Adobe Experience Platform] **flujos de trabajo**.
   ![Menú de flujos de trabajo en Adobe Experience Platform](assets/test-profiles-14.png)
1. Elija **Asignar CSV al esquema XDM** y, a continuación, haga clic en **Iniciar**.
   ![Asignar CSV a la opción de flujo de trabajo de esquema XDM](assets/test-profiles-16.png)
1. Seleccione el conjunto de datos en el que desea importar los perfiles. Haga clic en **Next**.
   ![Pantalla de selección de conjuntos de datos para importación de CSV](assets/test-profiles-17.png)
1. Haga clic en **Elegir archivos** y seleccione el archivo CSV. Cuando se cargue el archivo, haga clic en **Siguiente**.
   ![Pantalla de carga de archivos con el botón Elegir archivos](assets/test-profiles-18.png)
1. Asigne los campos csv de origen a los campos de esquema y haga clic en **Finalizar**.
   ![Interfaz de asignación de campos CSV que muestra los campos de origen y destino](assets/test-profiles-19.png)
1. Comienza la importación de datos. El estado pasará de **Procesando** a **Correcto**. Haga clic en **Vista previa del conjunto de datos**, en la parte superior derecha.
   ![Estado de importación que muestra Correcto con el botón Vista previa del conjunto de datos](assets/test-profiles-20.png)
1. Compruebe que los perfiles de prueba se hayan agregado correctamente.
   ![Vista previa del conjunto de datos que muestra perfiles de prueba importados](assets/test-profiles-21.png)

Los perfiles de prueba se han añadido y ahora se pueden utilizar para probar un recorrido. Consulte [esta sección](../building-journeys/testing-the-journey.md).

>[!NOTE]
>
>Para obtener más información sobre las importaciones de csv, consulte la [documentación de ingesta de datos](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=es#tutorials){target="_blank"}.

## Creación de perfiles de prueba mediante llamadas a API{#create-test-profiles-api}

También puede crear perfiles de prueba mediante llamadas a la API. Obtenga más información en [[!DNL Adobe Experience Platform] documentación](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}.

Debe utilizar un esquema de perfil que contenga el grupo de campos Detalles de la prueba de perfil. El indicador testProfile forma parte de este grupo de campos.
Al crear un perfil, asegúrese de pasar el valor: testProfile = true.

Tenga en cuenta que también puede actualizar un perfil existente para cambiar su indicador testProfile a &quot;true&quot;.

Este es un ejemplo de llamada de API para crear un perfil de prueba:

```bash
curl -X POST \
'https://dcs.adobedc.net/collection/xxxxxxxxxxxxxx' \
-H 'Cache-Control: no-cache' \
-H 'Content-Type: application/json' \
-H 'Postman-Token: xxxxx' \
-H 'cache-control: no-cache' \
-H 'x-api-key: xxxxx' \
-H 'x-gw-ims-org-id: xxxxx' \
-d '{
"header": {
"msgType": "xdmEntityCreate",
"msgId": "xxxxx",
"msgVersion": "xxxxx",
"xactionid":"xxxxx",
"datasetId": "xxxxx",
"imsOrgId": "xxxxx",
"source": {
"name": "Postman"
},
"schemaRef": {
"id": "https://example.adobe.com/mobile/schemas/xxxxx",
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"xdmEntity": {
"_id": "xxxxx",
"_mobile":{
"ECID": "xxxxx"
},
"testProfile":true
}
}
}'
```

## Vídeo práctico {#video}

Obtenga información sobre cómo crear perfiles de prueba.

>[!VIDEO](https://video.tv.adobe.com/v/3416330?captions=spa&quality=12)
