---
solution: Journey Optimizer
product: journey optimizer
title: Actualizar perfil
description: Aprenda a utilizar la actividad Actualizar perfil en un recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: perfil, actualizar, recorrido, actividad
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 9%

---

# Actualizar perfil {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Actividad Actualizar perfil"
>abstract="La actividad de la acción Actualizar perfil permite actualizar un perfil de Adobe Experience Platform existente con información proveniente del evento, una fuente de datos o con un valor específico."

Utilice el **[!UICONTROL Actualizar perfil]** actividad de acción para actualizar un perfil de Adobe Experience Platform existente con información proveniente de un evento, una fuente de datos o con un valor específico.

## Recommendations

* El **Actualizar perfil** la acción solo se puede utilizar en recorridos que comiencen por un evento que tenga un área de nombres.
* La acción solo actualiza los campos existentes, no crea nuevos campos de perfil.
* No puede usar el **Actualizar perfil** acción para generar eventos de experiencia, por ejemplo una compra.
* Al igual que cualquier otra acción, puede definir una ruta alternativa en caso de error o tiempo de espera, y no puede colocar dos acciones en paralelo.
* La solicitud de actualización enviada a Adobe Experience Platform es inmediata o está en un segundo. Tardará normalmente unos segundos, pero a veces más sin garantía. Como resultado, por ejemplo, si una acción utiliza &quot;campo 1&quot; actualizado por un **Actualizar perfil** acción colocada justo antes, no debería esperar que el &quot;campo 1&quot; se actualice en la acción.
* El **Actualizar perfil** La actividad no admite campos XDM definidos como una enumeración.

## Uso de la actualización de perfiles

1. Diseñe su recorrido empezando con un evento. Consulte esta [sección](../building-journeys/journey.md).

1. En el **Acción** de la paleta, suelte el **Actualizar perfil** actividad en el lienzo.

   ![](assets/profileupdate0.png)

1. Seleccione un esquema de la lista.

1. Haga clic en **Campo** para seleccionar el campo que desea actualizar. Solo se puede seleccionar un campo.

   ![](assets/profileupdate2.png)

1. Seleccione un conjunto de datos de la lista.

   >[!NOTE]
   >
   >El **Actualizar perfil** esta acción actualiza los datos de perfil en tiempo real, pero no actualiza los conjuntos de datos. La selección del conjunto de datos es necesaria, ya que el perfil es un registro relacionado con un conjunto de datos.

1. Haga clic en **Valor** para definir el valor que desea utilizar:

   * Con el editor de expresiones simple, puede seleccionar un campo de una fuente de datos o del evento entrante.

     ![](assets/profileupdate4.png)

   * Si desea definir un valor específico o aprovechar funciones avanzadas, haga clic en **Modo avanzado**.

     ![](assets/profileupdate3.png)

El **Actualizar perfil** ahora está configurado.

![](assets/profileupdate1.png)


## Uso del modo de prueba {#using-the-test-mode}

En el modo de prueba, la actualización de perfil no se simula. La actualización se realizará en el perfil de prueba.

Solo los perfiles de prueba pueden introducir un recorrido en el modo de prueba. Puede crear un nuevo perfil de prueba o convertir un perfil existente en un perfil de prueba. En Adobe Experience Platform, puede actualizar los atributos de perfiles mediante una importación de archivos csv o llamadas API. Un método más sencillo es utilizar una **Actualizar perfil** actividad de acción y cambie el campo booleano de perfil de prueba de false a true.

Para obtener más información sobre cómo convertir un perfil existente en un perfil de prueba, consulte [sección](../audience/creating-test-profiles.md#create-test-profiles-csv).
