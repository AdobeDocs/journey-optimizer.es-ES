---
title: Ejemplos de Personalization de plantilla
description: Ejemplos de Journey Optimizer Personalization
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
TQID: https://experienceleague.adobe.com/fZtkkz9pvdZ3G7ojmHlNhasxawVbXmBHX-uznq6hseY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: 378c98d4dc9552de3eed68eda59d9917c2b56347
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 2%

---

# Correo electrónico de prescripciones del plan de salud {#plan-prescription}

>[!BEGINSHADEBOX]

**En esta página:** Siga un caso de uso de personalización que se repite en matrices de perfiles anidadas con reglas condicionales para crear una lista de correo electrónico de plan de mantenimiento con recetas listas para ser recogidas o recuperadas.

>[!ENDSHADEBOX]

Un perfil contiene planes de salud y cada plan incluye recetas. Las recetas tienen varios estados, como &quot;listo&quot;, &quot;recordado&quot; o &quot;recogido&quot;.

En este caso de uso, queremos enviar un solo correo electrónico a cada perfil, incluidas todas las prescripciones que estén listas para ser recogidas o retiradas. Haga clic en cada pestaña a continuación para obtener más información sobre la sintaxis que se debe utilizar para implementar este caso de uso.

>[!BEGINTABS]

>[!TAB Mensaje procesado]

<p>Hola John Doe,</p>
<p>Estas son las recetas que están listas para ser recogidas o que han sido retiradas:</p>

**Plan de salud A**

<ul>

<li>
      <strong>Id. de prescripción:</strong> pres1<br>
      <strong>Nombre:</strong> Medicamento A<br>
      <strong>Estado:</strong> listo
   </li>

<li>
      <strong>Id. de prescripción:</strong> pres2<br>
      <strong>Nombre:</strong> Medicamento B<br>
      Recuperación de <strong>estado: </strong>
   </li>

</ul>

**Plan de salud B**

<ul>

<li>
      <strong>Id. de prescripción:</strong> pres4<br>
      <strong>Nombre:</strong> Medicamento D<br>
      <strong>Estado:</strong> listo
   </li>

</ul>

>[!TAB Plantilla de HTML]

```html
<p>Hi {{profile.person.firstName}} {{profile.person.lastName}},</p>
<p>Here are the prescriptions that are either ready for pick up or have been recalled:</p>
{{#each profile.plans as |plan|}}
<h3>{{plan.name}}</h3>
<ul>
   {{#each plan.prescriptions as |prescription|}}
   {%#if prescription.state = "ready" or prescription.state = "recall"%}
   <li>
      <strong>Prescription ID:</strong> {{prescription.prescription_id}}<br>
      <strong>Name:</strong> {{prescription.name}}<br>
      <strong>State:</strong> {{prescription.state}}
   </li>
   {%/if%}
   {{/each}}
</ul>
{{/each}}
```

>[!TAB Datos de perfil]

```javascript
{
  "profile": {
    "person": {
      "firstName": "John",
      "lastName": "Doe"
    },
    "plans": [
      {
        "planId": "plan1",
        "name": "Health Plan A",
        "prescriptions": [
          {
            "prescription_id": "pres1",
            "name": "Medication A",
            "state": "ready"
          },
          {
            "prescription_id": "pres2",
            "name": "Medication B",
            "state": "recall"
          }
        ]
      },
      {
        "planId": "plan2",
        "name": "Health Plan B",
        "prescriptions": [
          {
            "prescription_id": "pres3",
            "name": "Medication C",
            "state": "picked up"
          },
          {
            "prescription_id": "pres4",
            "name": "Medication D",
            "state": "ready"
          }
        ]
      }
    ]
  }
}
```

>[!ENDTABS]
