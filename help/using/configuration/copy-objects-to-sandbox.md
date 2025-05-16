---
solution: Journey Optimizer
product: journey optimizer
title: Copiar objetos de Journey Optimizer entre zonas protegidas
description: Aprenda a copiar recorridos, plantillas de contenido y fragmentos entre entornos limitados.
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: zona protegida, recorrido, copiar, entorno
exl-id: 356d56a5-9a90-4eba-9875-c7ba96967da9
source-git-commit: 0ad4c6a9024ea91d502ca2a733117f58c63ca50b
workflow-type: tm+mt
source-wordcount: '1375'
ht-degree: 5%

---

# Exportación de objetos a otra zona protegida {#copy-to-sandbox}

Puede copiar objetos, como recorridos, acciones personalizadas, plantillas de contenido o fragmentos, en varios entornos limitados mediante las funciones de exportación e importación de paquetes. Un paquete puede constar de un único objeto o de varios objetos. Los objetos incluidos en un paquete deben pertenecer a la misma zona protegida.

En esta página se describe el caso de uso de las herramientas de entorno limitado en el contexto de Journey Optimizer. Para obtener más información sobre la característica en sí, consulte la [documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html?lang=es).

>[!NOTE]
>
>Esta característica requiere los siguientes permisos de la funcionalidad **Administración de espacio aislado**: Administrar espacios aislados (o Ver espacios aislados) y Administrar paquetes. [Más información](../administration/ootb-permissions.md)

El proceso de copia se lleva a cabo mediante una exportación de paquetes y una importación entre las zonas protegidas de origen y destino. Estos son los pasos generales para copiar un recorrido de una zona protegida a otra:

1. Añada el objeto para exportar como paquete en la zona protegida de origen.
1. Exporte el paquete a la zona protegida de destino.

## Objetos exportados y prácticas recomendadas {#objects}

Journey Optimizer permite exportar recorridos, acciones personalizadas, plantillas de contenido y fragmentos a otra zona protegida. Las secciones siguientes proporcionan información y prácticas recomendadas para cada tipo de objeto.

### Prácticas recomendadas generales {#global}

* Al copiar un objeto, cualquier dependencia (como fragmentos anidados, audiencias de recorrido o acciones) se actualiza correctamente en el objeto principal, lo que garantiza una asignación adecuada en la zona protegida de destino.

* Si un objeto exportado contiene personalización de perfiles, asegúrese de que el esquema adecuado existe en la zona protegida de Target para evitar cualquier problema de personalización.

### Recorridos {#journeys}

