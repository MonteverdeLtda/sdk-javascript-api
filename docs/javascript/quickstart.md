#Inicio rápido: SDK de Monteverde para JavaScript

El SDK de Monteverde para JavaScript proporciona un amplio conjunto de funciones del lado del cliente que:

- Te permiten usar el botón ecoPunto (Punto Ecologico/Ambiental) y otros plugins sociales en el sitio web.
- Te permiten usar el inicio de sesión con Monteverde para que las personas encuentren menos obstáculos al registrarse en tu sitio web.
- Facilitan las llamadas a la API de Monteverde.
- Inician cuadros de diálogo para que las personas realicen acciones, como compartir historias.
- Facilitan la comunicación cuando creas un juego o una pestaña de la aplicación en Monteverde.

En esta guía de inicio rápido se mostrará cómo configurar el SDK para realizar llamadas básicas a la API. Si todavía no quieres configurarlo, puedes usar nuestra consola de pruebas de JavaScript para utilizar todos los métodos del SDK y ver algunos ejemplos (puedes omitir los pasos de configuración, pero el resto del contenido de esta guía se puede probar en la consola).

#### Navegadores compatibles

El SDK de Monteverde para JavaScript admite las últimas dos versiones de los navegadores más populares: Chrome, Firefox, Edge, Safari (incluido iOS) e Internet Explorer (solo versión 11).

## Configuración básica

Para utilizar el SDK de Monteverde para JavaScript no es necesario descargar ni instalar ningún archivo independiente. Solo necesitas incluir un breve fragmento de código JavaScript en tu HTML que cargará asincrónicamente el SDK en tus páginas. La carga asincrónica del SDK no bloqueará la de otros elementos de la página.

El siguiente fragmento de código te mostrará la versión básica del SDK, con las opciones configuradas en sus valores predeterminados más comunes. Insértalo directamente después de la etiqueta `<body>` de apertura en cada página en la que desees cargarlo:

~~~ js
	window.MonteverdeAPIInit = function() {
		Mv.init({
			clientId   : 'your-app-id',
			version     : '2.0.0',
			domain: 'your-domain',
			baseURL: 'your-app-url-used',
			cookie: {
				cookieName: 'your-cookie-name',
				headerName: 'your-cookie-header-name'
			},
		});
	};
	(function () {
		var s = document.createElement('script');
		s.type = 'text/javascript';
		s.async = true;
		s.src = 'https://connect.monteverdeltda.com/';
		var x = document.getElementsByTagName('script')[0];
		x.parentNode.insertBefore(s, x);
	})();
~~~
    
Este código se cargará e inicializará el SDK. Debes reemplazar los valores `your-*` con el los datos de tu aplicación de Monteverde. Puedes buscar este identificador mediante el panel de aplicaciones.