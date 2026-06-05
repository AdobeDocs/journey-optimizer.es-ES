---
title: Toma de decisiones por lotes en correo directo
description: Utilice Experience Decisioning para personalizar archivos de extracción de correo postal o exportar datos de toma de decisiones para utilizarlos en sistemas descendentes
feature: Decisioning, Direct Mail
topic: Integrations
role: User
level: Intermediate
keywords: toma de decisiones por lotes, correo directo, toma de decisiones
source-git-commit: 1b4e12b9433a819a3be34c4f01c489af1d6091ed
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---


# Toma de decisiones por lotes en correo directo {#batch-decisioning-direct-mail}

Con la toma de decisiones por lotes, la toma de decisiones selecciona el mejor elemento o elementos de decisión para cada perfil e incluye esos resultados en el archivo de extracción de correo postal. Puede devolver varios elementos por perfil estableciendo **[!UICONTROL Número de elementos]** al configurar la directiva de decisión. El archivo exportado se puede utilizar para la personalización del correo postal o para casos de uso por lotes en los que se exportan perfiles y atributos de decisión a otro sistema.

La toma de decisiones por lotes en el correo postal admite dos casos de uso principales:

* **Correo directo con toma de decisiones** - Personalizar correo físico por destinatario. Por ejemplo, seleccione la mejor imagen u oferta para cada perfil mediante reglas de idoneidad y clasificación (prioridad o fórmulas). El archivo de extracción incluye datos de perfil más atributos del elemento de decisión seleccionado o elementos (por ejemplo, la URL de la imagen de oferta) para su proveedor de correo postal.
* **Exportación por lotes para sistemas descendentes**: exporte perfiles y sus resultados de toma de decisiones (por ejemplo, ID de ofertas, atributos) para usarlos en otro sistema. Puede ejecutar la toma de decisiones por lotes y exportar el archivo a su servidor; las herramientas de flujo descendente (por ejemplo, un proveedor de servicios de correo electrónico de terceros) consumen esos datos para sus propias campañas o procesos.

>[!NOTE]
>
>Esta página se centra en los aspectos específicos de la toma de decisiones mediante el uso de la toma de decisiones por lotes con correo directo. Para obtener información detallada sobre la configuración y el uso del canal de correo postal, incluido el enrutamiento de archivos, la configuración del canal y la configuración del archivo de extracción, consulte [Introducción al correo postal](../direct-mail/get-started-direct-mail.md) y [Crear un mensaje de correo postal](../direct-mail/create-direct-mail.md).

## Resumen de flujo de trabajo {#workflow}

1. **Crear una campaña de correo directo o un recorrido**: cree un recorrido o una campaña, seleccione la acción **[!UICONTROL Correo directo]**, elija una configuración de correo directo y defina la audiencia.

   ➡️ [Aprenda a crear un mensaje de correo postal](../direct-mail/create-direct-mail.md)

