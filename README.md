# 🎨 Landing Page con Tailwind CSS

[![Ver en vivo](https://img.shields.io/badge/Ver_en_vivo-GitHub_Pages-222?style=for-the-badge&logo=github)](https://robertbrito1.github.io/tailwind/)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS_v4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)

Landing page personal hecha con **Tailwind CSS v4** para aprender a maquetar con clases de utilidad y mantener un **HTML limpio y fácil de leer**.

## 💡 Objetivo

Quería aprender a "pintar" con Tailwind. El problema que me encontré enseguida es que, si pones todas las utilidades directamente en el HTML, las etiquetas se vuelven larguísimas y cuesta leerlas. Así que el reto fue **agrupar las clases que se repiten** en componentes propios con `@apply` y dejar el HTML lo más limpio posible.

## ✨ Qué incluye

- Diseño **responsive** con enfoque *mobile-first* (prefijos `sm:`).
- Tarjetas de tecnologías con efectos al pasar el ratón (`hover:scale`, `group-hover:rotate`, transiciones).
- Botones de redes sociales con degradados (`bg-linear-to-tr`).
- Iconos en un **sprite SVG** para no repetir el código de cada icono.

## 🧠 Conceptos técnicos

**1. Componentes con `@apply`.** En lugar de esto en cada botón:

```html
<a class="p-4 rounded-full shadow-lg bg-linear-to-tr from-pink-500 via-red-500 to-yellow-500 hover:scale-105 transition-transform size-12 sm:size-16 flex items-center justify-center">
```

Defino la clase una vez en `input.css`:

```css
.social-button {
  @apply p-4 rounded-full shadow-lg bg-linear-to-tr from-pink-500 via-red-500 to-yellow-500
         hover:scale-105 transition-transform size-12 sm:size-16 flex items-center justify-center;
}
```

Y en el HTML solo queda `<a class="social-button">`.

**2. Tema propio con `@theme` (Tailwind v4).** Defino colores y breakpoints propios como variables CSS, dentro del propio CSS y sin `tailwind.config.js`:

```css
@theme {
  --color-variable: #1e2e30;
  --color-secondary: #ff6f91;
  --breakpoint-xs: 350px;
}
```

**3. Compilación con la CLI de Tailwind.** El archivo `input.css` se compila a `assets/output.css`, que solo incluye las clases que realmente se usan.

## 🚀 Ejecutarlo en local

```bash
git clone https://github.com/robertbrito1/tailwind.git
cd tailwind
pnpm install
pnpm run build:styles   # compila y vigila los cambios de input.css
```

Abre `index.html` en el navegador.

## 👤 Autor

**Robert Brito** · [GitHub](https://github.com/robertbrito1) · [LinkedIn](https://www.linkedin.com/in/robertbrito/)
