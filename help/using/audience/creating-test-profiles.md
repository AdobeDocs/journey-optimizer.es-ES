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
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '1351'
ht-degree: 4%

---

# Creación de perfiles de prueba {#create-test-profiles}

Se requieren perfiles de prueba al usar el [modo de prueba](../building-journeys/testing-the-journey.md) en un recorrido, y para [previsualizar y probar el contenido](../content-management/preview-test.md).


>[!NOTE]
>
>[!DNL Journey optimizer] permite probar diferentes variantes del contenido previsualizándolo y enviando pruebas utilizando datos de entrada de muestra cargados desde un archivo CSV o JSON, o añadidos manualmente. [Aprenda a probar el contenido con datos de entrada de ejemplo](../test-approve/simulate-sample-input.md)

Existen varias formas de crear perfiles de prueba. Puede encontrar en esta página los detalles para:

* Convertir un [perfil existente](#turning-profile-into-test) en un perfil de prueba

* Cree perfiles de prueba cargando un [archivo CSV](#create-test-profiles-csv) o usando [llamadas API](#create-test-profiles-api).

  Adobe Journey Optimizer también proporciona un [caso de uso en el producto](#use-case-1) específico para facilitar la creación del perfil de prueba.

Puede cargar un archivo JSON en un conjunto de datos existente. Para obtener más información, consulte la [Documentación de ingesta de datos](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=es#add-data-to-dataset){target="_blank"}.

Tenga en cuenta que la creación de un perfil de prueba es similar a la creación de perfiles normales en Adobe Experience Platform. Para obtener más información, consulte la [Documentación del perfil del cliente en tiempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}.

➡️ [Aprenda a crear perfiles de prueba en este vídeo](#video)

## Requisitos previos {#test-profile-prerequisites}

Para crear perfiles, primero debe crear un esquema y un conjunto de datos en Adobe [!DNL Journey Optimizer].

### Creación de un esquema

Para **crear un esquema**, siga estos pasos:

1. En la sección de menú ADMINISTRACIÓN DE DATOS, haga clic en **[!UICONTROL Esquemas]**.
   ![](assets/test-profiles-0.png)
1. Haga clic en **[!UICONTROL Crear esquema]**, en la parte superior derecha, seleccione un tipo de esquema, por ejemplo **Perfil individual** y haga clic en **Siguiente**.
   ![](assets/test-profiles-1.png)
1. Escriba un nombre para el esquema y haga clic en **Finalizar**.
   ![](assets/test-profiles-1-bis.png)
1. En la sección **Grupos de campos**, a la izquierda, haga clic en **Agregar** y seleccione los grupos de campos correspondientes. Asegúrese de agregar el grupo de campos **Detalles de la prueba del perfil**.
   ![](assets/test-profiles-1-ter.png)
Una vez finalizado, haga clic en **[!UICONTROL Agregar grupos de campos]**: la lista de grupos de campos se muestra en la pantalla de información general del esquema.
   ![](assets/test-profiles-2.png)

   >[!NOTE]
   >
   >Haga clic en el nombre del esquema para actualizar sus propiedades.

1. En la lista de campos, haga clic en el campo que desee definir como identidad principal.
   ![](assets/test-profiles-3.png)
1. En el panel derecho de **[!UICONTROL Propiedades del campo]**, compruebe las opciones **[!UICONTROL Identidad]** e **[!UICONTROL Identidad principal]** y seleccione un área de nombres. Si desea que la identidad principal sea una dirección de correo electrónico, elija el área de nombres **[!UICONTROL Correo electrónico]**. Haga clic en **[!UICONTROL Aplicar]**.
   ![](assets/test-profiles-4bis.png)
1. Seleccione el esquema y habilite la opción **[!UICONTROL Perfil]** en el panel **[!UICONTROL Propiedades del esquema]**.
   ![](assets/test-profiles-5.png)
1. Haga clic en **Guardar**.

>[!NOTE]
>
>Para obtener más información sobre la creación de esquemas, consulte la [documentación de XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=es#prerequisites){target="_blank"}.

### Crear un conjunto de datos

Entonces necesita **crear el conjunto de datos** en el que se importarán los perfiles. Siga estos pasos:

1. Vaya a **[!UICONTROL Conjuntos de datos]** y, a continuación, haga clic en **[!UICONTROL Crear conjunto de datos]**.
   ![](assets/test-profiles-6.png)
1. Elija **[!UICONTROL Crear conjunto de datos a partir del esquema]**.
   ![](assets/test-profiles-7.png)
1. Seleccione el esquema creado anteriormente y haga clic en **[!UICONTROL Siguiente]**.
   ![](assets/test-profiles-8.png)
1. Elija un nombre y haga clic en **[!UICONTROL Finalizar]**.
   ![](assets/test-profiles-9.png)
1. Habilite la opción **[!UICONTROL Perfil]**.
   ![](assets/test-profiles-10.png)

>[!NOTE]
>
> Para obtener más información sobre la creación de conjuntos de datos, consulte la [documentación del servicio de catálogo](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=es#getting-started){target="_blank"}.

## Caso de uso dentro del producto{#use-case-1}

Desde la página de inicio de Adobe Journey Optimizer, puede aprovechar los perfiles de prueba en el caso de uso del producto. Este caso de uso facilita la creación de perfiles de prueba utilizados para probar recorridos antes de publicar.

![](assets/use-cases-home.png)

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

## Conversión de un perfil en un perfil de prueba{#turning-profile-into-test}

Puede convertir un perfil existente en un perfil de prueba: puede actualizar los atributos de perfiles del mismo modo que cuando crea un perfil.

Una manera sencilla de hacerlo es usar una actividad de acción **[!UICONTROL Actualizar perfil]** en un recorrido y cambiar el campo booleano **testProfile** de falso a verdadero.

El recorrido estará compuesto por una actividad **[!UICONTROL Leer audiencia]** y **[!UICONTROL Actualizar perfil]**. Primero debe crear una audiencia dirigida a los perfiles que desea convertir en perfiles de prueba.

>[!NOTE]
>
> Como va a actualizar el campo **testProfile**, los perfiles elegidos deben incluir este campo. El esquema relacionado debe tener el grupo de campos **Detalles de prueba del perfil**. Consulte [esta sección](../audience/creating-test-profiles.md#test-profiles-prerequisites).

1. Vaya a **Audiencias** y luego a **Crear audiencia**, en la parte superior derecha.
   ![](assets/test-profiles-22.png)
1. Defina un nombre para la audiencia y genere la audiencia: elija los campos y los valores para segmentar los perfiles que desee.
   ![](assets/test-profiles-23.png)
1. Haga clic en **Guardar** y compruebe que la audiencia se ha dirigido correctamente a los perfiles.
   ![](assets/test-profiles-24.png)

   >[!NOTE]
   >
   > El cálculo de audiencias puede tardar un poco. Puede obtener más información sobre los públicos en [esta sección](../audience/about-audiences.md).

1. Ahora cree un nuevo recorrido y comience con una actividad de orquestación **[!UICONTROL Leer audiencia]**.
1. Elija la audiencia creada anteriormente y el área de nombres que utilizan los perfiles.
   ![](assets/test-profiles-25.png)
1. Agregue una actividad de acción **[!UICONTROL Actualizar perfil]**.
1. Seleccione el esquema, el campo **testProfiles**, el conjunto de datos y establezca el valor en **True**. Para ello, en el campo **[!UICONTROL VALUE]**, haga clic en el icono **Pluma** de la derecha, seleccione **[!UICONTROL Modo avanzado]** y escriba **true**.
   ![](assets/test-profiles-26.png)
1. Haga clic en **[!UICONTROL Publicar]**.
1. En la sección **[!UICONTROL Audiencias]**, compruebe que los perfiles se hayan actualizado correctamente.
   ![](assets/test-profiles-28.png)

   >[!NOTE]
   >
   > Para obtener más información sobre la actividad **[!UICONTROL Actualizar perfil]**, consulte [esta sección](../building-journeys/update-profiles.md).

## Creación de un perfil de prueba con un archivo csv{#create-test-profiles-csv}

En Adobe Experience Platform, puede crear perfiles cargando un archivo csv que contenga los diferentes campos de perfil en el conjunto de datos. Este es el método más sencillo.

1. Cree un archivo csv simple con un software de hoja de cálculo.
1. Agregue una columna para cada campo necesario. Asegúrese de agregar el campo de identidad principal (&quot;personID&quot; en el ejemplo anterior) y el campo &quot;testProfile&quot; establecido en &quot;true&quot;.
   ![](assets/test-profiles-11.png)
1. Añada una línea por perfil y rellene los valores de cada campo.
   ![](assets/test-profiles-12.png)
1. Guarde la hoja de cálculo como archivo csv. Asegúrese de que se utilizan comas como separadores.
1. Vaya a Adobe Experience Platform **Workflows**.
   ![](assets/test-profiles-14.png)
1. Elija **Asignar CSV al esquema XDM** y, a continuación, haga clic en **Iniciar**.
   ![](assets/test-profiles-16.png)
1. Seleccione el conjunto de datos en el que desea importar los perfiles. Haga clic en **Next**.
   ![](assets/test-profiles-17.png)
1. Haga clic en **Elegir archivos** y seleccione el archivo CSV. Cuando se cargue el archivo, haga clic en **Siguiente**.
   ![](assets/test-profiles-18.png)
1. Asigne los campos csv de origen a los campos de esquema y haga clic en **Finalizar**.
   ![](assets/test-profiles-19.png)
1. Comienza la importación de datos. El estado pasará de **Procesando** a **Correcto**. Haga clic en **Vista previa del conjunto de datos**, en la parte superior derecha.
   ![](assets/test-profiles-20.png)
1. Compruebe que los perfiles de prueba se hayan agregado correctamente.
   ![](assets/test-profiles-21.png)

Los perfiles de prueba se han añadido y ahora se pueden utilizar para probar un recorrido. Consulte [esta sección](../building-journeys/testing-the-journey.md).


>[!NOTE]
>
>Para obtener más información sobre las importaciones de csv, consulte la [documentación de ingesta de datos](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=es#tutorials){target="_blank"}.
>


## Creación de perfiles de prueba mediante llamadas a API{#create-test-profiles-api}

También puede crear perfiles de prueba mediante llamadas a la API. Obtenga más información en la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}.

Debe utilizar un esquema de perfil que contenga el grupo de campos Detalles de la prueba de perfil. El indicador testProfile forma parte de este grupo de campos.
Al crear un perfil, asegúrese de pasar el valor: testProfile = true.

Tenga en cuenta que también puede actualizar un perfil existente para cambiar su indicador testProfile a &quot;true&quot;.

Este es un ejemplo de llamada de API para crear un perfil de prueba:

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

## Vídeo práctico {#video}

Obtenga información sobre cómo crear perfiles de prueba.

>[!VIDEO](https://video.tv.adobe.com/v/334236?quality=12)
