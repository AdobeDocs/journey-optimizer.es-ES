---
title: Ayudantes
description: Ayudantes
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 5df4856c7be31a75116d906320ae50cd5dc6a2dc
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 4%

---

# Ayudantes {#gs-helpers}

## Valor de reserva predeterminado{#default-value}

La variable `Default Fallback Value` helper se utiliza para devolver un valor de reserva predeterminado si un atributo está vacío o es nulo. Este mecanismo funciona para los atributos de perfil y los eventos de Recorrido.

**Sintaxis**

```sql
Hello {%=profile.personalEmail.name.firstName ?: 'there' %}!
```

En este ejemplo, el valor `there` se muestra si la variable `firstName` el atributo de este perfil está vacío o es nulo.

## Condiciones{#if-function}

La variable `if` helper se utiliza para definir un bloque condicional.
Si la evaluación de la expresión devuelve el valor &quot;True&quot;, el bloque se procesa; de lo contrario, se omite.

**Sintaxis**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

A continuación se muestra la `if` ayuda, puede introducir un `else` para especificar un bloque de código que se va a ejecutar, si la misma condición es falsa.
La variable `elseif` especificará una nueva condición para comprobar si la primera sentencia devuelve el valor &quot;False&quot;.


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

1. **Representar diferentes vínculos de tienda basados en expresiones condicionales**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **Determinar la extensión de la dirección de correo electrónico**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Añadir un vínculo condicional**

   La siguiente operación agregará un vínculo al sitio web &quot;www.adobe.com/academia&#39;&quot; para perfiles con direcciones de correo electrónico &quot;.edu&quot; únicamente, al sitio web &quot;www.adobe.com/org&#39;&quot; para perfiles con direcciones de correo electrónico &quot;.org&quot; y a la URL predeterminada &quot;www.adobe.com/users&#39;&quot; para todos los demás perfiles:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Contenido condicional basado en la pertenencia a segmentos**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

1. **Determinar si un perfil ya es miembro**

   ```sql
   {%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
       You're a member!
   {%else%}
       You should be a member! Sign up now!
   {%/if%}
   ```

>[!NOTE]
>
>Para obtener más información sobre segmentación y servicio de segmentación, consulte esta [sección](../../segment/about-segments.md).


## Except{#unless}

La variable `unless` helper se utiliza para definir un bloque condicional. Por oposición a la `if`  ayuda, si la evaluación de la expresión devuelve false, se procesa el bloque .

**Sintaxis**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Ejemplo**

Representar contenido basado en la extensión de dirección de correo electrónico:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## Cada{#each}

La variable `each` ayuda se utiliza para iterar en una matriz.
La sintaxis del asistente es ```{{#each ArrayName}}``` YourContent {{/each}} Podemos hacer referencia a elementos de matriz individuales usando la palabra clave **this** dentro del bloque. El índice del elemento de la matriz se puede representar utilizando {{@index}}.

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

Representar una lista de productos que este usuario tiene en el carro de compras:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## con{#with}

La variable `with` ayuda se utiliza para cambiar el token de evaluación de template-part.

**Sintaxis**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

La variable `with` ayuda es útil para definir también una variable de acceso directo.

**Ejemplo**

Se utiliza con para alinear nombres de variables largos con nombres de variables más cortos:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

La variable `let` permite almacenar una expresión como variable para usarla más adelante en una consulta.

**Sintaxis**

```sql
{% let variable = expression %} {{variable}}
```

**Ejemplo**

El siguiente ejemplo permite todas las sumas de totales de productos con la transacción en USD donde la suma es buena a más de 100 $ y menor que 1000 $.

```sql
{% let variable = expression %} {{variable}}
```
