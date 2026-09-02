---
solution: Journey Optimizer
product: journey optimizer
title: Defina las propiedades de campaña activadas por API
description: Obtenga información sobre cómo definir las propiedades de campaña activadas por API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campañas, activadas por API, REST, optimizador, mensajes
exl-id: bda7e337-a246-4f01-b935-4a234d4c4baa
TQID: https://experienceleague.adobe.com/qUWCJifjUbLmapOtZlk9elkRZLcr-XGXNzuy0rayx-8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: a5c0537a45acbc708ce62bd05a569630230201ac
workflow-type: tm+mt
source-wordcount: 330
ht-degree: 18%

---

# Defina las propiedades de campaña activadas por API {#api-properties}

>[!BEGINSHADEBOX]

**En esta página:** Cree una campaña desencadenada por API y establezca su tipo, nombre, etiquetas y etiquetas de acceso para que tenga un ámbito correcto y sea fácil de encontrar desde el principio.

>[!ENDSHADEBOX]

Para crear una nueva campaña activada por API, siga estos pasos:

1. Vaya al menú **[!UICONTROL Campañas]** y seleccione la pestaña **[!UICONTROL API activada]**.

1. Haga clic en el botón **[!UICONTROL Crear campaña]** y seleccione el tipo de campaña:

   * **[!UICONTROL Activado por API - Marketing]** - Seleccione este tipo de campaña activada por API para enviar comunicaciones de marketing personalizadas a audiencias de destino.

   * **[!UICONTROL Activado por API - Transaccional]** - Las campañas transaccionales están destinadas a enviar mensajes transaccionales, es decir, mensajes enviados después de una acción realizada por un individuo: solicitud de restablecimiento de contraseña, compra en el carro de compras, etc.

     +++Modo de alto rendimiento

     Para las campañas transaccionales activadas por API, puede habilitar el modo **[!UICONTROL Alto rendimiento]**. Este modo está diseñado para mensajes a gran escala en tiempo real (hasta 5000 transacciones por segundo) y proporciona una mayor disponibilidad con una latencia más baja. [Aprenda a trabajar con el modo de alto rendimiento](../campaigns/api-triggered-high-throughput.md)

     >[!AVAILABILITY]
     >
     >Actualmente, el modo de alto rendimiento solo está disponible para el canal de correo electrónico y en la región de EE. UU.
     >
     >Esta funcionalidad solo está disponible para las organizaciones que hayan adquirido la oferta del complemento **Mensajería transaccional de alto rendimiento** de Adobe. Póngase en contacto con su representante de Adobe para obtener más información.

     +++

   ![](assets/api-triggered-modal.png)

1. En la ficha **[!UICONTROL Propiedades]**, escriba un nombre y una descripción para la campaña.

   ![](assets/create-campaign-properties.png)

1. Utilice el campo **Etiquetas** para asignar etiquetas unificadas de Adobe Experience Platform a su campaña. Esto le permite clasificarlos fácilmente y mejorar la búsqueda desde la lista de campañas. [Descubra cómo trabajar con etiquetas](../start/search-filter-categorize.md#tags).

1. Puede limitar el acceso a esta campaña en función de las etiquetas de acceso. Para añadir una limitación de acceso, vaya al botón **[!UICONTROL Administrar acceso]** en la parte superior de esta página. Asegúrese de seleccionar solo las etiquetas para las que tenga permiso. [Más información acerca del Control de acceso de nivel de objeto](../administration/object-based-access.md).

## Próximos pasos {#next}

Una vez que la configuración y el contenido de la campaña estén listos, puede configurar su acción. [Más información](api-triggered-campaign-action.md)
