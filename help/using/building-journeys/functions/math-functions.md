---
product: journey optimizer
title: Funciones matemáticas
description: Más información sobre las funciones matemáticas
feature: Journeys
role: Developer
level: Experienced
keywords: matemáticas, funciones, expresión, recorrido, cálculo, número
version: Journey Orchestration
exl-id: da710b22-3112-41fe-8b91-2b6563b79f27
TQID: https://experienceleague.adobe.com/POIbPCZrqtqGjHqn3ehGonxwv9KhKWlgg2igdN8Y4yw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 475
ht-degree: 2%

---

# Funciones matemáticas {#math-functions}

Las funciones matemáticas proporcionan operaciones matemáticas esenciales para los cálculos numéricos dentro de las expresiones de recorrido. Estas funciones permiten realizar cálculos numéricos y transformaciones precisos en los datos.

Utilice funciones matemáticas cuando necesite:

* Generar valores aleatorios para pruebas, muestreo o aleatorización ([random](#random))
* Redondear números decimales al entero más cercano para una presentación de datos más limpia ([round](#round))
* Realizar cálculos matemáticos en campos numéricos
* Transformar valores numéricos para la lógica empresarial y la toma de decisiones

Las funciones matemáticas administran tipos decimales y enteros, administrando automáticamente las conversiones de tipos para garantizar resultados precisos en las expresiones de recorrido.

## random {#random}

Genera un número aleatorio entre 0 y 1.

+++Sintaxis

`random()`

+++

+++Firma y tipo devuelto

`random()`

Devuelve un valor decimal.

+++

## round {#round}

Devuelve el valor entero más cercano al argumento con vínculos de redondeo al infinito positivo.

+++Sintaxis

`round(<parameters>)`

+++

+++Parámetros

* decimal
* entero

+++

+++Firmas y tipo devuelto

`round(<decimal>)`

`round(<integer>)`

Devuelve un entero.

+++

+++Ejemplos

`round(3.14)`

Devuelve 3.

`round(3.54)`

Devuelve 4.

`round(-3.14)`

Devuelve -3.

`round(3)`

Devuelve 3.

+++

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página documenta las dos funciones matemáticas disponibles en las expresiones de recorrido de AJO: `random` para generar un decimal aleatorio entre 0 y 1, y `round` para redondear un decimal o entero al entero más cercano.

**Intenciones:**
* Genere un valor decimal aleatorio entre 0 y 1 para la lógica de muestreo o aleatorización usando `random`
* Redondear un número decimal al entero más cercano mediante `round`
* Aplique el redondeo en la lógica empresarial donde se requieren números enteros de los cálculos decimales

**Glosario:**
* **random**: Una función que devuelve un valor decimal pseudoaleatorio de 0 (inclusive) a 1 (exclusivo) *(específico del producto)*
* **round**: Una función que devuelve el entero más cercano a la entrada, con valores medios redondeados hacia el infinito positivo

**Protecciones:**
* `random()` no toma parámetros
* `round` acepta entradas decimales o enteras y siempre devuelve un entero
* Las conexiones en `round` se resuelven redondeando hacia el infinito positivo (por ejemplo, 3,5 rondas a 4, -3,5 rondas a -3)

**Terminología:**
* Nombre canónico: Funciones matemáticas — Acrónimo: none — variantes: funciones matemáticas, funciones numéricas
* Sinónimos: &quot;round&quot; = &quot;round to near integer&quot;
* No confundir: &quot;redondear&quot; (redondea al entero más cercano) ≠ funciones de conversión como `toInteger` (trunca la parte decimal sin redondear)

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Qué devuelve `random()`?** — Devuelve un número decimal aleatorio entre 0 y 1.
* **Q: ¿Cómo gestiona `round` los números negativos?** — Se redondea hacia el infinito positivo, por lo que `round(-3.14)` devuelve -3 y `round(-3.54)` devuelve -3 también (el entero más cercano al infinito positivo).
* **Q: ¿Cuál es la diferencia entre `round` y `toInteger`?** — `round` redondea al entero más próximo (3,7 se convierte en 4), mientras que `toInteger` trunca la parte decimal sin redondear (3,7 se convierte en 3).
* **Q: ¿Toma `random` algún parámetro?** — No, `random()` no requiere parámetros y siempre devuelve un decimal entre 0 y 1.

+++
