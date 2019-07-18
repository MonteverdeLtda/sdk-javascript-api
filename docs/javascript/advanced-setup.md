# SDK para JavaScript: configuración avanzada

Consulta la guía de inicio rápido para obtener información sobre cómo cargar e inicializar el SDK de Monteverde para JavaScript. La guía de inicio rápido incluye las opciones predeterminadas comunes al inicializar el SDK, pero algunas de estas opciones se pueden personalizar.

### Navegadores compatibles

El SDK de Monteverde para JavaScript admite las últimas dos versiones de los navegadores más populares: Chrome, Firefox, Edge, Safari (incluido iOS) e Internet Explorer (solo versión 11).

## Comprobar el estado de inicio de sesión

Para obtener el estado de inicio de sesión de una persona, puedes usar Mv.getLoginStatus. Obtén más información sobre el uso del inicio de sesión con Monteverde con el SDK para JavaScript.

## Activar código tras la carga del SDK
La función asignada a window.fbAsyncInit se ejecuta cuando el SDK termina de cargarse. Todos los códigos que se quieran ejecutar una vez cargado el SDK deben insertarse en esta función y después de la llamada a FB.init. Se puede utilizar cualquier tipo de código de JavaScript, pero las funciones del SDK se deben llamar después de FB.init.

## Depurar
Para mejorar el rendimiento, el SDK para JavaScript se carga minimizado. También puedes cargar una versión depurada del SDK para JavaScript que incluya más registros y revisiones más estrictas de los argumentos, además de no estar minimizada. Para ello, cambia el valor de `js.src` en el código por este otro:

~~~ js
	s.src = 'https://connect.monteverdeltda.com/debug/';
~~~

La versión para depurar no debe usarse en tu entorno de producción, ya que su carga es más alta y peor para el rendimiento de tu página.