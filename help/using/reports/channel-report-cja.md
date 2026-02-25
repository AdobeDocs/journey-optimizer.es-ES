---
solution: Journey Optimizer
product: journey optimizer
title: Informes de nivel de canal
description: Aprenda a utilizar los datos del informe Información general
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 393f02c0-f54c-4222-b668-0931b67590ce
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 1%

---

# Informe de información general {#channel-report-cja}

El informe Información general ofrece a los usuarios un resumen exhaustivo de las métricas de tráfico y participación para todas las campañas y recorridos dentro de su entorno. Estas métricas se combinan para presentar valores unificados para acciones procedentes de diferentes canales, que abarcan varias campañas y recorridos.

Para obtener acceso al informe Información general, desplácese hasta el menú **Informes** dentro de la sección **Administración de Recorrido**.

La página del informe se muestra con las siguientes pestañas:

* [Recorridos](#journey)
* [Campañas](#campaign)
* [Canales](#channel)
* [Conjuntos de reglas](#rule-sets)

Para obtener más información sobre Customer Journey Analytics Workspace y cómo filtrar y analizar datos, consulte [esta página](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home).

## Características destacadas {#highlights}

![](assets/cja-highlights.png)

Los KPI **[!UICONTROL Características destacadas]** sirven como un tablero completo, que ofrece un desglose detallado de las métricas clave para todas las campañas y recorridos dentro de su entorno, lo que le permite evaluar rápidamente el rendimiento e identificar áreas para la mejora.

+++ Más información sobre las Métricas de resaltados

* **[!UICONTROL Participación en el Recorrido]**: Número total de individuos únicos que recibieron mensajes enviados a través del recorrido, que representan perfiles distintos que alcanzaron un punto de acción designado en el recorrido.

* **[!UICONTROL Entradas de Recorrido]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Errores de Recorrido]**: Número total de recorridos individuales que no se ejecutaron correctamente.

* **[!UICONTROL Tasa de clics]**: Porcentaje de clics en los mensajes.

* **[!UICONTROL Tasa de apertura de pulsaciones (CTOR)]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Personas]**: Número de perfiles de usuario que se califican como perfiles de destino para sus mensajes.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido de sus mensajes.

* **[!UICONTROL Quejas por correo no deseado]**: Número de veces que un mensaje se declaró como correo no deseado.

* **[!UICONTROL Cancelaciones de suscripción]**: número de clics en el vínculo de cancelación de suscripción.

+++

##  Recorrido  {#journey}

![](assets/cja-channel-journeys.png)

La tabla **[!UICONTROL Recorrido]** sirve como un tablero completo, que proporciona un análisis de las métricas clave relacionadas con su recorrido. Incluye detalles como el número de perfiles introducidos y los casos de recorridos individuales fallidos, lo que ofrece una comprensión exhaustiva de la eficacia y los niveles de participación de su recorrido.

Al hacer clic en el nombre de cualquier recorrido enumerado en esta tabla, puede explorar fácilmente cada recorrido individualmente y obtener acceso inmediato a su informe completo en una nueva pestaña.

+++ Más información sobre las métricas de Recorrido

* **[!UICONTROL Entradas de Recorrido]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Salidas de Recorrido]**: Número total de personas que salieron del recorrido.

* **[!UICONTROL Errores de Recorrido]**: Número total de recorridos individuales que no se ejecutaron correctamente.

+++

## Campañas {#campaign}

![](assets/cja-channel-campaigns.png)

La tabla **[!UICONTROL Campaign]** funciona como un panel que abarca todo, y presenta una descripción detallada de las métricas críticas para su campaña. Incluye datos esenciales como el número de perfiles y envíos, lo que le ofrece una insight completa de los niveles de rendimiento y participación de su campaña.

Al hacer clic en el nombre de cualquier campaña enumerada en esta tabla, puede explorar fácilmente cada campaña individualmente y obtener acceso inmediato a su informe completo en una nueva pestaña.

+++ Más información sobre las Métricas de Campaign

* **[!UICONTROL Personas]**: Número de perfiles de usuario que se califican como perfiles de destino para sus mensajes.

* **[!UICONTROL Tasa de clics (CTR)]**: porcentaje de clics en los mensajes.

* **[!UICONTROL Envíos]**: Número total de envíos para cada campaña.

* **[!UICONTROL Entregado]**: número de mensajes enviados correctamente.

* **[!UICONTROL Pantallas]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido de sus mensajes.

+++

## Canales {#channel}

### Canales

![](assets/cja-channels.png)

La tabla **[!UICONTROL Canales]** proporciona un desglose detallado de la participación de sus perfiles con sus mensajes en el nivel de canal. Esto le permite obtener información más detallada sobre el rendimiento de los distintos canales.

+++ Más información sobre las métricas de Canales

* **[!UICONTROL Personas]**: Número de perfiles de usuario que se califican como perfiles de destino para sus mensajes.

* **[!UICONTROL Tasa de clics (CTR)]**: porcentaje de clics en los mensajes.

* **[!UICONTROL Entregado]**: número de mensajes enviados correctamente.

* **[!UICONTROL Pantallas]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido de sus mensajes.

+++

### Errores salientes

![](assets/cja-channels-outbound-errors.png)

La tabla **[!UICONTROL Errores salientes]** le permite identificar los errores precisos que se produjeron durante el proceso de envío, lo que facilita una comprensión clara de los problemas encontrados.

### Exclusiones salientes

![](assets/cja-channels-outbound-excluded.png)

La tabla **[!UICONTROL Exclusiones salientes]** presenta una vista completa de los diferentes factores que tuvieron como resultado la exclusión de perfiles de usuario de la audiencia de destino, lo que resultó en que el mensaje no se recibiera.

## Límite de recorrido y conflictos {#rule-sets}

La tabla **[!UICONTROL Límite de Recorrido y conflictos]** proporciona información sobre el rendimiento de los conjuntos de reglas de mediación de recorrido, mostrando las entradas y exclusiones de recorrido en función de las reglas de límite y las puntuaciones de prioridad aplicadas a los recorridos.

+++ Más información sobre las Métricas de conjuntos de reglas

La columna **[!UICONTROL Entradas de Recorrido por conjunto de reglas]** muestra el número de perfiles que ingresaron al recorrido. Hay tres tipos de entradas:

* ****[!UICONTROL Sin conflicto]****: el perfil entró en la recorrido sin ningún conflicto en el conjunto de reglas. Ningún conjunto de reglas activo impidió esta entrada, y la entrada de recorrido se produjo independientemente de las reglas de mediación.

* **Prioridad más alta**: el perfil entró en el recorrido debido a que tiene mayor prioridad que otros recorridos de la competencia. Aunque se ha producido un conflicto (el perfil se clasifica para varios recorridos), este recorrido se ha seleccionado debido a su mayor puntuación de prioridad.

* **No obligatorio**: El perfil entró en la recorrido, pero el conjunto de reglas no estaba activo o no se aplicaba a esta entrada de recorrido en el momento de la entrada.

La columna **[!UICONTROL Exclusiones]** muestra el número de perfiles que se excluyeron de la entrada al recorrido. Los perfiles se pueden excluir por dos motivos:

* **Se ha alcanzado el límite**: El perfil ha alcanzado el número máximo de entradas de recorrido o recorridos simultáneos permitidos por la regla de límite.

* **Prioridad más baja**: no se ha alcanzado el límite, pero otros recorridos de prioridad más alta cumplen las restricciones. El perfil se ha excluido de este recorrido y, en su lugar, ha introducido un recorrido de prioridad más alto.

+++

➡️ [Más información acerca de la restricción y arbitraje de recorridos](../conflict-prioritization/journey-capping.md)