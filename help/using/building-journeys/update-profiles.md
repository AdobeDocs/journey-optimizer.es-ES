---
solution: Journey Optimizer
product: journey optimizer
title: Actualización de perfil
description: Aprenda a utilizar la actividad Actualizar perfil en un recorrido
feature: Journeys, Profiles, Activities
topic: Content Management
role: User
level: Intermediate
keywords: perfil, actualizar, recorrido, actividad
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 6%

---

# Actualización de perfil {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Actividad Actualizar perfil"
>abstract="La actividad de la acción Actualizar perfil permite actualizar un perfil de Adobe Experience Platform existente con información proveniente del evento, una fuente de datos o con un valor específico."

Utilice la actividad de acción **[!UICONTROL Actualizar perfil]** para actualizar un perfil de Adobe Experience Platform existente con información proveniente de un evento, una fuente de datos o con un valor específico.

## Conceptos clave {#key-concepts}

* La acción **Actualizar perfil** solo se puede usar en recorridos que tengan un área de nombres.
* La acción solo actualiza los campos existentes, no crea nuevos campos de perfil.
* No puede usar la acción **Actualizar perfil** para generar eventos de experiencia, por ejemplo una compra.
* Al igual que cualquier otra acción, puede definir una ruta alternativa en caso de error o tiempo de espera, y no puede colocar dos acciones en paralelo.
* La solicitud de actualización enviada a Adobe Experience Platform es inmediata o está en un segundo. Tardará normalmente unos segundos, pero a veces más sin garantía. Como resultado, por ejemplo, si una acción está usando &quot;campo 1&quot; actualizado por una acción **Actualizar perfil** colocada justo antes, no debería esperar que &quot;campo 1&quot; se actualice en la acción.
* La actividad **Actualizar perfil** no admite campos XDM definidos como enumeraciones o valores sugeridos.
* La actividad **[!UICONTROL Actualizar perfil]** solo actualiza el [Almacén de perfiles](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es#profile-data-store){target="_blank"}, no el lago de datos.

## Selección de conjuntos de datos {#dataset-selection}

La actividad **Actualizar perfil** requiere un conjunto de datos dedicado para almacenar actualizaciones. Dado que esta actividad solo actualiza el almacén de perfiles (no el conjunto de datos), todas las actualizaciones deben guardarse en un conjunto de datos habilitado para perfiles designado específicamente para **Actualizar perfil** acciones. El uso de un conjunto de datos usado para la ingesta por lotes o de flujo continuo hará que los datos recién incorporados sobrescriban los cambios realizados por la acción **Actualizar perfil**.

Además, la configuración de la actividad **Actualizar perfil** no requiere un área de nombres de identidad. De este modo, asegúrese de que el conjunto de datos seleccionado utilice el mismo **área de nombres de identidad** que utilizó la acción que inició el recorrido, ya que es este área de nombres que utilizarán estas actualizaciones. El conjunto de datos seleccionado también puede utilizar el mapa de identidad. Si no se selecciona un conjunto de datos con el área de nombres correcta o uno que utiliza el mapa de identidad, la actividad Actualizar perfil fallará.

## Uso de la actualización de perfiles

1. Diseñe su recorrido empezando con un evento. Consulte esta [sección](../building-journeys/journey.md).

1. En la sección **Acción** de la paleta, suelte la actividad **Actualizar perfil** en el lienzo.

   ![](assets/profileupdate0.png)

1. Seleccione un esquema de la lista.

1. Haga clic en **Campo** para seleccionar el campo que desea actualizar. Solo se puede seleccionar un campo.

   ![](assets/profileupdate2.png)

1. Seleccione un conjunto de datos de la lista.

   >[!NOTE]
   >
   >La acción **Actualizar perfil** actualiza los datos del perfil en tiempo real, pero no actualiza los conjuntos de datos. La selección del conjunto de datos es necesaria, ya que el perfil es un registro relacionado con un conjunto de datos.

1. Haga clic en el campo **Valor** para definir el valor que desea utilizar:

   * Con el editor de expresiones simple, puede seleccionar un campo de una fuente de datos o del evento entrante.

     ![](assets/profileupdate4.png)

   * Si desea definir un valor específico o aprovechar funciones avanzadas, seleccione **Modo avanzado**.

     ![](assets/profileupdate3.png)

El **perfil de actualización** ya está configurado.

![](assets/profileupdate1.png)


## Uso del modo de prueba {#using-the-test-mode}

En el modo de prueba, la actualización de perfil no se simula. La actualización se realizará en el perfil de prueba.

Solo los perfiles de prueba pueden introducir un recorrido en el modo de prueba. Puede crear un nuevo perfil de prueba o convertir un perfil existente en un perfil de prueba. En Adobe Experience Platform, puede actualizar los atributos de perfiles mediante una importación de archivos csv o llamadas API. Un método más sencillo consiste en usar una actividad de acción **Actualizar perfil** y cambiar el campo booleano del perfil de prueba de falso a verdadero.

Para obtener más información sobre cómo convertir un perfil existente en un perfil de prueba, consulte esta [sección](../audience/creating-test-profiles.md#create-test-profiles-csv).
