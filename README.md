# Mi Tienda Online — Carga dinámica de productos con Fetch API

**Nombre:** [Joshua eduardo Garcia Reyes]
**Carné:** [1890-22-5831]

## Descripción del proyecto

Ampliación de la maquetación de la tienda online (Bootstrap 5.3): los
productos ya **no están escritos directamente en el HTML**, sino que se
obtienen desde un servicio web (API REST) y se renderizan dinámicamente
con JavaScript.

**API utilizada:**
`https://backservicetest-g8emcvdff0fqe2b8.canadacentral-01.azurewebsites.net/api/producto`

## Funcionalidad nueva (esta semana)

- **Conexión al backend** con `fetch()` usando `async/await` y manejo de
  errores con `try/catch` (si la API falla se muestra una alerta
  `alert-danger` en lugar de los productos).
- **Renderizado dinámico:** los productos se recorren con `.forEach()` y por
  cada uno se genera su card, insertándola con `appendChild()` dentro de
  `<div class="row" id="contenedor-productos">`, ubicado en la columna
  derecha del layout principal.
- Cada producto muestra: **imagen, nombre, descripción, precio** y el botón
  **"Agregar al carrito"**.
- Si el producto tiene `enOferta == true`, se muestra el `precioOferta` en
  rojo y el precio original tachado, ambos formateados con
  `parseFloat(...).toFixed(2)`.
- **Carrito funcional (contador):** el botón "Agregar al carrito" incrementa
  el badge del carrito en la navbar (`#contadorCarrito`).
- **Diseño responsivo:** cada producto va dentro de un
  `div.col-sm-12.col-md-4.mb-4` → 1 producto por fila en pantallas pequeñas
  y 3 por fila en medianas/grandes, usando Bootstrap Cards (`row`, `card`,
  `card-body`, `img-fluid`, `btn`).

## Componentes de Bootstrap utilizados

- **Navbar** (`navbar`, `navbar-expand-lg`, `navbar-dark`, `bg-dark`) con
  marca, menú de navegación e ícono de carrito de compras con contador
  (badge) posicionado (`position-absolute`, `translate-middle`).
- **Carousel** (`carousel`, `carousel-inner`, `carousel-indicators`,
  `carousel-caption`) como encabezado principal con 3 diapositivas.
- **Grid system** (`container`, `row`, `col-sm-3`, `col-sm-9`, `col-sm-12`,
  `col-md-4`) para la distribución general de la página y de los productos.
- **Cards** (`card`, `card-img-top`, `card-body`, `card-title`) para mostrar
  cada producto obtenido de la API.
- **List group** (`list-group`, `list-group-item`, `list-group-item-action`)
  para el menú lateral de categorías.
- **Buttons** (`btn btn-primary`, `btn-outline-light`) para el botón
  "Agregar al carrito" y el ícono del carrito.
- **Spinner** (`spinner-border`) como indicador de carga mientras se
  consulta la API.
- **Bootstrap Icons** para el ícono del carrito (`bi-cart3`).
- CSS propio muy sencillo (`styles.css`), solo con algunos ajustes de
  tamaño de imágenes.

## Estructura del repositorio

```
├── index.html          → Página principal (incluye el script de Fetch API)
├── styles.css          → Estilos adicionales sobre Bootstrap
├── *.jpg.png           → Imágenes del carousel
└── README.md           → Este archivo
```

## Tecnologías utilizadas

- HTML5
- JavaScript (Fetch API, async/await)
- Bootstrap 5.3 (CDN)
- Bootstrap Icons (CDN)
- CSS3 (estilos propios)

## Cómo verlo

1. Clonar o descargar este repositorio.
2. Abrir el archivo `index.html` directamente en un navegador moderno
   (requiere conexión a internet para consultar la API y los CDN).
3. Para probar el diseño responsivo, usar las herramientas de desarrollador
   del navegador (F12 → "Toggle device toolbar").

## Sitio publicado (GitHub Pages)

1. En el repositorio: **Settings → Pages**.
2. En *Source* elegir **Deploy from a branch** → rama `main` → `/ (root)` → **Save**.
3. La URL publicada queda en `https://<usuario>.github.io/<repositorio>/`.
