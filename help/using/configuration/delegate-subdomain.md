---
title: Delegar subdominios
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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: a174944bb8efcb67d758d4fe215674c1b8bbee13
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 6%

---

# Delegar un subdominio

La delegación de nombres de dominio es un método que permite al propietario de un nombre de dominio (técnicamente: una zona DNS) para delegar una subdivisión de ella (técnicamente: una zona DNS bajo ella, que puede llamarse subzona) a otra entidad. Básicamente, como cliente, si está administrando la zona &quot;example.com&quot;, puede delegar la subzona &quot;marketing.example.com&quot; a Adobe.

Delegando un subdominio para usar con [!DNL Journey Optimizer], los clientes pueden confiar en el Adobe para mantener la infraestructura DNS necesaria para cumplir los requisitos de envío estándar del sector para sus dominios de envío de marketing por correo electrónico, a la vez que mantienen y controlan el DNS para sus dominios de correo electrónico internos.

[!DNL Journey Optimizer] le permite delegar completamente los subdominios a Adobes directamente desde la interfaz de producto. Al hacerlo, Adobe podrá enviar mensajes como un servicio administrado controlando y manteniendo todos los aspectos de DNS necesarios para la entrega, el procesamiento y el seguimiento de campañas de correo electrónico.

>[!NOTE]
>
>De forma predeterminada, [!DNL Journey Optimizer] contrato de licencia le permite delegar hasta 10 subdominios. Póngase en contacto con el Adobe si desea aumentar esta limitación.
>
>Journey Optimizer no admite actualmente el uso de CNAME para la delegación de subdominios.

Para delegar un nuevo subdominio, siga los pasos a continuación:

1. Acceda a la **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** a continuación, haga clic en **[!UICONTROL Delegate subdomain]**.

   ![](../assets/subdomain-delegate.png)

1. Especifique el nombre del subdominio que desea delegar.

   ![](../assets/subdomain-name.png)

   >[!CAUTION]
   >
   >No se permite delegar un subdominio no válido al Adobe. Asegúrese de introducir un subdominio válido que sea propiedad de su organización, como marketing.yourcompany.com.
   >
   >Tenga en cuenta que los subdominios de varios niveles, como email.marketing.yourcompany.com , no son compatibles actualmente.

1. Se muestra la lista de registros que se van a colocar en los servidores DNS. Copie estos registros, uno por uno o descargando un archivo CSV, y luego vaya a la solución de alojamiento de dominios para generar los registros DNS coincidentes.

1. Asegúrese de que todos los registros DNS se hayan generado en la solución de alojamiento de dominios. Si todo está configurado correctamente, marque la casilla &quot;Confirmo...&quot; y luego haga clic en **[!UICONTROL Submit]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Puede crear los registros y enviar la configuración del subdominio más adelante utilizando la variable **[!UICONTROL Save as draft]** botón. A continuación, podrá reanudar la delegación de subdominios abriéndola en la lista de subdominios.

1. Una vez enviada la delegación de subdominios, el subdominio se muestra en la lista con la variable **[!UICONTROL Processing]** estado. Para obtener más información sobre los estados de los subdominios, consulte [esta sección](access-subdomains.md).

   ![](../assets/subdomain-processing.png)

   Antes de poder utilizar ese subdominio para enviar mensajes, debe esperar hasta que el Adobe realice las comprobaciones necesarias, que pueden tardar hasta tres horas. Obtenga más información en [esta sección](#subdomain-validation).

1. Una vez realizadas las comprobaciones correctamente, el subdominio recibe la variable **[!UICONTROL Success]** estado. Está listo para utilizarse para enviar mensajes.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)

## Validación de subdominios {#subdomain-validation}

Las comprobaciones y acciones siguientes se realizarán hasta que se verifique el subdominio y se puedan utilizar para enviar mensajes.

>[!NOTE]
>
>Estos pasos se realizan por Adobe y pueden tardar hasta 3 horas.

1. **Validación previa**: Adobe comprueba si el subdominio se ha delegado a DNS de Adobe (registro NS, registro SOA, configuración de zona, registro de propiedad). Si el paso de prevalidación falla, se devuelve un error junto con el motivo correspondiente; de lo contrario, el Adobe pasa al siguiente paso.

1. **Configuración de DNS para el dominio**:

   * **Registro MX**: Registro eXchange de correo: registro del servidor de correo que procesa los correos electrónicos entrantes enviados al subdominio.
   * **Registro SPF**: Registro del marco de políticas del remitente : enumera las direcciones IP de los servidores de correo que pueden enviar correos electrónicos desde el subdominio.
   * **Registro DKIM**: Registro estándar de Correo identificado de DomainKeys : Utiliza el cifrado de clave pública y privada para autenticar el mensaje y evitar la suplantación.
   * **A**: Asignación de IP predeterminada.

1. **Creación de direcciones URL de seguimiento y de reflejo**: si el dominio es email.example.com, el dominio tracking/mirror será data.email.example.com. Se asegura instalando el certificado SSL.

1. **Aprovisionar CDN CloudFront**: si CDN no está configurado, Adobe lo aprovisiona para la impresión.

1. **Crear dominio de CDN**: si el dominio es email.example.com, el dominio de CDN será cdn.email.example.com.

1. **Crear y adjuntar un certificado SSL de CDN**: Adobe crea el certificado de CDN para el dominio de CDN y adjunta el certificado al dominio de CDN.

1. **Crear DNS de reenvío**: si este es el primer subdominio que delega, Adobe creará el DNS de reenvío necesario para crear registros PTR, uno para cada una de sus IP.

1. **Crear registro PTR**: Los ISP requieren el registro PTR, también conocido como registro DNS inverso, para que no marquen los correos electrónicos como correo no deseado. Gmail también recomienda tener registros PTR para cada IP. Adobe crea registros PTR solo cuando delega el primer subdominio, uno para cada IP, todas las IP que apuntan al primer subdominio. Por ejemplo, si la IP es *192.1.2.1* y el subdominio es *email.example.com*, el registro PTR será: *192.1.2.1 PTR r1.email.example.com*. Puede actualizar el registro PTR posteriormente para que apunte al nuevo dominio delegado.
