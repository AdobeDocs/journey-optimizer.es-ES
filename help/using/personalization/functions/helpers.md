---
title: Ayudantes
description: Ayudantes
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 7e7ff2f6451947d4d52efb2963d940ba3f50819f
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 5%

---

# Ayudantes {#gs-helpers}

## Valor de reserva predeterminado{#default-value}

El asistente `Default Fallback Value` se usa para devolver un valor de reserva predeterminado si un atributo está vacío o es nulo. Este mecanismo funciona para atributos de perfil y eventos de Recorrido.

**Sintaxis**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

En este ejemplo, el valor `there` se muestra si el atributo `firstName` de este perfil está vacío o es nulo.

## Condiciones{#if-function}

El asistente `if` se usa para definir un bloque condicional.
Si la evaluación de la expresión devuelve true, se procesa el bloque; de lo contrario, se omite.

**Sintaxis**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Después del asistente `if`, puede escribir una instrucción `else` para especificar un bloque de código que se va a ejecutar, si la misma condición es falsa.
La instrucción `elseif` especificará una nueva condición para comprobar si la primera instrucción devuelve el valor &quot;False&quot;.


**Formato**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**Ejemplos**

1. **Procesar vínculos de almacén diferentes basados en expresiones condicionales**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **Determinar extensión de dirección de correo electrónico**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Agregar un vínculo condicional**

   La siguiente operación añade un vínculo al sitio web www.adobe.com/academia&#39; solo para perfiles con direcciones de correo electrónico &quot;.edu&quot;, al sitio web www.adobe.com/org&#39; para perfiles con direcciones de correo electrónico &quot;.org&quot; y a la URL predeterminada www.adobe.com/users&#39; para el resto de perfiles:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Contenido condicional basado en la pertenencia a audiencias**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Para obtener más información acerca de las audiencias y el servicio de segmentación, consulte esta [sección](../../audience/about-audiences.md).


## Unless{#unless}

El asistente `unless` se usa para definir un bloque condicional. Por oposición al asistente `if`, si la evaluación de la expresión devuelve false, se procesará el bloque.

**Sintaxis**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Ejemplo**

Procese contenido en función de la extensión de dirección de correo electrónico:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## Each{#each}

El asistente `each` se usa para iterar en una matriz.
La sintaxis del asistente es ```{{#each ArrayName}}``` YourContent {{/each}}
Podemos hacer referencia a los elementos de matriz individuales usando la palabra clave **this** dentro del bloque. El índice del elemento de la matriz se puede representar con {{@index}}.

**Sintaxis**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

**Ejemplo**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Ejemplo**

Procese una lista de productos que este usuario tiene en el carro de compras:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## With{#with}

El asistente `with` se usa para cambiar el token de evaluación de la plantilla-parte.

**Sintaxis**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

El ayudante `with` también resulta útil para definir una variable de acceso directo.

**Ejemplo**

Use con para asignar nombres de variables largos a otros más cortos:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

La función `let` permite almacenar una expresión como variable para usarla posteriormente en una consulta.

**Sintaxis**

```sql
{% let variable = expression %} {{variable}}
```

**Ejemplo**

El siguiente ejemplo permite calcular la suma total de los precios de los productos del carro de compras con precios entre 100 y 1000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```
