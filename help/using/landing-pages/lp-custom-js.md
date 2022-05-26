---
title: Uso de JavaScript personalizado en una página de aterrizaje
description: Aprenda a diseñar el contenido de una página de aterrizaje en Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
source-git-commit: f4b3a9de47e724f7b23df8a02b8106c131cf1b12
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 2%

---

# Uso de JavaScript personalizado en una página de aterrizaje {#lp-custom-js}

Puede definir el contenido de la página de aterrizaje mediante JavaScript personalizado. Por ejemplo, si necesita realizar estilos avanzados o si desea agregar comportamientos personalizados a las páginas de aterrizaje, puede crear sus propios controles y ejecutarlos en [!DNL Journey Optimizer].

## Inserción de código JavaScript en una página de aterrizaje

Para insertar JavaScript personalizado en el contenido de la página de aterrizaje, puede hacer lo siguiente:

* Importe contenido de HTML existente al empezar a crear su contenido y seleccione el archivo que incluye su código personalizado de JavaScript. Obtenga información sobre cómo importar contenido [en esta sección](../design/existing-content.md).

* Diseñe la página de aterrizaje desde cero o desde una plantilla guardada. Arrastre y suelte la **[!UICONTROL HTML]** componente de contenido en el lienzo y mostrar el código fuente para añadir el JavaSCript al componente. Aprenda a utilizar el componente HTML en [esta sección](../design/content-components.md#HTML). <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

   ![](assets/lp_designer-html-component.png)

* Introduzca o pegue código JavaScript directamente en el diseñador de contenido. Aprenda a codificar su propio contenido [en esta sección](../design/code-content.md).

>[!NOTE]
>
>Actualmente no puede mostrar JavaScript en acción cuando [vista previa de la página de aterrizaje](create-lp.md#test-landing-page).

Para que la página de aterrizaje se muestre correctamente, utilice la siguiente sintaxis, tal como se describe en las secciones siguientes.

## Inicialización del código

Para inicializar el código JavaScript, debe utilizar la variable `lpRuntimeReady` evento. Este evento se activará tras la inicialización correcta de la biblioteca. La llamada de retorno se ejecutará con la variable `lpRuntime` para exponer el método de biblioteca y los enlaces.

`LpRuntime` significa &quot;Landing page Runtime&quot;. Este objeto es el identificador de la biblioteca principal. Expondrá los enlaces, los métodos de envío de formularios y otros métodos de utilidad que se pueden usar en JavaScript personalizado.

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

Mediante los enlaces, puede adjuntar un método durante el ciclo de vida del envío del formulario. Por ejemplo, puede utilizar los enlaces para realizar alguna validación del formulario antes de enviarlo.

Estos son los vínculos que puede utilizar:

| Nombre | Descripción |
|--- |--- |
| addBeforeSubmitHook | Se llamará a un vínculo personalizado antes del envío del formulario. Devuelve true para continuar con el envío; en caso contrario, devuelve false para bloquear el envío. |
| addBeforeSubmitHook | Se llamará a un vínculo personalizado en el envío de formulario fallido. |
| addOnSuccessHook | Se llamará a un vínculo personalizado en el envío correcto del formulario. |

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
>Dado que el envío del formulario se administra mediante JavaScript personalizado, el envío predeterminado debe deshabilitarse explícitamente al configurar una variable global `disableDefaultFormSubmission` a `true`.

| Nombre | Descripción |
|--- |--- |
| submitForm | Este método envía el formulario y gestiona el flujo de envío posterior. |
| submitFormPartial | Este método también enviará el formulario, pero omitirá el flujo posterior al envío. Por ejemplo, si ha configurado la redirección a una página de éxito tras el envío correcto, esa redirección no se producirá en caso de envío parcial del formulario. |

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
| getFormData | Este método se puede usar para obtener la variable `formData` en forma de objeto JSON. Este objeto se puede pasar a `submitForm` para el envío del formulario. |

**Ejemplo:**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## Casos de uso

### Caso de uso 1: Adición de validación antes del envío del formulario

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

Por ejemplo, tiene un formulario con varias casillas de verificación en la página. Al marcar cualquier casilla de verificación, desea que estos datos se guarden en el servidor sin esperar a que el usuario haga clic en el botón de envío.

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

Con JavaScript, puede agregar oyentes de campos de entrada y adjuntar un déclencheur de llamada de análisis personalizado.

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
