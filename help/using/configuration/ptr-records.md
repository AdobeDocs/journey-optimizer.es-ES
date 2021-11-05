---
title: Registros de PTR
description: Obtenga información sobre cómo administrar registros PTR
audience: administrators
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: 1e62715f35b50bba639657a1bef37aa61922c715
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# Registros de PTR

## Acerca de los registros PTR

Un registro de puntero (PTR) es un tipo de registro DNS (Sistema de nombres de dominio) que proporciona el nombre de dominio vinculado a una dirección IP.

Con los registros PTR, los servidores de correo receptores pueden comprobar la autenticidad de los servidores de correo electrónico al identificar si sus direcciones IP corresponden a los nombres con los que se conectan los servidores.

## Acceda a los registros PTR de sus subdominios

Una vez delegado un subdominio en Adobe Journey Optimizer, se crea automáticamente un registro PTR y se asocia a este subdominio. Puede acceder a él desde la **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL PTR records]** para abrir el Navegador.

![](../assets/ptr-records.png)

La lista muestra los registros PTR generados para cada subdominio delegado, utilizando la siguiente sintaxis:

* &quot;r&quot; para registrar,
* &quot;xx&quot; para las dos últimas cifras de la dirección IP,
* nombre de subdominio.

Puede abrir un registro PTR de la lista para mostrar el nombre de subdominio y la dirección IP asociados.

## Editar un registro PTR {#edit-ptr-record}

Puede modificar un registro PTR para editar el subdominio asociado con una dirección IP.

1. En la lista, haga clic en un nombre de registro PTR para abrirlo.

   ![](../assets/ptr-record-select.png)

1. Edite el subdominio como desee.

   ![](../assets/ptr-record-subdomain.png)

   >[!NOTE]
   >
   >No se puede modificar la variable **[!UICONTROL IP]** y **[!UICONTROL PTR record]** campos.

1. Haga clic en **[!UICONTROL SAve]** para confirmar los cambios.

Un **[!UICONTROL Updating]** aparece junto al nombre del registro PTR en la lista.

![](../assets/ptr-record-updating.png)

Para comprobar los detalles de actualización de registros PTR, haga clic en el botón **[!UICONTROL Updating]** o **[!UICONTROL Recent updates]** icono.

![](../assets/ptr-record-recent-update.png)

Puede ver información como el estado de actualización y los cambios solicitados.

![](../assets/ptr-record-updates.png)

## Actualizar estados

Una actualización de registro PTR puede tener los siguientes estados:

* **[!UICONTROL Processing]**: Se ha enviado la actualización del registro PTR, que está en proceso de verificación.
* **[!UICONTROL Success]**: El registro PTR actualizado se ha verificado y el nuevo subdominio ahora está asociado con la dirección IP.
* **[!UICONTROL Failed]**: Una o varias comprobaciones han fallado durante la verificación de actualización de registros PTR.

### Procesamiento

Se realizarán varias comprobaciones de la capacidad de envío para verificar que el nuevo subdominio que se va a asociar a la dirección IP sea válido. <!--The processing time is around **48h-72h**, and can take up to **7-10 days**. Learn more on the checks performed during the validation cycle in [this section](#create-message-preset).-->

>[!NOTE]
>
>No puede modificar un registro PTR mientras la actualización está en curso. Puede seguir haciendo clic en su nombre, pero la variable **[!UICONTROL Subdomain]** aparece atenuado. Los cambios no se reflejarán hasta que la actualización se realice correctamente.

Durante el proceso de validación, el antiguo subdominio sigue estando asociado a la dirección IP.

### Correcto

Una vez que el proceso de validación se ha realizado correctamente, el nuevo subdominio se asocia automáticamente a la dirección IP.

### Fallido

Si falla el proceso de validación, se muestra el registro PTR más antiguo. El subdominio válido que anteriormente estaba asociado con la dirección IP permanece sin cambios.

Los tipos de error de actualización posibles son los siguientes:
* Error al crear un nuevo DNS de reenvío para el registro PTR
* Error al actualizar el registro
* Error al volver a incorporar las afinidades

Al fallar la actualización, el registro PTR vuelve a ser editable. Puede hacer clic en su nombre y actualizar el subdominio de nuevo.
