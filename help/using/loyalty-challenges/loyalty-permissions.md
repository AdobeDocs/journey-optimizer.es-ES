---
solution: Journey Optimizer
product: journey optimizer
title: Permisos de retos de fidelización
description: Descubra qué permisos son necesarios para acceder, configurar y utilizar los Retos de fidelización en Adobe Journey Optimizer.
feature: Journeys
topic: Administration
role: Admin
level: Intermediate
exl-id: 7d6d4f18-8c5d-4c9c-9f7d-2d6c5f9a8b31
feature_v2: []
subfeature_v2: []
source-git-commit: b08de542c4f952f82a503103c783e54196c6d5b6
workflow-type: tm+mt
source-wordcount: 967
ht-degree: 6%

---

# Permisos de retos de fidelización {#loyalty-permissions}

## Información general {#overview}

[!DNL Adobe Journey Optimizer] La lealtad utiliza el control de acceso basado en roles (RBAC) de Adobe Admin Console para administrar el acceso de los usuarios.

La asignación de funciones es necesaria para que los usuarios puedan realizar operaciones de fidelización. A los usuarios sin una función asignada se les deniega el acceso a los extremos del servicio de fidelidad. Antes de incorporar usuarios a Lealtad, asigne una función adecuada a cada usuario que utilizará el servicio.

