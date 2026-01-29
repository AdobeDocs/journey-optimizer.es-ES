---
title: Prueba y envío de un mensaje de correo directo
description: Obtenga información sobre cómo comprobar y enviar un mensaje de correo postal en Journey Optimizer
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
source-git-commit: 916239c98c982acf9c6f999316e46036d36b2098
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 8%

---

# Prueba y envío de un mensaje de correo directo {#direct-mail-test-send}

## Previsualización del archivo de extracción {#preview-dm}

Una vez definido el contenido del archivo de extracción, puede utilizar perfiles de prueba para previsualizarlo. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este en el mensaje con los datos del perfil de prueba.

Para ello, haga clic en **[!UICONTROL Simular contenido]** y añada un perfil de prueba para comprobar cómo se representa el archivo de extracción con los datos del perfil de prueba.

![](assets/direct-mail-simulate.png){width="800" align="center"}

Encontrará información detallada sobre cómo seleccionar perfiles de prueba y obtener una vista previa del contenido en la sección [Administración de contenido](../content-management/preview-test.md).

Una vez que el contenido del archivo esté listo para enviarse, cierre la pantalla de simulación y haga clic en el botón **[!UICONTROL Revisar para activar]**.

## Validación y activación de la campaña de correo directo {#dm-validate}

>[!IMPORTANT]
>
> Si la campaña está sujeta a una directiva de aprobación, debe solicitar la aprobación para poder enviar la campaña de correo postal. [Más información](../test-approve/gs-approval.md)

Antes de activar la campaña de correo postal, asegúrese de que la campaña o el recorrido y el archivo de extracción estén correctamente configurados. Para ello, compruebe las alertas en la sección superior del editor. Algunas son simples advertencias, pero otras pueden impedir que envíe el mensaje. Pueden producirse dos tipos de alertas: advertencias y errores.

* **Advertencias** se refieren a recomendaciones y prácticas recomendadas. Por ejemplo, se muestra un mensaje de advertencia si el mensaje SMS está vacío.

* **Los errores** le impiden publicar la campaña, siempre y cuando no se resuelvan. Por ejemplo, un mensaje de error le advierte cuando falta la línea de asunto.

![](assets/direct-mail-review.png){width="800" align="center"}

Cuando tu campaña de correo postal esté lista, completa la configuración de tu [recorrido](../building-journeys/journey-gs.md) o [campaña](../campaigns/create-campaign.md) para enviarla.

>[!NOTE]
>
>El archivo exportado finaliza con una nueva línea de forma predeterminada. Esto garantiza la compatibilidad con las herramientas de procesamiento de datos estándar.

Una vez enviado, puede medir el impacto de su campaña de correo postal o su recorrido dentro de los informes. Para obtener más información sobre los informes de correo postal, consulte estas secciones:
* [Informe de campaña de correo directo](../reports/campaign-global-report-cja-direct.md)
* [Informe de recorrido de correo directo](../reports/journey-global-report-cja-direct.md)

## Administración del consentimiento para correo postal {#dm-consent-management}

En [!DNL Journey Optimizer], el consentimiento se gestiona mediante el [Esquema de consentimiento](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=es){target="_blank"} de Experience Platform. De forma predeterminada, el valor del campo de consentimiento está vacío y se trata como consentimiento para recibir sus comunicaciones.

Si un perfil se ha excluido de la recepción de correo postal, en los atributos de perfil de Experience Platform correspondientes, el valor de `consents.marketing.postalMail.val` será `n` y el perfil correspondiente se excluirá de las entregas posteriores.

Para volverlo a habilitar, el atributo de perfil debe cambiarse a `consents.marketing.postalMail.val` : `y`.

Para administrar los atributos de un perfil, vaya a Experience Platform y acceda al perfil seleccionando un área de nombres de identidad y un valor de identidad correspondiente. Obtenga más información en la [documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=es#getting-started){target="_blank"}.

Obtenga más información acerca de la administración de la exclusión en Journey Optimizer en [esta sección](../privacy/opt-out.md).
