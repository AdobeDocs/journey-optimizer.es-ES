---
solution: Journey Optimizer
product: journey optimizer
title: Prácticas recomendadas de Journey Optimizer Experimentation Accelerator
description: Mejore su capacidad para realizar experimentos de forma eficaz y generar perspectivas
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: contenido, experimento, múltiple, audiencia, tratamiento
hide: true
hidefromtoc: true
source-git-commit: ddeb3512fbe1d1de86456fe2c3ccd2b3805b5684
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 2%

---

# Prácticas recomendadas de Journey Optimizer Experimentation Accelerator {#content-experiment-best-practices}

>[!BEGINSHADEBOX]

* [Introducción a Journey Optimizer Experimentation Accelerator](experiment-accelerator.md)
* **[Prácticas recomendadas de Journey Optimizer Experimentation Accelerator](experiment-accelerator-best-practices.md)**
* [Privacidad, seguridad y administración en Journey Optimizer Experimentation Accelerator](experiment-accelerator-security.md)
* [Monitorización de experimentos](experiment-accelerator-monitor.md)
* [Métricas de experimentación](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

## ¿Qué es la prueba A/B?

Las pruebas A/B son el proceso de comparar dos o más versiones de algo para determinar cuál tiene un mejor rendimiento con un objetivo definido.

A los participantes se les asigna aleatoriamente una versión, conocida como variante, y se rastrea su comportamiento. Los resultados muestran si una versión supera estadísticamente a las demás.

## Terminología clave

| Término | Definición |
|-|-|
| Control | La versión original utilizada como línea de base para la comparación. |
| Variante o tratamiento | Una nueva versión creada para probar con el control. |
| Hipótesis | Una predicción sobre qué cambio producirá un mejor resultado y por qué. |
| Tamaño de muestra | El número de individuos o sesiones incluidos en la prueba. |
| Relevancia estadística | Una medida de confianza de que los resultados no se deben a una probabilidad aleatoria. |
| Alza | La mejora porcentual o la disminución de una variante en comparación con el control. |
| Métrica principal | Medida principal utilizada para determinar el éxito de la prueba. |
| Métricas secundarias | Métricas de soporte que ofrecen insight adicional o ayudan a monitorizar los efectos no deseados. |
| Intervalo de confianza | Intervalo estimado dentro del cual es probable que caiga el efecto verdadero. |
| Segmento | Un subconjunto específico de la audiencia analizada de forma independiente (por ejemplo, usuarios nuevos o visitantes móviles). |

## Prácticas recomendadas para ejecutar experimentos

* **Empiece con una hipótesis clara**

  Una hipótesis sólida incluye lo que está cambiando, lo que espera que ocurra y por qué.
Ejemplo: _Creemos que cambiar X aumentará Y debido a Z._

* **Definir una métrica de éxito significativa**

  Elija una métrica que se ajuste a sus objetivos más amplios. Evite las métricas &quot;mnemónicas&quot; que tengan buen aspecto, pero que no reflejen un impacto real.

* **Probar un cambio a la vez (cuando sea posible)**

  Aislar variables facilita la interpretación precisa de los resultados. Si prueba varios cambios a la vez, es posible que no sepa qué causó el efecto.

* **Deje que la prueba se ejecute el tiempo suficiente**

  Las conclusiones prematuras pueden ser engañosas. Espere un tamaño de muestra estadísticamente significativo antes de actuar.

* **Tenga en cuenta los factores externos**

  La estacionalidad, las vacaciones y otros cambios en su entorno pueden distorsionar los resultados. Documente todo lo que pueda influir en el comportamiento durante la prueba.

* **Use la segmentación cuidadosamente**

  Desglosar los resultados por segmento de audiencia puede revelar patrones ocultos, pero evita sobreinterpretar tamaños de muestra pequeños.

* **Documentar y compartir aprendizajes**

  Mantenga un registro claro de lo que se ha probado, por qué y lo que ha aprendido. Esto construye conocimiento institucional y evita errores repetidos.

## Métricas comunes

| Métrica | Qué Mide | Cuándo usar |
|-|-|-|
| Tasa de conversión | El porcentaje de usuarios que completan una acción deseada | Útil para rastrear el éxito de una experiencia basada en objetivos |
| Tasa de clics (CTR) | El porcentaje de usuarios que hacen clic en un elemento específico | Indica lo atractiva que es la experiencia |
| Tasa de participación | El nivel de interacción que los usuarios tienen con la experiencia | Positivo para medir el interés o la atención |
| Tasa de devoluciones | El porcentaje de usuarios que se van rápidamente sin realizar ninguna acción | Puede indicar un mal ajuste o una experiencia confusa |
| Tiempo en la página | Cantidad de tiempo que los usuarios invierten en una parte específica de la experiencia | Puede reflejar la profundidad del interés o la complejidad |
| Ingresos por visitante (RPV) | Ingresos medios obtenidos por usuario | A menudo se utiliza en experimentos centrados en el comercio |
| Tasa de retención | El porcentaje de usuarios que regresan o que siguen participando con el tiempo | Útil para evaluaciones de valor a largo plazo |

## ¿Qué hace un buen experimento?

Un buen experimento no solo produce una victoria, sino que produce un aprendizaje claro y procesable.
Esto es lo que hay que buscar:

&check; **Confianza estadística**: Es poco probable que la diferencia entre las variantes se deba a la casualidad.
&check; **Alineación con objetivos**: La métrica principal refleja un progreso significativo hacia un objetivo comercial.
&amp; check; **Impacto secundario**: No hay efectos secundarios negativos significativos en las métricas relacionadas.
&check; **Escalabilidad**: El resultado puede informar decisiones futuras o generalizarse a otras áreas.
&check; **Claridad**: La causa del resultado está razonablemente aislada y comprendida.

La experimentación no se trata solo de encontrar la &quot;mejor&quot; versión, se trata de generar conocimiento a través de pruebas e iteraciones. Cuando se hace bien, los experimentos revelan perspectivas que impulsan decisiones más inteligentes, mejores experiencias de usuario y resultados mejorados.

>[!BEGINSHADEBOX]

**Ejemplo:**

* **Empresa**: Cadena hotelera
* **Hipótesis**: Si usamos un lenguaje más urgente en la página principal, se generarán más reservas.
   * **Control**: versión original
   * **Variante**: nueva versión con urgencia agregada
   * **Métrica principal**: Tasa de reserva
   * **Métricas secundarias**: Tasa de salida hacia otro sitio, tiempo en el sitio
* **Resultado**: la variante produjo un alza del 14% en la tasa de reserva, sin cambios negativos en otras métricas.
* **Acción**: considere la posibilidad de desplegar la variante y ejecutar experimentos de seguimiento para probar enfoques similares en otras áreas.

>[!ENDSHADEBOX]
