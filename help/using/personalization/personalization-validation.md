---
title: Validación de personalización
description: Obtenga más información sobre validación de personalización y cómo solucionar problemas.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: 2d859a5dab19a419d424acefd17d254473c00818
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 2%

---

# Validación de personalización {#personalization-validation}

## Mecanismos de validación {#validation-mechanisms}

En el **Editor de expresiones** , utilice el **Validar** para comprobar la sintaxis de personalización.

>[!NOTE]
> La validación se ejecuta automáticamente al hacer clic en el **Agregar** para cerrar la ventana del editor.

![](assets/perso_validation1.png)

>[!IMPORTANT]
> Si la sintaxis de personalización no es válida, no se puede cerrar la ventana del editor de expresiones.

## Errores comunes {#common-errors}

* **Ruta &quot;XYZ&quot; no encontrada**

Al intentar hacer referencia a un campo que no está definido en el esquema.

En este caso **firstName1** no se define como atributo en el esquema de perfil:

```
{{profile.person.name.firstName1}}
```

* **El tipo no coincide con la variable &quot;XYZ&quot;. Matriz esperada. Se ha encontrado una cadena.**

Cuando se intenta iterar sobre una cadena en lugar de una matriz:

En este caso **producto** no es una matriz:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Sintaxis de controladores no válida. Encontrado`‘[XYZ}}’`**

Cuando se utiliza una sintaxis de controladores no válida.

Las expresiones de Handlebars están rodeadas de **{{expression}}**

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

La validación se realiza durante la publicación del mensaje o durante la validación del contenido de personalización en el editor de expresiones.

<table> 
 <thead> 
  <tr> 
   <th> Título de error<br /> </th> 
   <th> Validación / Resolución <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>No se encontró el recurso con id placementID y el tipo OfferPlacement <br/>
No se encontró el recurso con id activityID y el tipo OfferActivity<br/></td> 
   <td>Compruebe si ActivityID o PlacementID están disponibles</td> 
  </tr> 
   <tr> 
   <td>No se pudo validar el recurso.</td> 
   <td>El componentType de la ubicación debe coincidir con la oferta offerType</td> 
  </tr> 
   <tr> 
   <td>La dirección URL pública no está presente en offerId.</td> 
   <td>Las ofertas de imágenes (todas personalizadas y de reserva asociadas con el par de decisión y ubicación) deben tener la URL pública rellenada (deliveryURL no debe estar vacía).</td> 
  </tr> 
  <tr> 
   <td>La decisión contiene atributos que no son de perfil.</td> 
   <td>El uso del modelo de ofertas debe contener únicamente los atributos de perfil.</td> 
  </tr> 
  <tr> 
   <td>Error al recuperar el uso de la decisión.</td> 
   <td>Este error podría producirse cuando la API intenta recuperar el modelo de oferta.</td> 
  </tr>
  <tr> 
   <td>El atributo de oferta de atributo de oferta no es válido.</td> 
   <td>Compruebe si el atributo de oferta al que se hace referencia en la oferta es válido. A continuación se muestran los atributos válidos: <br/>
Imagen: deliveryURL, linkURL<br/>
Texto: contenido<br/>
HTML: contenido<br/></td> 
  </tr> 
 </tbody> 
</table>
