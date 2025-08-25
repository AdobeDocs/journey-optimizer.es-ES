---
solution: Journey Optimizer
product: journey optimizer
title: Uso de JavaScript personalizado en una página de aterrizaje
description: Aprenda a diseñar el contenido de una página de aterrizaje en Journey Optimizer
feature: Landing Pages
topic: Content Management
role: Developer
level: Experienced
keywords: landing, landing page, javascript, code
exl-id: 2a7ebead-5f09-4ea5-8f00-8b5625963290
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 2%

---

# Uso de JavaScript personalizado en una página de aterrizaje {#lp-custom-js}

Puede definir el contenido de la página de aterrizaje mediante JavaScript personalizado. Por ejemplo, si necesita aplicar estilos avanzados o si desea agregar comportamientos personalizados a las páginas de aterrizaje, puede crear sus propios controles y ejecutarlos en [!DNL Journey Optimizer].

## Inserción de código JavaScript en una página de aterrizaje

Para insertar JavaScript personalizado en el contenido de la página de aterrizaje, puede hacer lo siguiente:

* Importe el contenido existente de HTML al empezar a crear el contenido y seleccione el archivo que incluye el código personalizado de JavaScript. Obtenga información sobre cómo importar contenido [en esta sección](../email/existing-content.md).

* Diseñe la página de aterrizaje desde cero o desde una plantilla guardada. Arrastre y suelte el componente de contenido **[!UICONTROL HTML]** en el lienzo y muestre el código fuente para agregar su JavaScript al componente. Aprenda a utilizar el componente HTML en [esta sección](../email/content-components.md#HTML). <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

  ![](assets/lp_designer-html-component.png)

* Introduzca o pegue código JavaScript directamente en el diseñador de contenido. Aprenda a codificar su propio contenido [en esta sección](../email/code-content.md).

>[!NOTE]
>
>Actualmente no puedes mostrar JavaScript en acción al [obtener una vista previa de la página de aterrizaje](create-lp.md#test-landing-page).

Para que la página de aterrizaje se muestre correctamente, utilice la siguiente sintaxis, tal como se describe en las secciones siguientes.

## Inicialización de código

Para inicializar el código JavaScript, debe utilizar el evento `lpRuntimeReady`. Este evento se activará después de la inicialización correcta de la biblioteca. La llamada de retorno se ejecutará con el objeto `lpRuntime` para exponer el método de biblioteca y los vínculos.

`LpRuntime` significa &quot;Runtime de la página de aterrizaje&quot;. Este objeto es el identificador de biblioteca principal. Expondrá los vínculos, los métodos de envío de formularios y otros métodos de utilidad que se pueden utilizar en JavaScript personalizado.

**Ejemplo:**

```
if(window.lpRuntime){
    init(window.lpRuntime);
}else{
    window.addEventListener('lpRuntimeReady',function(e){
        init(e.detail);
    });
}
 
function init(lpRuntime){
    // Enter custom JavaScript here using methods from lpRuntime.
}
```

## Enlaces

Mediante los vínculos, puede adjuntar un método durante el ciclo de vida del envío del formulario. Por ejemplo, puede utilizar los enlaces para realizar alguna validación del formulario antes de enviarlo.

Aquí están los ganchos que puede utilizar:

| Nombre | Descripción |
|--- |--- |
| addBeforeSubmitHook | Se llamará al vínculo personalizado antes del envío del formulario. Devuelve verdadero para continuar el envío; de lo contrario, devuelve falso para bloquear el envío. |
| addOnFailureHook | Se llamará al vínculo personalizado en caso de error en el envío del formulario. |
| addOnSuccessHook | Se llamará al vínculo personalizado cuando el formulario se haya enviado correctamente. |

**Ejemplo:**

```
//LpRuntime hooks
lpRuntime.hooks.addBeforeSubmitHook(function(){
    // Add your validation logic here.
});
```

## Envío de formulario personalizado

Los métodos enumerados a continuación se utilizan para realizar envíos de formularios personalizados.

>[!NOTE]
>
>Dado que el envío del formulario lo administra JavaScript personalizado, el envío predeterminado debe deshabilitarse explícitamente estableciendo una variable global `disableDefaultFormSubmission` en `true`.

| Nombre | Descripción |
|--- |--- |
| submitForm | Este método envía el formulario y gestiona el flujo posterior al envío. |
| submitFormPartial | Este método también enviará el formulario, pero omitirá el flujo posterior al envío. Por ejemplo, si ha configurado la redirección a la página de éxito después del envío correcto, esa redirección no se producirá en caso de envío parcial del formulario. |

**Ejemplos:**

```
//LpRuntime methods
window.disableDefaultFormSubmission = true        // Flag to disable the default submission flow.
 
lpRuntime.submitForm(formSubmissionData);         // This will trigger the default form submission handling like redirecting to error or success page.
  
lpRuntime.submitFormPartial(formSubmissionData,{   // This will not trigger the default submission handling.
    beforeSubmit : callback,
    onFailure : failureCallback,                   // Custom onFailureCallback - will be used in partial submission of form.
    onSuccess : successCallback                    // Custom onSuccessCallback - will be used in partial submission of form.
})
```

## Función de utilidad

| Nombre | Descripción |
|--- |--- |
| getFormData | Este método se puede usar para obtener `formData` en forma de objeto JSON. Este objeto se puede pasar a `submitForm` para el envío del formulario. |

**Ejemplo:**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## Casos de uso

### Caso de uso 1: Agregar validación antes del envío del formulario

```
<html>
<body>
// Enter HTML body here.
  
<script>
        if(window.lpRuntime){
          console.log('got runtime',lpRuntime);
          init(window.lpRuntime);
        }else{
          window.addEventListener('lpRuntimeReady',function(e){
            init(window.lpRuntime);
          });
        }
        
  
      // Here validate the function is checking if the checkbox is selected. This method should return true if you want form submission.
      function validateForm(){
        return document.querySelector('.spectrum-Checkbox-input').checked;
      }    
  
      function init(lpRuntime){
          lpRuntime.hooks.addBeforeSubmitHook(function(){
              return validateForm(); // This method should return true if you want to proceed with submission.
          })
      }
  
</script>  
  
</body>
</html>
```

### Caso de uso 2: Envío parcial del formulario

Por ejemplo, tiene un formulario con varias casillas de verificación en la página. Al marcar cualquier casilla de verificación, desea que estos datos se guarden en el servidor sin esperar a que el usuario haga clic en el botón Enviar.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=true;
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            let formData = lpRuntime.getFormData();
            lpRuntime.submitFormPartial(formData);
        })
      }
    </script>
  
</body>
</html>
```

### Caso de uso 3: Etiquetas de análisis personalizadas

Con JavaScript puede añadir oyentes de campos de entrada y adjuntar un déclencheur de llamada de análisis personalizado.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;  
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
         window.getElementByTagName('input').addEventListener('change',function(e){
            //trigger analytics events
        })
      }
        
    </script>
  
</body>
</html>
```

### Caso de uso 4: Formulario dinámico

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <div class="hiddenInput hidden">
            <input type='text' name="name2"/>
        </div>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;     
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
      function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            document.querySelector('.hiddenInput').toggleClass('hidden');
        })
      }
        
    </script>
  
</body>
</html>
```
