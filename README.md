 Proyecto Web Gourmet - Pepe Vieira (La Última Cocina del Mundo)
¡Bienvenido al repositorio oficial del proyecto web para el restaurante Pepe Vieira! Este sitio web ha sido desarrollado como una plataforma interactiva, accesible y optimizada para la gestión de pedidos gourmet, consulta de información corporativa y análisis de afluencia.

Autor del Proyecto
Nombre del Alumno: Adam Barhoumi
Curso / Asignatura: Desarrollo Web / Diseño de Interfaces Web
Fecha: Mayo de 2026

Tecnologías y Características Técnicas
HTML5 Estricto y Semántico: Uso de etiquetas estructurales puras (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`) eliminando el "div-itis" para mejorar el SEO y el indexado de buscadores.
CSS3 Avanzado: Diseño responsivo basado en variables nativas (`:root`), Flexbox, transiciones fluidas y animaciones interactivas como el efecto pulso en el botón CTA.
Bootstrap 5.3.x: Integración limpia de componentes dinámicos de interfaz (Carrusel animado de imágenes, menús laterales Offcanvas para el carrito de compras, Ventanas modales de confirmación para borrado de ítems y menús colapsables estilo Accordion para las FAQs).
JavaScript Moderno (ES6+): Implementación avanzada de Programación Orientada a Objetos (POO) utilizando como apoyo la clase interactiva `ShoppingCart` basada en estructuras de datos de tipo `Map`.
Chart.js: Gráficas interactivas renderizadas dinámicamente según el selector de días de la semana para comprobar el nivel de ocupación del restaurante.

Funcionalidades Dinámicas e Interacciones Libres (Actividad 4)
El sitio web cuenta con un sistema de persistencia y renderizado dinámico global enlazado a través de todas sus pestañas mediante `localStorage`:
Carrito Persistente Multi-página: Permite añadir productos en la tienda, actualizar las burbujas (badges) notificadoras al instante y consultar el desglose total del dinero (con cálculos dinámicos de IVA del 10% en la ficha de compra) desde cualquier sección de la web.
Sistema de Confirmación de Borrado: El botón de eliminación del carrito intercepta la acción del usuario abriendo un modal nativo de Bootstrap para confirmar la remoción del elemento de forma segura mediante métodos de la clase `ShoppingCart`.
Interacción Libre - Reseñas Expandibles ("Leer más / Leer menos"): Integrado en la sección de opiniones de la Landing Page. Los comentarios extensos de los críticos gastronómicos aparecen inicialmente truncados con puntos suspensivos (`...`) para mantener la armonía de la altura visual. Al pulsar el enlace, la tarjeta se expande verticalmente mediante una animación suave de opacidad (fade-in) sin alterar el ancho responsivo del grid de diseño.

Auditoría de Accesibilidad y SEO (Actividad 5)
Se ha realizado una auditoría exhaustiva utilizando la herramienta automatizada Lighthouse de Google Chrome DevTools, obteniendo excelentes puntuaciones en todos los apartados:
Captura del Nivel de Accesibilidad (Lighthouse)
Inserta aquí tu captura de los resultados de Lighthouse en color verde.

Justificaciones Técnicas de Accesibilidad y SEO
Atributos ARIA: Los elementos interactivos críticos poseen descriptores semánticos para lectores de pantalla de personas con discapacidad visual, tales como `aria-label="Abrir menú"`, `aria-label="Ver carrito de compras"`, y configuraciones de anuncios asíncronos en Toasts informativos con `aria-live="assertive"` y `role="alert"`.
Accesibilidad del Teclado y Saltar Contenido: Se ha implementado un enlace de salto invisible `<a href="#cuerpo" class="skip-link">Saltar al contenido principal</a>` que se activa únicamente mediante navegación por tabulación (`Tab`), permitiendo a usuarios con discapacidades motrices saltarse la cabecera directamente al contenido.
SEO & Metadatos: Configuración estricta de meta-descripciones únicas por pestaña, etiquetas de idioma `<html lang="es">`, atajos de teclado rápidos (`Alt + T` para volver arriba con scroll smooth) y un contraste equilibrado contrastado por Lighthouse en paletas claras y oscuras automáticas (`@media (prefers-color-scheme: dark)`).
Métrica LCP (Largest Contentful Paint): Durante las auditorías locales fuera de servidor (`file:///`), el indicador registra un valor de 0 segundos debido a la nula latencia de red al servirse las imágenes directamente desde el disco de estado sólido (SSD), garantizando una renderización instantánea del elemento más grande del viewport (Hero banner).
