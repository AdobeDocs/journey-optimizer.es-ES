---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos de contenido de AEM
description: Descubra cómo administrar fragmentos de contenido de AEM
topic: Content Management
role: User
level: Beginner
source-git-commit: d1a9bae1f9f981ed23261ad1fe38c9a61519543c
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Administrar los fragmentos de contenido de Adobe Experience Manager {#aem-fragments}

Al integrar Adobe Experience Manager as a Cloud Service o Managed Services con Adobe Journey Optimizer, puede utilizar fragmentos de contenido de AEM en el contenido y comprobar los estados de los fragmentos sin salir de Journey Optimizer.

Cuando vuelve a publicar un fragmento ya utilizado en un Recorrido o campaña, el temporizador de sincronización se inicia después de que el fragmento se **publique** en Adobe Experience Manager. El contenido actualizado suele estar disponible en Journey Optimizer en unos **5 minutos** para recorridos unitarios y campañas; para envíos por lotes, el cambio aparece en el **siguiente lote de procesamiento**. Consulte [Trabajar con fragmentos de contenido de Adobe Experience Manager](aem-fragments.md). Si se producen retrasos, puede sincronizar manualmente ese fragmento desde Journey Optimizer para extraer la última versión publicada.

## Acceso a fragmentos de contenido de AEM {#access-aem-fragments}

1. En el menú **[!UICONTROL Administración de contenido]**, seleccione **[!UICONTROL Fragmentos]**.

1. Abra la pestaña **[!UICONTROL Fragmentos de AEM]** para ver los fragmentos de contenido disponibles en Adobe Experience Manager.

1. En la lista de fragmentos, haga clic en ![menú avanzado](assets/do-not-localize/Smock_FolderSearch_18_N.svg) para **[!UICONTROL explorar referencias]**.

   ![](assets/fragment-list-1.png)

1. Seleccione un fragmento para revisar su estado y las acciones disponibles:

   * **[!UICONTROL Explorar referencias]**: vea los Recorridos, campañas, campañas organizadas y plantillas que usan el fragmento.
   * **[!UICONTROL Abrir en AEM]**: abra el fragmento en Adobe Experience Manager para editarlo o volver a publicarlo.
   * **[!UICONTROL Sincronizar]**: extrae la última versión publicada de Adobe Experience Manager en Journey Optimizer, por ejemplo, cuando el contenido republicado no ha aparecido después de la ventana de sincronización habitual. Si el control está deshabilitado, el fragmento ya coincide con la versión publicada en Experience Manager.

     ![](assets/fragment-list-2.png)

1. El menú **[!UICONTROL Detalles]** le permite revisar los metadatos y previsualizar la carga útil sincronizada:

   * **[!UICONTROL Nombre]**: título del fragmento de contenido importado de Adobe Experience Manager.
   * **[!UICONTROL Descripción]**: descripción importada desde Adobe Experience Manager.
   * **[!UICONTROL Variación]**: variación publicada representada actualmente para este fragmento.
   * **[!UICONTROL Id. de repositorio]**: Identificador de repositorio para el fragmento en Adobe Experience Manager.
   * **[!UICONTROL Id. de fragmento de AEM]**: Identificador único de fragmento de contenido en Adobe Experience Manager.
   * **[!UICONTROL Etiquetas]**: etiquetas asignadas en Adobe Experience Manager, incluidas las etiquetas de habilitación de Journey Optimizer que determinan si el fragmento aparece en selectores para su organización y zona protegida. [Aprenda a crear y asignar etiquetas](aem-fragments.md#create-tag)
   * **[!UICONTROL Vista previa JSON]**: estructura JSON de solo lectura del contenido del fragmento que utiliza Journey Optimizer.

1. En **[!UICONTROL Explorar referencias]**, usa las pestañas para ver recorridos, campañas, campañas orquestadas y plantillas que hacen referencia al fragmento.

   ![](assets/fragment-list-3.png)

➡️ [Más información acerca del fragmento de contenido](aem-fragments.md)


