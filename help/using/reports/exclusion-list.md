---
solution: Journey Optimizer
product: journey optimizer
title: Lista de exclusiones
description: Obtenga más información sobre las exclusiones que se producen durante el envío
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a34ba1a8-87d5-4f9c-a181-2f49e74e8f09
source-git-commit: ca6f722c93fffe0cebcddb4f730f23d9a720ef9d
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 8%

---

# Motivos de exclusión {#exclusion-list}

## Cómo se cuentan las exclusiones en los informes de campaña

Cuando visualice informes de campaña, tenga en cuenta que la métrica *Exclusions* se calcula de la siguiente manera:

**Exclusiones = Exclusiones únicas + Eventos de exclusión duplicados**

Esto significa que si un perfil se excluye varias veces (por ejemplo, debido a varios eventos de exclusión para el mismo perfil), cada evento se cuenta en el total de Exclusiones. Como resultado, la suma de *Delivered* y *Exclusions* puede superar el tamaño de audiencia de destino original. Este comportamiento es predecible y refleja la forma en que se rastrean los eventos de exclusión en el sistema.

**Ejemplo:**

- Destinatarios objetivo: 94 000 perfiles
- Entregado: 69.000
- Exclusiones: 37 000 (incluye eventos de exclusión duplicados)
- Total (Entregados + Exclusiones): 106 000

El total supera la audiencia de destino porque en el recuento de exclusiones se incluyen eventos de exclusión duplicados.

Para obtener más información sobre los motivos de exclusión específicos, consulte la siguiente tabla.

## Lista de motivos de exclusión

