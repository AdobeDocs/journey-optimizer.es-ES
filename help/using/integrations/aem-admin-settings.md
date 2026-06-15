---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del repositorio de AEM
description: Descubra cómo los administradores configuran los repositorios de AEM, los dominios personalizados, la publicación autenticada y el acceso a fragmentos de contenido solo de autor en Journey Optimizer.
feature: Integrations
topic: Administration
role: Admin
level: Experienced
hide: true
keywords: AEM, Fragmentos de contenido, administración, repositorio, autenticación, autor, publicación
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
source-git-commit: 7cf2235a14f9ebb49fac02161743f75fee141504
workflow-type: tm+mt
source-wordcount: 467
ht-degree: 0%

---

# Configuración del acceso al repositorio de Adobe Experience Manager {#aem-admin-settings}

>[!BEGINSHADEBOX]

**En esta página:** Descubra cómo los administradores conectan una zona protegida a un repositorio de Adobe Experience Manager (configurando acceso de solo autor o publicación, dominios personalizados y autenticación) para que los especialistas en marketing puedan utilizar fragmentos de contenido de AEM en sus recorridos y campañas.

>[!ENDSHADEBOX]

Adobe Journey Optimizer se integra con **[!DNL Adobe Experience Manager as a Cloud Service]** para que pueda usar **Fragmentos de contenido** en Recorridos y campañas. Los **fragmentos de contenido** se leen desde el repositorio de publicación de Adobe Experience Manager de forma predeterminada, los administradores pueden cambiar a solo autor o ajustar el acceso de publicación en el menú **[!UICONTROL Integración de AEM]**.

➡️ Cuando el repositorio esté configurado, continúe con [Trabajar con fragmentos de contenido de Experience Manager](../integrations/aem-fragments.md) para las tareas de creación y selección en Journey Optimizer.

## Configuración de repositorios {#configure-ui}

>[!NOTE]
>
> **[!UICONTROL La integración de AEM]** guarda la configuración del repositorio **por zona protegida**. Cada zona protegida mantiene sus propias integraciones y no se aplican a todas ellas.

Journey Optimizer almacena una integración por organización, zona protegida y repositorio de Adobe Experience Manager. Si guarda una nueva integración para esa misma combinación y reemplaza la configuración anterior, solo se conserva la configuración más reciente.

Para configurar el repositorio:

1. Acceda a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Integración de AEM]**.

1. Haga clic en **[!UICONTROL Crear integración]**.

   ![](assets/aem-admin-settings-1.png)

1. Si usa **[!DNL Adobe Experience Manager Managed Services]**, escriba un nombre de host del repositorio que termine con `adobecqms.net` en el campo **[!UICONTROL Identificador de repositorio de AMS personalizado]**.

   ![](assets/aem-admin-settings-6.png)

1. Elija qué repositorio configurar y haga clic en **[!UICONTROL Siguiente]**.

   Además, puede hacer clic en **[!UICONTROL Ver]** para obtener acceso a este repositorio.

   >[!IMPORTANT]
   >
   >Al guardar una nueva configuración para la misma organización, zona protegida y repositorio **se reemplaza** la configuración predeterminada, es decir, el repositorio **publish**.

   ![](assets/aem-admin-settings-2.png)

1. Escriba un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]**.

1. Elija su configuración:

   +++ Configuración de solo autor

   Seleccione **[!UICONTROL Configuración de solo autor]** cuando Journey Optimizer solo deba leer fragmentos de contenido del entorno de Adobe Experience Manager **autor**. No se admite la replicación desde el autor a la publicación y las actualizaciones de publicación en directo.

   ![](assets/aem-admin-settings-3.png)

   +++

   +++ Configuración de instancia de publicación

   1. Seleccione **[!UICONTROL Configuración de instancia de publicación]** para activar la configuración de instancia de publicación.

      ![](assets/aem-admin-settings-4.png)

   1. Si lo desea, habilite **[!UICONTROL Enviar token a la instancia de publicación]** para que las credenciales del servicio se incluyan en las solicitudes a la instancia de publicación.

   1. Pegue una **[!UICONTROL credencial de servicio JSON]** válida para la autenticación.

   1. Opcionalmente, proporcione un dominio personalizado si su organización no puede alcanzar el host de publicación predeterminado de AEM (`publish-XX-XX.adobeaemcloud.com`) para recuperar contenido.

      ![](assets/aem-admin-settings-5.png)

   +++

1. Después de finalizar la configuración de la instancia, elija un fragmento de contenido para confirmar que la integración funciona.

   ![](assets/aem-admin-settings-7.png)

1. En la ventana **Asesor de contenido**, seleccione el fragmento que desee probar y, a continuación, haga clic en **[!UICONTROL Seleccionar]**.

1. Haga clic en **[!UICONTROL Save]**.

1. Al guardar con un fragmento de contenido de prueba seleccionado, la validación se ejecuta automáticamente. Si la validación falla, se muestra una lista de errores para que pueda corregir la configuración.

   ![](assets/aem-admin-settings-8.png)

1. Para editar o deshabilitar esta integración del repositorio, acceda a la configuración creada anteriormente desde el menú **[!UICONTROL Integración con AEM]**.

Al guardar esta configuración, Journey Optimizer la almacena para ese repositorio en la zona protegida actual. A continuación, puede usar ese repositorio y su configuración al examinar y seleccionar contenido en el selector **Asesor de contenido**.

