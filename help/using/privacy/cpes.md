---
solution: Journey Optimizer
product: journey optimizer
title: Administración de la exclusión
description: Obtenga información sobre cómo administrar la exclusión y la privacidad
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 58223b4b6e6e2ef5b7fc23c5b475e74ad72d0d13
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 100%

---

# Implementación del consentimiento de exclusión para la personalización {#cpes-opt-out}


## Editor de expresiones

Editor de expresiones al personalizar imágenes, texto, línea de asunto ( Segmento en Campañas): IU y sin encabezado

El editor de personalización en sí no realiza comprobaciones de consentimiento ni aplicación, ya que no participa en el envío de acciones de mensajes. El editor de personalización cumple con las etiquetas de control de acceso basadas en derechos proporcionadas por el servicio de perfil unificado para permitir o no permitir que se utilicen diferentes campos para la personalización. La previsualización del mensaje y el servicio de procesamiento enmascararán los campos identificados con información confidencial.

En Campañas AJO, la aplicación de la política de consentimiento puede producirse en dos lugares. Los clientes pueden incluir definiciones de políticas de consentimiento como parte de la creación de audiencias o segmentos para asegurarse de que la audiencia seleccionada para la campaña ya haya filtrado perfiles que no coinciden con los criterios de consentimiento. En segundo lugar, el servicio de tiempo de ejecución de mensajes realizará una comprobación de consentimiento general a nivel de canal para garantizar que los perfiles hayan elegido recibir comunicaciones de marketing en el canal específico. El propio objeto de campaña AJO no realiza ninguna comprobación de aplicación de directivas de consentimiento adicional en este momento.

Pasos de la Campaña y Personalización de AJO para aplicar manualmente el consentimiento:

El estado de inclusión y las preferencias de personalización de un usuario deben formar parte de las reglas y definiciones de audiencia antes de la activación en una campaña de Journey Optimizer. Un usuario de marketing de Adobe Experience Platform puede añadir una comprobación de consentimiento a su audiencia creando una nueva composición de audiencia o definiendo un nuevo segmento con el generador de reglas.

Si usa el compositor de audiencias, puede dividir la audiencia mediante atributos de perfil. Una vez que haya realizado las selecciones en los atributos de consentimiento adecuados que desee comprobar, puede guardar las audiencias resultantes para activarlas en una campaña. Tenga en cuenta que si crea una audiencia que no ha dado su consentimiento para la personalización y luego selecciona esta audiencia para activarla en una campaña, las herramientas de personalización permanecerán disponibles. Depende del usuario de marketing comprender que, si trabaja con una audiencia que no debería recibir personalización, no debe utilizar herramientas de personalización.

Para crear una audiencia dividida en composición de audiencia, siga estos pasos:

1. Seleccione la audiencia de inicio.

1. Haga clic en el icono &quot;+&quot; para crear una audiencia dividida.

1. En las propiedades de División, elija &quot;división de atributos&quot; como tipo.

1. En el campo de atributo, haga clic en el icono de lápiz para que aparezca la ventana de selección de atributos.

1. Escriba el Valor de opción para buscar el atributo de consentimiento de personalización (tenga en cuenta que este será el atributo de ruta profile.consents.personalize.content.val

1. Seleccione este atributo.

1. En Ruta 1: elija una etiqueta para definir la audiencia no personalizada.

1. Elija el valor apropiado de esta lista: https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=es#choice-values

   En este caso, utilizaremos una &quot;n&quot; para indicar NO como opción de exclusión para la personalización

   Puede crear una ruta independiente para otros valores de opción o puede elegir eliminar las rutas restantes y activar &quot;otros perfiles&quot; que incluirían todos los demás perfiles que no tuvieran un valor de opción de &quot;n&quot;.

1. Una vez finalizado, haga clic en el cuadro que dice &quot;Guardar audiencia&quot;. Se abrirá una nueva ventana de propiedades que le permitirá elegir qué nombre desea utilizar para las audiencias derivadas.

1. Una vez finalizado, publique la composición de la audiencia.

Si utiliza el generador de reglas de segmentos para crear su audiencia, puede seleccionar opciones de valor de personalización y consentimiento como parámetros de exclusión en la definición de audiencia. Al agregar parámetros de exclusión, puede crear un único segmento de audiencia de perfiles en el que se filtran las personas que no han dado su consentimiento.