* Al exportar un recorrido, además del propio recorrido, Journey Optimizer también copia la mayoría de los objetos de los que depende el recorrido: audiencias, acciones personalizadas, esquemas, eventos y acciones. Para obtener más información sobre los objetos copiados, consulte esta [sección](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html?lang=es#abobe-journey-optimizer-objects).

* No garantizamos que todos los elementos vinculados se copien en la zona protegida de destino. Le recomendamos encarecidamente que realice una comprobación exhaustiva, por ejemplo, antes de publicar un recorrido. Esto le permite identificar cualquier posible objeto que falte.

* Los objetos copiados en la zona protegida de destino son únicos y no hay riesgo de sobrescribir elementos existentes. Tanto el recorrido como los mensajes dentro del recorrido se transfieren en modo de borrador. Esto le permite realizar una validación completa antes de la publicación en la zona protegida de destino.

* El proceso de copia solo copia los metadatos sobre el recorrido y los objetos de ese Recorrido. No se están copiando datos de perfil o conjunto de datos como parte de este proceso.

### Acciones personalizadas {#custom-actions}

* Al exportar acciones personalizadas, la configuración de URL y los parámetros de carga útil se copian. Sin embargo, por motivos de seguridad, los parámetros de autenticación no se copian y, en su lugar, se sustituyen por &quot;INSERTAR SECRETO AQUÍ&quot;. Los valores de encabezado de solicitud constante y parámetro de consulta también se sustituyen por &quot;INSERTAR SECRETO AQUÍ&quot;.

  Esto incluye las acciones personalizadas de propósito especial ([!DNL Adobe Campaign Standard], [!DNL Campaign Classic], [!DNL Marketo Engage]).

* Al copiar un recorrido en otra zona protegida, si selecciona &quot;Usar existente&quot; para una acción personalizada durante el proceso de importación, la acción personalizada existente que seleccione debe ser la misma que la acción personalizada de origen (es decir, la misma configuración, parámetros, etc.). De lo contrario, la nueva copia de recorrido tendrá errores que no se podrán resolver en el lienzo.

### Campañas {#campaigns}

Las campañas se copian junto con todos los elementos relacionados con el perfil, el público, el esquema, los mensajes en línea y los objetos dependientes. Sin embargo, los siguientes elementos se **no** copiaron:

* Variantes multilingües y configuración de idioma,
* Reglas empresariales,
* Etiquetas,
* Etiquetado y aplicación del uso de datos (Data Usage Labeling and Enforcement, DULE).

Al copiar campañas, asegúrese de que los objetos enumerados a continuación se validan en la zona protegida de destino para evitar configuraciones incorrectas:

* **Configuraciones de canal**: las configuraciones de canal se copian junto con las campañas. Una vez copiadas las campañas, las configuraciones de canal deben seleccionarse manualmente en la zona protegida de Target.
* **Variantes y configuración de experimento**: las variantes y la configuración de experimento se incluyen en el proceso de copia de campaña. Valide esta configuración en la zona protegida de destino después de la importación.
* **Toma de decisiones unificada**: se admiten directivas de decisión y elementos de decisión para la exportación e importación. Asegúrese de que las dependencias relacionadas con la toma de decisiones se asignan correctamente en la zona protegida de destino.

### Plantillas de contenido {#content-templates}

* Al exportar una plantilla de contenido, todos los fragmentos anidados también se copian junto con ella.

* La exportación de plantillas de contenido a veces puede provocar la duplicación de fragmentos. Por ejemplo, si dos plantillas comparten el mismo fragmento y se copian en paquetes separados, ambas plantillas deberán reutilizar el mismo fragmento en la zona protegida de destino. Para evitar duplicaciones, seleccione la opción &quot;Usar existente&quot; durante el proceso de importación. [Obtenga información sobre cómo importar un paquete](#import)

* Para evitar duplicaciones, se recomienda exportar las plantillas de contenido en un solo paquete. Esto garantiza que el sistema gestione la deduplicación de forma eficaz.

### Toma de decisiones {#decisioning}

* Los objetos siguientes deben estar presentes en la zona protegida de destino antes de copiar los objetos de Decisioning:

   * Atributos de perfil utilizados en objetos de Decisioning,
   * El grupo de campos de atributos de oferta personalizados,
   * Los esquemas de flujos de datos utilizados para atributos de contexto en reglas, clasificación o límite.

* Actualmente no se admite la copia de zona protegida para fórmulas de clasificación con modelos de IA.

* Al copiar entidades de Decisioning, asegúrese de copiar los elementos de decisión **antes de** cualquier otro objeto. Por ejemplo, si copia una colección primero y no hay ofertas en la nueva zona protegida, la nueva colección permanecerá vacía.

### Fragmentos {#fragments}

* Los fragmentos pueden tener varios estados, como Activo, Borrador y Activo con el borrador en curso. Al exportar un fragmento, su último estado de Borrador se copia en la zona protegida de destino.

* Al exportar un fragmento, todos los fragmentos anidados también se copian junto con él.

## Adición de objetos como paquete{#export}

Para copiar objetos en otra zona protegida, primero debe añadirlos como paquete en la zona protegida de origen. Siga estos pasos:

1. Vaya al inventario donde está almacenado el primer objeto que desea copiar, como la lista recorridos. Haga clic en el icono **Más acciones** (los tres puntos junto al nombre del objeto) y haga clic en **Agregar al paquete**.

   ![](assets/journey-sandbox1.png)

1. En la ventana **Agregar al paquete**, elija si desea agregar el objeto a un paquete existente o crear un nuevo paquete:

   ![](assets/journey-sandbox2.png)

   * **Paquete existente**: seleccione el paquete en el menú desplegable.
   * **Crear nuevo paquete**: escriba el nombre del paquete. También puede añadir una descripción.

1. Repita estos pasos para añadir todos los objetos que desee exportar con el paquete.

>[!NOTE]
>
>Para la exportación de recorridos, además del propio recorrido, Journey Optimizer también copia la mayoría de los objetos de los que depende el recorrido: audiencias, esquemas, eventos y acciones. Para obtener más información sobre la exportación de recorridos, consulte [esta sección](../building-journeys/copy-to-sandbox.md).

## Publicación del paquete para exportar {#publish}

Una vez que el paquete esté listo para exportarse, siga estos pasos para publicarlo:

1. Vaya al menú **[!UICONTROL Administración]** > **[!UICONTROL Zonas protegidas]** y seleccione la pestaña **Paquetes**.

1. Abra el paquete que desea exportar, seleccione los objetos que desea exportar y haga clic en **Publicar**.

   En este ejemplo, deseamos exportar un recorrido, una plantilla de contenido y un fragmento.

   ![](assets/journey-sandbox4.png)

1. Para realizar un seguimiento del estado de la publicación del paquete desde la ficha **[!UICONTROL Trabajos]**. Para obtener más información sobre un trabajo, selecciónelo en la lista y haga clic en el botón **[!UICONTROL Ver detalles de importación]**.

   ![](assets/journey-sandbox9.png)

## Importe el paquete en la zona protegida de Target {#import}

Una vez publicado el paquete, debe importarlo en la zona protegida de destino. Siga estos pasos:

1. Vaya al menú **[!UICONTROL Zonas protegidas]** y seleccione la pestaña **[!UICONTROL Examinar]**.

1. Busque la zona protegida en la que desea importar el paquete y, a continuación, haga clic en el icono + junto a su nombre.

   ![](assets/journey-sandbox5.png)

   >[!NOTE]
   >
   >Solo están disponibles las zonas protegidas de su organización.

1. En el campo **Entorno aislado de destino**, compruebe que esté seleccionada la zona protegida de destino correcta y seleccione el paquete que desea importar de la lista desplegable **[!UICONTROL Nombre del paquete]**. Haga clic en **Next**.

   ![](assets/journey-sandbox6.png)

1. Revise los objetos de paquete y las dependencias. Esta es la lista de objetos que se han añadido al paquete, junto con otros objetos de los que dependen los recorridos, como audiencias, esquemas, eventos o acciones.

   Para cada objeto, puede elegir crear uno nuevo o utilizar uno existente en la zona protegida de destino. Esto le permite, por ejemplo, evitar la duplicación de fragmentos que puede ocurrir al importar plantillas de contenido utilizando fragmentos comunes.

   ![](assets/journey-sandbox7.png)

1. Haga clic en el botón **Finalizar**, en la esquina superior derecha, para comenzar a copiar el paquete en la zona protegida de destino. El proceso de copia varía según la complejidad de los objetos y la cantidad de objetos que deben copiarse.

1. Haga clic en el trabajo de importación para revisar el resultado de la copia:

   * Haga clic en el botón **Ver objetos importados** para mostrar cada objeto individual copiado.
   * Haga clic en el botón **Ver detalles de importación** para comprobar los resultados de importación de cada objeto.

   ![](assets/journey-sandbox8.png)

1. Acceda a la zona protegida de destino y realice una comprobación exhaustiva de todos los objetos copiados.
