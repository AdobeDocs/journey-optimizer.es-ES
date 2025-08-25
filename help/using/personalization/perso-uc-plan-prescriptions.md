---
title: Ejemplos de Personalization de plantilla
description: Ejemplos de Journey Optimizer Personalization
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
source-git-commit: c7ecfdbc9c97c49c77f3c4fb8bcb1656e04819a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# Correo electrónico de prescripciones del plan de salud {#plan-prescription}

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
