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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 0%

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
