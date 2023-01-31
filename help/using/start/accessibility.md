---
solution: Journey Optimizer
product: journey optimizer
title: Funciones de accesibilidad en Journey Optimizer
description: Obtenga más información sobre la accesibilidad en la interfaz de usuario de Journey Optimizer
feature: Overview
role: User
level: Beginner
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 54%

---

# Accesibilidad en Journey Optimizer{#accessibility}

La accesibilidad se refiere a una serie de características que hacen utilizable un producto de software, con el menor esfuerzo posible, para usuarios con discapacidades visuales, auditivas, cognitivas, motoras u otros tipos de discapacidades. Adobe es un líder del sector en accesibilidad y apoya la creación de experiencias web destacadas al alentar a los desarrolladores a producir contenido rico y atractivo accesible a todos los usuarios. Obtenga más información sobre el compromiso del Adobe con la accesibilidad en la [Página de accesibilidad del Adobe](https://www.adobe.com/accessibility.html){target="_blank"}.

Para ayudar a alcanzar el objetivo de la conformidad de accesibilidad, [!DNL Journey Optimizer] sigue las prácticas recomendadas reconocidas internacionalmente en las Directrices de accesibilidad al contenido web (WCAG) 2.1 Nivel A y Nivel AA. Obtenga más información sobre las últimas [Informe de conformidad de accesibilidad de Adobe Journey Optimizer](https://www.adobe.com/accessibility/compliance/adobe-journey-optimizer-2022.html){target="_blank"}.


Las funciones de accesibilidad de [!DNL Adobe Journey Optimizer] se heredan de Adobe Experience Platform:

* Accesibilidad del teclado
* Contraste de color
* Validación de campos obligatorios

Las funciones de accesibilidad de Adobe Experience Platform se detallan [en esta documentación](https://experienceleague.adobe.com/docs/experience-platform/accessibility/features.html?lang=es){target="_blank"}.

Los siguientes métodos abreviados del teclado comunes están disponibles en [!DNL Journey Optimizer]:

| Acción | Acceso directo |
| --- | --- |
| Desplazamiento entre elementos, secciones y grupos de menús de la interfaz de usuario | Tabulación |
| Retroceder entre elementos, secciones y grupos de menús de la interfaz de usuario | Mayús + Tab |
| Desplazarse dentro de las secciones para definir el enfoque en elementos individuales | Flecha |
| Seleccionar o borrar un elemento que esté enfocado | Intro o barra espaciadora |
| Cancelar una selección, contraer un panel o cerrar un cuadro de diálogo | ESC |

Puede utilizar estos métodos abreviados en áreas específicas de [!DNL Journey Optimizer] interfaz de usuario:

<table>
  <thead>
    <tr>
      <th>Elemento de interfaz</th>
      <th>Acción</th>
      <th>Acceso directo</th>
    </tr>
  </thead>
  <tr>
    <td>Lista de recorridos, acciones, fuentes de datos o eventos</td>
    <td>Crear un recorrido, una acción, una fuente de datos o un evento</td>
    <td>C</td>
  </tr>
  <tr>
    <td rowspan="3">Lienzo de recorrido en estado de borrador</td>
    <td>Añadir una actividad de la paleta izquierda en la primera posición disponible, de arriba a abajo</td>
    <td>Doble clic en la actividad</td>
  </tr>
  <tr>
    <td>Seleccionar todas las actividades</td>
    <td>CTRL + A (Windows)<br/>CMD + A (Mac)</td>
  </tr>
  <tr>
    <td>Eliminación de las actividades seleccionadas</td>
    <td>Use la tecla Suprimir o Retroceso y a continuación Intro para confirmar la eliminación</td>
  </tr>
  <tr>
    <td>Acercar o alejar (enfoque en el lienzo o en cualquiera de sus elementos secundarios)</td>
    <td>CTRL +/- (Windows) o CMD +/- (Mac)</td>
  </tr>  
  <tr>
    <td>Desplazarse entre cada actividad y ruta (enfoque en el lienzo) o entre los botones de la barra de herramientas (enfoque en la barra de herramientas)</td>
    <td>Claves de FLECHA</td>
  </tr>   
  <tr>
    <td>Mover el foco al siguiente elemento procesable del lienzo; la barra de herramientas es la primera</td>
    <td>Tabulación</td>
  </tr>  
  <tr>
    <td>Abra el panel de configuración correcto (enfoque en una actividad)</td>
    <td>ENTER</td>
  </tr>   
  <tr>
    <td>Mover una actividad al lienzo (enfoque en una actividad)</td>
    <td>MAYÚS + teclas de flecha</td>
  </tr>  
  <tr>
  <td rowspan="3">

Panel de configuración de estos elementos:

<ul>
  <li>Actividad en un recorrido</li>
  <li>Evento</li>
  <li>Fuente de datos</li>
  <li>Acción</li>
</ul>

</td>
    <td>Mover al campo siguiente que se va a configurar</td>
    <td>Tabulación</td>
  </tr>
  <tr>
    <td>Guarde los cambios y cierre el panel de configuración</td>
    <td>Intro</td>
  </tr>
  <tr>
    <td>Descartar cambios y cerrar el panel de configuración</td>
    <td>ESC</td>
  </tr>
  <tr>
    <td rowspan="4">Recorrido en modo de prueba</td>
    <td>Habilitar o deshabilitar el modo de prueba</td>
    <td>T</td>
  </tr>
  <tr>
    <td>Activa un evento en un recorrido basado en eventos</td>
    <td>E</td>
  </tr>
  <tr>
    <td>

Activar un evento en un recorrido basado en segmentos para el cual la opción **[!UICONTROL Un solo perfil a la vez]** está activada

</td>
    <td>P</td>
  </tr>
  <tr>
    <td>Mostrar los registros de prueba</td>
    <td>L</td>
  </tr>
<!-- //Ajouter ce raccourci quand il marchera (actuellement, le raccourci Ctrl/Cmd+F du navigateur a priorité sur celui de AJO).//
  <tr>
    <td>Page with a search bar</td>
    <td>Select the search bar</td>
    <td>Ctrl/Command + F</td>
  </tr>
-->
  <tr>
    <td>Campo de texto</td>
    <td>Seleccionar todo el texto del campo seleccionado</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
  <tr>
    <td rowspan="2">Ventana emergente</td>
    <td>Guardar los cambios o confirmar la acción</td>
    <td>Intro</td>
  </tr>
  <tr>
    <td>Cerrar la ventana</td>
    <td>ESC</td>
  </tr>
  <tr>
    <td>Editor de expresiones simples</td>
    <td>Seleccionar y añadir un campo</td>
    <td>Doble clic en un campo</td>
  </tr>
  <tr>
    <td>Explorar los campos XDM</td>
    <td>Seleccionar todos los campos de un nodo</td>
    <td>Seleccionar el nodo principal</td>
  </tr>
  <tr>
    <td>Vista previa de carga útil</td>
    <td>Seleccionar la carga útil</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
</table>
