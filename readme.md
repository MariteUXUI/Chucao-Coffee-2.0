☕ Chucao Coffee 2.0 - Sitio Web de venta de café de grano.

¡Bienvenido al repositorio de Chucao Coffee 2.0! Este proyecto es un sitio web de comercio electrónico y presentación de productos de café. Fue desarrollado como parte de un [Indicar el propósito, curso o módulo, ej: Tarea de desarrollo web].

## 📋 Tabla de Contenidos

1.  Tecnologías Utilizadas
2.  Características Principales
3.  Estructura del Proyecto
4.  Instalación y Ejecución
5.  Autoría y Créditos

---

## 1. Tecnologías Utilizadas

Este proyecto fue construido con un enfoque en la modernización de estilos y la adaptabilidad.

* **HTML5:** Estructura semántica de la página.
* **SCSS (Sass):** Preprocesador CSS utilizado para una gestión de estilos modular y jerárquica.
* **Bootstrap 4.6:** Framework de CSS fundamental para la rejilla (grid), el carrusel y el diseño responsivo general.
* **jQuery 3.7.1:** Librería requerida por los componentes de Bootstrap (como el carrusel y el *toggler*).
* **Font Awesome:** Utilizado para la iconografía (redes sociales, contacto).

## 2. Características Principales

El sitio web incluye las siguientes funcionalidades y elementos de diseño:

* **Barra de Navegación Fija (*Fixed Navbar*):** El menú principal permanece visible en la parte superior de la ventana al hacer *scroll*.
* **Hero Slider:** Un carrusel de imágenes de alta resolución en la cabecera, con altura definida de 500px (`.hero-slider`).
* **Diseño Flexbox:** La navegación (`.flex-navbar`) utiliza `display: flex` para alinear el logo, los enlaces de menú (`.nav-links`) y el botón "Comprar" en línea.
* **Sección de Productos:** Display de tarjetas de productos (`.product-card`) organizado mediante la rejilla de Bootstrap.
* **Pie de Página (Footer):** Información de contacto, enlaces rápidos y redes sociales.

## 3. Estructura del Proyecto

La estructura de carpetas es la siguiente:

. ├── scss/ # Archivos fuente SCSS │ ├── css/ # Directorio para el CSS compilado (main.css) │ └── [Otros directorios SCSS, ej: abstracts/, components/] ├── css/ │ └── img/ # Imágenes de producto, slider y logo ├── index.html # Archivo principal de la aplicación └── README.md # Este archivo


## 4. Instalación y Ejecución

Para ver y ejecutar este proyecto de forma local:

