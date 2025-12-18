---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos de contenido de AEM
description: Obtenga información sobre cómo acceder y administrar fragmentos de contenido de AEM
topic: Content Management
role: User
level: Beginner
source-git-commit: b06229e7a2fc64fbe28154c798b152cca8203a86
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 6%

---

# Introducción a los fragmentos de contenido de Adobe Experience Manager {#aem-fragments}

Al integrar Adobe Experience Manager as a Cloud Service con Adobe Journey Optimizer, puede incorporar sin problemas los fragmentos de contenido de AEM en el contenido de Journey Optimizer. Esta conexión optimizada simplifica el proceso de acceso y uso del contenido de AEM, lo que permite crear campañas y recorridos personalizados y dinámicos.

Para obtener más información sobre los fragmentos de contenido de AEM, consulte [Trabajar con fragmentos de contenido](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} en la documentación de Experience Manager.

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


### Ciclo de fragmento de contenido

![](assets/do-not-localize/AEM_CF.png)

Los fragmentos de contenido siguen diferentes etapas del ciclo vital según el nivel de Adobe Experience Manager en el que existan. [Obtenga más información en la documentación de Adobe Experience Manager](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

El contenido se crea y administra en el **nivel de creación**, donde los fragmentos pueden tener estados como Nuevo, Borrador, Publicado, Modificado o No publicado. Estos estados se aplican solamente en el **nivel de creación** y admiten la creación y revisión de contenido.

Cuando se publica un fragmento de contenido, se crea una copia en el **nivel de publicación** y se expone a través de un extremo público no autenticado. Journey Optimizer se integra exclusivamente con este **nivel de publicación**.

Como resultado, Journey Optimizer muestra solo fragmentos de contenido publicados o modificados y siempre utiliza la última versión publicada. Los cambios realizados después de la publicación no se reflejarán en Journey Optimizer hasta que se vuelva a publicar el fragmento de contenido.


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
