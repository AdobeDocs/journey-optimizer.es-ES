---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos de contenido de AEM
description: Obtenga información sobre cómo acceder y administrar fragmentos de contenido de AEM
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: 92690f1b3f73c75d9b81746b49836a24ebf7c457
workflow-type: tm+mt
source-wordcount: '1510'
ht-degree: 4%

---

# Fragmentos de contenido de Adobe Experience Manager {#aem-fragments}

Al integrar Adobe Experience Manager as a Cloud Service con Adobe Journey Optimizer, puede incorporar sin problemas los fragmentos de contenido de AEM en el contenido de Journey Optimizer. Esta conexión optimizada simplifica el proceso de acceso y uso del contenido de AEM, lo que permite crear campañas y recorridos personalizados y dinámicos.

Para obtener más información sobre los fragmentos de contenido de AEM, consulte [Trabajar con fragmentos de contenido](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} en la documentación de Experience Manager.

## Antes de empezar {#start}

>[!AVAILABILITY]
>
>Para los clientes del sector sanitario, la integración solo se activa tras obtener la licencia de las ofertas adicionales de Journey Optimizer Healthcare Shield y Adobe Experience Manager Enhanced Security.

### Limitaciones {#limitations}

Tenga en cuenta las siguientes limitaciones al trabajar con fragmentos de contenido de Adobe Experience Manager en Journey Optimizer:

* **Tipos de fragmentos de contenido**: se admiten fragmentos de contenido simples y fragmentos de contenido anidados. Actualmente no se admiten las variaciones de fragmentos de contenido.

* **Contenido multilingüe**: solo se admite el flujo manual. Cada variante de idioma debe crearse de forma independiente en Adobe Experience Manager, etiquetarse, publicarse y seleccionarse manualmente en Journey Optimizer. No hay resolución automática de idioma ni mecanismo de reserva.

* **Acceso al repositorio**: Journey Optimizer se integra exclusivamente con el nivel de publicación de Adobe Experience Manager, donde los fragmentos de contenido están disponibles a través de un extremo público no autenticado. Aunque los repositorios de Autor pueden aparecer en el selector de repositorios, solo los fragmentos de contenido publicados en el nivel Publicar pueden utilizarse en Journey Optimizer.

* **Estado del fragmento de contenido**: Journey Optimizer muestra fragmentos de contenido con el estado **Publicado** y **Modificado**. En todos los casos, solo se utiliza la última versión publicada. Si se modifica un fragmento después de la publicación, esos cambios no se reflejarán en Journey Optimizer hasta que el fragmento de contenido se vuelva a publicar en Adobe Experience Manager. No existe una conciliación automática de versiones entre Adobe Experience Manager y Journey Optimizer.

* **Personalization**: solo se admiten atributos de perfil, atributos contextuales, cadenas estáticas y variables predeclaradas. No se admiten atributos derivados o calculados.

* **Actualizaciones y versiones**: Las actualizaciones de fragmentos de contenido requieren la republicación manual desde Adobe Experience Manager. No existe una conciliación automática de versiones entre Adobe Experience Manager y Journey Optimizer. Cuando se publica un fragmento de contenido en Adobe Experience Manager, Journey Optimizer recibe un evento y actualizaciones en Journey Optimizer. Si se realiza correctamente, la actualización estará disponible después de 5 minutos para Recorridos unitarios y en el siguiente lote para casos de uso por lotes.

* **Almacenamiento en caché y revisión**: los fragmentos de contenido se recuperan en tiempo real del nivel de publicación de Adobe Experience Manager. No hay almacenamiento en caché de instantáneas o procesamientos previos. Las pruebas para campañas y recorridos siempre reflejan la versión publicada más recientemente del fragmento de contenido y las versiones históricas no se pueden bloquear para la revisión.

* **Acceso de usuario**: Se recomienda limitar el número de usuarios con acceso para publicar fragmentos de contenido y reducir el riesgo de errores accidentales.

### Flujo de sincronización de contenido {#content-sync-flow}

La integración entre Adobe Experience Manager y Journey Optimizer sigue este flujo de datos:

