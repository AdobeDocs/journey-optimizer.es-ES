---
solution: Journey Optimizer
product: journey optimizer
title: Control de acceso de nivel de objeto
description: Obtenga información sobre el control de acceso de nivel de objeto que le permite definir autorizaciones para administrar el acceso a datos a una selección de objetos
feature: Access Management
topic: Administration
role: Admin, Developer
level: Experienced
keywords: objeto, nivel, acceso, control, etiquetas, olac, autorización
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
feature_v2: id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
subfeature_v2: []
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 1017
ht-degree: 10%

---

# Control de acceso de nivel de objeto {#object-level-access}

>[!BEGINSHADEBOX]

**En esta página:** Use el control de acceso a nivel de objeto para restringir objetos individuales como recorridos, campañas y ofertas con etiquetas de acceso, de modo que pueda mantener el contenido confidencial y los datos personales limitados a los usuarios autorizados.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Etiquetas de administración de acceso"
>abstract="Puede limitar el acceso a un objeto en función de las etiquetas de acceso. Este enfoque protege los recursos digitales confidenciales de los usuarios no autorizados y garantiza una mayor protección de los datos personales. **Asegúrese de seleccionar solo las etiquetas para las que tenga permiso.**"

Puede limitar el acceso a un objeto en función de las etiquetas de acceso. Este enfoque protege los recursos digitales confidenciales de los usuarios no autorizados y garantiza una mayor protección de los datos personales.

La capacidad Control de acceso a nivel de objeto (OLAC) permite definir autorizaciones para administrar el acceso a datos para una selección de objetos:

* Recorrido
* Campaign
* Plantilla
* Fragmento
* Landing page
* Oferta
* Colección de ofertas estáticas
* Decisión de oferta
* Configuración de canal
* plan de calentamiento de IP


## Requisitos previos {#prereq-labels}

Para poder [crear etiquetas](#create-labels), debe pertenecer a un rol con el permiso **[!UICONTROL Administrar etiquetas de uso]**.

Para poder [asignar etiquetas](#assign-labels), debe pertenecer a un rol con el permiso **Administrar**, es decir, [!DNL Manage journeys], [!DNL Manage Campaigns] o [!DNL Manage decisions]. Sin este permiso, el botón **[!UICONTROL Administrar acceso]** aparece atenuado.

Puede obtener más información sobre permisos en [esta sección](../administration/permissions.md).

## Creación de etiquetas {#create-labels}

Las **[!UICONTROL etiquetas]** le permiten categorizar conjuntos de datos y campos según las políticas de uso que se aplican a esos datos. **[!UICONTROL Las etiquetas]** se pueden aplicar en cualquier momento, lo que proporciona flexibilidad en la forma en que se gestionan los datos.

Utilice etiquetas para proporcionar acceso a los usuarios y aplicar políticas de consentimiento y gobernanza de datos. Estas etiquetas de gobernanza pueden afectar al consumo descendente.

Puede crear etiquetas en el producto [!DNL Permissions]. Para obtener más información, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html){target="_blank"}.

También puede crear **[!UICONTROL Etiquetas]** directamente en Journey Optimizer. Para crear una etiqueta, siga estos pasos:

1. Desde un objeto de Adobe Journey Optimizer, como una **[!UICONTROL Campaña]** recién creada, haz clic en el botón **[!UICONTROL Administrar acceso]**.

   ![Botón Administrar acceso en Adobe Journey Optimizer](assets/olac_1.png)

1. En la ventana **[!UICONTROL Administrar acceso]**, haga clic en **[!UICONTROL Crear etiqueta]**.

   ![](assets/olac_2.png)

1. Configure la etiqueta. Debe especificar:

   * **[!UICONTROL Nombre]**
   * **[!UICONTROL Nombre descriptivo]**
   * **[!UICONTROL Descripción]**

   ![Campos de configuración de etiquetas](assets/olac_3.png)

1. Haga clic en **[!UICONTROL Crear]** para guardar la **[!UICONTROL etiqueta]**.

La **[!UICONTROL etiqueta]** recién creada ya está disponible en la lista. Si es necesario, puede modificarlo en el producto [!DNL Permissions].

## Asignar etiquetas {#assign-labels}

Para asignar etiquetas de uso de datos personalizadas o principales a los objetos de Journey Optimizer:

1. Desde un objeto de Adobe Journey Optimizer, como una **[!UICONTROL Campaña]** recién creada, haz clic en el botón **[!UICONTROL Administrar acceso]**.

   ![Botón Administrar acceso en Adobe Journey Optimizer](assets/olac_1.png)

1. En la ventana **[!UICONTROL Administrar acceso]**, seleccione las etiquetas personalizadas o de uso de datos principales para administrar el acceso a este objeto.

   Para obtener más información sobre las etiquetas de uso de datos principales, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=es){target="_blank"}.

   ![](assets/olac_4.png)

