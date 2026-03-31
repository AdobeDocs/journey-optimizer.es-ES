---
title: Ayudantes
description: Ayudantes
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 4519c873e3391b63d0e879d797a99d9e67f83b87
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 4%

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
   <a href="https://www.somedomain.com/en">Checkout our catalog</a>
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
   {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Para obtener más información acerca de las audiencias y el servicio de segmentación, consulte [esta sección](../../audience/about-audiences.md).


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
Some edu specific content
{%/unless%}
```

## Cada{#each}

El asistente `each` se usa para iterar en una matriz.
La sintaxis del asistente es ```{{#each ArrayName}}``` YourContent `{{/each}}`
Podemos hacer referencia a los elementos de matriz individuales usando la palabra clave **this** dentro del bloque. El índice del elemento de la matriz se puede representar con `{{@index}}`.

**Sintaxis**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
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
{{/each}}
```

>[!NOTE]
>
>También puede usar el asistente `each` para repetir matrices devueltas por respuestas de acciones personalizadas. Para ver un ejemplo de repetir matrices anidadas a partir de una respuesta de acción personalizada, vea [Usar respuestas de acción personalizadas en canales nativos](../../action/action-response.md#response-in-channels).

## Con{#with}

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

## Metadatos de ejecución {#execution-metadata}

El asistente `executionMetadata` permite capturar y almacenar dinámicamente pares de clave-valor personalizados en el contexto de ejecución del mensaje.

**Sintaxis**

```
{{executionMetadata key="your_key" value="your_value"}}
```

En esta sintaxis, `key` hace referencia al nombre de los metadatos y `value` son los metadatos que se van a conservar.

**Caso de uso**

Con esta función, puede anexar información contextual a cualquier acción nativa desde sus campañas o recorridos. Esto permite exportar datos contextuales de envío en tiempo real a sistemas externos para varios fines, como seguimiento, análisis, personalización y procesamiento descendente.

>[!NOTE]
>
>* [acciones personalizadas](../../action/action.md) no admiten la función de metadatos de ejecución.
>* La función de metadatos de ejecución no está visible cuando se muestra el contenido en sí.

Por ejemplo, puede utilizar el asistente de Metadatos de ejecución para anexar un ID específico a cada entrega enviada a cada perfil. Esta información se genera durante el tiempo de ejecución y los metadatos de ejecución enriquecidos se pueden exportar para la reconciliación de flujo descendente con una plataforma de informes externa.

**Funcionamiento**

Seleccione cualquier elemento del contenido del canal dentro de una campaña o un recorrido y, con el editor de personalización, agregue el asistente de `executionMetadata` a este elemento.


Durante el tiempo de ejecución, el valor de los metadatos se agrega al **[!UICONTROL Conjunto de datos de evento de comentarios de mensajes]** existente con la siguiente adición de esquema:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!NOTE]
>
>Obtenga más información sobre los conjuntos de datos en [esta sección](../../data/get-started-datasets.md).

**Limitaciones**

Hay un límite superior de 2 kb en los pares de valor clave por acción. Si se supera el límite de 2 KB, el mensaje se envía, pero cualquiera de los pares de valor clave se puede truncar.

No se capturan metadatos para perfiles excluidos de la acción. Cuando se excluye a un perfil de la recepción de un mensaje, no se crea ninguna entrada de metadatos para ese perfil en el conjunto de datos.

**Ejemplo**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

En este ejemplo, suponiendo `profile.person.name.firstName` = &quot;Alex&quot;, la entidad resultante es:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

## Cifrado de parámetro de URL {#url-parameter-encryption-helper}

>[!AVAILABILITY]
>
>Esta función está disponible con disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.
>
>Actualmente, esta funcionalidad solo está disponible para el canal de correo electrónico.

El asistente `EncryptParam` le permite cifrar cualquier valor de expresión en tiempo de procesamiento (normalmente un atributo de perfil, un token o incluso una estructura JSON estructurada que genere en la expresión) antes de escribirlo en un parámetro de consulta en vínculos de seguimiento o páginas de aterrizaje.

Los valores que aparecerían como texto sin formato en la dirección URL (incluida la PII u otros datos confidenciales) no se pueden leer cuando se inspecciona o reenvía el vínculo. Solo se cifran los valores que ajuste con este asistente; el resto de la dirección URL no se modifica.

Puede aplicar el asistente a un parámetro, a varios o a todos los parámetros de un vínculo, según el diseño de la URL y las restricciones de longitud.

**Requisitos previos**

* El cifrado de parámetros de URL debe estar habilitado para su organización (disponibilidad limitada). Póngase en contacto con su representante de Adobe para obtener acceso.
* Un administrador debe crear al menos una clave activa en el registro de claves a nivel de zona protegida. [Aprenda a crear y administrar claves](../url-parameter-encryption.md)

**Funcionamiento**

1. En la lista de ayuda, seleccione el asistente `EncryptParam`.

1. Paso `data`: el valor o expresión que se va a cifrar (por ejemplo, `profile` campos, una variable o un token de cadena compuesto).

1. Pasar `key`: un identificador de clave activa desde el registro de claves de la zona protegida.

>[!NOTE]
>
>El uso de una clave revocada o no activa debería provocar un error en la personalización en el momento del procesamiento, de modo que no se envíe un mensaje con una clave no válida.

**Ejemplo**

Supongamos que define o calcula un valor (por ejemplo, una variable `stringToken` que contiene una carga útil JSON o identificadores concatenados) que no debe aparecer como texto sin formato en el parámetro de consulta `token`. Una dirección URL final puede seguir este patrón: reemplace `stringToken` por su expresión y `encrypt-key` por un identificador de clave activa del registro de claves:

```text
https://example.com/verify?token={{encrypt data=stringToken key="encrypt-key"}}
```

**Mecanismos de protección**

El descifrado se administra fuera de [!DNL Journey Optimizer] en sus páginas de aterrizaje, aplicaciones o API. Planifique el ciclo vital de la clave y la rotación con su equipo de seguridad para que las cargas útiles históricas se puedan descifrar donde sea necesario.

Las claves revocadas no deben utilizarse para el nuevo cifrado. Siga su política de seguridad para la rotación y el desmantelamiento.

