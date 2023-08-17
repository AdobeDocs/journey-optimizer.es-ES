---
solution: Journey Optimizer
product: journey optimizer
title: Validación de personalización
description: Obtenga más información sobre la validación de personalización y cómo solucionar problemas.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor, validación, errores, personalización
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---

# Validación de personalización {#personalization-validation}

## Mecanismos de validación {#validation-mechanisms}

En el **Editor de expresiones** pantalla, utilice el **Validate** para comprobar la sintaxis de personalización.

>[!NOTE]
> La validación se ejecuta automáticamente al hacer clic en **Añadir** para cerrar la ventana del editor.
>

![](assets/perso_validation1.png)

>[!IMPORTANT]
> Si la sintaxis de personalización no es válida, no se puede cerrar la ventana del editor de expresiones.
>

## Errores comunes {#common-errors}

* **No se encontró la ruta &quot;XYZ&quot;**

Al intentar hacer referencia a un campo que no está definido en el esquema.

En este caso **firstName1** no se define como atributo en el esquema de perfil:

```
{{profile.person.name.firstName1}}
```

* **No coinciden los tipos para la variable &quot;XYZ&quot;. Matriz esperada. Cadena encontrada.**

Al intentar repetir una cadena en lugar de una matriz:

En este caso **producto** no es una matriz:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Sintaxis de handlebars no válida. Encontrado`‘[XYZ}}’`**

Cuando se utiliza sintaxis de handlebars no válida.

Las expresiones Handlebars están rodeadas por **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **Definición de segmento no válida**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## Errores específicos relacionados con las ofertas {#specific-errors}

Los errores relacionados con la integración de ofertas en un mensaje de correo electrónico o push tienen el siguiente patrón:

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

La validación se realiza durante la validación del contenido de personalización en el Editor de expresiones.

<table> 
 <thead> 
  <tr> 
   <th> Título de error<br /> </th> 
   <th> Validación/resolución <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>No se ha encontrado el recurso con ID de colocación y tipo OfferPlacement <br/>
No se ha encontrado el recurso con ID de actividad y tipo de actividad de oferta<br/></td> 
   <td>Comprobar si ActivityID o PlacementID están disponibles</td> 
  </tr> 
   <tr> 
   <td>No se ha podido validar el recurso.</td> 
   <td>El componentType de Placement debe coincidir con la oferta de offerType</td> 
  </tr> 
   <tr> 
   <td>La URL pública no está presente en offerId.</td> 
   <td>Las ofertas de imágenes (todas personalizadas y de reserva asociadas con el par de decisión y ubicación) deben tener rellenada una URL pública (deliveryURL no debe estar vacío).</td> 
  </tr> 
  <tr> 
   <td>La decisión contiene atributos que no son de perfil.</td> 
   <td>El uso del modelo de ofertas debe contener solo los atributos de perfil.</td> 
  </tr> 
  <tr> 
   <td>Error al recuperar el uso de decisión.</td> 
   <td>Este error se puede producir cuando la API intenta recuperar el modelo de oferta.</td> 
  </tr>
  <tr> 
   <td>Offer Attribute offer-attribute no es válido.</td> 
   <td>Compruebe si el atributo de oferta al que se hace referencia en la colocación de oferta es válido. A continuación se muestran los atributos válidos: <br/>
Imagen: deliveryURL, linkURL<br/>
Texto: content<br/>
HTML: content<br/></td> 
  </tr> 
 </tbody> 
</table>
