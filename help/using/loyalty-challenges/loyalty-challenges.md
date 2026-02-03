---
solution: Journey Optimizer
product: journey optimizer
title: Desafíos de fidelización
description: Aprenda a crear y administrar desafíos de lealtad en Adobe Journey Optimizer para crear programas de lealtad atractivos.
feature: Loyalty challenges
topic: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privada" type="Informative"
version: Journey Orchestration
source-git-commit: b68c2610cbaaa8dbd86deb677562185e08d517ea
workflow-type: tm+mt
source-wordcount: '5146'
ht-degree: 1%

---


# Desafíos de fidelización {#loyalty-challenges}

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Póngase en contacto con su representante de Adobe para obtener acceso.

Los retos de fidelidad le permiten crear ofertas de participación personalizadas para sus clientes, lo que le ayuda a orquestar programas de fidelidad a escala. Puede diseñar desafíos con tareas e hitos específicos, recompensar a los clientes por completarlos y ofrecer la experiencia a través de canales de Adobe Journey Optimizer.

>[!BEGINSHADEBOX]
>
>**En esta guía:**
>
>* [Información general](#overview) - Comprender lo que ofrecen los desafíos de fidelidad
>* [Cómo funciona](#how-it-works): flujo de trabajo paso a paso desde la configuración hasta la supervisión
>* [Requisitos previos](#prerequisites): configurar la ingesta de datos y los permisos
>* [Desafíos de fidelidad de acceso](#access): abre el menú y ve los desafíos
>* [Crear desafíos](#create-challenges) - Crear nuevos desafíos de lealtad
>* [Crear tareas](#create-tasks) - Definir lo que los clientes deben hacer
>* [Administrar desafíos](#manage-challenges): editar, supervisar y optimizar
>
>[!ENDSHADEBOX]

## Información general {#overview}

Los retos de fidelidad le permiten diseñar e implementar ofertas de participación personalizadas que motiven a los clientes a completar acciones específicas y obtener recompensas. La funcionalidad proporciona una solución completa para crear programas de fidelidad a escala, desde definir tareas e hitos hasta ofrecer contenido y rastrear el rendimiento en todos los canales. Puede crear tres tipos de experiencias de desafío, configurar recompensas, enviar notificaciones de varios canales en etapas clave del ciclo vital y monitorizar el rendimiento a través de recorridos generados automáticamente, todo mientras mantiene la integración con su sistema de administración de lealtad externo.

## Funcionamiento {#how-it-works}

La creación y el lanzamiento de un desafío de fidelidad siguen este flujo de trabajo:

1. **Configurar la ingesta de datos**: configure los conectores de origen de Experience Platform (como Capillary) para introducir datos de evento de lealtad que hagan un seguimiento de las acciones y el progreso de los clientes.

2. **Crear un desafío**: defina las propiedades básicas del desafío, como nombre, tipo (Estándar, Streak o Secuencial), audiencia e intervalo de fechas.

3. **Agregar tareas**: defina las acciones específicas que deben completar los clientes, incluidos los tipos de tareas (compras, gastos, visitas, etc.), cantidades, filtros de productos y recompensas.

4. **Diseñar tarjetas de contenido**: cree la representación visual de su desafío con tarjetas de contenido de Journey Optimizer que se muestran en los dispositivos del cliente.

5. **Configurar mensajes** (opcional): configure mensajes multicanal (en la aplicación, correo electrónico, push) para las fases clave: inicio, en curso y finalización.

6. **Revisar y publicar**: pruebe el desafío con perfiles de prueba y, a continuación, publíquelo para que esté disponible para la audiencia de destino.

7. **recorrido generado automáticamente**: cuando publica, Journey Optimizer crea automáticamente un recorrido que organiza la entrega y la mensajería de la tarjeta de contenido.

8. **Activar recorrido**: el recorrido generado automáticamente se activa en la fecha de inicio del desafío y administra todas las interacciones con los clientes.

9. **Monitorizar el rendimiento**: haga un seguimiento de la participación, las tasas de finalización, la distribución de recompensas y la participación en los mensajes mediante informes integrados y el lienzo de recorrido.

>[!NOTE]
>
>El recorrido generado automáticamente aparece en el inventario de recorridos y se puede personalizar si es necesario. Sin embargo, los cambios realizados directamente en el recorrido no se sincronizan con la configuración de desafío.

## Funcionalidades clave

Utilice los retos de fidelización para:

* **Crear tres tipos de desafíos**:
   * **Estándar**: Los clientes completan cualquier cantidad de tareas para obtener recompensas.
   * **Streak**: Los clientes completan la misma tarea varias veces.
   * **Secuencial**: Los clientes completan tareas en un orden específico.

* **Diseñar contenido de desafío**: use tarjetas de contenido de Journey Optimizer para crear la representación visual de su desafío en los dispositivos de los clientes. Las tarjetas de contenido muestran la información del desafío, el progreso y las recompensas en el dispositivo del cliente.

* **Configurar los requisitos de las tareas**: Defina lo que los clientes deben hacer para obtener recompensas, entre ellas:
   * Tipos de tareas (compra, cantidad de gasto, visita, etc.)
   * Requisitos de cantidad
   * Inclusiones/exclusiones de productos con SKU
   * Atributos y condiciones personalizados

* **Configurar recompensas**: defina las recompensas que los clientes ganan al finalizar la tarea o después de completar todo el desafío

* **Enviar notificaciones**: Envíe mensajes a través de varios canales (en la aplicación, correo electrónico, push) en las fases clave:
   * **Lanzamiento**: Cuando comienza el desafío
   * **En curso**: Cuando los clientes están en mitad de
   * **Completar**: cuando los clientes terminen el desafío

* **Seguimiento del rendimiento**: supervise los recorridos generados automáticamente y revise el rendimiento de los desafíos

### Limitaciones importantes {#limitations}

* **Sin sistema de contabilidad**: Los retos de fidelización no hacen un seguimiento de los valores monetarios ni de los saldos de puntos. Cuando los clientes completan un desafío y obtienen una recompensa, Journey Optimizer llama a su sistema de administración de lealtad externo para administrar la asignación de puntos.

* **Solo selección de audiencias**: puede seleccionar audiencias existentes, pero no puede crear nuevas audiencias desde la interfaz de usuario de Desafíos de fidelización.

## Requisitos previos {#prerequisites}

Antes de usar Desafíos de fidelización, asegúrese de lo siguiente:

* Configuración de ingesta de datos

  Los desafíos de fidelización dependen de los datos introducidos a través de los conectores de origen de Experience Platform para rastrear el progreso de los clientes y la finalización de las tareas.

   1. **Configurar un conector de origen admitido**: actualmente, el conector Capillary está disponible de forma general. Se han planificado conectores adicionales.

   2. **Validar la ingesta de datos**: Asegúrese de que los eventos de lealtad y los datos de clientes fluyen a Experience Platform y están disponibles en Journey Optimizer.

  Para obtener instrucciones detalladas, consulte:

   * [Documentación de fuentes de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/sources/home)
   * [Configuración de conectores de origen en Journey Optimizer](../start/get-started-sources.md)

* Permisos necesarios {#required-permissions}

Para utilizar Desafíos de fidelización, necesita los permisos adecuados en Journey Optimizer. Póngase en contacto con el administrador si no puede acceder a la función.

## Acceder a retos de fidelización {#access}

Para acceder a Desafíos de fidelización:

1. En Adobe Journey Optimizer, seleccione **[!UICONTROL Desafíos de fidelización]** en el menú de navegación de la izquierda.

   <!--![Loyalty challenges menu in left navigation](assets/loyalty-challenges-menu.png)-->

2. El inventario Retos de fidelización muestra todos los desafíos existentes con información como la siguiente:
   * Nombre y descripción del desafío
   * Estado (Borrador, Activo, Detenido, etc.)
   * Tipo de desafío (estándar, ramificado, secuencial)
   * Fecha de inicio y de finalización
   * Fecha de la última modificación

   <!--![Loyalty challenges inventory showing list of challenges](assets/loyalty-challenges-inventory.png)-->

3. Seleccione **[!UICONTROL Crear desafío]** para comenzar a crear un nuevo desafío.

### Buscar y filtrar desafíos {#search-filter}

Utilice las funciones de búsqueda y filtrado para encontrar rápidamente desafíos específicos:

#### Buscar {#search}

Escriba el nombre del desafío o las palabras clave para encontrar desafíos coincidentes en el campo **[!UICONTROL Buscar]**.

#### Filtrar por estado {#filter-by-status}

Mostrar desafíos con estados específicos en **[!UICONTROL Filtrar por estado]**:

* Borrador
* Programado
* Activo
* Completado
* Detenido
* Archivado

#### Filtrar por tipo {#filter-by-type}

Mostrar solo los desafíos estándar, de ramificación o secuenciales usando **[!UICONTROL Filtrar por tipo]**.

#### Filtrar por fecha {#filter-by-date}

Mostrar desafíos dentro de un intervalo de fechas específico mediante **[!UICONTROL Filtrar por fecha]**.

#### Filtrar por etiquetas {#filter-by-tags}

Mostrar desafíos con etiquetas específicas aplicadas usando **[!UICONTROL Filtrar por etiquetas]**.


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

#### Ejemplo de configuración de recompensa {#reward-example}

**Desafío**: &quot;Desafío del amante del café&quot;

**Tarea 1**: Compra 3 cafés

* Recompensa: 30 puntos (10 puntos por café)
* Intervalo: después de finalizar la tarea

**Tarea 2**: Prueba 2 nuevas bebidas de temporada

* Recompensa: 50 puntos
* Intervalo: después de finalizar la tarea

**Premio por finalización de desafío**:

* Recompensa: Café gratis + 100 puntos de bonificación
* Intervalo: una vez completadas todas las tareas

**Recompensas totales posibles**: 180 puntos + 1 café gratis

### Atributos de tarea avanzados {#advanced-attributes}

En los casos de uso avanzados, puede configurar atributos de tarea adicionales:

**[!UICONTROL Condiciones personalizadas]**: agregue lógica o condiciones personalizadas más allá de los tipos de tareas estándar mediante segmentos o reglas de Experience Platform.

**[!UICONTROL Geoperimetraje]**: (para tareas de visita) requiere visitas a ubicaciones específicas definidas por coordenadas geográficas y radio.

**[!UICONTROL Requisitos basados en tiempo]**: requieren que las tareas se completen durante horas, días o intervalos de fechas específicos.

**[!UICONTROL Período de reutilización]**: establezca un tiempo mínimo entre las finalizaciones de las tareas para evitar que se repitan acciones rápidamente.

**[!UICONTROL Dependencias de tareas]**: (para desafíos secuenciales) Defina los requisitos previos que deben completarse antes de que esta tarea esté disponible.

## Crear desafíos {#create-challenges}

Cree un desafío de fidelidad para definir la oferta de participación, configurar las tarjetas de contenido para la entrega, añadir tareas, configurar recompensas y, opcionalmente, configurar la mensajería entre canales.

### Antes de comenzar {#before-you-start}

Antes de crear un desafío, asegúrese de lo siguiente:

* Ingesta de datos configurada y validada mediante conectores de origen
* Se han creado las audiencias necesarias en Experience Platform
* Recursos de contenido preparados (imágenes, texto, etc.) para su desafío
* Se han definido las tareas y las recompensas que desea ofrecer

### Crear un desafío {#create-a-challenge}

Para crear un nuevo desafío de fidelidad:

1. En Journey Optimizer, seleccione **[!UICONTROL Desafíos de fidelización]** en el menú de navegación de la izquierda.

2. Seleccione **[!UICONTROL Crear desafío]** en la esquina superior derecha.

   <!--![Create challenge button in loyalty challenges inventory](assets/create-challenge-button.png)-->

3. En la pantalla de propiedades del desafío, configure lo siguiente:

#### Propiedades básicas {#basic-properties}

**[!UICONTROL Nombre]**: escriba un nombre descriptivo para el desafío. Este nombre aparece en el inventario y se incluye en el nombre del recorrido generado automáticamente.

**[!UICONTROL Descripción]**: (Opcional) Agregue una descripción para ayudarle a usted y a su equipo a comprender el propósito y los detalles de este desafío.

**[!UICONTROL Tipo de desafío]**: seleccione el tipo de desafío que desea crear:

* **[!UICONTROL Estándar]**: los clientes pueden completar cualquier cantidad de tareas especificadas en cualquier orden para obtener el premio. Ejemplo: &quot;Realizar 5 compras este mes&quot;.

* **[!UICONTROL Streak]**: los clientes deben completar la misma tarea repetidamente. Ejemplo: &quot;Visite nuestra tienda 10 veces seguidas&quot;.

* **[!UICONTROL Secuencial]**: los clientes deben completar las tareas en un orden específico. Ejemplo: &quot;Primero realice una compra, luego escriba una opinión y luego recomendar a un amigo&quot;.

<!--![Challenge type selection showing Standard, Streak, and Sequential options](assets/challenge-type-selection.png)-->

**[!UICONTROL Fecha de inicio]**: seleccione cuándo el desafío se activará y estará disponible para los clientes.

**[!UICONTROL Fecha de finalización]**: seleccione cuándo caduca el desafío. Los clientes que no hayan completado el desafío en esta fecha ya no podrán obtener el premio.

#### Selección de audiencia {#audience-selection}

**[!UICONTROL Seleccionar audiencia]**: elige la audiencia elegible para este desafío. Solo puede seleccionar audiencias existentes; no puede crear nuevas audiencias desde la interfaz de usuario de Retos de fidelización.

Para crear o refinar audiencias, consulte [Crear audiencias en Journey Optimizer](../audience/about-audiences.md).

1. Seleccione **[!UICONTROL Guardar como borrador]** para seguir configurando el desafío.

## Creación de tareas {#create-tasks}

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

   <!--![Tasks section in challenge creation interface](assets/tasks-section.png)-->

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

<!--![Task type selection dropdown showing available task types](assets/task-type-selection.png)-->

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

   <!--![Add product criteria button in task configuration](assets/add-product-criteria.png)-->

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

## Configuración de tarjetas de contenido {#configure-content-cards}

Las tarjetas de contenido son la forma principal en que se muestran los desafíos a los clientes en sus dispositivos. Debe configurar una tarjeta de contenido para el desafío.

1. En su desafío, vaya a la ficha **[!UICONTROL Contenido]**.

2. Seleccione **[!UICONTROL Editar contenido]** para abrir el editor de la tarjeta de contenido.

   <!--![Content tab with Edit content button](assets/content-tab-edit.png)-->

3. Configure las propiedades de la tarjeta de contenido:

   **[!UICONTROL Nombre de configuración]**: escriba un nombre para esta configuración de la tarjeta de contenido.

   **[!UICONTROL Configuración]**: seleccione o cree una configuración de tarjeta de contenido. Define la configuración técnica de cómo se entrega la tarjeta de contenido.

4. En el editor de la tarjeta de contenido, diseñe la tarjeta de desafío:

   * Añada texto para describir el desafío, las tareas y las recompensas
   * Incluir imágenes u otros elementos visuales
   * Utilizar la personalización para incluir información específica del cliente
   * Mostrar indicadores de progreso, si corresponde
   * Añadir botones de call-to-action

   El editor de la tarjeta de contenido proporciona las mismas capacidades que otros canales de Journey Optimizer. Para obtener instrucciones detalladas, consulte [Diseño de tarjetas de contenido](../content-card/design-content-card.md).

5. Seleccione **[!UICONTROL Guardar]** para guardar la configuración de la tarjeta de contenido.

>[!NOTE]
>
>La tarjeta de contenido se entrega a través del recorrido generado automáticamente. Se muestra a los miembros de la audiencia aptos cuando el desafío está activo.

## Configuración de mensajería {#configure-messaging}

Si lo desea, puede configurar los mensajes que se enviarán a los clientes en las etapas clave del ciclo de vida del desafío. La mensajería está disponible en tres etapas:

* **[!UICONTROL Launch]**: envía un mensaje cuando el desafío se active
* **[!UICONTROL En curso]**: envía un mensaje cuando los clientes estén a mitad del desafío
* **[!UICONTROL Completar]**: envía un mensaje cuando los clientes completen el desafío

### Añadir mensajes {#add-messages}

1. En su desafío, vaya a la ficha **[!UICONTROL Mensajería]**.

   <!--![Messaging tab showing Launch, In progress, and Complete stages](assets/messaging-tab-stages.png)-->

2. Seleccione la fase en la que desea añadir un mensaje: Launch, In progress o Complete.

3. Seleccione **[!UICONTROL Agregar mensaje]**.

4. Elija el canal para el mensaje:
   * **[!UICONTROL En la aplicación]**: muestra un mensaje en la aplicación
   * **[!UICONTROL Correo electrónico]**: Enviar una notificación por correo electrónico
   * **[!UICONTROL Push]**: enviar una notificación push

5. Seleccione **[!UICONTROL Editar contenido]** para abrir el editor de contenido del canal seleccionado.

6. Diseñe el mensaje con el editor de contenido estándar:
   * Agregar texto, imágenes y otros elementos de contenido
   * Utilizar la personalización para incluir información específica del cliente
   * Incluir detalles del desafío como progreso o recompensas
   * Añadir contenido dinámico en función de los atributos o comportamientos del cliente

   Para obtener instrucciones específicas del canal, consulte:
   * [Creación de mensajes en la aplicación](../in-app/create-in-app.md)
   * [Creación de correos electrónicos](../email/create-email.md)
   * [Creación de notificaciones push](../push/create-push.md)

7. Seleccione **[!UICONTROL Guardar]** para guardar el mensaje.

8. Repita estos pasos para agregar mensajes para otras etapas o canales según sea necesario.

>[!NOTE]
>
>Puede agregar varios mensajes por fase, lo que le permite llegar a los clientes a través de diferentes canales. Por ejemplo, puede enviar un correo electrónico y una notificación push cuando se inicie un desafío.

### Déclencheur y tiempo de los mensajes {#message-timing}

**Mensajes de lanzamiento**: se envían cuando el desafío se activa a la audiencia elegible.

**Mensajes en curso**: Se activa cuando los clientes alcanzan un punto de progreso especificado. Puede configurar las condiciones de déclencheur en función de lo siguiente:

* Número de tareas completadas
* Porcentaje de desafíos completados
* Finalización de tarea específica
* Tiempo transcurrido desde el inicio del desafío

**Mensajes completos**: se envían cuando los clientes completan correctamente todas las tareas necesarias.

>[!TIP]
>
>**Prácticas recomendadas para la mensajería**:
>
>* Mantenga los mensajes concisos y centrados en el desafío
>* Comunicar claramente el valor y las recompensas
>* Usar una marca y un tono coherentes
>* Incluir llamadas a la acción claras
>* Mensajes de prueba antes de publicar el desafío

## Generar y personalizar recorridos {#generate-journey}

Al guardar un desafío con el contenido y la mensajería configurados, Journey Optimizer genera automáticamente un recorrido en el servidor.

### Funcionamiento de la generación de recorridos {#journey-generation-process}

1. Al guardar un desafío y seleccionar **[!UICONTROL Generar recorrido]**, Journey Optimizer crea un nuevo recorrido.

2. El nombre del recorrido se asigna automáticamente en función del nombre del desafío (por ejemplo, &quot;Desafío: [Nombre del desafío]&quot;).

3. El lienzo de recorrido incluye:
   * Actividad de **[!UICONTROL Leer audiencia]** con la audiencia que seleccionó
   * **Acción de envío de la tarjeta de contenido**
   * **Actividades de mensajes** para cualquier mensaje que haya configurado (Inicio, En curso, Completado)
   * **Espere** y **Condicione** actividades según sea necesario según su configuración

   <!--![Auto-generated journey canvas showing content card and message activities](assets/generated-journey-canvas.png)-->

4. El recorrido aparece en el inventario de recorrido y es visible para todos los usuarios con los permisos adecuados.

### Ver el recorrido generado {#view-journey}

Para ver el recorrido generado automáticamente:

1. Vaya a **[!UICONTROL Recorridos]** en el menú de navegación de la izquierda.

2. Busque el recorrido por nombre de desafío o filtre por etiquetas si las ha asignado.

3. Seleccione el recorrido para ver su lienzo y configuración.

### Personalización del recorrido {#customize-journey}

Puede editar el recorrido generado automáticamente para agregar lógica personalizada, actividades adicionales o configuraciones avanzadas.

>[!IMPORTANT]
>
>**Consideraciones importantes al editar recorridos**:
>
>* Los cambios realizados en el lienzo de recorrido **no se sincronizan** con la interfaz de usuario de los desafíos de fidelidad
>* El desafío sigue siendo la fuente fiable para la definición de la experiencia principal
>* Journey Optimizer muestra una advertencia cuando se entra en el modo de edición personalizado
>* Si necesita realizar cambios en las tareas, las recompensas o las propiedades del desafío principal, edítelos en la interfaz de usuario de Desafíos de fidelidad, no en el recorrido
>* Las ediciones de recorrido personalizadas son adecuadas para la lógica avanzada de enrutamiento, sincronización o integración

Para personalizar el recorrido:

1. Abra el recorrido generado desde el inventario de recorridos.

2. Journey Optimizer muestra una advertencia sobre la edición personalizada. Lea detenidamente la advertencia y reconózcala.

3. Realice los cambios que desee con el lienzo de recorrido:
   * Agregar actividades adicionales (esperas, condiciones, acciones)
   * Configuración de reglas de frecuencia o temporización avanzadas
   * Añadir acciones o integraciones personalizadas
   * Modificar condiciones de entrada de audiencia

4. Pruebe exhaustivamente los cambios antes de publicar.

5. Publique el recorrido cuando esté listo.

Para obtener instrucciones detalladas sobre la edición de recorridos, consulte [recorridos de compilación](../building-journeys/journey-gs.md).

### Consideraciones del lienzo de recorrido {#journey-considerations}

Al trabajar con recorridos generados automáticamente:

* **No se puede editar la audiencia en el recorrido**: Si necesita cambiar la audiencia, hágalo en la interfaz de usuario de Desafíos de fidelidad y vuelva a generar el recorrido.

* **Actualizaciones del contenido del mensaje**: los cambios en el contenido del mensaje deben realizarse en la interfaz de usuario de los retos de fidelidad para mantener la coherencia.

* **Estado del Recorrido**: El estado del recorrido (Borrador, Activo, Detenido) se administra independientemente del estado del desafío.

* **Pruebas**: Pruebe toda la experiencia del desafío, no solo el recorrido, para asegurarse de que todos los componentes funcionan juntos correctamente.

## Revisión y publicación {#review-and-publish}

Antes de publicar el desafío:

1. **Revisar todos los componentes**:
   * Propiedades y fechas del desafío
   * Tareas y requisitos de las tareas
   * Configuración de premios
   * Diseño de tarjeta de contenido
   * Contenido y tiempo de mensajería
   * Estructura del recorrido generada

2. **Probar la experiencia**:
   * Uso de perfiles de prueba para validar la representación de contenido
   * Comprobar que las tareas entran correctamente en déclencheur según los datos de prueba
   * Verificar lógica de asignación de recompensas
   * Prueba de mensajería en todos los canales configurados
   * Revise la ejecución del recorrido con las audiencias de prueba

3. **Publicar su desafío**:
   * Cuando esté listo, seleccione **[!UICONTROL Publicar]** de las propiedades del desafío
   * El desafío se activa en la fecha de inicio especificada
   * El recorrido generado automáticamente se activa
   * Los miembros de la audiencia aptos pueden ver el desafío y participar en él

## Gestionar desafíos {#manage-challenges}

Después de crear y publicar desafíos de fidelidad, puede verlos, editarlos, monitorizarlos y optimizarlos para garantizar que proporcionen los resultados deseados para su programa de fidelidad.

### Estados de desafío {#challenge-statuses}

Cada reto se desplaza por un ciclo de vida reflejado en su estado:

**[!UICONTROL Borrador]**: el desafío se está creando o editando, pero aún no se ha publicado. Puede realizar cualquier cambio en los desafíos de borrador.

**[!UICONTROL Programado]**: el desafío se ha publicado y se activa en su fecha de inicio. Los clientes aún no pueden ver ni participar en los desafíos programados.

**[!UICONTROL Activo]**: el desafío está activo y los clientes de la audiencia elegible pueden verlo y participar en él. Este estado aparece cuando la fecha actual está entre las fechas de inicio y finalización.

**[!UICONTROL Completado]**: el desafío ha pasado su fecha de finalización o se han cumplido todos los objetivos. Los clientes ya no pueden participar, pero puede ver los datos históricos y los resultados.

**[!UICONTROL Detenido]**: el desafío se detuvo manualmente antes de completarse. Los clientes ya no pueden participar. Para reactivar un desafío detenido, debe duplicarlo y crear una nueva versión.

**[!UICONTROL Archivado]**: el desafío se archivó con fines organizativos. Los desafíos archivados se pueden recuperar mediante filtros, pero están ocultos en la vista predeterminada.

### Ver detalles del desafío {#view-details}

Para ver información detallada sobre un desafío:

1. En el inventario, haga clic en el nombre del desafío o seleccione el menú **[!UICONTROL Más acciones]** (tres puntos) y elija **[!UICONTROL Ver detalles]**.

   <!--![Challenge inventory with More actions menu highlighted](assets/challenge-more-actions.png)-->

2. Se muestra la pantalla de detalles del desafío:

   **[!UICONTROL Ficha Información general]**:
   * Propiedades básicas (nombre, descripción, tipo, fechas)
   * Estado actual e información del ciclo vital
   * Información de audiencia
   * Historial de creación y modificación

   Ficha **[!UICONTROL Tareas]**:
   * Lista de todas las tareas del desafío
   * Tipos de tareas, requisitos y condiciones
   * Recompensas configuradas por tarea

   **[!UICONTROL Contenido]** ficha:
   * Configuración y previsualización de la tarjeta de contenido
   * Representación visual de cómo los clientes ven el desafío

   Ficha **[!UICONTROL Mensajes]**:
   * Mensajes configurados para las fases de Launch, In progress y Complete
   * Asignaciones de canales y previsualizaciones de contenido

   **[!UICONTROL Rendimiento]** (para desafíos activos y completados):
   * Métricas de participación
   * Tasas de finalización
   * Distribución de recompensas
   * Estadísticas de participación de mensajes

### Editar desafíos {#edit-challenges}

Puede editar los desafíos según su estado actual.

#### Editar borrador de desafíos {#edit-draft}

Para desafíos en estado **[!UICONTROL Borrador]**:

1. Haz clic en el nombre del desafío o selecciona **[!UICONTROL Editar]** en el menú de acciones.

2. Modifique cualquier aspecto del desafío:
   * Propiedades básicas
   * Tareas y premios
   * Tarjetas de contenido
   * Mensajería
   * Selección de audiencia

3. Seleccione **[!UICONTROL Guardar como borrador]** para guardar los cambios sin publicarlos, o **[!UICONTROL Publicar]** para activar el desafío.

#### Editar desafíos publicados {#edit-published}

Para desafíos que están **[!UICONTROL programados]** o **[!UICONTROL activos]**:

>[!IMPORTANT]
>
>**Impacto de editar desafíos en vivo**: Los cambios en los desafíos en vivo pueden afectar a los clientes que ya participan. Tenga en cuenta lo siguiente antes de realizar cambios:
>
>* Modificar los requisitos de las tareas puede invalidar el progreso del cliente
>* Cambiar recompensas puede crear incoherencias en los clientes que ya han obtenido recompensas
>* Los cambios de audiencia pueden excluir a los clientes que anteriormente eran aptos
>* Los cambios de contenido aparecen inmediatamente a los clientes
>
>Para ver cambios significativos, considere la posibilidad de detener el desafío actual y crear una nueva versión.

**Edición limitada para desafíos en vivo**:

Puede realizar estos cambios en los desafíos en directo sin detenerlos:

* Actualizar descripción del desafío (orientado hacia dentro)
* Modificar texto e imágenes de la tarjeta de contenido
* Actualización del contenido de mensajería
* Ajustar fecha de finalización (solo ampliación, no se puede acortar)
* Adición o modificación de etiquetas

**Cambios que requieren duplicación de desafío**:

Para cambiar estas propiedades, debe duplicar el desafío y crear una nueva versión:

* Tipo de desafío (estándar, ramificado, secuencial)
* Requisitos y condiciones de las tareas
* Valores de recompensa y reglas de asignación
* Fecha de inicio (para desafíos en directo)
* Audiencia (cambios importantes)

### Duplicación de un desafío {#duplicate-challenge}

Al duplicar, se crea una copia de un desafío existente que se puede modificar y publicar como un nuevo desafío:

1. En el inventario, seleccione el menú **[!UICONTROL Más acciones]** (tres puntos) para el desafío que desee duplicar.

2. Seleccione **[!UICONTROL Duplicar]**.

3. En el cuadro de diálogo de duplicación:
   * Introduzca un nuevo nombre para el desafío duplicado
   * Si lo desea, modifique la descripción
   * Elija si quiere copiar la configuración de la audiencia
   * Elija si desea copiar las configuraciones de mensajería

4. Seleccione **[!UICONTROL Duplicar]**.

5. El desafío duplicado se abre en modo de borrador, donde puede realizar cambios antes de publicar.

**Escenarios de duplicación comunes**:

* Volver a ejecutar un desafío correcto para un nuevo período de tiempo
* Crear variaciones de un desafío para diferentes audiencias
* Actualizar los requisitos o recompensas de las tareas para una nueva versión
* Reactivar un desafío detenido o completado

### Detener un desafío {#stop-challenge}

Para detener un desafío activo o programado antes de su fecha de finalización natural:

1. Seleccione el desafío en el inventario.

2. Seleccione **[!UICONTROL Detener desafío]** en el menú de acciones.

3. En el cuadro de diálogo de confirmación, revise el impacto:
   * Los clientes que participan actualmente ya no pueden realizar ningún progreso
   * Los clientes que hayan completado tareas pero no el desafío completo no recibirán recompensas finales
   * El recorrido asociado se ha detenido
   * El desafío no se puede reiniciar (debe duplicarse para reutilizarse)

4. Seleccione **[!UICONTROL Detener]** para confirmar.

>[!NOTE]
>
>**Detención frente a finalización**: un desafío detenido finaliza antes de tiempo y no sigue el proceso de finalización normal. Los clientes reciben recompensas parciales ya asignadas, pero no recompensas de finalización de desafío final. Considere la posibilidad de comunicar el extremo anticipado a los clientes afectados.

### Archivar desafíos {#archive}

Archivar los desafíos completados o detenidos para mantener el inventario organizado:

1. Seleccione el menú **[!UICONTROL Más acciones]** (tres puntos) para el desafío.

2. Seleccione **[!UICONTROL Archivar]**.

3. El desafío pasa al estado archivado y está oculto de la vista de inventario predeterminada.

Para ver los desafíos archivados:

1. En el inventario, aplique el filtro **[!UICONTROL Estado]**.

2. Seleccione **[!UICONTROL Archivado]**.

3. Los desafíos archivados se muestran con la misma información que los desafíos activos.

Para desarchivar un desafío:

1. Busque el desafío archivado mediante filtros.

2. Seleccione **[!UICONTROL Desarchivar]** del menú de acciones.

3. El desafío vuelve a su estado anterior (Completado o Detenido).

### Eliminar desafíos {#delete}

Elimine los desafíos que ya no sean necesarios:

>[!IMPORTANT]
>
>**La eliminación es permanente**: los desafíos eliminados no se pueden recuperar. Solo elimine los desafíos que esté seguro de que no necesitará en el futuro. Considere la posibilidad de archivar en lugar de eliminar para mantener los registros históricos.

**Reglas de eliminación**:

* Solo puedes eliminar desafíos en estado **[!UICONTROL Borrador]**
* Los desafíos publicados, programados, activos o completados no se pueden eliminar
* Para eliminar un desafío publicado, primero debe detenerlo y luego archivarlo

Para eliminar un desafío de borrador:

1. Seleccione el menú **[!UICONTROL Más acciones]** (tres puntos) para el desafío.

2. Seleccione **[!UICONTROL Eliminar]**.

3. En el cuadro de diálogo de confirmación, confirme la eliminación.

## Monitorización del rendimiento {#monitor-performance}

Realice un seguimiento de cómo los clientes se relacionan con los desafíos mediante métricas de rendimiento integradas.

### Métricas de rendimiento {#performance-metrics}

La pestaña Rendimiento muestra métricas clave para los desafíos activos y completados:

<!--![Performance metrics dashboard showing participation and completion data](assets/performance-metrics-dashboard.png)-->

**[!UICONTROL Métricas de participación]**:

* **Clientes elegibles totales**: Cantidad de clientes en la audiencia de destino
* **Clientes inscritos**: Cantidad de clientes que vieron el desafío o participaron en él
* **Tasa de inscripción**: Porcentaje de clientes elegibles que se inscribieron
* **Participantes activos**: número de clientes que progresan actualmente

**[!UICONTROL Métricas de finalización]**:

* **Clientes completados**: Cantidad de clientes que terminaron todas las tareas
* **Tasa de finalización**: Porcentaje de clientes inscritos que completaron el desafío
* **Tiempo promedio de finalización**: Tiempo promedio desde la inscripción hasta la finalización
* **Tareas completadas**: Número total de tareas individuales completadas en todos los clientes

**[!UICONTROL Métricas de recompensa]**:

* **Recompensas totales distribuidas**: Suma de todas las recompensas asignadas
* **Recompensas por tipo**: desglose por puntos, descuentos, artículos gratis, etc.
* **Recompensa promedio por cliente**: Valor de recompensa promedio para los clientes participantes

**[!UICONTROL Métricas de participación]**:

* **Impresiones de tarjetas de contenido**: Número de veces que se mostró el desafío
* **Clics en la tarjeta de contenido**: Número de veces que los clientes interactuaron con la tarjeta de desafío
* **Envío de mensaje**: número de mensajes enviados para las fases de lanzamiento, en curso y completados
* **Participación en mensajes**: Tasas de apertura y de clics para mensajes por fase y canal

### Ver informes de rendimiento {#view-reports}

Para acceder a los datos de rendimiento detallados:

1. Abra el desafío y vaya a la ficha **[!UICONTROL Rendimiento]**.

2. Seleccione el intervalo de fechas para la creación de informes (hoy, últimos 7 días, últimos 30 días, intervalo personalizado).

3. Revisar métricas por:
   * **Información general**: resumen de alto nivel de métricas clave
   * **Cronología**: Tendencias de rendimiento con el tiempo
   * **Desglose**: Métricas segmentadas por atributos, canales o tareas del cliente

4. Exportar informes con el botón **[!UICONTROL Exportar]** para un análisis más detallado.

### Monitorización del recorrido generado {#monitor-journey}

El recorrido generado automáticamente contiene datos valiosos sobre la ejecución:

1. En los detalles del desafío, seleccione **[!UICONTROL Ver recorrido]** para abrir el recorrido asociado.

2. En el lienzo del recorrido, revise:
   * **Informe de Recorrido**: Estadísticas generales de ejecución
   * **Informes de actividades**: Rendimiento de actividades individuales
   * **Métricas de entrada y salida**: Cuántos clientes entraron y salieron
   * **Registros de errores**: Cualquier problema o error de ejecución

3. Utilice la monitorización del recorrido para identificar:
   * Cuellos de botella en los que los clientes abandonan
   * Problemas técnicos que afectan al envío
   * Rendimiento de los mensajes por canal
   * Oportunidades de optimización de tiempo

Para obtener instrucciones detalladas sobre la supervisión del recorrido, consulte [Supervisión de los recorridos](../building-journeys/report-journey.md).

### Optimización de desafíos {#optimize}

Utilice los datos de rendimiento para mejorar los desafíos actuales y futuros:

**[!UICONTROL Variaciones de pruebas]**: cree desafíos duplicados con diferentes tareas, recompensas o mensajes para comparar el rendimiento.

**[!UICONTROL Ajustar tiempo]**: modifique la duración del desafío o las fechas límites de la tarea según los patrones de finalización.

**[!UICONTROL Refinar audiencia]**: amplía o reduce la selección de audiencias en función de las tasas de participación y finalización.

**[!UICONTROL Actualizar contenido]**: actualice las tarjetas de contenido y los mensajes para mantener el interés y la claridad.

**[!UICONTROL Optimización de recompensas]**: ajuste los valores de recompensas para equilibrar el costo y la participación.

**[!UICONTROL Dificultad de la tarea]**: modifica los requisitos de las tareas si son demasiado fáciles o difíciles según los datos de finalización.

## Validación y prueba de tareas {#validation-testing}

Antes de publicar el desafío, compruebe que las tareas estén configuradas correctamente:

1. **Comprobar lógica de tarea**:
   * Verificar que los requisitos de cantidad son realistas
   * Asegúrese de que los criterios de filtrado de productos son correctos
   * Confirmar que las recompensas están configuradas correctamente

2. **Prueba con perfiles de prueba**:
   * Crear perfiles de prueba que representen diferentes escenarios de cliente
   * Envío de eventos de prueba a través de su canalización de ingesta de datos
   * Comprobar que las tareas se realizan correctamente en déclencheur
   * Confirmar que las recompensas se asignan según lo esperado

3. **Revisar asignación de datos**:
   * Asegúrese de que los datos de evento entrantes se asignan correctamente a los requisitos de tareas
   * Compruebe que los SKU, las categorías y los atributos coinciden entre su sistema de origen y Journey Optimizer
   * Casos extremos de prueba (faltan datos, valores no válidos, etc.)

## Prácticas recomendadas {#best-practices}

### Creación de desafío

**Empiece de forma sencilla**: para su primer desafío, comience con un desafío estándar simple para familiarizarse con el proceso.

**Realice pruebas exhaustivas**: Pruebe siempre el desafío con perfiles y audiencias de prueba antes de publicarlo en toda la base de clientes.

**Comunicación clara**: Asegúrate de que los clientes entienden lo que tienen que hacer, lo que ganarán y para cuándo.

**Momento realista**: establezca fechas de inicio y finalización apropiadas, lo que permitirá a los clientes disponer de tiempo suficiente para completar el desafío.

**Recompensas atractivas**: haga que las recompensas sean valiosas y relevantes para su audiencia para impulsar la participación.

### Configuración de tarea

**Borrar requisitos**: Haga que los requisitos de las tareas sean claros y alcanzables. Evite condiciones demasiado complejas.

**Dificultad apropiada**: Equilibre la dificultad de la tarea con el valor de recompensa. Las tareas más difíciles deberían ofrecer mayores recompensas.

**Precisión en el filtrado de productos**: Compruebe los SKU, las categorías y los atributos para garantizar una coincidencia precisa de los productos.

**Recompensas progresivas**: Use recompensas de hito (después de la finalización de la tarea) para mantener la participación del cliente durante todo el desafío.

**Flexibilidad**: para los desafíos estándar, permita flexibilidad en la forma en que los clientes completan las tareas para adaptarse a diferentes comportamientos y preferencias.

### Gestión y monitorización

**Supervisión regular**: compruebe el rendimiento del desafío al menos una vez por semana para detectar desafíos en vivo a fin de identificar los problemas de forma temprana.

**Borrar nombres**: Use nombres descriptivos que indiquen el propósito del desafío, la audiencia o el período de tiempo para facilitar la organización.

**Use etiquetas**: Aplique etiquetas coherentes para categorizar los desafíos por campaña, temporada, segmento de audiencia u otros atributos relevantes.

**Cambios de documento**: anote por qué realizó cambios en los desafíos para referencia y aprendizaje futuros.

**Archivar de forma coherente**: Archive los desafíos completados con regularidad para mantener un inventario manejable.

**Comunicar cambios**: Si modifica un desafío activo, informe a los clientes afectados sobre los cambios que afectan su participación.

**Analizar tras la finalización**: revise el rendimiento después de que finalice cada desafío para identificar las lecciones aprendidas para los desafíos futuros.

**Despliegue gradual**: para nuevos tipos de desafío o cambios significativos, considere la posibilidad de comenzar con una audiencia más pequeña antes de la implementación completa.

**Control de versiones**: use un control de versiones claro en los nombres de desafío al crear iteraciones (por ejemplo, &quot;Desafío de vacaciones 2024 - v2&quot;).

## Solución de problemas {#troubleshooting}

**El desafío no aparece para los clientes**:

* Verificar que el desafío esté en estado Activo
* Compruebe que los clientes estén en la audiencia elegible
* Confirme que la configuración de la tarjeta de contenido es correcta
* Revise los registros de ejecución del recorrido para ver los problemas de envío

**Tasas de participación bajas**:

* Revisar la visibilidad y el atractivo de la tarjeta de contenido
* Compruebe que la mensajería comunique claramente el valor
* Asegúrese de que las tareas sean alcanzables y de que las recompensas sean atractivas
* Verifique que la segmentación de audiencia sea adecuada

**Tareas que no se desencadenan**:

* Compruebe que los datos se están ingiriendo correctamente desde los conectores de origen
* Compruebe que los atributos de evento coinciden con los requisitos de tareas
* Revisar elegibilidad de audiencia

**No se asignan las recompensas**:

* Confirme que la configuración de recompensa es correcta
* Verificar la conexión con el sistema de administración de fidelidad externo
* Comprobar errores en los registros de envío de recompensas

**El filtrado de productos no funciona**:

* Validar códigos SKU y nombres de categorías
* Asegúrese de que la asignación de atributos sea correcta
* Probar con datos de compra de muestra

**El Recorrido no genera**:

* Confirme que se ha completado toda la configuración necesaria
* Compruebe si hay errores en la pestaña Mensajería
* Verificar que la tarjeta de contenido esté configurada
* Revisar registros de errores del sistema

**No se muestran los datos de rendimiento**:

* Deje tiempo para que los datos se propaguen (hasta 24 horas)
* Verificar que los eventos se rastrean correctamente
* Comprobar estado de ingesta de datos
* Asegúrese de que los clientes hayan empezado a participar

## comentarios de Beta {#beta-feedback}

Durante la fase beta, sus comentarios son valiosos para ayudarnos a mejorar los Retos de fidelidad. Comparta su experiencia, preguntas y sugerencias con su representante de Adobe o a través de los canales de comentarios beta proporcionados durante el inicio.

## Temas relacionados {#related-topics}

* [Crear audiencias en Journey Optimizer](../audience/about-audiences.md)
* [Diseño de tarjetas de contenido](../content-card/design-content-card.md)
* [Creación de mensajes en la aplicación](../in-app/create-in-app.md)
* [Creación de correos electrónicos](../email/create-email.md)
* [Creación de notificaciones push](../push/create-push.md)
* [Generar recorridos](../building-journeys/journey-gs.md)
* [Monitorización de los recorridos](../building-journeys/report-journey.md)
* [Documentación de fuentes de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/sources/home)
* [Configuración de conectores de origen en Journey Optimizer](../start/get-started-sources.md)
