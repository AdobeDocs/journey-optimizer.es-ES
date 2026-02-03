---
solution: Journey Optimizer
product: journey optimizer
title: Crear desafíos de fidelidad
description: Aprenda a crear y configurar desafíos de lealtad en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privada" type="Informative"
source-git-commit: 7b075996eebd03f0aa812da3ece9cfebef8c65fc
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 1%

---


# Crear desafíos {#create-challenges}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_create_challenge"
>title="Crear un desafío de fidelidad"
>abstract="Cree un desafío de fidelidad para definir la oferta de participación, configurar las tarjetas de contenido para la entrega, añadir tareas, configurar recompensas y, opcionalmente, configurar la mensajería entre canales."

Cree un desafío de fidelidad para definir la oferta de participación, configurar las tarjetas de contenido, añadir tareas, configurar recompensas y configurar la mensajería entre canales.

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* [Introducción a los retos de fidelización](gs-loyalty-challenges.md): información general rápida y pasos siguientes
* [Comprender los desafíos de fidelidad](get-started.md): características, flujo de trabajo, requisitos previos
* **Crear desafíos** ◀︎ **Usted está aquí** - Generar y configurar desafíos
* [Administrar desafíos](manage-challenges.md): editar, supervisar y optimizar

>[!ENDSHADEBOX]

## Antes de comenzar {#before-you-start}

Antes de crear un desafío, asegúrese de lo siguiente:

* Ingesta de datos configurada y validada mediante conectores de origen
* Se han creado las audiencias necesarias en Experience Platform
* Recursos de contenido preparados (imágenes, texto, etc.) para su desafío
* Se han definido las tareas y las recompensas que desea ofrecer

## Crear un desafío {#create-a-challenge}

Para ver los pasos detallados sobre la creación de desafíos, incluidos:
* Configuración de propiedades de desafío
* Tipos de desafío (estándar, de racha, secuencial)
* Selección de audiencia
* Configuración de fecha

## Agregar tareas {#add-tasks}

Las tareas definen las acciones o los hitos específicos que los clientes deben completar para obtener recompensas en un desafío de lealtad. Puede configurar tipos de tareas, cantidades, requisitos de productos y valores de recompensa para crear experiencias de lealtad atractivas y personalizadas.

### Resumen de tareas {#task-overview}

Cada tarea representa una acción mensurable que contribuye a la finalización del desafío. Según el tipo de desafío (estándar, en Streak o secuencial), los clientes completan las tareas de forma diferente:

* **Desafíos estándar**: Los clientes completan cualquier número especificado de tareas en cualquier orden
* **Retos de la racha**: Los clientes completan la misma tarea varias veces consecutivamente
* **Desafíos secuenciales**: Los clientes completan las tareas en un orden definido

### Agregar una tarea {#add-task}

Para agregar una tarea al desafío:

1. Abra el desafío o cree uno nuevo.

2. Vaya a la sección **[!UICONTROL Tareas]**.

3. Seleccione **[!UICONTROL Agregar tarea]** o **[!UICONTROL Crear nueva tarea]**.

4. En la pantalla de creación de tareas, configure las siguientes propiedades.

### Propiedades de tarea {#task-properties}

#### Información básica de la tarea {#basic-info}

**[!UICONTROL Nombre de tarea]**: escriba un nombre descriptivo para la tarea. Este nombre es visible para usted y para su equipo, pero es posible que no se muestre a los clientes según el diseño de la tarjeta de contenido.

**[!UICONTROL Descripción de la tarea]**: (Opcional) Agregue detalles sobre el propósito o los requisitos de la tarea.

**[!UICONTROL Tipo de tarea]**: seleccione el tipo de acción que deben realizar los clientes. Los tipos de tareas disponibles incluyen:

* **[!UICONTROL Compra]**: el cliente realiza una transacción de compra
* **[!UICONTROL Importe del gasto]**: El cliente gasta un importe monetario especificado
* **[!UICONTROL Visita]**: El cliente visita una ubicación física o una propiedad digital
* **[!UICONTROL Participación]**: El cliente se involucra con contenido, como ver un vídeo o leer un artículo
* **[!UICONTROL Evento personalizado]**: el cliente déclencheur un evento personalizado rastreado a través de su ingesta de datos

#### Requisitos de cantidad {#quantity-requirements}

**[!UICONTROL Cantidad requerida]**: especifique cuántas veces debe realizar el cliente la tarea para completarla.

Por ejemplo:

* Para una tarea de compra: &quot;Comprar 2 artículos&quot; (cantidad = 2)
* Para una tarea de importe de gasto: &quot;Gasto de 50 $&quot; (cantidad = 50)
* Para una tarea de visita: &quot;Visita 5 veces&quot; (cantidad = 5)

**[!UICONTROL Período de seguimiento]**: (Opcional) Defina la ventana de tiempo para completar esta tarea:

* Duración por desafío (predeterminado)
* Por día
* Por semana
* Por mes
* Intervalo de fechas personalizado

### Filtrado de productos y SKU {#product-filtering}

Para las tareas de importe de compra y gasto, puede especificar qué productos cumplen los requisitos para la finalización de la tarea.

#### Inclusiones de productos {#product-inclusions}

Defina qué productos o categorías se contabilizan en la tarea:

1. Seleccione **[!UICONTROL Agregar criterios de producto]**.

2. Elija cómo definir los productos aptos:
   * **[!UICONTROL Por SKU]**: escribe códigos SKU de productos específicos
   * **[!UICONTROL Por categoría]**: selecciona categorías de productos de tu catálogo
   * **[!UICONTROL Por atributo]**: Filtre por atributos de producto como marca, tamaño, color o atributos personalizados