1.  **Clonar (o descargar) el repositorio:**
    ```bash
    git clone 

2.  **Abrir el archivo:** Simplemente haz doble clic en el archivo `index.html` para abrir la página en tu navegador web.

## 5. Autoría y Créditos

* **Autor:** María Esther González Zúñiga
* **Proyecto:** Chucao Coffee 2.0
* **Fecha de Creación:** Diciembre 2025

💻 Planificación y Diseño de la Página Web
1. Estructura de la Página Web (HTML/Archivos)
Definiré la estructura del proyecto de archivos y las secciones principales de la página web para garantizar una organización lógica y mantenible.

A. Estructura de Archivos (Directorios)
Organizaré el proyecto utilizando directorios específicos para cada tipo de recurso:
Directorio
Contenido
Propósito
root/index.html, 
README.md
Archivos base del proyecto.
css/Imágenes, iconos, fuentes.
Todos los recursos multimedia.
css/Archivos CSS finales (compilados).
Solo el CSS que se enlaza al HTML.
js/Archivos JavaScript (módulos, scripts).
Lógica interactiva de la web.
sass/Todos los archivos fuente 
.scss.Archivos fuente de estilos.

B. Estructura Lógica (HTML)
La página se estructurará semánticamente utilizando las etiquetas de HTML5.

<header>: Contiene el logo y la barra de navegación (<nav>).

<main>: El contenido principal y único de la página.

<section>: Bloques temáticos principales 

<article>: Contenido independiente que puede distribuirse por separado 

<footer>: Información de contacto, derechos de autor y enlaces secundarios.

📄 Chucao Coffee 2.0
1. Diseño y Estructura de la Página Web
El diseño de la página se basa en un esquema de una sola página principal (landing page) con enfoque en la venta de productos.
Estructura de Archivos: Se utiliza una organización modular de directorios para separar responsabilidades: scss/ para el código fuente de estilos, css/ para el resultado compilado, assets/ para imágenes y index.html como punto de entrada.
Estructura HTML (Semántica): El index.html utiliza etiquetas semánticas de HTML5 (<header>, <nav>, <main>, <footer>) para mejorar la legibilidad del código, el SEO y la accesibilidad.

Framework Base: Se integra Bootstrap 4.6 para el sistema de grid (columnas) y componentes de UI prediseñados (Carrusel, tarjetas), acelerando el desarrollo.

2. Metodología de Organización y Modularización de Estilos CSS

Para garantizar la escalabilidad y el mantenimiento del proyecto, se combinan dos metodologías líderes: BEM y la arquitectura Sass 7-en-1.

A. Metodología de Nomenclatura Elegida: BEM (Block, Element, Modifier)
Definición: BEM es una convención de nombres que clasifica las clases CSS en tres entidades: Bloque, Elemento y Modificador.
Razón de la Elección:
Aislamiento: Evita colisiones de nombres y problemas de cascada o especificidad al mantener las clases planas y únicas.
Reutilización: Permite mover y reutilizar componentes (.product-card) en cualquier parte del sitio sin temor a romper sus estilos.
Claridad: Permite a cualquier desarrollador entender inmediatamente la relación entre una clase CSS y el componente HTML al que pertenece.
B. Preprocesador Elegido: Dart Sass (v1.94.2)
Razón de la Elección: Sass es la opción más robusta y estándar de la industria, elegida por su capacidad de modularizar el código CSS, lo cual es fundamental para el patrón 7-en-1.
Variables: Centralizan el branding (colores y tipografía) en _variables.scss.
Mixins: Reutilizan bloques de código complejo (como los media queries para responsividad).
Partials: Permiten dividir el CSS en pequeños archivos (_nombre.scss) que luego son ensamblados por el archivo main.scss.

3. Estructura de Estilos: Arquitectura Sass 7-en-1
El código fuente en la carpeta scss/ se organiza en siete capas lógicas importadas secuencialmente, siguiendo el patrón 7-en-1 para una gestión precisa de la especificidad y la dependencia:
Capa (Directorio)
Propósito Ejemplo Orden de Importación abstracts/Herramientas, configuraciones, variables._variables.scss
1° (Lo más bajo)
vendors/Estilos de librerías de terceros._normalice.scss
2°base/Estilos para elementos HTML puros._typography.scss
3°layout/Estructura principal de la página (Header/Footer)._footer.scss
4°components/Estilos de módulos BEM reutilizables._cards.scss
5°pages/Estilos específicos para la vista._exercise.scss
6°themes/Temas alternativos o modos (Ej. Modo Oscuro)._dark-theme.scss
7° (Lo más alto)📝 README.md 
 ☕ Chucao Coffee 2.0 

Este proyecto implementa un diseño web basado en las mejores prácticas de modularización de estilos, utilizando la arquitectura **Sass 7-en-1** y la metodología **BEM** para garantizar la escalabilidad y la mantenibilidad del código CSS.

---

### 1.2. Estructura de la Carpeta SCSS (7-en-1)

El archivo `main.scss` ensambla todos los *partials* de la siguiente estructura en un orden estricto, asegurando la cascada correcta de estilos:

scss/├── abstracts/      # 1. Variables, Mixins, Functions (Herramientas de diseño).│   ├── _functions.scss│   ├── _mixins.scss│   └── _variables.scss├── vendors/        # 2. Estilos de librerías de terceros (ej. Normalize).│   └── _normalice.scss├── base/           # 3. Estilos de bajo nivel (etiquetas HTML).│   ├── _base.scss│   ├── _reset.scss│   └── _typography.scss├── layout/         # 4. Estructura principal del sitio (Header, Footer, Page).│   ├── _footer.scss│   └── _page.scss├── components/     # 5. Bloques BEM reutilizables (_cards.scss, _button.scss).│   ├── _button.scss│   └── _cards.scss├── pages/          # 6. Estilos específicos para la vista actual.│   └── _exercise.scss├── themes/         # 7. Modificadores de tema (ej. _dark-theme.scss).│   ├── _dark-theme.scss│   └── _default.scss└── main.scss       # Punto de entrada y compilación.

---

## 2. Dependencias y Compilación

### 2.1. Dependencias externas

El proyecto utiliza las siguientes librerías mediante CDN:
* **CSS:** Bootstrap 4.6 (para *grid* y componentes base).
* **Iconografía:** FontAwesome 5.
* **JavaScript:** jQuery 3.7.1.

### 2.2. Guía de Compilación

Para compilar la estructura modular de Sass en el archivo CSS final (`css/main.css`) que se enlaza al HTML, se debe ejecutar el siguiente comando en la terminal:

```bash
sass --watch scss/main.scss:css/main.css