Las funciones se pueden asignar directamente a usuarios individuales o a través de grupos de usuarios. [Aprenda a asignar funciones a los usuarios](#assign-roles).

## Funciones recomendadas {#recommended-roles}

La fidelidad proporciona tres funciones predeterminadas preconfiguradas para la zona protegida **Prod**. Los nuevos clientes pueden utilizar estas funciones tal cual.

### Administrador de fidelización {#loyalty-administrator}

La función **Administrador de fidelización** proporciona acceso administrativo completo a todas las funciones de fidelidad: desafíos, configuración, catálogo de productos y perspectivas.

| Permiso | Descripción |
| - | - |
| Administrar retos de fidelización | Crear, editar, eliminar, publicar, cancelar la publicación y archivar desafíos; generación de recorridos de déclencheur |
| Administrar configuración principal de fidelización | Crear, editar y eliminar la configuración de la organización principal |
| Administrar configuración avanzada de fidelización | Administrar los extremos de recompensa y la configuración de transformación de eventos, incluido el acceso de lectura y escritura a valores de credenciales confidenciales |
| Administrar catálogo de productos de fidelización | Ver, importar y editar entradas del catálogo de productos |
| Administrar perspectivas de fidelización | Ver perspectivas, actualizar la configuración de KPI y almacenar en déclencheur la canalización de perspectivas |

### Profesional fiel {#loyalty-practitioner}

La función **Profesional fiel** está diseñada para propietarios de empresas que administran el ciclo de vida completo del desafío y editan la configuración principal. La configuración de recompensas, la configuración de eventos y el acceso al catálogo de productos son de solo lectura. No se permiten las escrituras de eliminación y configuración avanzada.

| Permiso | Descripción |
| - | - |
| Administrar retos de fidelización | Crear, editar, eliminar, publicar, cancelar la publicación y archivar desafíos; generación de recorridos de déclencheur |
| Configurar la configuración principal de fidelización | Cree y edite la configuración de organización principal. No se permite la eliminación |
| Ver configuración de recompensa de fidelización | Vea la configuración de recompensas, incluidos proveedores, definiciones y proxies. Se excluyen los valores confidenciales |
| Ver configuración de evento de fidelización | Ver definiciones de eventos y asignaciones de transformación de eventos |
| Ver catálogo de productos de fidelización | Ver entradas del catálogo de productos e importar estado del trabajo |
| Desarrollar perspectivas de fidelización | Ver datos de perspectivas y actualizar tarjetas de insight |

### Analista de fidelización {#loyalty-analyst}

La función **Analista de fidelización** proporciona acceso de solo lectura a desafíos, catálogos de productos y perspectivas. Utilice esta función para fines de informes y auditoría.

| Permiso | Descripción |
| - | - |
| Ver retos de fidelización | Ver desafíos |
| Ver catálogo de productos de fidelización | Ver entradas del catálogo de productos e importar estado del trabajo |
| Ver perspectivas de fidelización | Vea tarjetas de insight generadas por IA, constantes vitales y datos de rendimiento de desafíos |

## Funcionalidades de rol {#role-capabilities}

| Operación | Administrador | Profesional | Analista |
| - | - | - | - |
| Desafíos: ver | Sí | Sí | Sí |
| Desafíos: crear o editar | Sí | Sí | No |
| Retos: eliminar | Sí | Sí | No |
| Retos: publicar, cancelar la publicación o archivar | Sí | Sí | No |
| Retos: generación de recorridos de déclencheur | Sí | Sí | No |
| Configuración de la organización principal: vista | Sí | Sí | No |
| Configuración de la organización principal: crear o editar | Sí | Sí | No |
| Configuración de la organización principal: eliminar | Sí | No | No |
| Configuración de recompensa: vista, valores confidenciales excluidos | Sí | Sí | No |
| Configuración de recompensa: escribir o acceder a valores confidenciales | Sí | No | No |
| Configuración de eventos: vista | Sí | Sí | No |
| Configuración de eventos - escritura | Sí | No | No |
| Catálogo de productos: ver | Sí | Sí | Sí |
| Catálogo de productos: importar o editar | Sí | No | No |
| Perspectivas: vista | Sí | Sí | Sí |
| Perspectivas: escribir o actualizar la configuración de KPI | Sí | No | No |

## Ámbito de función predeterminado {#default-role-scope}

>[!IMPORTANT]
>
>Los roles de fidelización predeterminados solo se asignan a la zona protegida **Prod**.

Para conceder a los usuarios acceso a una zona protegida que no sea de producción, como una zona protegida de ensayo o desarrollo, cree una función personalizada para esa zona protegida y asigne los mismos permisos que a la función predeterminada correspondiente.

## Permisos disponibles para funciones personalizadas {#custom-role-permissions}

Cuando cree una función personalizada para una zona protegida que no sea de producción, seleccione uno de los permisos siguientes. Para replicar una función predeterminada, consulte los permisos enumerados en la sección de la función correspondiente anterior.

| Permiso | Descripción |
| - | - |
| Administrar retos de fidelización | Operaciones de desafío completo: crear, editar, eliminar, publicar, cancelar la publicación, archivar y generar recorridos de déclencheur |
| Desarrollar retos de fidelización | Cree y edite desafíos mediante API. No se permiten las acciones de eliminación y ciclo vital |
| Ver retos de fidelización | Ver solo desafíos |
| Administrar configuración principal de fidelización | Crear, editar y eliminar la configuración de la organización principal |
| Configurar la configuración principal de fidelización | Cree y edite la configuración de organización principal. No se permite la eliminación |
| Administrar configuración avanzada de fidelización | Administrar los extremos de recompensa y la configuración de transformación de eventos, incluido el acceso de lectura y escritura a valores de credenciales confidenciales |
| Ver configuración de recompensa de fidelización | Ver proveedores de recompensas, definiciones de recompensas y proxies de recompensas. Se excluyen los valores confidenciales |
| Ver configuración de evento de fidelización | Ver definiciones de eventos y asignaciones de transformación de eventos |
| Administrar catálogo de productos de fidelización | Ver, importar desde CSV y editar entradas del catálogo de productos, incluidas inclusiones y exclusiones; supervisar el estado del trabajo de importación |
| Ver catálogo de productos de fidelización | Ver entradas del catálogo de productos e importar el estado del trabajo. No se permiten las acciones de carga y edición |
| Administrar perspectivas de fidelización | Ver perspectivas, actualizar la configuración de KPI y almacenar en déclencheur la canalización de perspectivas |
| Desarrollar perspectivas de fidelización | Ver datos de perspectivas y actualizar tarjetas de insight |
| Ver perspectivas de fidelización | Vea tarjetas de insight generadas por IA, constantes vitales y datos de rendimiento de desafíos únicamente |

## Asignar funciones a los usuarios {#assign-roles}

>[!IMPORTANT]
>
>Solamente los administradores de productos y de sistemas pueden administrar usuarios, grupos y roles.

Adobe Admin Console admite dos métodos para asociar funciones con usuarios.

### Asignar usuarios directamente a una función {#assign-users-directly}

Agregar usuarios individuales directamente a una función. Este método es más adecuado para equipos pequeños o asignaciones únicas.

### Uso de grupos de usuarios {#use-user-groups}

Cree un grupo de usuarios y luego asigne usuarios y una función al grupo. Este enfoque es el más adecuado para administrar el acceso por departamento o función a escala.

Para obtener instrucciones paso a paso sobre la administración de funciones, grupos y usuarios, consulte la documentación de control de acceso de Adobe Journey Optimizer:

* [Administración de usuarios y funciones](../administration/permissions.md)
* [Permisos integrados](../administration/ootb-permissions.md)

## Solución de problemas de acceso {#troubleshooting}

Si un usuario no puede acceder a Retos de fidelización o a una función relacionada, marque la siguiente opción:

* El usuario se asigna a un rol de Fidelidad.
* La función incluye la zona protegida donde Retos de fidelidad está habilitado.
* La función incluye el permiso necesario para la acción que el usuario intenta realizar.
* Para las zonas protegidas que no son de producción, se ha creado una función personalizada para esa zona protegida.
* La organización y la zona protegida están habilitadas para Retos de fidelidad.

Si los problemas de acceso persisten después de actualizar los permisos, póngase en contacto con su representante de Adobe.

