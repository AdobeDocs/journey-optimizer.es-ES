---
solution: Journey Optimizer
product: journey optimizer
title: Conjunto de datos personalizado para palabras clave entrantes
description: Obtenga información sobre cómo almacenar palabras clave de SMS entrantes en un conjunto de datos personalizado habilitado para perfiles en Adobe Journey Optimizer mediante esquemas de Experience Platform, conjuntos de datos y credenciales de API de SMS.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: a4c92daab69394e6a736517f2e23a941135f7eb4
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 8%

---

# Usar un conjunto de datos personalizado para palabras clave entrantes {#custom-dataset-inbound-keywords}

Las palabras clave de SMS entrantes se pueden almacenar en un conjunto de datos personalizado habilitado para perfiles. La configuración consiste en un esquema de Adobe Experience Platform, un conjunto de datos creado a partir de ese esquema y credenciales de la API de SMS de Journey Optimizer que hacen referencia al conjunto de datos para los mensajes entrantes.

>[!NOTE]
>
>Si no se ha configurado ningún conjunto de datos personalizado, las palabras clave entrantes se almacenan en el sistema _AJO Inbound Activity Event Dataset_ de forma predeterminada. Un perfil debe tener al menos un mensaje enviado desde [!DNL Journey Optimizer] para que los mensajes entrantes se capturen en este conjunto de datos. [Más información sobre los conjuntos de datos del sistema](../data/get-started-datasets.md#system-datasets)

Para obtener información general sobre esquemas, grupos de campos y conjuntos de datos, consulte la siguiente documentación de Adobe Experience Platform:

* [Información general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}
* [Conceptos básicos de composición de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=es){target="_blank"}
* [Información general sobre conjuntos de datos](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=es){target="_blank"}

Para utilizar un conjunto de datos personalizado para la palabra clave entrante, debe:

1. [Creación de un esquema](#create-schema)
1. [Crear un conjunto de datos](#create-dataset)
1. [Configurar credenciales de API](#configure-api-credentials)

## Creación de un esquema {#create-schema}

Un esquema define la estructura y las reglas de validación que se aplican a los datos introducidos. Componga un esquema de Evento de experiencia para la colección de palabras clave de entrada agregando los grupos de campos existentes que se enumeran a continuación.

➡️ [Obtenga más información acerca de la creación de esquemas en la documentación de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/schema/composition)

1. En Adobe Experience Platform, desde **[!UICONTROL Administración de datos]**, acceda a **[!UICONTROL Esquemas]** y seleccione **[!UICONTROL Crear esquema]**.

   ![](assets/schema-sms-1.png)

1. Elija **[!UICONTROL esquema estándar]**.

1. Seleccione **[!UICONTROL Evento de experiencia]**.

   ![](assets/schema-sms-2.png)

1. Escriba un **[!UICONTROL nombre para mostrar]** para el esquema y haga clic en **[!UICONTROL Finalizar]**.

   El esquema se guarda y se abre el editor de esquemas.

1. Abra **[!UICONTROL Propiedades del esquema]** y habilite el esquema para **[!UICONTROL Perfil]**.

   ![](assets/schema-sms-3.png)

1. En **[!UICONTROL Grupos de campos]**, agregue estos grupos de campos existentes:

   * [!DNL Adobe CJM ExperienceEvent - Message interaction details]
   * [!DNL Adobe CJM ExperienceEvent - Message Execution Details]
   * [!DNL Adobe CJM ExperienceEvent - Message Profile Details]

1. Haga clic en **[!UICONTROL Guardar]**.

## Crear un conjunto de datos {#create-dataset}

Un conjunto de datos es el contenedor de almacenamiento para los datos ingeridos. Cada conjunto de datos está asociado exactamente a un esquema y los registros escritos en el conjunto de datos deben ajustarse a ese esquema.

1. En Adobe Experience Platform, desde **[!UICONTROL Administración de datos]**, acceda a **[!UICONTROL Conjuntos de datos]** y seleccione **[!UICONTROL Crear conjunto de datos]**.

   ![](assets/schema-sms-4.png)

1. Elija **[!UICONTROL Crear conjunto de datos a partir del esquema]**.

1. Seleccione el esquema creado en la sección anterior y haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/schema-sms-5.png)

1. Escriba un **[!UICONTROL Nombre]** y haga clic en **[!UICONTROL Finalizar]**.

1. En la ficha **[!UICONTROL Actividad de datos]**, habilite los datos para el **[!UICONTROL perfil]**.

   Seleccione la directiva **[!UICONTROL Retención de datos]** adecuada para los requisitos de control de la organización.

   ![](assets/schema-sms-6.png)

1. Haga clic en **[!UICONTROL Guardar]**.

## Configurar credenciales de API {#configure-api-credentials}

Configure las credenciales según su proveedor de SMS con [Introducción a la configuración de SMS / MMS / RCS](mobile-configuration.md). A continuación, complete los pasos a continuación para seleccionar el conjunto de datos de entrada personalizado.

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** `>` **[!UICONTROL Configuración de SMS]** y seleccione el menú **[!UICONTROL Credenciales de API]**. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

1. Cree o edite credenciales según el proveedor.

1. Habilite la opción **[!UICONTROL Usar conjunto de datos personalizado para entrada]**.

1. Seleccione el **[!UICONTROL conjunto de datos]** creado en la sección anterior.

   ![](assets/schema-sms-7.png)

1. Complete los campos obligatorios restantes y haga clic en **[!UICONTROL Guardar]**.

   >[!NOTE]
   >
   >Al guardar las credenciales de la API, Journey Optimizer valida que el conjunto de datos de palabras clave de entrada esté configurado correctamente. Si la validación falla, un mensaje de error indica la corrección necesaria.

Una vez guardadas las credenciales, el comportamiento de la mensajería saliente y entrante no cambia; las palabras clave entrantes para esa credencial se registran en el conjunto de datos personalizado seleccionado.
