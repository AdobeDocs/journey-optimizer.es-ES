---
solution: Journey Optimizer
product: journey optimizer
title: Acceder a subdominios delegados
description: Obtenga información sobre cómo acceder a los subdominios delegados.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: cb3248c5-f444-47aa-80b2-c1a9fbebfcc0
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 4%

---

# Acceder a subdominios delegados {#access-delegated-subdomains}

Todos los subdominios delegados se muestran en la sección **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Subdominios]** para abrir el Navegador. Los filtros están disponibles para ayudarle a refinar la lista (fecha de delegación, usuario o estado).

![](assets/subdomain-list.png)

La variable **[!UICONTROL Estado]** proporciona información sobre el proceso de delegación de subdominios:

* **[!UICONTROL Borrador]**: La delegación de subdominios se ha guardado como borrador. Haga clic en el nombre del subdominio para reanudar el proceso de delegación.
* **[!UICONTROL Procesamiento]**: El subdominio está pasando por varias comprobaciones de configuración antes de poder utilizarlo,
* **[!UICONTROL Correcto]**: El subdominio ha pasado por las comprobaciones correctamente y puede utilizarse para enviar mensajes,
* **[!UICONTROL Error]**: Una o varias comprobaciones han fallado después de enviar la delegación de subdominios.

Para acceder a información detallada sobre un subdominio con la variable **[!UICONTROL Correcto]** , ábralo desde la lista.

![](assets/subdomain-delegated.png)

Puede hacer lo siguiente:

* Recupere el nombre de subdominio (solo lectura) configurado durante el proceso de delegación, así como las direcciones URL generadas (recursos, páginas espejo, URL de seguimiento).

* Agregue un registro TXT de verificación de sitio de Google al subdominio para asegurarse de que esté verificado (consulte [Añadir un registro TXT de Google a un subdominio](google-txt.md)).


>[!CAUTION]
>
>La configuración del subdominio es común a todos los entornos. Por lo tanto, cualquier modificación en un subdominio también afectará a los entornos limitados de producción.