| Razón de exclusión | Código de error | Canal | Explicación |
|-|-|-|-|
| RuntimeDispatchError | 050301 | Todos los canales | Evento de exclusión genérico para cualquier error de envío de tiempo de ejecución. |
| RuntimeRenderingError | 050302 | Todos los canales | Evento de exclusión genérico para cualquier error de procesamiento en tiempo de ejecución. |
| NamespaceErrorForExperimentation | 050017 | Todos los canales | Se genera un evento de exclusión cuando el área de nombres en el experimento es diferente del área de nombres del perfil. |
| ExperimentationHoldoutExclusion | 050018 | Todos los canales | Este evento de exclusión se genera cuando el tratamiento cualificado para un experimento es &quot;Holdout&quot;. |
| ExcludedForControlRules | 050002 | Todos los canales | Este evento de exclusión se genera cuando el envío del mensaje actual infringe las reglas de control, por ejemplo, el número de correos electrónicos permitidos en un mes. |
| DirectMailNoVariantDefined | 050062 | DirectMail | Se genera un evento de exclusión cuando no se define en la variante de correo postal. |
| DirectMailNoMessageFoundForTreatment | 050061 | DirectMail | Se genera un evento de exclusión cuando el experimento está habilitado para el mensaje y no se encuentra ningún mensaje para el tratamiento cualificado. |
| EmailNoConsent | 050101 | Correo electrónico | Se genera un evento de exclusión cuando el usuario ha optado por no recibir correos electrónicos de marketing. |
| Suprimido | 050107 | Correo electrónico | Exclusión debido a uno de los motivos de supresión. |
| EmailSuppression | 050102 | Correo electrónico | Se genera un evento de exclusión cuando se suprime el correo electrónico de destinatario. |
| DomainSuppression | 050105 | Correo electrónico | Se genera un evento de exclusión cuando se suprime el dominio del correo electrónico de destino. |
| No permitido | 050108 | Correo electrónico | Se genera un evento de exclusión cuando la lista de permitidos está habilitada y el correo electrónico de destino se excluye de la lista de permitidos. |
| Correo electrónico no permitido | 050103 | Correo electrónico | Se genera un evento de exclusión cuando la lista de permitidos está habilitada y el correo electrónico de destino se excluye de la lista de permitidos. |
| DomainNotAllowed | 050106 | Correo electrónico | Se genera un evento de exclusión cuando la lista de permitidos está habilitada y el dominio del correo electrónico de destino se excluye de la lista de permitidos. |
| EmailNoSubscriberIdFoundInProfile | 050025 | Correo electrónico | Se genera un evento de exclusión cuando subscriberId no se encuentra en el perfil de un correo electrónico de suscripción. |
| EmailNoAddressFoundInProfile | 050020 | Correo electrónico | Se genera un evento de exclusión cuando no se encuentra la dirección de correo electrónico en la dirección de ejecución. |
| EmailNoAddressDefinedInPreset | 050021 | Correo electrónico | Se genera un evento de exclusión cuando la dirección de ejecución no está definida en la configuración. |
| EmailNoVariantDefined | 050026 | Correo electrónico | Se genera un evento de exclusión cuando no se define ninguna variante en el mensaje de correo electrónico. |
| EmailNoMessageFoundForTreatment | 050027 | Correo electrónico | Se genera un evento de exclusión cuando el experimento está habilitado para el mensaje y no se encuentra ningún mensaje para el tratamiento cualificado. |
| EmailMalformattedAddress | 050024 | Correo electrónico | Se genera un evento de exclusión cuando el correo electrónico contiene una dirección mal formada. |
| InAppNoVariantDefined | 050041 | InApp | Se genera un evento de exclusión cuando no se define ninguna variante para el mensaje en la aplicación. |
| InAppNoMessageFoundForTreatment | 050042 | InApp | Se genera un evento de exclusión cuando el experimento está habilitado para el mensaje y no se encuentra ningún mensaje para el tratamiento cualificado. |
| PushNoTokenFoundInProfile | 050030 | Push | Se genera un evento de exclusión cuando el perfil no tiene tokens push. |
| PushNoValidTokenFoundForApps | 050031 | Push | Se genera un evento de exclusión cuando no se encuentra ningún token válido para las aplicaciones de destino en la configuración. **Importante:** Al usar un certificado de producción, el atributo `pushNotificationDetails.platform` del perfil de usuario debe establecerse en `apns`. Si usa un certificado de zona protegida, establézcalo en `apnsSandbox`. Una discrepancia entre el atributo platform y el tipo de certificado almacenará en déclencheur esta exclusión. |
| PushMalformattedProfile | 050034 | Push | Se genera un evento de exclusión cuando pushNotificationDetails tiene un formato incorrecto en el perfil. |
| PushNoConsent | 050111 | Push | Se genera un evento de exclusión cuando el usuario ha excluido las notificaciones push de marketing. |
| PushNoApplicationDefinedInPreset | 050033 | Push | Se genera un evento de exclusión cuando la configuración no contiene ninguna aplicación de destino. |
| PushNoVariantDefined | 050035 | Push | Se genera un evento de exclusión cuando no se define ninguna variante. |
| PushNoMessageFoundForTreatment | 050036 | Push | Se genera un evento de exclusión cuando el experimento está habilitado para el mensaje y no se encuentra ningún mensaje para el tratamiento cualificado. |
| SMSNoConsent | 050104 | SMS | Se genera un evento de exclusión cuando el usuario ha excluido los SMS de marketing. |
| SMSFromNumberNotDefinedInPreset | 050152 | SMS | Se genera un evento de exclusión cuando &quot;FromNumber&quot; no está definido en la configuración. |
| SMSNoToNumberDefinedInProfile | 050153 | SMS | Se genera un evento de exclusión cuando &quot;ToNumber&quot; no está definido en la configuración. |
| SMSNoVariantDefined | 050154 | SMS | Se genera un evento de exclusión cuando no se define ninguna variante. |
| SMSNoMessageFoundForTreatment | 050155 | SMS | Se genera un evento de exclusión cuando el experimento está habilitado para el mensaje y no se encuentra ningún mensaje para el tratamiento cualificado. |
| WebNoVariantDefined | 050041 | Web | Se genera un evento de exclusión cuando no se define ninguna variante para un mensaje web. |
| WebNoMessageFoundForTreatment | 050042 | Web | Se genera un evento de exclusión cuando el experimento está habilitado para el mensaje y no se encuentra ningún mensaje para el tratamiento cualificado. |
