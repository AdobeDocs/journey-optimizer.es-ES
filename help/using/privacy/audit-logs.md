---
solution: Journey Optimizer
product: journey optimizer
title: Acciones de auditoría en recursos de Journey Optimizer
description: Obtenga información sobre cómo rastrear acciones ejecutadas en recursos de Journey Optimizer.
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
TQID: https://experienceleague.adobe.com/Usk3qin9P4IZlKw-gEI4zaKO-aRtaKq9-0GMVlOecjA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 100%

---

# Acciones de auditoría en recursos de Journey Optimizer {#track-changes}

## Acerca de los registros de auditoría {#audit-logs}

>[!IMPORTANT]
>
>Para ver y exportar el registro de auditoría, debe tener **[!DNL View User Activity Log]** permiso para hacerlo. [Más información](../administration/ootb-product-profiles.md)

Con Journey Optimizer, puede identificar las acciones ejecutadas por los usuarios en el sistema en distintos servicios y funcionalidades, como recorridos, mensajes, páginas de destino, etc.

Esto le permite aumentar la visibilidad de las actividades realizadas en el sistema, solucionar problemas y ayudar a su empresa a cumplir con las regulaciones y las políticas de administración de datos corporativos..

Cada acción se registra con metadatos en “registros de auditoría” a los que se puede acceder desde Adobe Experience Platform. Para obtener más información sobre los registros de auditoría, incluido cómo verlos y administrarlos en la IU o la API, consulte [ la documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=es).

![](assets/audit-logs.png)

## Tipos de eventos capturados por los registros de auditoría {#events}

La siguiente tabla indica qué acciones y sobre qué recursos de Journey Optimizer se registran en los registros de auditoría. La lista completa de acciones capturadas en los registros de auditoría está disponible en la [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=es#category).

>[!NOTE]
>
>Los registros de auditoría relacionados con la **gestión de decisiones** solo están visibles desde el archivo CSV que se puede descargar mediante el botón **[!UICONTROL Descargar registro]**.

| Recurso | Acción |
|-----------|------------------|
| Campaña de AJO | Creación/eliminación/actualización/activación/detención |
| Configuración general del canal AJO | Creación/eliminación/actualización |
| Grupo de IP de AJO | Creación/eliminación/actualización |
| Página de destino de AJO | Creación/eliminación/actualización/publicación/cancelación de la publicación |
| Plantilla HTML de página de destino de AJO | Creación/eliminación/actualización |
| Ajuste preestablecido de página de destino de AJO | Creación/eliminación/actualización |
| Subdominio de página de destino de AJO | Creación/eliminación/actualización |
| Ajuste preestablecido de mensaje de AJO | Creación/eliminación/actualización |
| Registro de PTR de AJO | Creación/eliminación/actualización |
| Plantilla de expresión guardada de AJO | Creación/eliminación/actualización |
| Credenciales de API de SMS de AJO | Creación/eliminación/actualización |
| Subdominio de AJO | Creación/eliminación/actualización |
| Lista de supresión de AJO | Creación/eliminación/descarga de CSV |
| Grupo de campos | Creación/eliminación/actualización |
| Recorrido | Creación/eliminación/actualización/detención/publicación |
| Acción personalizada de recorrido | Creación/eliminación/actualización |
| Fuente de datos de recorrido | Creación/eliminación/actualización |
| Evento de recorrido | Creación/eliminación/actualización |
| Regla de frecuencia de mensajes | Creación/eliminación/actualización |
| Estrategia de clasificación | Creación/eliminación/actualización |
