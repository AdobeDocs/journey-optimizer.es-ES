---
solution: Journey Optimizer
title: Limitación del rendimiento con fuentes de datos externas y acciones personalizadas
description: Limitación del rendimiento con fuentes de datos externas y acciones personalizadas
feature: Journeys
topic: Content Management
role: User, Developer
level: Experienced
keywords: recorrido, fuentes de datos, límite, rendimiento, personalizado, acciones
exl-id: 45d6bb82-88ea-4510-a023-a75a82cc6f7b
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 3%

---

# Caso de uso: limitar el rendimiento con fuentes de datos externas y acciones personalizadas{#limit-throughput}

## Descripción del caso de uso

Adobe Journey Optimizer permite a los profesionales enviar llamadas de API a sistemas externos mediante el uso de acciones personalizadas y fuentes de datos.

Esto se puede hacer con :

* **Fuentes de datos**: para recopilar información de sistemas externos y utilizarla en el contexto del recorrido, por ejemplo para obtener información meteorológica sobre la ciudad del perfil y tener un flujo de recorrido específico basado en eso.

* **Acciones personalizadas**: para enviar información a sistemas externos, por ejemplo, para enviar correos electrónicos a través de una solución externa mediante las funciones de organización de Journey Optimizer junto con información de perfil, datos de audiencia y contexto de recorrido.

Si está trabajando con fuentes de datos externas o acciones personalizadas, es posible que desee proteger los sistemas externos limitando el rendimiento del recorrido: hasta 5000 instancias/segundo para recorridos unitarios y hasta 20 000 instancias/segundo para instancias activadas por segmentos. Puede definir límites de límite en el nivel de extremo para evitar sobrecargar esos sistemas externos a través de las API de restricción de Journey Optimizer. Sin embargo, todas las solicitudes restantes después de alcanzar el límite se retirarán.

En esta sección, encontrará soluciones alternativas que puede utilizar para optimizar su rendimiento. Para obtener más información sobre cómo integrarse con sistemas externos, consulte esta [página](../configuration/external-systems.md).

## Implementación

Para **recorridos activados por segmentos**, puede definir la tasa de regulación de la actividad Leer segmento que afectará al rendimiento del recorrido.  [Más información](../building-journeys/read-segment.md)

![](assets/limit-throughput-1.png)

Puede modificar este valor de 500 a 20 000 instancias por segundo. Si necesita bajar más de 500/s, también puede agregar condiciones de &quot;división porcentual&quot; con actividades de espera para dividir el recorrido en varias ramas y hacer que se ejecuten en un momento específico.

![](assets/limit-throughput-2.png)

Veamos un ejemplo de un **recorridos activados por segmentos** trabajar con una población de **10 000 perfiles** y enviar datos a un sistema externo compatible **100 solicitudes/segundo**.

1. Puede definir el segmento Leer para que lea perfiles con un rendimiento de 500 perfiles/segundo, lo que significa que tardará 20 segundos en leer todos los perfiles. En el segundo 1, leerá 500 de ellos, en el segundo 2 500 más, etc.

1. A continuación, puede agregar una actividad Condición de &quot;división porcentual&quot; con una división del 20 % para tener en cada segundo 100 perfiles en cada rama.

1. Después, agregue actividades de Espera con un temporizador específico en cada rama. Aquí hemos configurado una espera de 30 segundos para cada uno. En cada segundo, 100 perfiles fluirán en cada rama.

   * En la rama 1, esperarán 30 segundos, lo que significa que:
      * en el segundo 1, 100 perfiles esperarán al segundo 31
      * en el segundo 2, 100 perfiles esperarán al segundo 32, etc.
   * En la rama 2, esperarán 60 segundos, lo que significa que:
      * En el segundo 1, 100 perfiles esperarán al segundo 61 (1&#39;01&#39;&#39;)
      * En el segundo 2, 100 perfiles esperarán al segundo 62 (1&#39;02&#39;&#39;), etc.
   * Sabiendo que esperamos un máximo de 20 segundos para leer todos los perfiles, no habrá superposición entre cada rama, siendo el segundo 20 el último en el que los perfiles fluirán a la condición. Entre el segundo 31 y el segundo 51, se procesarán todos los perfiles de la rama 1. Entre el segundo 61 (1&#39;01&#39;&#39;) y el segundo 81 (1&#39;21&#39;&#39;), se procesarán todos los perfiles de la rama 2, etc.

   * Como protección, también puede agregar una sexta rama para tener menos de 100 perfiles por rama, especialmente si el sistema externo solo admite 100 solicitudes por segundo.



>[!IMPORTANT]
>
>Como con cualquier solución alternativa, pruebe esa solución a fondo antes de entrar en producción para asegurarse de que hace lo que desea.

Como protección adicional, también puede utilizar las capacidades de restricción.

>[!NOTE]
>
>A diferencia de las capacidades de restricción, que protegen un punto final al ser global para todos los recorridos de un entorno limitado, esta solución solo funciona a nivel de recorrido. Esto significa que si varios recorridos se ejecutan en paralelo y se dirigen al mismo punto final, tendrá que tenerlo en cuenta al diseñar el recorrido. Por lo tanto, esta solución no es adecuada para cada caso de uso.
