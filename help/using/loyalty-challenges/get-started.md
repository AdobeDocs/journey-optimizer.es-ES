---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los retos de fidelización
description: Aprenda a crear y administrar desafíos de lealtad en Adobe Journey Optimizer para crear programas de lealtad atractivos.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privada" type="Informative"
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 2%

---


# Introducción a los retos de fidelización {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Documentación de retos de fidelización:**

* **Introducción a los retos de fidelización** ◀︎ **Está aquí**: información general, flujo de trabajo, requisitos previos
* [Desafíos de fidelidad de acceso](access-loyalty-challenges.md): inventario y filtrado
* [Crear desafíos](create-challenges.md) - Generar y configurar desafíos
* [Administrar desafíos](manage-challenges.md): editar, supervisar y optimizar

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="Acerca de los retos de fidelización"
>abstract="Los retos de fidelidad le permiten crear ofertas de participación personalizadas que motivan a los clientes a completar acciones específicas y a obtener recompensas."

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Póngase en contacto con su representante de Adobe para obtener acceso.

## Información general {#overview}

Los Desafíos de fidelidad proporcionan una solución completa para crear programas de fidelidad a escala, desde la definición de tareas e hitos hasta la entrega de contenido y el seguimiento del rendimiento en todos los canales. Puede crear tres tipos de experiencias de desafío, configurar recompensas, enviar notificaciones de varios canales en etapas clave del ciclo vital y monitorizar el rendimiento a través de recorridos generados automáticamente, todo mientras mantiene la integración con su sistema de administración de lealtad externo.

## Funcionalidades clave {#key-capabilities}

Utilice los retos de fidelización para:

* **Crear tres tipos de desafíos**:
   * **Estándar**: Los clientes completan cualquier cantidad de tareas en cualquier orden para obtener recompensas
   * **Streak**: Los clientes completan la misma tarea varias veces de forma consecutiva
   * **Secuencial**: Los clientes completan tareas en un orden específico

* **Diseñar contenido de desafío**: use tarjetas de contenido de Journey Optimizer para crear la representación visual de su desafío en los dispositivos de los clientes. Las tarjetas de contenido muestran la información del desafío, el progreso y las recompensas.

* **Configurar los requisitos de las tareas**: Defina lo que los clientes deben hacer para obtener recompensas, entre ellas:
   * Tipos de tareas (compra, cantidad de gasto, visita, participación, eventos personalizados)
   * Requisitos de cantidad
   * Inclusiones/exclusiones de productos con SKU, categorías o atributos
   * Atributos y condiciones personalizados

* **Configurar recompensas**: Defina las recompensas que los clientes ganan al finalizar la tarea (recompensas progresivas) o después de completar todo el desafío (recompensas finales).

* **Enviar notificaciones multicanal**: Envíe mensajes a través de varios canales (en la aplicación, por correo electrónico, push) en las fases clave:
   * **Lanzamiento**: Cuando comienza el desafío
   * **En curso**: Cuando los clientes están en mitad de
   * **Completar**: cuando los clientes terminen el desafío

* **Seguimiento del rendimiento**: supervise los recorridos generados automáticamente y revise el rendimiento de los desafíos a través de informes integrados.

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

## Requisitos previos {#prerequisites}

Antes de usar Desafíos de fidelización, asegúrese de lo siguiente:

### Configuración de ingesta de datos {#data-ingestion}

Los desafíos de fidelización dependen de los datos introducidos a través de los conectores de origen de Experience Platform para rastrear el progreso de los clientes y la finalización de las tareas.

1. **Configurar un conector de origen admitido**: actualmente, el conector Capillary está disponible de forma general. Se han planificado conectores adicionales.

2. **Validar la ingesta de datos**: Asegúrese de que los eventos de lealtad y los datos de clientes fluyen a Experience Platform y están disponibles en Journey Optimizer.

Para obtener instrucciones detalladas, consulte:

* [Documentación de fuentes de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/sources/home)
* [Configuración de conectores de origen en Journey Optimizer](../start/get-started-sources.md)

### Permisos necesarios {#required-permissions}

Para utilizar Desafíos de fidelización, necesita los permisos adecuados en Journey Optimizer. Póngase en contacto con el administrador si no puede acceder a la función.

### Públicos destinatarios {#target-audiences}

Cree audiencias de destino en Experience Platform antes de crear desafíos. Puede seleccionar audiencias existentes, pero no puede crear nuevas audiencias desde la interfaz de usuario de Retos de fidelización.

## Limitaciones importantes {#limitations}

* **Sin sistema de contabilidad**: Los retos de fidelización no hacen un seguimiento de los valores monetarios ni de los saldos de puntos. Cuando los clientes completan un desafío y obtienen una recompensa, Journey Optimizer llama a su sistema de administración de lealtad externo para administrar la asignación de puntos.

* **Solo selección de audiencias**: puede seleccionar audiencias existentes, pero no puede crear nuevas audiencias desde la interfaz de usuario de Desafíos de fidelización.

## Próximos pasos {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Desafíos de fidelidad de acceso</strong></a>
    </div>
    <p>
    <em>Aprenda a acceder al inventario y filtrar los desafíos</em>
    <p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong>Crear desafíos</strong></a>
    </div>
    <p>
    <em>Cree y configure su primer desafío de fidelidad</em>
    <p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <!--<img alt="Manage" src="../assets/do-not-localize/monitor-button.svg">-->
    </a>
    <div>
    <a href="manage-challenges.md"><strong>Administrar desafíos</strong></a>
    </div>
    <p>
    <em>Editar, supervisar y optimizar desafíos</em>
    <p>
  </td>
</tr>
</table>
