---
solution: Journey Optimizer
product: journey optimizer
title: Informe de campaña
description: Aprenda a utilizar los datos de correo directo desde el informe de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: b0771fd9-72bd-4891-a394-f08e3dde6126
TQID: https://experienceleague.adobe.com/osXElzbgWRE7mAx4rhJyJfRV7nmBy1EGM9JlS-edLAY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 388
ht-degree: 3%

---

# Informe de campaña de correo directo {#campaign-global-report-cja-direct}

>[!BEGINSHADEBOX]

Puede acceder a su informe de campaña de correo postal haciendo clic en el botón **[!UICONTROL Informes]** de su campaña y después seleccionando **[!UICONTROL Ver informe de todo el tiempo]**. [Más información](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Envío de estadísticas {#sending-statistics-directmail}

![](assets/cja-direct-sending-stat.png)

La tabla **[!UICONTROL Estadísticas de envío]** proporciona un resumen completo de los datos esenciales relacionados con sus campañas de correo postal. Detalla métricas clave como el tamaño de la audiencia objetivo y la cantidad de correo postal entregado correctamente, lo que ofrece valiosas perspectivas sobre la eficacia y el alcance de sus mensajes de correo postal.

+++ Más información sobre el envío de métricas de estadísticas

* **[!UICONTROL Personas]**: Número de perfiles de usuario que se califican como perfiles de destino para sus mensajes.

* **[!UICONTROL Segmentado]**: número de perfiles aptos para la audiencia antes de aplicar las exclusiones, las supresiones o las eliminaciones de consentimiento. En los recorridos con la reentrada habilitada, un perfil se puede definir como objetivo varias veces.

* **[!UICONTROL Envíos]**: Número total de envíos para sus mensajes de correo postal.

* **[!UICONTROL Entregado]**: número de mensajes de correo directo enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores salientes]**: Número total de errores que se produjeron durante el proceso de envío para evitar que se enviara a los perfiles.

* **[!UICONTROL Exclusiones salientes]**: número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

## Estado del envío {#delivery-status-directmail}

![](assets/cja-direct-delivery-status.png)

El gráfico **[!UICONTROL Estado de entrega]** proporciona una vista completa de los datos relacionados con los mensajes de correo postal enviados en su campaña, y ofrece detalles sobre métricas clave como errores y envíos. Esto permite un análisis detallado del proceso de envío de mensajes de correo postal, lo que proporciona información valiosa sobre la eficacia y el rendimiento de sus campañas.

+++ Más información sobre las Métricas de estado de entrega

* **[!UICONTROL Entregado]**: número de mensajes de correo postal enviados correctamente en relación con el número total de mensajes de correo postal enviados.

* **[!UICONTROL Errores salientes]**: Número total de errores que se produjeron durante un proceso de envío que impidió que los mensajes de correo postal se enviaran a los perfiles.

* **[!UICONTROL Exclusiones salientes]**: número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

## Motivos de error {#error-reasons-directmail}

La tabla **[!UICONTROL Motivos del error]** le permite identificar los errores específicos que se produjeron durante el proceso de envío de los mensajes de correo postal, lo que facilita un análisis exhaustivo de los problemas encontrados.

## Motivos excluidos {#exclude-reasons-directmail}

[&#128279;](assets/cja-direct-excluded.png)

La tabla **[!UICONTROL Razones de exclusión]** muestra visualmente los diversos factores que llevaron a la exclusión de perfiles de usuarios de la audiencia de destino, lo que les impidió recibir sus mensajes de correo postal.

Consulte [esta página](exclusion-list.md) para obtener una lista completa de motivos de exclusión.
