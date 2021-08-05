---
title: Lista de permitidos
description: Aprenda a utilizar la lista de permitidos .
feature: Capacidad de entrega
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: 288c27d4fc64a6d0a6f07b634ed044a6e858d0c1
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 2%

---

# Lista de permitidos {#allow-list}

Ahora es posible definir una lista específica de envío seguro en el nivel [sandbox](administration/sandboxes.md), para tener un entorno seguro con fines de prueba. En una instancia que no es de producción, donde pueden producirse errores, la lista de permitidos garantiza que no tendrá riesgo de enviar mensajes no deseados a sus clientes.

>[!CAUTION]
>
>Esta función no está disponible en entornos limitados de producción.

La lista de permitidos permite especificar direcciones de correo electrónico o dominios individuales que serán los únicos destinatarios o dominios autorizados para recibir los correos electrónicos que envía desde un entorno limitado específico. Esto puede impedir que envíe correos electrónicos accidentalmente a direcciones de clientes reales cuando se encuentre en un entorno de prueba.

>[!NOTE]
>
>Esta función solo se aplica al canal de correo electrónico.

## Habilitar la lista de permitidos {#enable-allow-list}

Para habilitar la lista de permitidos en un simulador para pruebas que no sean de producción, debe realizar una llamada de API de Adobe.

* Con esta API, también puede deshabilitar la función en cualquier momento.

* Puede actualizar la lista de permitidos antes o después de habilitar la función.

* La lógica de lista de permitidos se aplica cuando la función está habilitada y si la lista de permitidos no está vacía. Obtenga más información en [esta sección](#logic).

>[!NOTE]
>
>Cuando está habilitada, la función de lista de permitidos se cumple al ejecutar recorridos, pero también al probar mensajes con [pruebas](preview.md#send-proofs) y probar recorridos usando el [modo de prueba](building-journeys/testing-the-journey.md).

## Añadir entidades a la lista de permitidos {#add-entities}

>[!CAUTION]
>
>Esta función **no** está disponible en entornos limitados de producción. Solo se aplica al canal de correo electrónico.

Para agregar nuevas direcciones de correo electrónico o dominios a la lista de permitidos para un entorno limitado específico, debe llamar a la API de supresión con el valor `ALLOWED` del atributo `listType`. Por ejemplo:

![](assets/allow-list-api.png)

Puede realizar las operaciones **Add**, **Delete** y **Get**.

>[!NOTE]
>
>La lista de permitidos puede contener hasta 1000 entradas.

Obtenga más información sobre cómo realizar llamadas a la API de Adobe en la [documentación del Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).

## lógica de lista de permitidos {#logic}

<!-- When the allowed list is \[enabled\]\(\add link here\) at the sandbox level using the API call above, the following applies.-->

1. Cuando la lista de permitidos está **vacía**, no se aplica la lógica de lista de permitidos. Esto significa que puede enviar correos electrónicos a cualquier perfil, siempre que no estén en la [lista de supresión](suppression-list.md).

1. Cuando la lista de permitidos es **no está vacía**, se aplica la lógica de lista de permitidos:

   * Si una entidad **no está en la lista de permitidos** y no está en la lista de supresión, el destinatario correspondiente no recibirá el correo electrónico, por lo que es **[!UICONTROL Not allowed]**.

   * Si una entidad está **en la lista de permitidos** y no en la lista de supresión, el correo electrónico se puede enviar al destinatario correspondiente. Sin embargo, si la entidad también está en la [lista de supresión](suppression-list.md), el destinatario correspondiente no recibirá el correo electrónico, por lo que es **[!UICONTROL Suppressed]**.