1. **Agregar una directiva de decisión**:

   1. Haga clic en **[!UICONTROL Editar contenido]** para configurar el archivo de extracción.
   1. Agregue una columna al archivo de extracción y abra el editor de personalización utilizando el icono ![](assets/do-no-localize/editor-icon.svg).

      ![](assets/decision-policy-dm-add.png)

   1. Vaya al menú **[!UICONTROL Toma de decisiones]** para crear una directiva de decisión. En la configuración de directiva, establezca **[!UICONTROL Número de elementos]** si necesita más de un elemento de decisión por perfil y, a continuación, configure la estrategia de selección y la reserva opcional.

      ![](assets/decision-policy-dm-create.png)

   ➡️ [Aprenda a agregar y configurar una directiva de decisión en el correo postal](create-decision-policy.md#add)

1. **Personalice el archivo de correo postal con atributos de toma de decisiones**: Para las columnas que deben contener el resultado de la decisión, abra el Editor de Personalization, vaya a **[!UICONTROL Directivas de decisión]** y seleccione **[!UICONTROL Insertar directiva]** para agregar el código para la directiva de decisión.

   Utilice los atributos de elemento de decisión devueltos para que la información de oferta seleccionada se incluya en el archivo de extracción de cada perfil. Cuando se devuelven varios elementos, asigne los atributos de cada elemento de las columnas mediante la directiva `#each`.

   ➡️ [Aprenda a utilizar las directivas de decisión en los mensajes: ficha Correo directo](use-decision-policy.md)

1. Use **[!UICONTROL Simular contenido]** con un perfil de prueba para obtener una vista previa de la fila exportada (incluido el valor de toma de decisiones).

   ![](assets/batch-decisioning-simulate.png)

   ➡️ [Obtenga información sobre cómo obtener una vista previa y probar el contenido](../content-management/preview-test.md)

1. Active la campaña o publique el recorrido para generar y exportar el archivo (CSV o delimitado por texto) a su servidor de configurado.

   ➡️ [Obtenga información sobre cómo revisar y activar una campaña](../campaigns/review-activate-campaign.md) | [Más información sobre cómo publicar un recorrido](../building-journeys/publish-journey.md)

## Ejemplo de correo directo + toma de decisiones {#example-direct-mail}

Ejemplo: un retailer de fitness envía una postal personalizada a cada cliente con una de las diez imágenes posibles. Utilizan Decisioning para elegir la mejor imagen por perfil.

1. Cree 10 elementos de decisión (uno por imagen), cada uno con reglas de idoneidad (por ejemplo, edad, sexo).
2. Añádalos a una colección y cree una estrategia de selección con un método de clasificación (por ejemplo, una prioridad manual o una fórmula).
3. En una campaña de correo directo o un recorrido, habilite la toma de decisiones y agregue una directiva de decisión que utilice esta estrategia de selección.
4. En el archivo de extracción, añada una columna cuyos datos sean el atributo del elemento de decisión que contenga la imagen elegida (por ejemplo, la URL de la imagen de oferta). Otras columnas pueden ser nombre completo, dirección, estado, zip, etc.
5. Cuando se ejecuta la campaña, cada perfil obtiene una fila en la exportación con la imagen seleccionada para ese perfil. El proveedor de correo postal utiliza este archivo para generar el correo físico.

Puede usar **[!UICONTROL Simular contenido]** con un perfil de prueba para ver el resultado de la toma de decisiones (por ejemplo, la imagen) que se exportaría para ese perfil.

## Caso de uso de exportación por lotes (middleware) {#example-batch-export}

Algunos clientes utilizan la toma de decisiones por lotes para exportar perfiles y sus resultados de decisión para utilizarlos en otros sistemas (por ejemplo, un proveedor de servicios de correo electrónico o CRM). El flujo es:

1. Configure el correo postal (enrutamiento de archivos + configuración de canal) como se indica arriba.
2. Cree una campaña de correo postal o un recorrido y agregue una política de decisión.
3. Añada columnas para los campos de perfil y para los atributos del elemento de decisión que necesite en la exportación.
4. Active la campaña. El archivo se exporta al servidor (por ejemplo, Amazon S3 o SFTP).
5. El sistema descendente recupera el archivo y utiliza los datos de perfil y toma de decisiones para sus propias campañas o procesos.

Esto admite casos de uso de toma de decisiones por lotes a través del canal de correo postal con Experience Decisioning.

## Documentación relacionada {#related}

* [Crear un mensaje de correo postal](../direct-mail/create-direct-mail.md): configure el archivo de extracción y habilite la toma de decisiones
* [Crear directivas de decisión](create-decision-policy.md#add): agregue una directiva de decisión en la ficha Correo directo
* [Configuración de correo directo](../direct-mail/direct-mail-configuration.md): enrutamiento de archivos y configuración de canal
* [Introducción a la toma de decisiones](gs-experience-decisioning.md): conceptos y protecciones
