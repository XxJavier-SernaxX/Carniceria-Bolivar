"# frontend-base" 
Documentación del Proyecto: Carnicería Bolívar
Portada

Título del proyecto: Página web "Carnicería Bolívar"

Integrantes: Santiago Forero - Nixon Vergel - Jhon Gomez - Javier Serna


________________________________________
Introducción
Esta documentación describe el desarrollo de una página web con diseño orientado a dispositivos móviles (mobile-first). Se detalla la arquitectura del proyecto, los eventos implementados en JavaScript, el diseño del menú interactivo, la distribución de roles y la lógica empleada para crear una experiencia de usuario óptima en diferentes dispositivos.
1. Diseño Mobile-First
El diseño "mobile-first" implica que primero se crea la interfaz para dispositivos móviles pequeños, y luego se adapta a pantallas más grandes mediante "breakpoints" en CSS.
Breakpoint principal:
Se ha definido un tamaño general para pantallas móviles: Samsung SE (ancho de 360px) y para computadoras de escritorio: 1280px.

Fragmento de código CSS:


 

Explicación:
●	Se oculta el botón del menú (menu-btn) en pantallas de tamaño mayor o igual a 768px.
●	El menú de navegación (nav-menu) cambia a una disposición horizontal utilizando display: flex.
________________________________________

2. Menú Interactivo con JavaScript
El menú de navegación se implementa con eventos para garantizar su funcionalidad en dispositivos móviles y escritorios.
Funciones principales:
1.	Apertura y cierre del menú móvil.
2.	Adaptación automática al tamaño de la ventana.
3.	Cierre del menú al hacer clic fuera de él.

Fragmento de código JavaScript:



 
Explicación:
●	menuToggle.addEventListener: Escucha los clics en el botón del menú y alterna la clase hidden en el menú.
●	window.addEventListener('resize'): Detecta cuando se cambia el tamaño de la ventana y adapta la visibilidad del menú.
●	document.addEventListener('click'): Cierra el menú si el usuario hace clic fuera de él.
________________________________________
3. Efectos Visuales con Eventos
Evento: Animación de fondo al mover el mouse
Se implementó un efecto visual en el fondo de la página, basado en la posición del cursor.


Fragmento de código JavaScript:


 
Explicación:
●	mousemove: Detecta el movimiento del mouse.
●	Calcula las posiciones relativas del cursor (x, y) en la ventana.
●	Cambia dinámicamente el color de fondo según la posición del cursor.
________________________________________
4. Arquitectura del Proyecto
El proyecto está organizado de la siguiente manera:
●	index.html: Página principal con la estructura HTML.
●	styles/style.css: Archivo CSS con los estilos de la página.
●	js/main.js: Archivo JavaScript con la lógica del menú y eventos.
●	pages: Subdirectorios para cada sección de la página (Productos, Contacto, etc.).
________________________________________
5. Distribución de Roles
●	Diseñador: Responsable de la estética (CSS, imágenes, colores).
●	Desarrollador Frontend: Implementa los eventos de JavaScript y asegura la funcionalidad del menú.
●	Documentador: Realiza esta documentación, explicando el proceso y el código.
________________________________________
Conclusión
Este proyecto demuestra el uso de un enfoque mobile-first, la implementación de eventos interactivos y una arquitectura clara para facilitar la navegación y el mantenimiento del sitio web. Cada miembro contribuyó según su rol para garantizar un resultado exitoso.