1. **[Crear y crear](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#creating-a-content-fragment)**: el contenido se crea y configura en Adobe Experience Manager como fragmentos de contenido.

1. **[Etiquetado](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#manage-tags)**: los fragmentos de contenido deben etiquetarse con la etiqueta específica de Journey Optimizer (`ajo-enabled:{OrgId}/{SandboxName}`).

1. **[Publicar](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#publishing-and-previewing-a-fragment)**: Los fragmentos de contenido se publican en Adobe Experience Manager, por lo que están disponibles para Journey Optimizer.

1. **[Acceso](#aem-add)**: Journey Optimizer busca y muestra en tiempo real los fragmentos de contenido disponibles en la instancia de publicación de Adobe Experience Manager.

1. **[Integración](#aem-add)**: los fragmentos de contenido se seleccionan e integran en campañas o recorridos.

Cuando se publica un fragmento de contenido en Adobe Experience Manager, se envía un evento para actualizar el contenido en Journey Optimizer. Si la actualización se realiza correctamente, el fragmento de contenido estará disponible en un plazo aproximado de 5 minutos para recorridos unitarios y en el siguiente lote de procesamiento para casos de uso por lotes. Una vez que la actualización esté disponible en Journey Optimizer, se utilizará el contenido publicado más reciente en todas las campañas y recorridos aplicables.

### Ciclo de fragmento de contenido

![](assets/do-not-localize/AEM_CF.png)

Los fragmentos de contenido siguen diferentes etapas del ciclo vital según el nivel de Adobe Experience Manager en el que existan. [Obtenga más información en la documentación de Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

El contenido se crea y administra en el **nivel de creación**, donde los fragmentos pueden tener estados como Nuevo, Borrador, Publicado, Modificado o No publicado. Estos estados se aplican solamente en el **nivel de creación** y admiten la creación y revisión de contenido.

Cuando se publica un fragmento de contenido, se crea una copia en el **nivel de publicación** y se expone a través de un extremo público no autenticado. Journey Optimizer se integra exclusivamente con este **nivel de publicación**.

Como resultado, Journey Optimizer muestra solo fragmentos de contenido publicados o modificados y siempre utiliza la última versión publicada. Los cambios realizados después de la publicación no se reflejarán en Journey Optimizer hasta que se vuelva a publicar el fragmento de contenido.

## Creación y asignación de una etiqueta en Experience Manager

Antes de usar el fragmento de contenido en Journey Optimizer, debe crear una etiqueta específica para Journey Optimizer:

1. Acceda a su entorno de **Experience Manager**.

1. En el menú **Herramientas**, seleccione **Etiquetado**.

   ![](assets/do-not-localize/aem_tag_1.png)

1. Haga clic en **Crear etiqueta**.

1. Asegúrese de que el identificador cumple la siguiente sintaxis: `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

1. Haga clic en **Crear**.

1. Defina su modelo de fragmento de contenido como se detalla en [Documentación de Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"} y asigne la etiqueta de Journey Optimizer recién creada.

Esta conexión en tiempo real garantiza que el contenido siempre esté actualizado, pero también significa que cualquier cambio en los fragmentos publicados afectará inmediatamente a las campañas y recorridos activos.

Ahora puede empezar a crear y configurar el fragmento de contenido para utilizarlo posteriormente en Journey Optimizer. Obtenga más información en [Documentación de Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing){target="_blank"}.

## Añadir fragmentos de contenido de Experience Manager {#aem-add}

Después de crear y personalizar los fragmentos de contenido de AEM, ahora puede importarlos a su campaña o recorrido de Recorrido Optimizer.

1. Cree su [campaña](../campaigns/create-campaign.md) o [Recorrido](../building-journeys/journey-gs.md).

1. Para acceder a su fragmento de contenido de AEM, haga clic en ![Personalization icon](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) en cualquier campo de texto o abra el código fuente a través de un componente de contenido de HTML.

   ![](assets/aem_campaign_2.png)

1. En el menú **[!UICONTROL Fragmento de contenido de AEM]** del panel izquierdo, haga clic en **[!UICONTROL Abrir el selector de AEM CF]**.

   ![](assets/aem_campaign_3.png)

1. Seleccione un **[!UICONTROL fragmento de contenido]** de la lista disponible para importarlo al contenido de Journey Optimizer.

1. Haga clic en **[!UICONTROL Mostrar filtros]** para ajustar la lista de fragmentos de contenido.

   De forma predeterminada, el filtro Fragmento de contenido está preestablecido para mostrar solo el contenido aprobado.

   ![](assets/aem_campaign_4.png)

1. Después de seleccionar su **[!UICONTROL fragmento de contenido]**, haga clic en **[!UICONTROL Seleccionar]** para abrirlo.

   ![](assets/aem_campaign_5.png)

1. Haga clic en **[!UICONTROL Ver fragmento]** para mostrar la información del fragmento. Tenga en cuenta que al abrir el menú **[!UICONTROL Información del fragmento]**, el editor se colocará en modo de solo lectura.

   Seleccione **[!UICONTROL Vista previa]** en el menú de la derecha para ver su fragmento en Adobe Experience Manager.

   ![](assets/aem_campaign_7.png)

1. Haga clic en ![Icono de más acciones](assets/do-not-localize/Smock_MoreSmallList_18_N.svg) para acceder al menú avanzado del fragmento:

   * **[!UICONTROL Intercambiar fragmento]**
   * **[!UICONTROL Explorar referencias]**
   * **[!UICONTROL Abrir en AEM]**

   ![](assets/aem_campaign_8.png)

1. Elija los campos que desee de su **[!UICONTROL Fragmento]** para agregarlos al contenido.
   <!--
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.-->

   ![](assets/aem_campaign_6.png)

1. Para habilitar la personalización en tiempo real, el usuario debe declarar explícitamente todos los marcadores de posición utilizados en un **[!UICONTROL fragmento de contenido]** como parámetros en la etiqueta de ayuda de fragmento. Puede asignar estos marcadores de posición a atributos de perfil, atributos contextuales, cadenas estáticas o variables predefinidas mediante los siguientes métodos:

   1. **Asignación de atributos contextuales o de perfil**: asigne el marcador de posición a un perfil o atributo contextual; por ejemplo, name = profile.person.name.firstName.

   1. **Asignación de cadenas estáticas**: asigne un valor de cadena fijo poniéndolo entre comillas dobles, por ejemplo name = &quot;John&quot;.

   1. **Asignación de variables**: Haga referencia a una variable declarada anteriormente en la misma HTML, por ejemplo name = &#39;variableName&#39;.
En este caso, asegúrese de que se ha declarado **_variableName_** antes de agregar el ID de fragmento, utilizando la siguiente sintaxis:

      ```html
      {% let variableName = attribute name %} 
      ```

   En el ejemplo siguiente, el marcador de posición **_name_** está asignado al atributo **_profile.person.name.firstName_** dentro del fragmento.

   ![](assets/aem_campaign_9.png){zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**. Ahora puede probar y comprobar el contenido del mensaje como se detalla en [esta sección](../content-management/preview.md).
Una vez que hayas realizado las pruebas y validado el contenido, puedes [enviar tu campaña](../campaigns/review-activate-campaign.md) o [publicar tu recorrido](../building-journeys/publish-journey.md) a tu audiencia.

Adobe Experience Manager le permite identificar las campañas o recorridos de Journey Optimizer en los que se utiliza un fragmento de contenido. Obtenga más información en [Documentación de Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references).

## Resolución de problemas {#troubleshooting}

Si tiene problemas al trabajar con fragmentos de contenido de Adobe Experience Manager en Journey Optimizer, consulte los siguientes problemas y resoluciones comunes:

| Problema | Causa | Resolución |
|-|-|-|
| **No se encontró la etiqueta** o **El fragmento de contenido no está visible en el selector** | La sintaxis de etiquetas de Adobe Experience Manager no coincide con el formato requerido `ajo-enabled:{OrgId}/{SandboxName}` | Valide que el identificador de etiqueta use **identificador de organización** y **nombre de espacio aislado** correctos. Asegúrese de que no haya espacios ni separadores incorrectos. Vuelva a publicar el fragmento de contenido después de corregir la etiqueta. |
| **El fragmento de contenido no aparece en la lista** | El fragmento de contenido está en estado de borrador o no está aprobado | En el selector de Journey Optimizer solo se muestran los fragmentos de contenido aprobados y publicados. Publique el fragmento de contenido en Adobe Experience Manager y asegúrese de que tiene el estado aprobado. |
| **Error variable sin definir** | Marcador de posición de Personalization no declarado en la etiqueta de ayuda del fragmento | Añada todos los parámetros necesarios en la etiqueta de ayuda del fragmento. Cada marcador de posición utilizado en el fragmento de contenido debe declararse explícitamente con su asignación. |
| **La prueba muestra contenido inesperado** | La revisión utiliza la última versión publicada de Adobe Experience Manager | Las pruebas siempre reflejan la publicación más reciente del fragmento de contenido en Adobe Experience Manager. Si ha realizado cambios recientes en Adobe Experience Manager, vuelva a publicar el fragmento y actualice la revisión. |
| **Error de acceso denegado (CPES)** | Función de usuario no autorizada para acceder a determinados atributos | Póngase en contacto con el administrador del sistema para comprobar que su función tiene los permisos adecuados para el perfil o los atributos contextuales utilizados en la personalización. |
| **El fragmento muestra contenido vacío o ausente** | Faltan parámetros de personalización obligatorios o valores de reserva | Asegúrese de que se proporcionan todos los parámetros necesarios y considere la posibilidad de agregar valores de reserva para atributos opcionales. |

Si el problema persiste, póngase en contacto con su representante de Adobe con detalles sobre el ID del fragmento de contenido, el ID de campaña o recorrido y cualquier mensaje de error que se muestre.
