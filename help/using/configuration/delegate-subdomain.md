---
title: Delegación de subdominios
description: Obtenga información sobre cómo delegar subdominios
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: e569e992530df5429ffb96f78ba28b53de0ded81
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 8%

---


# Delegación de un subdominio

La delegación de nombres de dominio es un método que permite al propietario de un nombre de dominio (técnicamente: una zona DNS) para delegar una subdivisión de ella (técnicamente: una zona DNS bajo ella, que puede llamarse subzona) a otra entidad. Básicamente, si un cliente está manejando la zona &quot;example.com&quot;, puede delegar la subzona &quot;marketing.example.com&quot; a Adobe.

Al delegar un subdominio para utilizarlo con Adobe Optimizer, los clientes pueden confiar en el Adobe para mantener la infraestructura DNS necesaria para cumplir los requisitos de entrega estándar del sector para sus dominios de envío de marketing por correo electrónico, a la vez que mantienen y controlan el DNS para sus
dominios de correo electrónico internos.

Journey Optimizer le permite delegar completamente sus subdominios a Adobe. Al hacerlo, Adobe podrá enviar mensajes como un servicio administrado controlando y manteniendo todos los aspectos de DNS necesarios para la entrega, el procesamiento y el seguimiento de campañas de correo electrónico.

>[!NOTE]
>
>De forma predeterminada, el contrato de licencia [!DNL Journey Optimizer] permite delegar hasta 10 subdominios. Póngase en contacto con el Adobe si desea aumentar esta limitación.
>
>Journey Optimizer no admite actualmente el uso de CNAME para la delegación de subdominios.

Para delegar un nuevo subdominio, siga los pasos a continuación:

1. Acceda al menú **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** y haga clic en **[!UICONTROL Delegate subdomain]**.

   ![](../assets/subdomain-delegate.png)

1. Especifique el nombre del subdominio que desea delegar.

   ![](../assets/subdomain-name.png)

1. Se muestra la lista de registros que se van a colocar en los servidores DNS. Copie estos registros, uno por uno o descargando un archivo CSV, y luego vaya a la solución de alojamiento de dominios para generar los registros DNS coincidentes.

   Asegúrese de que todos los registros DNS se hayan generado en la solución de alojamiento de dominios. Si todo está configurado correctamente, marque la casilla &quot;I confirm...&quot; y luego haga clic en **[!UICONTROL Submit]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Puede crear los registros y enviar la configuración del subdominio más adelante con el botón **[!UICONTROL Save as draft]**. A continuación, podrá reanudar la delegación de subdominios abriéndola en la lista de subdominios.

1. Una vez enviada la delegación de subdominios, el subdominio se muestra en la lista con el estado **[!UICONTROL Processing]**. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](access-subdomains.md).

   Las comprobaciones y acciones siguientes se realizarán hasta que se verifique el subdominio y se puedan utilizar para enviar mensajes.

   Este paso se realiza por Adobe y puede tardar hasta 3 horas.

   1. Compruebe si el subdominio se ha delegado a DNS de Adobe (registro NS, registro SOA, configuración de zona, registro de propiedad),
   1. Configurar DNS para el dominio,
   1. Cree direcciones URL de seguimiento y de reflejo,
   1. Aprovisionar el frontal de la nube de CDN,
   1. Crear, validar y adjuntar certificado SSL de CDN,
   1. Crear DNS de reenvío,
   1. Crear registro PTR.

   ![](../assets/subdomain-processing.png)

1. Una vez realizadas las comprobaciones correctamente, el subdominio obtiene el estado **[!UICONTROL Success]**. Está listo para utilizarse para enviar mensajes.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)


