---
solution: Journey Optimizer
product: journey optimizer
title: Informe de recorrido
description: Aprenda a utilizar los datos directos del informe de recorrido
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 6fae8beb-ca40-40a1-8939-c309fbf46c4f
TQID: https://experienceleague.adobe.com/PJzFoRuT00YI5StKCspzxvklhZKh-53PLDvJjTRuGk4
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
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 401
ht-degree: 3%

---

# Informe de recorrido de correo directo {#journey-global-report}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a leer las métricas de correo postal en el informe de recorrido, incluidas las estadísticas de envío, el estado de envío, los motivos de error y los motivos de exclusión de los mensajes de correo postal.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Puede acceder a su informe de recorrido de correo postal haciendo clic en el botón **[!UICONTROL Ver informe]** del recorrido. [Más información](report-gs-cja.md)

![](assets/report-access-jo.png)

>[!ENDSHADEBOX]

## Envío de estadísticas {#sending-statistics-directmail}

![](assets/cja-direct-sending-stat.png)

La tabla **[!UICONTROL Estadísticas de envío]** le proporciona un insight del rendimiento de sus recorridos de correo postal. Consulte métricas clave como la cantidad de destinatarios objetivo y las piezas enviadas correctamente, lo que le ayuda a medir el alcance y la eficacia de sus envíos de correo.

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

El gráfico **[!UICONTROL Estado de entrega]** proporciona una vista completa de los datos relacionados con los mensajes de correo postal enviados en su recorrido, y ofrece detalles sobre métricas clave como errores y envíos. Esto permite un análisis detallado del proceso de envío de mensajes de correo postal, proporcionando información valiosa sobre la eficacia y el rendimiento de sus recorridos.

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
