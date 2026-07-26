# Mi Tienda Online — Maquetación de Página Principal

**Nombre:** [Joshua eduardo Garcia Reyes]
**Carné:** [1890-22-5831]

## Descripción del proyecto

Maquetación visual (sin funcionalidad) de la página principal de una tienda
online, desarrollada con **Bootstrap 5.3** como parte de la tarea de diseño
de interfaces. El proyecto se centra únicamente en la estructura, el diseño
y la responsividad de la página; no incluye lógica de programación (el
carrito de compras y los botones son solo visuales, usando el atributo
`disabled`).

## Componentes de Bootstrap utilizados

- **Navbar** (`navbar`, `navbar-expand-lg`, `navbar-dark`, `bg-dark`) con
  marca, menú de navegación e ícono de carrito de compras con contador
  (badge) simulado, siguiendo el ejemplo oficial de Bootstrap para badges
  posicionados (`position-absolute`, `translate-middle`).
- **Carousel** (`carousel`, `carousel-inner`, `carousel-indicators`,
  `carousel-caption`) como encabezado principal con 3 diapositivas.
- **Grid system** (`container`, `row`, `col-sm-3`, `col-sm-9`, `col-12`,
  `col-md-4`) para la distribución general de la página y de los productos.
- **Cards** (`card`, `card-img-top`, `card-body`, `card-title`) para mostrar
  cada uno de los 6 productos.
- **List group** (`list-group`, `list-group-item`, `list-group-item-action`)
  para el menú lateral de categorías.
- **Buttons** (`btn btn-primary`, `btn-outline-light`) para el botón
  "Agregar al carrito" y el ícono del carrito.
- **Bootstrap Icons** para el ícono del carrito (`bi-cart3`).
- CSS propio muy sencillo (`css/styles.css`), solo con algunos ajustes de
  tamaño de imágenes; el resto del estilo usa las clases y colores por
  defecto de Bootstrap.

## Diseño responsivo

- **Pantallas pequeñas (celulares):** los productos se muestran uno por fila
  al 100% del ancho (`col-12`).
- **Pantallas medianas o grandes:** los productos se muestran tres por fila
  (`col-md-4`).
- El menú lateral de categorías usa `col-sm-3` y el área de productos usa
  `col-sm-9`, apilándose verticalmente en pantallas muy pequeñas y
  mostrándose en columnas horizontales a partir del breakpoint `sm`.

## Estructura del repositorio

```
├── index.html          → Página principal de la tienda
├── css/
│   └── styles.css      → Estilos adicionales sobre Bootstrap
└── README.md            → Este archivo
```

## Tecnologías utilizadas

- HTML5
- Bootstrap 5.3 (CDN)
- Bootstrap Icons (CDN)
- CSS3 (estilos propios)
- Imágenes de ejemplo generadas con [picsum.photos](https://picsum.photos/)

## Cómo verlo

1. Clonar o descargar este repositorio.
2. Abrir el archivo `index.html` directamente en el navegador (no requiere
   servidor ni instalación adicional, ya que Bootstrap se carga desde CDN).
3. Para probar el diseño responsivo, usar las herramientas de desarrollador
   del navegador (F12 → "Toggle device toolbar").
