---
title: Lista de permitidos
description: Aprenda a utilizar la lista de permitidos .
feature: Capacidad de entrega
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: 2d03285400b86b2c296997537852bb89ae0f6d0a
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 1%

---

# Lista de permitidos {#allow-list}

Ahora es posible definir una lista específica de envío seguro en el nivel [sandbox](administration/sandboxes.md), para tener un entorno seguro con fines de prueba. En una instancia que no es de producción, donde pueden producirse errores, la lista de permitidos garantiza que no tendrá riesgo de enviar mensajes no deseados a sus clientes.

La lista de permitidos permite especificar direcciones de correo electrónico o dominios individuales que serán los únicos destinatarios o dominios autorizados para recibir los correos electrónicos que envía desde un entorno limitado específico. Esto puede impedir que envíe correos electrónicos accidentalmente a direcciones de clientes reales cuando se encuentre en un entorno de prueba.


>[!CAUTION]
>
>Esta función **no** está disponible en entornos limitados de producción. Solo se aplica al canal de correo electrónico.


## Habilitar la lista de permitidos {#enable-allow-list}

Para habilitar la lista de permitidos en un simulador para pruebas que no sean de producción, actualice la lista de permitidos para que ya no esté vacía. Para desactivar la función, borre la lista para que vuelva a estar vacía.

<!--
you need to make an Adobe API call.

* Using this API, you can also disable the feature at any time.

* You can update the allowed list before or after enabling the feature.

* The allowed list logic applies when the feature is enabled and if the allowed list is not empty. Learn more in [this section](#logic).

-->
>[!NOTE]
>
>Cuando está habilitada, la función de lista de permitidos se cumple al ejecutar recorridos, pero también al probar mensajes con [pruebas](preview.md#send-proofs) y probar recorridos usando el [modo de prueba](building-journeys/testing-the-journey.md).

## Añadir entidades a la lista de permitidos {#add-entities}

Para agregar nuevas direcciones de correo electrónico o dominios a la lista de permitidos para un entorno limitado específico, debe llamar a la API de supresión con el valor `ALLOWED` del atributo `listType`. Por ejemplo:

![](assets/allow-list-api.png)

Puede realizar las operaciones **Add**, **Delete** y **Get**.

>[!NOTE]
>
>La lista de permitidos puede contener hasta 1000 entradas.

<!--
Learn more on making Adobe API calls in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).
-->


## lógica de lista de permitidos {#logic}

<!-- When the allowed list is [enabled](#enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Cuando la lista de permitidos está **vacía**, no se aplica la lógica de lista de permitidos. Esto significa que puede enviar correos electrónicos a cualquier perfil, siempre que no estén en la [lista de supresión](suppression-list.md).

Cuando la lista de permitidos es **no está vacía**, se aplica la lógica de lista de permitidos:

* Si una entidad **no está en la lista de permitidos** y no está en la lista de supresión, el destinatario correspondiente no recibirá el correo electrónico, por lo que es **[!UICONTROL Not allowed]**.

* Si una entidad está **en la lista de permitidos** y no en la lista de supresión, el correo electrónico se puede enviar al destinatario correspondiente. Sin embargo, si la entidad también está en la [lista de supresión](suppression-list.md), el destinatario correspondiente no recibirá el correo electrónico, por lo que es **[!UICONTROL Suppressed]**.




