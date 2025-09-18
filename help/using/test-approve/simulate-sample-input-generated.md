---
solution: Journey Optimizer
product: journey optimizer
title: Generación automática de variantes de contenido (Beta)
description: Obtenga información sobre cómo generar automáticamente variantes de contenido mediante simulación basada en IA.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="Beta privada" type="Informative"
hidefromtoc: true
hide: true
source-git-commit: 53d8fbb28e8516e4ee79f556a335b2d084af42e7
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---


# Generación automática de variantes de contenido (Beta){#auto-generate-variants}

>[!AVAILABILITY]
>
>Esta característica está actualmente en **versión beta privada** y puede que no esté disponible en su entorno. Póngase en contacto con su representante de Adobe para obtener acceso.

[!DNL Journey Optimizer] presenta una simulación basada en IA que puede generar automáticamente varias variantes para probar el contenido. Esta función reduce la necesidad de crear variantes manualmente, lo que facilita la validación de la lógica de personalización en plantillas complejas.

Al procesar contenido para simulación o prueba, el sistema analiza el contenido e identifica todos los tokens de personalización y las reglas de ramificación. Sustituye los tokens de personalización por valores significativos que proporcionan una previsualización casi realista del contenido final.

Considere una plantilla de correo electrónico de servicios financieros con lógica de ramificación basada en **tipo de inversor**, **grupo de edad**, **estado civil**, **verificación de identificación fiscal** y **ubicación**. Sin la generación de variantes, tendría que crear manualmente decenas de variantes para validar todas las rutas. Con las variantes generadas automáticamente, el sistema produce variantes representativas que cubren automáticamente estas condiciones.  Cada variante generada se procesa en el panel de vista previa, que muestra exactamente qué bloques y condiciones se aplican.

## Generar variantes de contenido

Para generar variaciones para el contenido y previsualizarlas, siga estos pasos:

1. Abra el contenido y seleccione **[!UICONTROL Simular contenido]** / **[!UICONTROL Simular variaciones de contenido]**.

   ![](assets/simulate-sample.png)

2. Haga clic en el botón **[!UICONTROL Generar]**.

   ![](assets/simulate-generate-variant.png)

3. [!DNL Journey Optimizer] genera automáticamente variantes basadas en atributos detectados.

4. Revise la lista de variantes generadas en el panel izquierdo y seleccione una variante para ver su renderización personalizada en el panel de vista previa.

>[!NOTE]
>
>Esta capacidad funciona del mismo modo que la función estándar Simular variaciones de contenido. Para obtener más información sobre las simulaciones de variaciones de contenido y las limitaciones y protecciones asociadas, consulte esta sección: [Simular variaciones de contenido](../test-approve/simulate-sample-input.md)