3. Introduzca o seleccione los identificadores de producto:

   **Ejemplo - Por SKU**:

   ```text
   SKU001, SKU002, SKU003
   ```

   **Ejemplo - Por categoría**:

   * Bebidas > Café
   * Panadería > Bollería

   **Ejemplo - Por atributo**:

   * Brand = &quot;Premium Brand&quot;
   * Categoría = &quot;Artículos de temporada&quot;
   * Precio > 20 $

4. Seleccione **[!UICONTROL Agregar]** para guardar los criterios del producto.

#### Exclusiones de productos {#product-exclusions}

De forma opcional, excluya productos específicos del recuento para la tarea:

1. Seleccione **[!UICONTROL Agregar exclusiones]**.

2. Utilice los mismos métodos de filtrado que las inclusiones de productos para especificar qué productos deben excluirse.

3. Escenarios de exclusión comunes:

   * Artículos de venta o despacho
   * Tarjetas de regalo
   * Artículos promocionales o gratuitos
   * Marcas o categorías específicas

>[!NOTE]
>
>**Lógica de inclusión y exclusión**: Cuando se definen inclusiones y exclusiones:
>
>* Los productos deben coincidir con los criterios de inclusión
>* Los productos que coinciden con los criterios de exclusión se eliminan, incluso si coinciden con las inclusiones
>* Si no se define ninguna inclusión, se clasifican todos los productos excepto los excluidos explícitamente

#### Ejemplos de filtrado de productos {#product-filtering-examples}

##### Ejemplo 1: Desafío de café {#example-1}

* Tipo de tarea: compra
* Cantidad requerida: 3
* Inclusiones: Categoría = &quot;Bebidas > Café&quot;
* Resultado: El cliente debe comprar 3 bebidas de café

##### Ejemplo 2: Gasto premium {#example-2}

* Tipo de tarea: Importe de gasto
* Cantidad requerida: 100 $
* Inclusiones: Marca = &quot;Marca Premium&quot;
* Exclusiones: Categoría = &quot;Liquidación&quot;
* Resultado: el cliente debe gastar 100 $ en artículos de marca Premium, sin incluir los de liquidación

##### Ejemplo 3: Compra de un producto específico {#example-3}

* Tipo de tarea: compra
* Cantidad requerida: 1
* Inclusiones: SKU = &quot;NEWPRODUCT2024&quot;
* Resultado: el cliente debe comprar el producto específico con el SKU &quot;NEWPRODUCT2024&quot;

### Configuración de recompensas {#configure-rewards}

Defina lo que los clientes ganan por completar tareas. Las recompensas se pueden otorgar en el nivel de tarea o en el nivel de desafío una vez que se hayan completado todas las tareas.

#### Momento de recompensa {#reward-timing}

Elija cuándo reciben los clientes las recompensas:

**[!UICONTROL Después de finalizar la tarea]**: Los clientes reciben una recompensa inmediatamente después de completar esta tarea específica (también denominada &quot;recompensas progresivas&quot; o &quot;recompensas de hito&quot;).

**[!UICONTROL Después de la finalización del desafío]**: Los clientes reciben una recompensa solo después de completar todas las tareas requeridas en el desafío (también llamadas &quot;recompensas finales&quot; o &quot;grandes premios&quot;).

>[!TIP]
>
>Puede combinar ambos tipos de recompensas en un único desafío para mantener la participación a lo largo del recorrido del cliente. Por ejemplo:
>
>* Otorgue 10 puntos después de completar cada tarea (recompensas progresivas)
>* Otorgue 100 puntos adicionales después de completar todo el desafío (recompensa final)

#### Tipos de recompensas y valores {#reward-types}

**[!UICONTROL Puntos]**: Otorgue puntos de lealtad a la cuenta del cliente.

* Introduzca el número de puntos (por ejemplo, 100)
* Los puntos se comunican al sistema de administración de lealtad externo a través de la API

**[!UICONTROL Descuento]**: proporcione un código o valor de descuento.

* Introducir tipo de descuento (porcentaje o importe fijo)
* Introducir valor de descuento
* Si lo desea, especifique el código de descuento o deje que el sistema genere uno

**[!UICONTROL Artículo gratuito]**: otorga un producto o servicio gratuito.

* Especifique el SKU o la descripción del artículo
* Indica cómo se debe reclamar el artículo gratuito

**[!UICONTROL Recompensa personalizada]**: define un tipo de recompensa personalizado.

* Escriba la descripción del premio
* Proporcione códigos o identificadores relevantes
* Configurar cómo se entrega o reclama la recompensa

## Configuración de tarjetas de contenido {#configure-content-cards}

Para ver los pasos detallados sobre la configuración de tarjetas de contenido, incluyendo:
* Configuración de tarjeta de contenido
* Diseño y personalización
* Previsualización y pruebas

## Configuración de mensajería {#configure-messaging}

Para ver los pasos detallados sobre la configuración de la mensajería multicanal, incluyendo:
* Canales de mensajes (en la aplicación, correo electrónico, push)
* Fases del mensaje (inicio, en curso, finalización)
* Déclencheur y tiempo de los mensajes

## Revisión y publicación {#review-and-publish}

Antes de publicar el desafío:

1. **Revisar todos los componentes**: Desafío de propiedades, tareas, recompensas, contenido, mensajes
2. **Probar la experiencia**: Use perfiles de prueba para validar déclencheur de tareas y contenido
3. **Publicar**: Active el desafío para la audiencia de destino

El recorrido generado automáticamente se activa en la fecha de inicio especificada.

## Próximos pasos {#next-steps}

* [Administrar desafíos](manage-challenges.md): Aprenda a editar, monitorizar y optimizar desafíos
* [Comprender los desafíos de fidelidad](get-started.md): revise las características y capacidades
