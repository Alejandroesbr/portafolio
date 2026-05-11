# Presentación Personal – Alejandro Escobar

Página web estática de presentación personal desarrollada como parte de la **Actividad 2** del módulo de Diseño Web, con énfasis en semántica HTML5 y accesibilidad web.

---

## Cómo visualizar la página

1. Descarga o clona este repositorio:
   ```bash
   git clone https://github.com/Alejandroesbr/portafolio.git
   ```
2. Abre el archivo `index.html` directamente en tu navegador (doble clic o arrastrar al navegador).
3. No requiere servidor ni dependencias adicionales.

> **GitHub Pages:** También puedes ver la página en línea en:
> `https://github.com/Alejandroesbr/portafolio.git`

---

## Estructura de archivos

```
actividad2-html5/
├── index.html          # Página principal
├── assets/
│   └── foto-perfil.jpg # Foto de perfil
└── README.md           # Este documento
```

---

## Propósito de la página

La página presenta el perfil de **Alejandro Escobar**, estudiante de Ingeniería de Sistemas con énfasis en Desarrollo Web. Su objetivo es servir como carta de presentación digital para posibles colaboradores, docentes o empleadores. El público objetivo son personas del ámbito tecnológico y académico.

**Contenido incluido:**
- Sección "Sobre mí" con fotografía y descripción personal
- Lista de habilidades técnicas
- Tarjetas de proyectos destacados con enlaces a GitHub
- Formulario de contacto
- Encabezado con navegación y pie de página

---

## Buenas prácticas aplicadas

### Semántica HTML5

| Etiqueta | Uso en esta página |
|---|---|
| `<header>` | Encabezado con nombre y subtítulo del sitio |
| `<nav>` | Menú de navegación principal con enlaces de anclaje |
| `<main>` | Contenedor del contenido principal de la página |
| `<section>` | Secciones temáticas: "Sobre mí", "Habilidades", "Proyectos" |
| `<article>` | Cada tarjeta de proyecto individual (contenido autónomo) |
| `<aside>` | Formulario de contacto (contenido complementario) |
| `<footer>` | Pie de página con créditos y enlace al perfil GitHub |

La jerarquía de encabezados es correcta y no salta niveles: `h1` → `h2` → `h3`, lo que define un contorno (outline) lógico del documento para lectores de pantalla.

### Accesibilidad web (WCAG 2.1 AA)

1. **Skip link:** Enlace "Ir al contenido principal" visible al enfocar con teclado, que permite saltar la navegación repetitiva.

2. **Texto alternativo en imágenes:** El atributo `alt` de la fotografía describe el contexto visual de forma significativa (quién es, dónde está, qué hace), no solo el nombre.

3. **Formulario accesible:**
   - Cada `<input>` y `<textarea>` tiene su `<label>` asociado mediante `for`/`id` coincidentes.
   - `aria-required="true"` complementa el atributo `required` nativo.
   - `autocomplete` facilita el llenado a usuarios con dificultades motoras.

4. **Atributos ARIA:**
   - `aria-label` en `<nav>` para identificar la región de navegación.
   - `aria-labelledby` en cada `<section>` y `<aside>` apuntando a su encabezado.
   - `aria-label` descriptivo en enlaces con texto genérico ("Ver en GitHub") para que el lector de pantalla anuncie a qué proyecto corresponde.

5. **Contraste de colores:** El color de texto principal (`#1a1a2e`) sobre el fondo (`#f4f1eb`) supera la relación de contraste 7:1 exigida por WCAG AA. El texto blanco sobre el color primario (`#2c5f6e`) también supera 4.5:1.

6. **Navegación por teclado:** Todos los enlaces y controles del formulario son accesibles con `Tab`. Los estados `:focus` tienen estilos visibles (`outline`) que no se eliminan, solo se reemplazan por indicadores igualmente visibles.

7. **HTML semánticamente válido:** La página fue validada con el servicio **W3C Markup Validation Service** sin errores.

---

## Tecnologías utilizadas

- HTML5 (sin frameworks)
- CSS3 (variables, Flexbox, Grid, media queries — embebido en `<style>`)
- Fuentes web: [Alegreya](https://fonts.google.com/specimen/Alegreya) + [Source Sans 3](https://fonts.google.com/specimen/Source+Sans+3) vía Google Fonts

---

## Recursos de referencia

- [MDN Web Docs: HTML Semántico](https://developer.mozilla.org/es/docs/Glossary/Semantics#sem%C3%A1ntica_en_html)
- [MDN Web Docs: Accesibilidad web](https://developer.mozilla.org/es/docs/Web/Accessibility)
- [W3C: Introducción a la accesibilidad web](https://www.w3.org/WAI/fundamentals/accessibility-intro/es)
- [W3C Validator](https://validator.w3.org/)
