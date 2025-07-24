# Shopify Theme - Prueba Técnica

Este repositorio contiene un tema de Shopify personalizado desarrollado como parte de una prueba técnica. El tema está basado en [Dawn](https://github.com/Shopify/dawn), el tema de referencia de Shopify, y ha sido extendido con varias secciones y funcionalidades personalizadas para mejorar la experiencia de compra y la gestión de contenido.

## Tecnologías Utilizadas

-  **Liquid:** El lenguaje de plantillas de Shopify, utilizado para cargar contenido dinámico en las páginas de la tienda.
-  **HTML5:** Para la estructura semántica de las páginas.
-  **CSS3:** Para los estilos y el diseño visual, siguiendo una arquitectura de componentes.
-  **JavaScript (ES6):** Para las funcionalidades interactivas del lado del cliente, como temporizadores y modales.
-  **JSON:** Utilizado para la configuración de la estructura de las plantillas y los ajustes del tema.

## Características Principales

### 1. Secciones Personalizadas

Se han desarrollado varias secciones personalizadas que se pueden gestionar fácilmente desde el editor de temas de Shopify:

-  **Collage de Descuentos (`discount-collage.liquid`):**

   -  Muestra una selección de productos en oferta de una colección específica.
   -  Permite elegir entre un diseño de 2 o 3 productos.
   -  Diseño de cuadrícula asimétrica y moderna.
   -  Totalmente responsivo.

-  **Banner con Cuenta Regresiva (`countdown-banner.liquid`):**

   -  Anuncia promociones por tiempo limitado con un temporizador de cuenta regresiva.
   -  Configurable para establecer una fecha y hora de finalización.
   -  Incluye opciones para un título, texto descriptivo y un botón de llamada a la acción.
   -  El script y los estilos están autocontenidos en el archivo de la sección para facilitar el mantenimiento.

-  **Productos Destacados (`custom-featured-products.liquid`):**

   -  Una sección para mostrar una colección de productos seleccionados.

-  **Productos Relacionados (`custom-related-products.liquid`):**
   -  Muestra productos relacionados en la página de detalles del producto.

### 2. Integración de Metacampos

El tema integra el uso de metacamos para añadir contenido personalizado a los productos de forma estructurada.

-  **Política de Devoluciones (`main-product.liquid`):**
   -  Se ha añadido un bloque específico en la página de producto para mostrar la política de devoluciones.
   -  Esta información se extrae de un metacampo del producto.
   -  **Para que funcione**, se debe crear un metacampo en los productos con las siguientes características:
      -  **Espacio de nombres:** `custom`
      -  **Clave:** `politica_de_devoluciones`
      -  **Tipo de contenido:** Texto de una sola línea o de varias líneas.

## Estructura del Proyecto

El tema sigue la estructura estándar de los temas de Shopify 2.0:

-  `assets/`: Contiene todos los archivos de recursos, como CSS, JavaScript e imágenes.
-  `config/`: Archivos de configuración del tema, como `settings_data.json` y `settings_schema.json`.
-  `layout/`: El diseño principal del tema, como `theme.liquid` y `password.liquid`.
-  `locales/`: Archivos de traducción para internacionalizar el tema.
-  `sections/`: Archivos de secciones individuales, que son los componentes modulares de las páginas.
-  `snippets/`: Pequeños fragmentos de código reutilizables.
-  `templates/`: Plantillas JSON que definen la estructura de las diferentes páginas (página de inicio, producto, colección, etc.).

## Cómo Empezar

Para utilizar este tema en una tienda Shopify, puedes seguir estos pasos:

1. **Clonar el repositorio:**

   ```bash
   git clone https://github.com/tu-usuario/shopify-prueba-tecnica.git
   ```

2. **Instalar Shopify CLI:**
   Si no lo tienes instalado, sigue las [instrucciones oficiales de Shopify](https://shopify.dev/docs/themes/tools/cli).

3. **Subir el tema a tu tienda:**
   Puedes subir el tema a tu tienda como un tema de desarrollo:
   ```bash
   shopify theme push --development
   ```
   O puedes previsualizar los cambios en tiempo real mientras desarrollas:
   ```bash
   shopify theme dev
   ```
