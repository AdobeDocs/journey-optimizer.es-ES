---
solution: Journey Optimizer
product: journey optimizer
title: Registros PTR
description: Obtenga información sobre cómo administrar registros PTR
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: subdominio, PTR, registros, DNS, dominio, correo
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 1%

---

# Registros PTR {#ptr-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record"
>title="Registros PTR de subdominios"
>abstract="Un registro de puntero (PTR) es un tipo de registro DNS que proporciona el nombre de dominio vinculado a una dirección IP, lo que ayuda a los servidores de correo de recepción a comprobar las direcciones IP de los remitentes. Edite un registro PTR únicamente después de las debidas consideraciones y discusiones con el experto en capacidad de entrega."

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record_header"
>title="Registros PTR de subdominios"
>abstract="Una vez delegado un subdominio al Adobe en Journey Optimizer, se crea automáticamente un registro PTR y se asocia a este subdominio."

## Acerca de los registros PTR {#about-ptr-records}

Un registro de puntero (PTR) es un tipo de registro del Sistema de nombres de dominio (DNS) que proporciona el nombre de dominio vinculado a una dirección IP.

Con los registros PTR, los servidores de correo receptores pueden comprobar la autenticidad de los servidores de correo de envío identificando si sus direcciones IP corresponden a los nombres a los que se conectan los servidores.

## Acceso a los registros PTR de los subdominios {#access-ptr-records}

Una [se ha delegado un subdominio](delegate-subdomain.md) en Adobe Journey Optimizer, se crea automáticamente un registro PTR y se asocia a este subdominio. Puede acceder a ella desde el **[!UICONTROL Administration]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Registros PTR]** menú.

![](assets/ptr-records.png)

La lista muestra los registros PTR generados para cada subdominio delegado, con la siguiente sintaxis:

* &quot;r&quot; para que conste,
* &quot;xx&quot; para las dos últimas cifras de la dirección IP,
* nombre de subdominio.

Puede abrir un registro PTR de la lista para mostrar el nombre de subdominio y la dirección IP asociados.

## Edición de un registro PTR {#edit-ptr-record}

Puede modificar un registro PTR para editar el subdominio asociado a una dirección IP.

>[!CAUTION]
>
>Los registros PTR son comunes a todos los entornos. Por lo tanto, cualquier modificación en un registro PTR también afectará a las zonas protegidas de producción.
>
>Proceda con mucho cuidado al editar registros PTR. En caso de duda, póngase en contacto con un experto en capacidad de entrega.

### Subdominios totalmente delegados {#fully-delegated-subdomains}

Para editar un registro PTR con un subdominio que es [totalmente delegado](delegate-subdomain.md#full-subdomain-delegation) para realizar el Adobe, siga los pasos a continuación.

1. En la lista, haga clic en el nombre de un registro PTR para abrirlo.

   ![](assets/ptr-record-select.png)

1. Seleccionar un subdominio [totalmente delegado](delegate-subdomain.md#full-subdomain-delegation) al Adobe de la lista.

   ![](assets/ptr-record-subdomain.png)

1. Clic **[!UICONTROL Guardar]** para confirmar los cambios.

>[!NOTE]
>
>No se puede modificar la variable **[!UICONTROL IP]** y **[!UICONTROL Registro PTR]** campos.

### Subdominios delegados mediante el método CNAME {#edit-ptr-subdomains-cname}

Para editar un registro PTR con un subdominio delegado al Adobe mediante [método CNAME](delegate-subdomain.md#cname-subdomain-delegation), siga los pasos a continuación.

1. En la lista, haga clic en el nombre de un registro PTR para abrirlo.

   ![](assets/ptr-record-select-cname.png)

1. Seleccione un subdominio delegado al Adobe mediante la variable [método CNAME](delegate-subdomain.md#cname-subdomain-delegation) de la lista.

   ![](assets/ptr-record-subdomain-cname.png)

1. Debe crear un nuevo registro DNS de reenvío en la plataforma de alojamiento. Para ello, copie el registro generado por el Adobe. Una vez finalizado, marque la casilla &quot;Confirmo...&quot;.

   ![](assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >Si recibe este mensaje: &quot;Cree el DNS de reenvío primero y vuelva a intentarlo&quot;, siga los pasos a continuación:
   >   * Compruebe en el proveedor DNS si el registro DNS de reenvío se creó correctamente.
   >   * Es posible que los registros en el DNS no se sincronicen inmediatamente. Espere unos minutos e inténtelo de nuevo.


1. Clic **[!UICONTROL Guardar]** para confirmar los cambios.

>[!NOTE]
>
>No se puede modificar la variable **[!UICONTROL IP]** y **[!UICONTROL Registro PTR]** campos.

## Comprobar detalles de actualización de registro PTR {#check-ptr-record-update}

Una vez confirmada la edición de registros PTR, la variable **[!UICONTROL Procesando]** aparece junto al nombre del registro PTR en la lista.

![](assets/ptr-record-updating.png)

>[!NOTE]
>
>El [procesamiento de actualización](#processing) puede tardar hasta tres horas.

Para comprobar los detalles de actualización del registro PTR, haga clic en el icono situado junto a él. Obtenga más información sobre los estados asociados con los distintos iconos de [esta sección](#ptr-record-update-statuses).

![](assets/ptr-record-recent-update.png)

Puede ver información como el estado de la actualización y los cambios solicitados.

![](assets/ptr-record-updates.png)

## Estados de actualización de registro PTR {#ptr-record-update-statuses}

Una actualización de registro PTR puede tener los siguientes estados:

* ![](assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL Procesando]**: la actualización del registro PTR se ha enviado y está pasando por un proceso de verificación.
* ![](assets/do-not-localize/ptr-record-success.png) **[!UICONTROL Correcto]**: el registro PTR actualizado se ha verificado y el nuevo subdominio ahora está asociado con la dirección IP.
* ![](assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL Error]**: una o varias comprobaciones han fallado durante la verificación de la actualización del registro PTR.

### Procesamiento {#processing}

Se realizarán varias comprobaciones de entrega para verificar que el nuevo subdominio asociado a la dirección IP es válido. Esto puede tardar hasta tres horas.

>[!NOTE]
>
>No se puede modificar un registro PTR mientras la actualización está en curso. Puede seguir haciendo clic en su nombre, pero la variable **[!UICONTROL Subdominio]** el campo está atenuado. Los cambios no se reflejarán hasta que la actualización se realice correctamente.

Durante el proceso de validación, el subdominio antiguo sigue asociado a la dirección IP.

### Correcto {#success}

Una vez que el proceso de validación se realiza correctamente, el nuevo subdominio se asocia automáticamente a la dirección IP.

### Fallido {#failes}

Si falla el proceso de validación, se muestra el registro PTR más antiguo. El subdominio válido asociado anteriormente a la dirección IP permanece sin cambios.

Los posibles tipos de error de actualización son los siguientes:
* Error al crear un nuevo DNS de reenvío para el registro PTR
* Error al actualizar el registro
* Error al volver a incorporar las afinidades

Si la actualización falla, el registro PTR vuelve a poder editarse. Puede hacer clic en su nombre y actualizar el subdominio de nuevo.
