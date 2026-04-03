---
solution: Journey Optimizer
product: journey optimizer
title: Consideraciones y solución de problemas sobre fragmentos de contenido de Adobe Experience Manager
description: Consideraciones y problemas comunes para los fragmentos de contenido de AEM en Journey Optimizer.
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# Consideraciones y solución de problemas {#aem-fragments-limitations}

## Consideraciones clave {#considerations}

Tenga en cuenta lo siguiente al utilizar fragmentos de contenido de [!DNL Adobe Experience Manager] en [!DNL Journey Optimizer]:

* **Tipos de fragmentos de contenido**
   * Se admiten fragmentos de contenido simples, fragmentos de contenido anidados y **variaciones de fragmentos de contenido**. Elija la variación cuando inserte el fragmento en [!DNL Journey Optimizer]. Si no selecciona ninguna variación, se utilizará la variación **Principal** (el contenido principal del fragmento en [!DNL Adobe Experience Manager]).

* **Contenido multilingüe**
   * Cada variación debe ser creada, etiquetada y publicada en [!DNL Adobe Experience Manager]. En [!DNL Journey Optimizer], seleccione la variación del fragmento que coincida con cada idioma o configuración regional del mensaje.
   * No hay resolución automática de idioma ni alternativa entre las variaciones.

* **Acceso al repositorio**
   * [!DNL Journey Optimizer] se integra con el nivel [!DNL Adobe Experience Manager] **Publicar** solamente (Sitios, Fragmentos de contenido). Los fragmentos de contenido están disponibles a través de un extremo público no autenticado.
   * Los repositorios de creación pueden aparecer en el selector de repositorios, pero solo los fragmentos publicados en **Publish** se pueden usar en [!DNL Journey Optimizer].

* **Estado del fragmento de contenido**
   * Los fragmentos pueden mostrar el estado **[!UICONTROL Publicado]** o **[!UICONTROL Modificado]**; [!DNL Journey Optimizer] siempre usa la **última versión publicada**.
   * Los cambios realizados después de la publicación no se reflejarán en [!DNL Journey Optimizer] hasta que el fragmento se vuelva a publicar en [!DNL Adobe Experience Manager]. No existe una conciliación automática de versiones entre los dos productos.

* **Personalización**
   * Admitido: atributos de perfil, atributos contextuales, cadenas estáticas y variables predeclaradas.
   * No admitido: atributos derivados o calculados.

* **Actualizaciones y versiones**
   * Las actualizaciones requieren la republicación manual de [!DNL Adobe Experience Manager]. No hay reconciliación automática de versiones.
   * Cuando se publica o vuelve a publicar un fragmento de contenido en [!DNL Adobe Experience Manager], [!DNL Journey Optimizer] actualiza ese fragmento y **todas las variaciones de ese fragmento a las que se hace referencia** en campañas o recorridos activos.
   * La [!DNL Adobe Experience Manager] [acción de publicación](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/manage/manage-publication) se puede retrasar. Una vez finalizado, [!DNL Journey Optimizer] recibe un evento y actualiza el contenido.
   * Después de una actualización correcta, los cambios suelen estar disponibles en unos **5 minutos** para los recorridos unitarios y en el **siguiente lote** para los casos de uso por lotes.

* **Almacenamiento en caché y revisión**
   * Cuando se agrega un fragmento por primera vez a una campaña o recorrido, [!DNL Journey Optimizer] lo almacena en caché. Si selecciona un fragmento que ya se usó en otra parte mediante **[!UICONTROL Abrir el selector de AEM CF]**, se cargará desde la caché de [!DNL Journey Optimizer].
   * Después de volver a publicar un fragmento modificado en [!DNL Adobe Experience Manager], [!DNL Journey Optimizer] escucha el evento y actualiza la caché.
   * Las revisiones siempre reflejan la **última versión publicada**; no puede bloquear versiones históricas para revisiones.

## Solución de problemas {#troubleshooting}

Si tiene problemas al trabajar con fragmentos de contenido de Adobe Experience Manager en Journey Optimizer, consulte los siguientes problemas y resoluciones comunes:

| Problema | Causa | Resolución |
|-|-|-|
| **No se encontró la etiqueta** o **El fragmento de contenido no está visible en el selector** | La sintaxis de etiquetas de Adobe Experience Manager no coincide con el formato requerido `ajo-enabled:{OrgId}/{SandboxName}` | Valide que el identificador de etiqueta use **identificador de organización** y **nombre de espacio aislado** correctos. Asegúrese de que no haya espacios ni separadores incorrectos. Vuelva a publicar el fragmento de contenido después de corregir la etiqueta. |
| **El fragmento de contenido no aparece en la lista** | El fragmento de contenido está en estado de borrador o no se ha publicado | En el selector de Journey Optimizer solo se muestran los fragmentos de contenido aprobados y publicados. Publique el fragmento de contenido en Adobe Experience Manager y asegúrese de que tiene el estado publicado. |
| **Error variable sin definir** | Marcador de posición de Personalization no declarado en la etiqueta de ayuda del fragmento | Añada todos los parámetros necesarios en la etiqueta de ayuda del fragmento. Cada marcador de posición utilizado en el fragmento de contenido debe declararse explícitamente con su asignación. |
| **La prueba muestra contenido inesperado** | La revisión utiliza la última versión publicada de Adobe Experience Manager | Las pruebas siempre reflejan la publicación más reciente del fragmento de contenido en Adobe Experience Manager. Si ha realizado cambios recientes en Adobe Experience Manager, vuelva a publicar el fragmento y actualice la revisión. |
| **Error de acceso denegado (CPES)** | Función de usuario no autorizada para acceder a determinados atributos | Póngase en contacto con el administrador del sistema para comprobar que su función tiene los permisos adecuados para el perfil o los atributos contextuales utilizados en la personalización. |
| **El fragmento muestra contenido vacío o ausente** | Faltan parámetros de personalización obligatorios o valores de reserva | Asegúrese de que se proporcionan todos los parámetros necesarios y considere la posibilidad de agregar valores de reserva para atributos opcionales. |
| **La imagen no se representa o parece dañada** | La URL de imagen en el fragmento de contenido es una ruta relativa o no accesible desde el canal | Use **direcciones URL absolutas** (`https://...`) para los campos de imagen. No se admiten rutas relativas de Adobe Experience Manager. Confirme la URL en un navegador o en la vista previa del mensaje. |
| **El vínculo de Experience League AEM devuelve el valor 404** | Marcador antiguo, versión de vista previa o página de ayuda de AEM sin publicar | Abra el tema [Fragmentos de contenido con Adobe Journey Optimizer](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} de la documentación activa de Experience Manager y navegue desde la tabla de contenido en la página o busque el nombre de la sección (por ejemplo **Configuración de Dispatcher**). |

Si el problema persiste, póngase en contacto con su representante de Adobe con detalles sobre el ID del fragmento de contenido, el ID de campaña o recorrido y cualquier mensaje de error que se muestre.
