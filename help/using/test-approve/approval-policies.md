---
title: Crear y administrar directivas de aprobación
description: Obtenga información sobre cómo crear y administrar directivas de aprobación.
role: User
level: Beginner
feature: Approval
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 94114fac56b68aa0940ae9843f672823d64c19df
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 5%

---


# Crear y administrar directivas de aprobación {#approval-policies}

>[!AVAILABILITY]
>
> Actualmente, las directivas de aprobación solo están disponibles para un conjunto de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

Las políticas de aprobación permiten a los administradores establecer un proceso de validación para recorridos y campañas. Este sistema describe condiciones específicas que determinan si un recorrido o una campaña requiere aprobación. Estas políticas pueden variar en complejidad, desde requerir que todas las campañas sean revisadas por un usuario o equipo en particular, hasta establecer criterios basados en quién creó la campaña.

## Crear directivas de aprobación {#create-policies}

1. Desde el menú **[!UICONTROL Administración]**, accede a **[!UICONTROL Permisos]** y luego a **[!UICONTROL Políticas]**.

   ![](assets/policy_create_1.png)

1. Haga clic en **[!UICONTROL Crear]** en la ficha **[!UICONTROL Directiva de aprobación]**, elija **[!UICONTROL Directiva de aprobación]** y haga clic en **[!UICONTROL Confirmar]**.

1. Escriba un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]** para la directiva.

1. Seleccione si la directiva se aplicará a **[!UICONTROL Recorridos]** o **[!UICONTROL Campañas]**.

   ![](assets/policy_create_2.png)

Ahora puede refinar las condiciones para especificar quién inicia la solicitud de aprobación y quién la valida.

## Establecer condiciones para directivas de aprobación {#conditions}

1. Acceda a su **[!UICONTROL directiva de aprobación]**.

1. En el menú **[!UICONTROL If]**, haga clic en **[!UICONTROL Agregar condición]** para definir qué objeto o usuario almacenará en déclencheur una solicitud de aprobación.

1. Elija la **[!UICONTROL categoría]**, **[!UICONTROL regla coincidente]** y **[!UICONTROL opciones]** adecuadas.

   Por ejemplo, &quot;si la acción coincide con cualquier correo postal&quot; o &quot;Si el nombre de usuario del solicitante coincide con John Doe&quot;.

   ![](assets/policy_condition_1.png)

+++ Más información sobre las categorías y opciones disponibles
   <table>
    <tr>
      <th>Categoría</th>
      <th>Opción</th>
    </tr>
    <tr>
      <td rowspan="3">Tipo de campaña</td>
      <td>Programado (Marketing)</td>
    </tr>
    <tr>
    <td>Activado por API (Marketing)</td>
    </tr>
    <tr>
    <td>Activado por API (transaccional)</td>
    </tr>
    <tr>
    <td rowspan="8">Acción</td>
    <td>En la aplicación</td>
    </tr>
    <tr>
    <td>Notificación push</td>
   </tr>
    <tr>
    <td>SMS</td>
    </tr>
    <tr>
    <td>Correo electrónico</td>
    </tr>
    <tr>
    <td>Correo directo</td>
    </tr>
    <tr>
    <td>Web</td>
    </tr>
    <tr>
    <td>Basado en código</td>
    </tr>
    <tr>
    <td>Tarjeta de contenido</td>
    </tr>
    <tr>
    <td>Nombre de usuario del solicitante</td>
    <td>Nombre y dirección de correo electrónico del solicitante diseñado</td>
    </tr>
    <tr>
    <td>Grupo de usuarios solicitante</td>
    <td>Nombre del grupo de usuarios de los solicitantes diseñados</td>
    </tr>
    </table>


1. Para agregar más criterios, haga clic en **[!UICONTROL Agregar condición]** para definir reglas adicionales y seleccione **[!UICONTROL And]** o **[!UICONTROL Or]** para especificar cómo se conectan las condiciones.

1. En el menú **[!UICONTROL Entonces, enviar solicitud de aprobación a]**, haga clic en **[!UICONTROL Agregar condición]** para definir qué usuario puede aceptar la solicitud de aprobación.

1. En la lista desplegable **[!UICONTROL Categoría]**, seleccione si desea elegir un grupo de usuarios o un usuario individual.

1. A continuación, en la lista desplegable **[!UICONTROL Opción]**, seleccione el grupo de usuarios o usuario específico.

   El usuario o grupo de usuarios seleccionado será responsable de validar la solicitud de aprobación.

   ![](assets/policy_condition_2.png)

1. Para agregar más criterios, haga clic en **[!UICONTROL Agregar condición]** para definir reglas adicionales y seleccione **[!UICONTROL And]** o **[!UICONTROL Or]** para especificar cómo se conectan las condiciones.

1. Una vez que la directiva esté completamente configurada, haga clic en **[!UICONTROL Guardar]**.

Ahora puede activar la directiva de aprobación para aplicarla.

## Activación y administración de directivas de aprobación {#activate-policies}

1. Acceda a su **[!UICONTROL directiva de aprobación]**.

1. A continuación, haga clic en **[!UICONTROL Activar]** para aplicar las condiciones configuradas a su entorno.

   >[!NOTE]
   >
   >Una vez activadas, las directivas no se pueden editar. Para modificar las condiciones, desactive primero la directiva.

   ![](assets/policy_activate_1.png)

1. En el menú **[!UICONTROL Directiva]**, abra las opciones avanzadas para **[!UICONTROL Editar]**, **[!UICONTROL Desactivar]** o **[!UICONTROL Duplicar]** la directiva según sea necesario.

   ![](assets/policy_activate_2.png)

