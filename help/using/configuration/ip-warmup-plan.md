---
solution: Journey Optimizer
product: journey optimizer
title: Creación de un plan de calentamiento de IP
description: Obtenga información sobre cómo crear un plan de calentamiento de IP en Journey Optimizer
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, grupo, subdominios, capacidad de entrega
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: 2060b18bfcc62e02127776f05de1448378a7a06a
workflow-type: tm+mt
source-wordcount: '1558'
ht-degree: 6%

---

# Creación de un plan de calentamiento de IP {#ip-warmup}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción al calentamiento de IP](ip-warmup-gs.md)
* [Creación de campañas de calentamiento de IP](ip-warmup-campaign.md)
* **[Crear un plan de calentamiento de IP](ip-warmup-plan.md)**
* [Ejecución del plan de calentamiento de IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Una vez que haya creado una o más [Campañas de calentamiento de IP](ip-warmup-campaign.md) con una superficie dedicada y la opción correspondiente habilitada, puede empezar a crear su plan de calentamiento de IP.

Para acceder, crear, editar y eliminar los planes de calentamiento de IP, debe tener **[!UICONTROL Consultor de capacidad de entrega]** función o planes de calentamiento de IP permisos relacionados.

+++Obtenga información sobre cómo asignar la función de consultor de capacidad de entrega o los permisos relacionados con los planes de calentamiento de IP

Para asignar el permiso correspondiente a un elemento específico **[!UICONTROL Rol]**:

1. Desde el [!DNL Permissions] producto, vaya a la **[!UICONTROL Funciones]** y seleccione la función que desea actualizar con el nuevo **[!UICONTROL Configuraciones de calentamiento de IP]** permisos.

1. De su **[!UICONTROL Rol]** panel, haga clic en **[!UICONTROL Editar]**.

   ![](assets/ip_permissions_1.png)

1. Arrastre y suelte el **[!UICONTROL Configuraciones de calentamiento de IP]** recurso para asignar permiso.

1. Desde el **[!UICONTROL Configuraciones de calentamiento de IP]** menú desplegable de recursos, seleccione los permisos que necesita el usuario.

   ![](assets/ip_permissions_2.png)

1. Haga clic en **[!UICONTROL Guardar]**.

Para asignar la función correspondiente a un **[!UICONTROL Usuario]**:

1. Desde el [!DNL Permissions] producto, vaya a la **[!UICONTROL Funciones]** y seleccione la opción **[!UICONTROL Consultor de capacidad de entrega]** función integrada.

1. De su **[!UICONTROL Rol]** panel, acceda al **[!UICONTROL Usuarios]** pestaña.

   ![](assets/ip_permissions_3.png)

1. Clic **[!UICONTROL Agregar usuario]** para asignar el **[!UICONTROL Consultor de capacidad de entrega]** función integrada.

   ![](assets/ip_permissions_4.png)

1. Seleccione su **[!UICONTROL Usuario]** y haga clic en **[!UICONTROL Guardar]**.

   ![](assets/ip_permissions_5.png)

+++

## Preparar el archivo de plan de calentamiento de IP {#prepare-file}

El calentamiento de IP es una actividad que consiste en aumentar gradualmente el volumen de correos electrónicos que salen de sus IP y dominios a los principales proveedores de servicios de Internet (ISP), con el fin de establecer su reputación como remitente legítimo.

Esta actividad se realiza típicamente con la ayuda de un experto en capacidad de envío que ayuda a preparar un plan bien pensado basado en los dominios del sector, casos de uso, regiones, ISP y varios otros factores.

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

Antes de poder crear un plan de calentamiento de IP en la [!DNL Journey Optimizer] , debe rellenar una plantilla de Excel con todos los datos que alimentan su plan.

* Aquí puede descargar el espacio en blanco [Plantilla de plan de calentamiento IP de Excel](assets/ip-warmup-csv.zip) para rellenar.

* También puede descargar una [plantilla de plan de calentamiento de IP de muestra](assets/sample-ip-warmup-plan.zip) ya se ha rellenado con algunos datos que puede utilizar como ejemplo.

>[!CAUTION]
>
>Póngase en contacto con el consultor del equipo de entrega para asegurarse de que el archivo del plan de calentamiento de IP esté correctamente configurado.
>
>Asegúrese de utilizar el formato proporcionado en la plantilla.

A continuación se muestra un ejemplo de un archivo que contiene un plan de calentamiento de IP.

![](assets/ip-warmup-sample-file.png)

>[!NOTE]
>
>Por ahora, debería dejar el **Propiedades** y **Valor** células intactas.

### Pestaña Plan de calentamiento de IP {#ip-warmup-plan-tab}

* En este ejemplo, se ha preparado un plan que abarca más de 17 días (denominado &#39;**ejecuciones**&#39;) para alcanzar un volumen objetivo de más de un millón de perfiles.

* Este planificado se ejecuta a través de seis **fases**, cada uno de ellos con al menos una ejecución.

* Puede tener tantas columnas como desee para los dominios a los que desee enviar. En este ejemplo, el plan se divide en seis columnas:

   * Cuatro de los cuales corresponden a **grupos de dominio listos para usar** para usar en su plan (Gmail, Microsoft, Yahoo y Orange).
   * Uno corresponde a un grupo de dominio personalizado (que debe agregar mediante el [Grupo de dominio personalizado](#custom-domain-group-tab) pestaña).
   * La sexta columna, **Otros**, contiene todas las direcciones restantes de otros dominios que no están cubiertos explícitamente en el plan. Esta columna es opcional: si se omite, los correos electrónicos solo irán a los dominios especificados.
* El **Días de participación** Esta columna muestra que solo están segmentados los perfiles comprometidos con su marca durante el último periodo introducido.

La idea es aumentar progresivamente el número de direcciones objetivo en cada ejecución, al mismo tiempo que se reduce el número de ejecuciones para cada fase.

Los grupos de dominios principales listos para usar que puede agregar a su plan se enumeran a continuación:

<!--
* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigpond
* Orange
* Softbank
* Docomo
* United Internet
* Microsoft
* KDDI
* Italia Online
* La Poste
* Apple
-->

+++ Gmail gmail.com;google.com;googlemail.com;googlemail.co.uk
+++

+++ Adobe adobe.com
+++

+++WP.wp.pl;o2.pl
+++

+++Comcast comcast.net
+++

+++Yahoo.aol.fi;games.com;cs.com;yahoo.com.in;y7mail.com;yahoo.co.uk;yahoo.hu;yahoo.co.hu;yahoo.cn;yahoogroups.com.sg;yahoogroups.com.au;aol.es;yahoo.com.au;yahoo.com.vn;yahoo.ca;aol.hk;aol.co.nz;yahoo.com.br;aolpoland.pl;aolnorge.no;yahoo.ne.jp;yahoo.fi;ymail.com;netscape.com;yahoo.com.pe;yahoo.hr;aol.cz;yahoo.ee;aol.be;aolcom.tr;yahoo.si;yahoo.co.id;aol.it;citlink.net;wmconnect.com yahoo.es;yahoo.dk;yahoogroups.ca;yahoo.com.jp;yahoo.com.hk;aol.kr;yahoo.ie;aol.jp;aol.com.br;yahoo.lt;yahoo.co.kr;aol.nl;yahoo.com.ar;yahoo.bg;ygm.com;yahoo.co.nz;aol.se;aol.com;yahoo.de;goowy.com;rocketmail.com;frontiernet.net;aim.com;yahoo.nl;yahoogroups.co.in;aol.dk;netscape.net;aol.cl;luckymail.com;yahoo.no;yahoo.co.jp;yahoo.com.kr;yahoo.cz;yahoo.sk;yahoogroups.de;yahoo.gr;yahoo.co.za;verizon.net;yahoo.ro;aol.com.ve;aol.com.ar;aol.com.co;yahoo.at;wild4music.com;yahoogroups.com.cn;yahoo.com.co;aol.fr;yahoo.in;aol.in;wow.com;yahoo.rs;aol.de;yahoo.com;yahooxtra.co.nz;yahoo.com.mx;yahoo.com.ph;sky.com;yahoo.se;myaol.jp;aol.com.mx;yahoo.pt;aol.com.au;aolchina.com;yahoogrupper.dk;yahoo.fr;yahoo.com.net;aol.pl;yahoo.com.tw;talk21.com ol.ch;yahoo.it;compuserve.com;yahoo.com.sg;yahoogroups.com.tw;aolpolcka.pl;frontier.com;yahoo.co.in;yahoogruppi.it;yahoo.co.il;yahoo.cl;verizon.net.in;yahoo.com.tr;yahoogroups.com.hk;yahoogroups.co.uk;yahoo.be;yahoo.com.biz;yahoo.com.hr;aol.tw;aol.co.uk;ybb.ne.jp;yahoogroups.co.kr;yahoo.com.my;rogers.com;gte.net;yahoogroups.com;yahoo.co.th;yahoo.com.cn;aol.ru;love.com bellatlantic.net yahoo.com.ve yahoo.com.ua;yahoo.lv;aolpolska.pl;aol.at;yahoo.pl
+++

+++Bigpond bigpond.com;bigpond.com.au;bigpond.net;telstra.com;bigpond.net.au
+++

+++Naranja voila.com;francetelecom.com;orange.com;orange.fr;wanadoo.fr;voila.fr
+++

+++Softbank c.vodafone.ne.jp;jp-h.ne.jp;k.vodafone.ne.jp;jp-d.ne.jp;jp-c.ne.jp;t.vodafone.ne.jp;h.vodafone.ne.jp;r.vodafone.ne.jp;q.vodafone.ne.jp;jp-t.ne.jp;jp-q.ne.jp;s.vodafone.ne.jp;jp-s.ne.jp;jp-r.ne.jp;jp-k.ne.jp;n.vodafone.ne.jp;d.vodafone.ne.jp;softbank.ne.jp jp-n.ne.jp
+++

+++Docomo docomo.ne.jp
+++

+++Internet unido gmx.de;1and1.com;gmx.fr;mail.com;1und1.de;gmx.com;gmx.net;gmx.at;web.de;gmx.ch
+++

++Microsoft hotmail.com.tr;live.de;live.ru;live.nl;windowslive.com;live.jp;mts.net;xbox.com;hotmail.fr;hotmail.cl;hotmail.jp;live.cl;live.at;live.com.au;hotmail.co.th;live.hk;hotmail.com.au;hotmail.com;live.com.my;hotmail.co.kr;live.ie;outlook.com.br;hotmail.dk;hotmail.co.il;live.co.kr;live.co.uk;outlook.ie;live.cn;live.com.mx;hotmail.co.uk;hotmail.es;live.fr;live.no;live.dk;hotmail.it;live.se;live.com.sg;live.be;msn.com;live.in;hotmail.se;hotmail.co.jp;hotmail.ch;live.co.za;live.com.pt;hotmail.gr;live.it;outlook.com;hotmail.ca;live.com;live.com.ar hotmail.com.br hotmail.com.ar;live.ca;hotmail.de
+++

+++KDDI au.com;ezweb.ne.jp;uqmobile.jp
+++

+++Italia Online inwind.it;blu.it;virgilio.it;giallo.it;iol.it;libero.it
+++

+++La Poste laposte.net
+++

+++Apple mac.com;icloud.com;apple.com;me.com
+++

### Pestaña Grupo de dominios personalizado {#custom-domain-group-tab}

También puede agregar más columnas al plan incluyendo grupos de dominio personalizados.

Utilice el **[!UICONTROL Grupo de dominio personalizado]** para definir un nuevo grupo de dominios. Para cada dominio, puede agregar todos los subdominios que cubre.<!--TBC-->

Por ejemplo, si agrega el dominio personalizado Luma, desea que se incluyan los siguientes subdominios: luma.com, luma.co.uk, luma.it, luma.fr, luma.de, etc.

![](assets/ip-warmup-sample-file-custom.png)

### Ejemplo {#example}

Supongamos que desea tener dos grupos de dominios personalizados:

* Uno solo para dominios de Hotmail.
* Uno para todos los demás dominios del grupo de dominios Microsoft (excluyendo así todos los dominios de Hotmail).

Tenga en cuenta que todos los demás dominios se recopilarán en **[!UICONTROL Otros]** columna.

1. En el **[!UICONTROL Grupo de dominio personalizado]** , cree la pestaña **Hotmail** grupo de dominios.

1. Agregue todos los dominios de Hotmail en la misma fila.

   Puede [copiar y pegar](#copy-paste) todos los dominios de Hotmail enumerados en la [Pestaña Plan de calentamiento de IP](#ip-warmup-plan-tab) sección.

1. Añada otra fila.

1. Cree el **Microsoft_X** grupo de dominios.

1. Agregue todos los dominios de Microsoft que no sean Hotmail en la misma fila. Del mismo modo, puede copiarlos y pegarlos de la lista anterior. [Más información](#copy-paste)

1. Vuelva a la **[!UICONTROL Plan de calentamiento de IP]** pestaña.

1. Cree tres columnas: una para **Hotmail**, uno para **Microsoft_X** y uno para **Otros**.

1. Rellene las columnas según sus necesidades.

>[!NOTE]
>
>Una vez cargado el plan de calentamiento de IP en [!DNL Journey Optimizer], no es necesario excluir los grupos de dominio de Microsoft.

<!--Only the domain groups listed in the **[!UICONTROL IP Warmup Plan]** tab will be taken into account.-->

### Copiar y pegar dominios predeterminados {#copy-paste}

Si desea crear un grupo de dominios personalizado que contenga todos los dominios de Hotmail, por ejemplo, puede copiar y pegar los dominios de la lista predeterminada proporcionada [superior](#ip-warmup-plan-tab).

A continuación, utilice la herramienta de conversión de Excel para convertir texto en columnas:

1. Seleccionar **[!UICONTROL Datos]** > **[!UICONTROL Texto a columnas...]**, elija **[!UICONTROL Delimitado]** y seleccione **[!UICONTROL Siguiente]**.

1. Seleccionar **[!UICONTROL Punto y coma]**, haga clic en **[!UICONTROL Siguiente]** y **[!UICONTROL Finalizar]**.

Cada dominio ahora se muestra en una columna diferente en la misma fila.

## Acceso y administración de planes de calentamiento de IP {#manage-ip-warmup-plans}

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Canales]** > **[!UICONTROL planes de calentamiento de IP]** menú. Se muestran todos los planes de calentamiento de IP creados hasta el momento.

   ![](assets/ip-warmup-filter-list.png)

1. Puede filtrar por el estado. Los diferentes estados son:

   * **Sin iniciar**: aún no se ha activado ninguna ejecución. [Más información](ip-warmup-execution.md#define-runs)
   * **Activo**: el plan cambia a este estado en cuanto se activa correctamente la primera ejecución de la primera fase. [Más información](ip-warmup-execution.md#define-runs)
   * **Completado**: el plan se ha marcado como completado. <!--This option is only available if all the runs in the plan are in **[!UICONTROL Completed]** or **[!UICONTROL Draft]** status (no run can be **[!UICONTROL Live]**).--> [Más información](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. Para eliminar un plan de calentamiento de IP, seleccione la **[!UICONTROL Eliminar]** junto al nombre de un plan y confirme la eliminación.

   >[!NOTE]
   >
   >Solo planes con el **Sin iniciar** se puede eliminar el estado.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >El plan de calentamiento de IP seleccionado se eliminará de forma permanente.

## Creación de un plan de calentamiento de IP {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Especificación del plan de calentamiento de IP"
>abstract="Descargue la plantilla CSV y rellénela con datos de las fases de calentamiento de IP y el número de destino de los perfiles."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Selección de una superficie de marketing"
>abstract="Debe seleccionar la misma superficie que la seleccionada en la campaña que desea asociar con su plan de calentamiento de IP."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=es" text="Configuración de superficies de canal"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=es" text="Creación de campañas de calentamiento de IP"

Para crear un plan de calentamiento de IP, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Canales]** > **[!UICONTROL planes de calentamiento de IP]** y haga clic en **[!UICONTROL Crear plan de calentamiento de IP]**.

   ![](assets/ip-warmup-create-plan.png)

1. Complete los detalles del plan de calentamiento de IP: asígnele un nombre y una descripción.

   ![](assets/ip-warmup-plan-details.png)

1. Seleccione el [emerger](channel-surfaces.md) que usted quiere calentar. Solo las superficies de marketing están disponibles para su selección. [Más información sobre el tipo de correo electrónico](../email/email-settings.md#email-type)

   >[!NOTE]
   >
   >Las campañas que desee asociar con su plan de calentamiento de IP deben utilizar la misma superficie. [Obtenga información sobre cómo crear una campaña de calentamiento de IP](ip-warmup-campaign.md)

1. Cargue el archivo de Excel que contiene el plan de calentamiento de IP. [Más información](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

   >[!NOTE]
   >
   >En caso de que la carga falle, asegúrese de que está utilizando el formato y el formato de archivo correctos (.xls o .xlsx). Utilice el [muestra](assets/ip-warmup-csv.zip) que le proporcione el Adobe.

1. Haga clic en **[!UICONTROL Crear]**. Todas las fases, ejecuciones, columnas y su contenido definido en el archivo cargado se muestran automáticamente en [!DNL Journey Optimizer] interfaz.

   ![](assets/ip-warmup-plan-uploaded.png)

   >[!NOTE]
   >
   >El **[!UICONTROL Objetivos]** muestra la suma de todos los perfiles segmentados para cada ejecución, es decir, todos los perfiles de cada grupo de dominio que haya definido, incluido el **Otros** columna, si la hay.

Ya está listo para ejecutar su plan de calentamiento de IP. [Más información](ip-warmup-execution.md)