1. Haga clic en **[!UICONTROL Guardar]** para aplicar esta restricción de etiqueta.

Para tener acceso a este objeto, los usuarios deben tener la **[!UICONTROL Etiqueta]** específica incluida en sus **[!UICONTROL Roles]**. Por ejemplo, un usuario con la etiqueta C1 solo tendrá acceso a objetos con etiquetas C1 o sin etiquetas.

Para obtener más información sobre cómo asignar una **[!UICONTROL etiqueta]** a un **[!UICONTROL rol]**, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role){target="_blank"}.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** El control de acceso de nivel de objeto (OLAC) le permite aplicar etiquetas de acceso a objetos específicos de Journey Optimizer, como recorridos, campañas y ofertas, de modo que sólo los usuarios cuya función incluya la etiqueta coincidente pueden ver esos objetos o interactuar con ellos.

**Intenciones:**

* Cree una etiqueta de acceso personalizada directamente en Journey Optimizer o a través del producto Permisos
* Asignar etiquetas de acceso a objetos de Journey Optimizer (recorridos, campañas, ofertas, etc.)
* Restringir contenido confidencial únicamente a usuarios autorizados
* Comprender qué permisos son necesarios para crear y asignar etiquetas

**Glosario:**

* **OLAC (control de acceso de nivel de objeto)**: capacidad para definir autorizaciones para administrar el acceso a datos para una selección de objetos Journey Optimizer específicos *(específicos del producto)*
* **Etiqueta**: etiqueta aplicada a un objeto para categorizarlo por directiva de uso y restringir el acceso según la pertenencia a funciones *(específica del producto)*
* **Administrar acceso**: botón o interfaz disponible en objetos Journey Optimizer admitidos para crear y asignar etiquetas de acceso *(específicas del producto)*
* **Etiquetas de uso de datos principales**: etiquetas predefinidas proporcionadas por Adobe Experience Platform, a diferencia de las etiquetas personalizadas creadas por la organización *(específicas del producto)*

**Protecciones:**

* La creación de etiquetas requiere el permiso **Administrar etiquetas de uso** (requisito previo)
* La asignación de etiquetas requiere un permiso **Administrar** para el tipo de objeto (por ejemplo, Administrar recorridos, Administrar campañas o Administrar decisiones); sin él, el botón **Administrar acceso** aparece atenuado (requisito previo)
* Objetos admitidos para las etiquetas OLAC: Recorrido, Campaña, Plantilla, Fragmento, Página de aterrizaje, Oferta, Colección de ofertas estáticas, Decisión de oferta, Configuración de canal, Plan de calentamiento de IP

**Terminología:**

* Nombre canónico: Control de acceso de nivel de objeto — Acrónimo: OLAC — variantes: control de acceso basado en objetos, administración de acceso basado en objetos
* No confunda: OLAC (restringe el acceso a objetos AJO específicos como recorridos y campañas mediante etiquetas) ≠ ABAC (basado en atributos, aplica políticas de etiquetas a campos de esquema, conjuntos de datos y audiencias a nivel de plataforma)
* No confunda: &quot;etiquetas de uso de datos principales&quot; (etiquetas creadas previamente desde Adobe Experience Platform) ≠ &quot;etiquetas personalizadas&quot; (etiquetas creadas por la organización)

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Puedo crear una etiqueta directamente en Journey Optimizer sin ir al producto Permisos?** — Sí; utilice la ventana Administrar acceso en cualquier objeto compatible y haga clic en Crear etiqueta.
* **Q: ¿Qué tipos de objeto admiten etiquetas OLAC?** — Recorrido, campaña, plantilla, fragmento, página de aterrizaje, oferta, colección de ofertas estáticas, decisión de oferta, configuración de canal y plan de calentamiento de IP.
* **Q: ¿Qué permiso se necesita para asignar una etiqueta a un recorrido?** — el permiso Administrar recorridos; sin permiso Administrar, el botón Administrar acceso aparece atenuado.
* **Q: si un usuario sólo tiene la etiqueta C1 en su rol, ¿a qué objetos puede tener acceso?** — Sólo objetos etiquetados o sin etiquetar C1.

+++
<!-- ai-accordion-version: 1 | source-hash: 4e9b2577 -->
