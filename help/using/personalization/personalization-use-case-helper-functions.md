---
title: Caso de uso personalizado&dos puntos; correo electrónico de abandono del carro de compras
description: Obtenga información sobre cómo personalizar un mensaje mediante las funciones de ayuda
feature: Personalización
topic: Personalización
role: Data Engineer
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '1016'
ht-degree: 4%

---


# Caso de uso de personalización: correo electrónico de abandono del carro de compras {#personalization-use-case-helper-functions}

En este ejemplo, personalizará el cuerpo de un mensaje de correo electrónico. Este mensaje está dirigido a los clientes que han dejado artículos en el carro de compras, pero no han completado su compra.

Utilizará estos tipos de funciones de ayuda:

* La función de cadena `upperCase`, para insertar el nombre del cliente en mayúsculas. [Más información](functions/string.md#upper).
* El asistente `each`, para enumerar los elementos que están en el carro de compras. [Más información](functions/helpers.md#each).
* El `if` ayuda para insertar una nota específica del producto si el producto relacionado está en el carro de compras. [Más información](functions/helpers.md#if-function).

<!-- **Context**: personalization based on contextual data from the journey -->

Antes de comenzar, asegúrese de que sabe cómo configurar estos elementos:
* Un mensaje de correo electrónico. [Más información](../create-message.md)
* El cuerpo de un correo electrónico. [Más información](../create-email-content.md).
* Un evento unitario. [Más información](../event/about-events.md).
* Recorrido que comienza con un evento. [Más información](../building-journeys/using-the-journey-designer.md).

Siga estos pasos:
1. [Crear un mensaje de correo electrónico](#configure-email).
2. [Inserte el nombre del cliente en mayúsculas](#uppercase-function).
3. [Cree el evento inicial y el recorrido](#create-context).
4. [Añada el contenido del carro de compras al correo electrónico](#each-helper).
5. [Inserte una nota](#if-helper) específica del producto.
6. [Prueba y publicación del recorrido](#test-and-publish).

## Paso 1: Creación del correo electrónico{#configure-email}

1. Cree o modifique un mensaje de correo electrónico y haga clic en **[!UICONTROL Email Designer]**.
   ![](../assets/personalization-uc-helpers-1.png)

2. En la paleta izquierda de la página principal del Diseñador de correo electrónico, arrastre y suelte tres componentes de estructura en el cuerpo del mensaje.

3. Arrastre y suelte un componente de contenido HTML en cada componente de estructura nuevo.

   ![](../assets/personalization-uc-helpers-2.png)

## Paso 2: Inserte el nombre del cliente en mayúsculas {#uppercase-function}

1. En la página de inicio del Diseñador de correo electrónico, haga clic en el componente HTML donde desee agregar el nombre del cliente.
2. En la barra de herramientas contextual, haga clic en **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

3. En la ventana **[!UICONTROL Edit HTML]**, añada la función de cadena `upperCase`:
   1. En la lista, seleccione **[!UICONTROL Helper functions]**.
   2. Utilice el campo de búsqueda para buscar &quot;mayúsculas&quot;.
   3. En los resultados de la búsqueda, añada la función `upperCase`. Para ello, haga clic en el signo más (+) situado junto a `{%= upperCase(string) %}: string`.

      El editor de expresiones muestra esta expresión:

      ```handlebars
      {%= upperCase(string) %}
      ```

      ![](../assets/personalization-uc-helpers-4.png)

4. Elimine el marcador de posición &quot;cadena&quot; de la expresión.
5. Añada el token de nombre:
   1. En la lista, seleccione **[!UICONTROL Profile]**.
   2. Seleccione **[!UICONTROL Profile]** > **[!UICONTROL Person]** > **[!UICONTROL Full name]**.
   3. Agregue el token **[!UICONTROL First name]** a la expresión.

      El editor de expresiones muestra esta expresión:

      ```handlebars
      {%= upperCase(profile.person.name.firstName) %}
      ```

      ![](../assets/personalization-uc-helpers-5.png)

      Obtenga más información sobre el tipo de datos de nombre de persona en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/person-name.html){target=&quot;_blank&quot;}.

6. Haga clic en **[!UICONTROL Validate]**, luego en **[!UICONTROL Save]**.

   ![](../assets/personalization-uc-helpers-6.png)
7. Guarde el mensaje.

## Paso 3: Crear el evento inicial y el recorrido relacionado {#create-context}

El contenido del carro de compras es información contextual del recorrido. Por lo tanto, debe añadir un evento inicial y el correo electrónico a un recorrido para poder añadir al correo electrónico información específica del carro de compras.

1. Cree un evento cuyo esquema incluya la matriz `productListItems`.
2. Defina todos los campos de esta matriz como campos de carga útil para este evento.

   Obtenga más información sobre el tipo de datos del elemento de la lista de productos en [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target=&quot;_blank&quot;}.

3. Cree un recorrido que comience con este evento.
4. Añada el mensaje al recorrido.
5. Finalice el recorrido con una actividad final.

   Como aún no ha publicado el mensaje, no puede probar ni publicar el recorrido.

   ![](../assets/personalization-uc-helpers-7.png)

6. Haga clic en **[!UICONTROL OK]**.

   Un mensaje le informa de que el contexto del recorrido se ha pasado al mensaje.

   ![](../assets/personalization-uc-helpers-8.png)

## Paso 4: Inserte la lista de elementos del carro de compras {#each-helper}

1. Vuelva a abrir el mensaje.

   ![](../assets/personalization-uc-helpers-18.png)

2. En la página de inicio del Diseñador de correo electrónico, haga clic en el componente HTML en el que desea enumerar el contenido del carro de compras.
3. En la barra de herramientas contextual, haga clic en **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

4. En la ventana **[!UICONTROL Edit HTML]**, añada el asistente `each`:
   1. En la lista, seleccione **[!UICONTROL Helper functions]**.
   2. Utilice el campo de búsqueda para encontrar &quot;cada uno&quot;.
   3. Desde los resultados de búsqueda, añada el asistente `each`.

      El editor de expresiones muestra esta expresión:

      ```handlebars
      {{#each someArray as |variable|}} {{/each}}
      ```

      ![](../assets/personalization-uc-helpers-9.png)

5. Agregue la matriz `productListItems` a la expresión:

   1. Elimine el marcador de posición &quot;someArray&quot; de la expresión.
   2. En la lista, seleccione **[!UICONTROL Context]**.

      La opción **[!UICONTROL Context]** solo está disponible una vez que el contexto de recorrido se ha pasado al mensaje.

   3. Seleccione **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Events]** > ***[!UICONTROL event_name]*** y, a continuación, expanda el nodo **[!UICONTROL productListItems]**.

      En este ejemplo, *event_name* representa el nombre del evento.

   4. Agregue el token **[!UICONTROL Product]** a la expresión.

      El editor de expresiones muestra esta expresión:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems.product as |variable|}} {{/each}}
      ```
      En este ejemplo, *event_ID* representa el ID del evento.

      ![](../assets/personalization-uc-helpers-10.png)

   5. Modifique la expresión:
      1. Elimine la cadena &quot;.product&quot;.
      2. Reemplace el marcador de posición &quot;variable&quot; por &quot;product&quot;.

      Este ejemplo muestra la expresión modificada:

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems as |product|}}
      ```
6. Pegue este código entre la etiqueta `{{#each}}` de apertura y la etiqueta `{/each}}` de cierre:

   ```html
   <table>
      <tbody>
         <tr>
            <td><b>#name</b></td>
            <td><b>#quantity</b></td>
            <td><b>$#priceTotal</b></td>
         </tr>
      </tbody>
   </table>
   ```

7. Agregue los tokens de personalización para el nombre del artículo, la cantidad y el precio:

   1. Elimine el marcador de posición &quot;#name&quot; de la tabla HTML.
   2. A partir de los resultados de búsqueda anteriores, añada el token **[!UICONTROL Name]** a la expresión.

   Repita estos pasos dos veces:
   * Sustituya el marcador de posición &quot;#quantity&quot; por el token **[!UICONTROL Quantity]**.
   * Sustituya el marcador de posición &quot;#priceTotal&quot; por el token **[!UICONTROL Total price]**.

   Este ejemplo muestra la expresión modificada:

   ```handlebars
   {{#each context.journey.events.event_ID.productListItems as |product|}}
      <table>
         <tbody>
            <tr>
               <td><b>{{context.journey.events.event_ID.productListItems.name}}</b></td>
               <td><b>{{context.journey.events.event_ID.productListItems.quantity}}</b></td>
               <td><b>${{context.journey.events.event_ID.productListItems.priceTotal}}</b></td>
            </tr>
         </tbody>
      </table>
   {{/each}}
   ```
8. Haga clic en **[!UICONTROL Validate]**, luego en **[!UICONTROL Save]**.
   ![](../assets/personalization-uc-helpers-11.png)

## Paso 5: Insertar una nota específica del producto {#if-helper}

1. En la página de inicio del Diseñador de correo electrónico, haga clic en el componente HTML en el que desea insertar la nota.
2. En la barra de herramientas contextual, haga clic en **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

3. En la ventana **[!UICONTROL Edit HTML]**, añada el asistente `if`:
   1. En la lista, seleccione **[!UICONTROL Helper functions]**.
   2. Utilice el campo de búsqueda para encontrar &quot;if&quot;.
   3. Desde los resultados de búsqueda, añada el asistente `if`.

      El editor de expresiones muestra esta expresión:

      ```handlebars
      {%#if condition1%} render_1
         {%else if condition2%} render_2
         {%else%} default_render
      {%/if%}
      ```
      ![](../assets/personalization-uc-helpers-12.png)

4. Elimine esta condición de la expresión:

   ```handlebars
   {%else if condition2%} render_2
   ```

   Este ejemplo muestra la expresión modificada:

   ```handlebars
   {%#if condition1%} render_1
      {%else%} default_render
   {%/if%}
   ```

5. Agregue el token del nombre del producto a la condición:
   1. Elimine el marcador de posición &quot;condición1&quot; de la expresión.
   2. En la lista, seleccione **[!UICONTROL Context]**.
   3. Seleccione **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Events]** > ***[!UICONTROL event_name]*** y, a continuación, expanda el nodo **[!UICONTROL productListItems]**.

      En este ejemplo, *event_name* representa el nombre del evento.

   4. Agregue el token **[!UICONTROL Name]** a la expresión.

      El editor de expresiones muestra esta expresión:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name%}
         render_1
         {%else%} default_render
      {%/if%}
      ```
      ![](../assets/personalization-uc-helpers-13.png)

6. Modifique la expresión:
   1. En el editor de expresiones, especifique el nombre del producto después del token `name`.

      Utilice esta sintaxis, donde *product_name* representa el nombre del producto:

      ```javascript
      = "product_name"
      ```

      En este ejemplo, el nombre del producto es &quot;Juno Jacket&quot;:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         render_1
         {%else%} default_render
      {%/if%}
      ```

   2. Reemplace el marcador de posición &quot;render_1&quot; por el texto de la nota.

      Ejemplo:

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         Due to longer than usual lead times on the Juno Jacket, please expect item to ship two weeks after purchase.
         {%else%} default_render
      {%/if%}
      ```
   3. Elimine el marcador de posición &quot;default_render&quot; de la expresión.
7. Haga clic en **[!UICONTROL Validate]**, luego en **[!UICONTROL Save]**.

   ![](../assets/personalization-uc-helpers-14.png)

8. Guarde y publique el mensaje.

## Paso 6: Prueba y publicación del recorrido {#test-and-publish}

1. Abra el recorrido. Si el recorrido ya está abierto, actualice la página.
2. Active la opción **[!UICONTROL Test]** y haga clic en **[!UICONTROL Trigger an event]**.

   Solo puede activar el modo de prueba después de publicar el mensaje.

   ![](../assets/personalization-uc-helpers-15.png)

3. En la ventana **[!UICONTROL Event configuration]**, introduzca los valores de entrada y haga clic en **[!UICONTROL Send]**.

   El modo de prueba solo funciona con perfiles de prueba.

   ![](../assets/personalization-uc-helpers-16.png)

   El correo electrónico se envía a la dirección del perfil de prueba.

   En este ejemplo, el correo electrónico contiene la nota sobre la Chaqueta Juno porque este producto está en el carro de compras:

   ![](../assets/personalization-uc-helpers-17.png)

4. Compruebe que no haya error y, a continuación, publique el recorrido.


## Temas relacionados

### Funciones de Handlebars

* [Ayudantes](functions/helpers.md)

* [Funciones de cadena](functions/string.md)

### Casos de uso

* [Personalización con información de perfil, contexto y oferta](personalization-use-case.md)

* [Personalización con oferta basada en decisiones](../offers/offers-e2e.md)

## Tutorial en vídeo{#helper-functions-video}

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)