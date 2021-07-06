---
title: Creación de un perfil de prueba
description: Obtenga información sobre cómo crear un perfil de prueba
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '1328'
ht-degree: 1%

---

# Creación de perfiles de prueba {#create-test-profiles}

Los perfiles de prueba son obligatorios al utilizar el modo de prueba Para aprender a utilizar el [modo de prueba](../building-journeys/testing-the-journey.md) en un recorrido y para [obtener una vista previa y probar los mensajes](../preview.md).

A continuación se describen los métodos disponibles para crear perfiles de prueba:

* Puede convertir un [perfil existente](#turning-profile-into-test) en un perfil de prueba

* Puede crear un perfil de prueba cargando un [archivo csv](#create-test-profiles-csv) o utilizando [llamadas API](#create-test-profiles-api). Además de estos dos métodos, Adobe Journey Optimizer viene con un [caso de uso específico del producto](#use-case-1) para facilitar la creación de perfiles de prueba.

* También puede cargar un archivo json en un conjunto de datos. Para obtener más información, consulte la [Documentación de ingesta de datos](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html#add-data-to-dataset){target=&quot;_blank&quot;}.

Tenga en cuenta que la creación de un perfil de prueba es similar a la creación de perfiles normales en Adobe Experience Platform. Para obtener más información, consulte la [Documentación del perfil del cliente en tiempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}.

## Requisitos previos {#test-profile-prerequisites}

Para poder crear perfiles, primero debe crear un esquema y un conjunto de datos en el Adobe [!DNL Journey Optimizer].

En primer lugar, debe **crear un esquema**. Siga estos pasos:

1. En la sección del menú ADMINISTRACIÓN DE DATOS , haga clic en **[!UICONTROL Schemas]**.
   ![](../assets/test-profiles-0.png)
1. Haga clic en **[!UICONTROL Create schema]**, en la parte superior derecha, y luego seleccione un tipo de esquema, por ejemplo **XDM Individual Profile**.
   ![](../assets/test-profiles-1.png)
1. Seleccione los grupos de campos correspondientes. Asegúrese de agregar el grupo de campos **Detalles de prueba de perfil**.
   ![](../assets/test-profiles-1-ter.png)
Una vez finalizado, haga clic en  **[!UICONTROL Add field groups]**: la lista de grupos de campos se muestra en la pantalla de descripción general del esquema.
   ![](../assets/test-profiles-2.png)

   >[!NOTE]
   >
   >* Haga clic en el nombre del esquema para cambiarlo y actualizar sus propiedades.
      >
      >
   * Haga clic en el botón **[!UICONTROL Add]** de la sección Field groups para seleccionar otros grupos de campos a agregar en el esquema


1. En la lista de campos, haga clic en el campo que desee definir como identidad principal.
   ![](../assets/test-profiles-3.png)
1. En el panel derecho **[!UICONTROL Field properties]**, marque las opciones **[!UICONTROL Identity]** y **[!UICONTROL Primary Identity]** y seleccione un área de nombres. Si desea que la identidad principal sea una dirección de correo electrónico, elija el espacio de nombres **[!UICONTROL Email]**. Haga clic en **[!UICONTROL Apply]**.
   ![](../assets/test-profiles-4bis.png)
1. Seleccione el esquema y active la opción **[!UICONTROL Profile]** en el panel **[!UICONTROL Schema properties]**.
   ![](../assets/test-profiles-5.png)
1. Haga clic en **Guardar**.

>[!NOTE]
>
>Para obtener más información sobre la creación de esquemas, consulte la [documentación de XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#prerequisites){target=&quot;_blank&quot;}.

A continuación, debe **crear el conjunto de datos** en el que se importarán los perfiles. Siga estos pasos:

1. Vaya a **[!UICONTROL Datasets]** y haga clic en **[!UICONTROL Create dataset]**.
   ![](../assets/test-profiles-6.png)
1. Seleccione **[!UICONTROL Create dataset from schema]**.
   ![](../assets/test-profiles-7.png)
1. Seleccione el esquema creado anteriormente y haga clic en **[!UICONTROL Next]**.
   ![](../assets/test-profiles-8.png)
1. Elija un nombre y haga clic en **[!UICONTROL Finish]**.
   ![](../assets/test-profiles-9.png)
1. Active la opción **[!UICONTROL Profile]**.
   ![](../assets/test-profiles-10.png)

>[!NOTE]
>
> Para obtener más información sobre la creación de conjuntos de datos, consulte la [Documentación del servicio de catálogo](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#getting-started){target=&quot;_blank&quot;}.

## Caso de uso dentro del producto{#use-case-1}

Desde la página de inicio de Adobe Journey Optimizer, puede aprovechar los perfiles de prueba en el caso de uso del producto. Este caso de uso facilita la creación de perfiles de prueba utilizados para probar recorridos antes de la publicación.

![](../assets/use-cases-home.png)

Haga clic en el botón **[!UICONTROL Begin]** para iniciar el caso de uso.

Se requiere la siguiente información:

1. **Área de nombres de identidad**: El espacio de  [nombres de ](../get-started-identity.md) identidad utilizado para identificar de forma exclusiva los perfiles de prueba. Por ejemplo, si se utiliza correo electrónico para identificar los perfiles de prueba, se debe seleccionar el área de nombres de identidad **Email**. Si el identificador único es el número de teléfono, se debe seleccionar el área de nombres de identidad **Phone**.

2. **Archivo** CSV: Archivo separado por comas que contiene la lista de perfiles de prueba que se van a crear. El caso de uso espera un formato predefinido para el archivo CSV que contiene la lista de perfiles de prueba que se van a crear. Cada fila del archivo debe incluir los siguientes campos en el orden correcto de la siguiente manera:

   1. **Id** de persona: Identificador único del perfil de prueba. Los valores de este campo deben reflejar el área de nombres de identidad seleccionada. (Por ejemplo, si **Phone** está seleccionado para el área de nombres de identidad, los valores de este campo deben ser números de teléfono. Del mismo modo, si **Email** está seleccionado, los valores de este campo deben ser correos electrónicos)
   1. **Dirección** de correo electrónico: Probar la dirección de correo electrónico del perfil. (El campo **Person Id** y el campo **Email Address** podrían contener potencialmente los mismos valores si se selecciona **Email** como el área de nombres de identidad)
   1. **Nombre**: Nombre del perfil de prueba.
   1. **Apellidos**: Nombre del perfil de prueba.
   1. **Ciudad**: Prueba del perfil de ciudad de residencia
   1. **País**: País de residencia del perfil de prueba
   1. **Sexo**: Pruebe el sexo del perfil. Los valores disponibles son **macho**, **hembra** y **no_especificado**

Después de seleccionar el área de nombres de identidad y proporcionar el archivo CSV en función del formato anterior, haga clic en el botón **[!UICONTROL Run]** en la parte superior derecha. El caso de uso puede tardar unos minutos en completarse. Una vez que el caso de uso termina de procesarse y crearse los perfiles de prueba, se envía una notificación para notificar al usuario.

>[!NOTE]
>
>Los perfiles de prueba pueden anular los perfiles existentes. Antes de ejecutar el caso de uso, asegúrese de que el CSV contenga únicamente perfiles de prueba y de que se ejecute con el simulador de pruebas correcto.

## Conversión de un perfil en un perfil de prueba{#turning-profile-into-test}

Puede convertir un perfil existente en un perfil de prueba: puede actualizar los atributos de perfiles del mismo modo que cuando crea un perfil.

Una forma sencilla de hacerlo es usar una actividad de acción **[!UICONTROL Update Profile]** en un recorrido y cambiar el campo booleano testProfile de false a true.

El recorrido estará compuesto por una actividad **[!UICONTROL Read Segment]** y una actividad **[!UICONTROL Update Profile]**. Primero debe crear un segmento dirigido a los perfiles que desea convertir en perfiles de prueba.

>[!NOTE]
>
> Dado que se va a actualizar el campo **testProfile**, los perfiles seleccionados deben incluir este campo. El esquema relacionado debe tener el grupo de campos **Profile test details**. Consulte [esta sección](../building-journeys/creating-test-profiles.md#test-profiles-prerequisites).

1. Vaya a **Segmentos** y, a continuación, **Crear segmento**, en la parte superior derecha.
   ![](../assets/test-profiles-22.png)
1. Defina un nombre para el segmento y genere el segmento: elija los campos y los valores para dirigirse a los perfiles que desee.
   ![](../assets/test-profiles-23.png)
1. Haga clic en **Save** y compruebe que el segmento tenga correctamente en cuenta los perfiles.
   ![](../assets/test-profiles-24.png)

   >[!NOTE]
   >
   > El cálculo de segmentos puede tardar algún tiempo. Obtenga más información sobre los segmentos en [esta sección](../segment/about-segments.md).

1. Ahora cree un nuevo recorrido y comience con una actividad de organización **[!UICONTROL Read Segment]** .
1. Elija el segmento creado anteriormente y el área de nombres que utilizan sus perfiles.
   ![](../assets/test-profiles-25.png)
1. Agregue una actividad **[!UICONTROL Update Profile]** acción.
1. Seleccione el esquema, el campo **testProfiles**, el conjunto de datos y establezca el valor en **True**. Para ello, en el campo **[!UICONTROL VALUE]**, haga clic en el icono **Pen** de la derecha, seleccione **[!UICONTROL Advanced mode]** y escriba **true**.
   ![](../assets/test-profiles-26.png)
1. Agregue una actividad **End** y haga clic en **[!UICONTROL Publish]**.
1. En la sección **[!UICONTROL Segments]** , compruebe que los perfiles se hayan actualizado correctamente.
   ![](../assets/test-profiles-28.png)

   >[!NOTE]
   >
   > Para obtener más información sobre la actividad **[!UICONTROL Update Profile]**, consulte [esta sección](../building-journeys/update-profiles.md).

## Creación de un perfil de prueba mediante un archivo csv{#create-test-profiles-csv}

En Adobe Experience Platform, puede crear perfiles cargando un archivo csv que contenga los distintos campos de perfil en el conjunto de datos. Este es el método más sencillo.

1. Cree un archivo csv simple usando un programa de hojas de cálculo.
1. Agregue una columna para cada campo necesario. Asegúrese de agregar el campo de identidad principal (&quot;personID&quot; en nuestro ejemplo anterior) y el campo &quot;testProfile&quot; establecido en &quot;true&quot;.
   ![](../assets/test-profiles-11.png)
1. Añada una línea por perfil y rellene los valores de cada campo.
   ![](../assets/test-profiles-12.png)
1. Guarde la hoja de cálculo como archivo csv. Asegúrese de que las comas se utilizan como separadores.
1. Vaya a Adobe Experience Platform **Workflows**.
   ![](../assets/test-profiles-14.png)
1. Elija **Asignar CSV al esquema XDM** y haga clic en **Iniciar**.
   ![](../assets/test-profiles-16.png)
1. Seleccione el conjunto de datos en el que desea importar los perfiles. Haga clic en **Siguiente**.
   ![](../assets/test-profiles-17.png)
1. Haga clic en **Choose files** y seleccione su archivo csv. Cuando se cargue el archivo, haga clic en **Siguiente**.
   ![](../assets/test-profiles-18.png)
1. Asigne los campos csv de origen a los campos de esquema y haga clic en **Finish**.
   ![](../assets/test-profiles-19.png)
1. Se inicia la importación de datos. El estado pasará de **Processing** a **Success**. Haga clic en **Preview dataset** en la parte superior derecha.
   ![](../assets/test-profiles-20.png)
1. Compruebe que los perfiles de prueba se hayan añadido correctamente.
   ![](../assets/test-profiles-21.png)

Se añaden los perfiles de prueba, que ahora se pueden utilizar al probar un recorrido. Consulte [esta sección](../building-journeys/testing-the-journey.md).
>[!NOTE]
>
> Para obtener más información sobre las importaciones de csv, consulte la [Documentación de ingesta de datos](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html#tutorials){target=&quot;_blank&quot;}.

## Creación de perfiles de prueba mediante llamadas a API{#create-test-profiles-api}

También puede crear perfiles de prueba mediante llamadas a la API. Obtenga más información en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}.

Debe utilizar un esquema de perfil que contenga el grupo de campos &quot;Detalles de prueba de perfil&quot;. El indicador testProfile forma parte de este grupo de campos.
Al crear un perfil, asegúrese de pasar el valor: testProfile = true.

Tenga en cuenta que también puede actualizar un perfil existente para cambiar su indicador testProfile a &quot;true&quot;.

Este es un ejemplo de una llamada a la API para crear un perfil de prueba:

```
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
