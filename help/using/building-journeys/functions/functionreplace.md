---
product: journey optimizer
title: replace
description: Obtenga información acerca de la sustitución de funciones
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: reemplazar, función, expresión, recorrido
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 11%

---

# replace {#replace}

Reemplaza la primera incidencia que coincida con la cadena de destino por la cadena de reemplazo de la cadena base.

La sustitución se realiza desde el principio de la cadena hasta el final, por ejemplo, si se sustituye &quot;a&quot; por &quot;b&quot; en la cadena &quot;aaa&quot;, el resultado será &quot;ba&quot; en lugar de &quot;ab&quot;.

## Categoría

Cadena

## Sintaxis de función

`replace(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|--------------|
| basar | cadena |
| destino | cadena (RegExp) |
| reemplazo | cadena |

## Firma y tipo devuelto

`replace(<base>,<target>,<replacement>)`

Devolver una cadena.

## Ejemplo 1

`replace("Hello World", "l", "x")`

Devuelve &quot;Mundo Hexlo&quot;.

## Ejemplo 2 {#example_2}

Dado que el parámetro de destino es RegExp, en función de la cadena que desee reemplazar, es posible que tenga que omitir algunos caracteres. Vea el siguiente ejemplo:

* cadena que evaluar: `|OFFER_A|OFFER_B`
* proporcionado por un atributo de perfil `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Cadena que reemplazar: `|OFFER_A`
* Cadena reemplazada por: `''`
* Debe agregar `\\` antes del carácter `|`.

La expresión es:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

La cadena devuelta es: `|OFFER_B`

También puede generar la cadena que desea reemplazar desde un atributo determinado:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`
