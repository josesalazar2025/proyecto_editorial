
## EDITOLINE

Proyecto web responsive desarrollado como ejercicio de maquetación avanzada utilizando HTML y CSS moderno.

---

## Descripción

EDITOLINE es una web responsive construida desde cero aplicando técnicas avanzadas de CSS como:

- Layout con Grid y Flexbox
- Tipografía fluida con clamp()
- Transiciones y transformaciones
- Scroll Snap
- Estados interactivos (hover, focus)
- Enfoque Mobile First

---

El objetivo del proyecto es consolidar la capacidad de maquetación profesional sin el uso de JavaScript.


Apostamos por una identidad de marca con corte alternativo que ofrece una plataforma de distribución de ilustraciones y narrativas gráficas para artistas independientes. 
El giro de negocio 
La estética del website se mantiene con fondos oscuros y minima intervención de elementos de diseño, centrando el protagonismo en las obras de los artistas. 
Para favorecer una experiencia de navegación fluida y predecible se mantiene un patrón de diseño  layout consistente en toda la página.

---

## Objetivos del proyecto

- Construir una web completamente responsive.
- Aplicar buenas prácticas de estructura HTML semántica.
- Utilizar CSS moderno para crear layouts complejos.
- Implementar microinteracciones visuales.
- Mantener un código limpio y organizado.

---

## Tecnologías utilizadas

- HTML5 (semántico)
- CSS3
  - Flexbox
  - CSS Grid
  - clamp()
  - Scroll Snap
  - Transiciones
  - Transformaciones
- Git y GitHub para control de versiones (en caso de haberlo usado)

---

## 📂 Estructura del proyecto

/editoline
│
├── index.html
├── css/
│ └── styles.css
├── assets/
│ ├── images/
│ └── fonts/
└── README.md

---

Breve explicación de la organización:

- `index.html`: estructura principal del documento.
- `css/`: hojas de estilo.
- `assets/`: recursos estáticos.

---

## Responsive Design

El proyecto está desarrollado con enfoque **Mobile First**.

Breakpoints utilizados:

- Mobile: diseño base.
- Tablet: ajustes de layout.
- Desktop: distribución avanzada con Grid.

Se han utilizado unidades relativas (`rem`, `%`, `vw`) y tipografía fluida mediante `clamp()` para garantizar escalabilidad.

---

## Decisiones técnicas relevantes

Aquí deben explicar cosas como:

- Por qué se eligió Grid para el layout principal.
- En qué partes se utilizó Flexbox y por qué.
- Cómo se resolvió el scroll horizontal con Scroll Snap.
- Cómo se gestionaron las transformaciones y transiciones.
- Cómo se abordó la accesibilidad básica (si lo han hecho).

Este apartado es clave para la defensa oral.

---

## Retos encontrados

Explicar brevemente:

- Qué problemas surgieron.
- Qué soluciones se aplicaron.
- Qué se aprendió técnicamente.

Este apartado demuestra pensamiento técnico.

---

## Mejoras futuras

Ejemplos:

- Añadir funcionalidad con JavaScript.
- Optimización de rendimiento.
- Mejora de accesibilidad.
- Añadir modo oscuro.

Este apartado demuestra mentalidad profesional.

---

## Demo

Enlace a GitHub Pages / Vercel / Netlify (si está desplegado).

---

## Autores

Nzinga Mbande y José Salazar
Curso de confección y publicación de páginas web CIFO-La Violeta
Barcelona, 2026

---






## USO RESPONSABLE DE IA:

**PROMPT-CHAT GPT:**

Una plataforma pensada en ofrecer espacios de visibilidad a artistas nuevos y emergentes en donde encontrarás un curaduría basada en originalidad e itención, además de impulsar géneros opacados por las tendencias convencionales. 

Corrige la redaccion y amplia las ideas. Se trata de una editorial de revistas ilustradas como comics, manga enfocada en talento under.

**RESPUESTA:**

Va, te dejo una introducción más amplia y cuidada, con un tono editorial y cultural, ideal para una editorial independiente:

> Somos una editorial de revistas ilustradas dedicada al impulso de talento under, nuevos y emergentes, con un enfoque especial en el cómic, el manga y las narrativas gráficas contemporáneas. Nacemos como una plataforma pensada para ofrecer espacios reales de visibilidad a artistas que crean desde los márgenes, apostando por propuestas auténticas y arriesgadas.
>
> Nuestra curaduría se basa en la originalidad, la intención y la fuerza del discurso visual, priorizando obras que se alejan de las fórmulas dominantes y de las tendencias convencionales. Buscamos amplificar géneros, estilos y voces que suelen quedar opacados, construyendo un catálogo diverso que dialogue con la ilustración, la narrativa gráfica y la experimentación artística.
>

**PRONT-CLAUDE SONNET 4.5**

Explain in detail how to apply CSS hamburguer button trick with pure CSS

RESPUESTA:

<nav class="navbar">
  <!-- Hidden checkbox that controls everything -->
  <input type="checkbox" id="menu-toggle" class="menu-toggle">
  
  <!-- The hamburger icon (label acts as the clickable button) -->
  <label for="menu-toggle" class="hamburger">
    <span class="bar"></span>
    <span class="bar"></span>
    <span class="bar"></span>
  </label>
  
  <!-- The navigation menu -->
  <ul class="menu">
    <li><a href="#home">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>
/* Hide the checkbox completely */
.menu-toggle {
  display: none;
}

/* Style the hamburger container */
.hamburger {
  display: none; /* Hidden on desktop */
  cursor: pointer;
  flex-direction: column;
  gap: 5px;
  padding: 10px;
  z-index: 1000;
}

/* The three bars of the hamburger */
.bar {
  width: 25px;
  height: 3px;
  background-color: #333;
  transition: all 0.3s ease;
  border-radius: 3px;
}

/* Desktop menu styling */
.menu {
  display: flex;
  gap: 20px;
  list-style: none;
  margin: 0;
  padding: 0;
}

/* Mobile styles */
@media (max-width: 768px) {
  .hamburger {
    display: flex; /* Show hamburger on mobile */
  }
  
  /* Hide menu by default on mobile */
  .menu {
    position: fixed;
    top: 0;
    right: -100%; /* Off-screen */
    height: 100vh;
    width: 250px;
    flex-direction: column;
    background-color: white;
    box-shadow: -2px 0 5px rgba(0,0,0,0.1);
    padding: 60px 20px 20px;
    transition: right 0.3s ease;
  }
  
  /* THE KEY TRICK: When checkbox is checked, slide menu in */
  .menu-toggle:checked ~ .menu {
    right: 0;
  }
  
  /* Transform hamburger into X when checked */
  .menu-toggle:checked ~ .hamburger .bar:nth-child(1) {
    transform: rotate(45deg) translate(7px, 7px);
  }
  
  .menu-toggle:checked ~ .hamburger .bar:nth-child(2) {
    opacity: 0; /* Hide middle bar */
  }
  
  .menu-toggle:checked ~ .hamburger .bar:nth-child(3) {
    transform: rotate(-45deg) translate(7px, -7px);
  }

}

How It Works

The Checkbox: A hidden <input type="checkbox"> serves as the state manager. When checked, it changes the state without JavaScript.
The Label: The <label for="menu-toggle"> is connected to the checkbox through the for attribute. Clicking the label toggles the checkbox.
The Sibling Selector: The ~ (general sibling combinator) allows you to target elements that come after the checkbox in the DOM when it's checked: .menu-toggle:checked ~ .menu
The Animation: CSS transitions smooth the transformation of both the menu position and the hamburger icon.

Key Advantages

No JavaScript required - purely declarative CSS
Accessible - uses native checkbox semantics
Performant - CSS transitions are hardware-accelerated
SEO-friendly - content is in the HTML, just hidden visually

Alternative Patterns
You can also create variations like:
Overlay background:

.menu-toggle:checked ~ .menu::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.5);
  z-index: -1;
}

Slide from left:
.menu {
  left: -100%; /* Instead of right */
}

.menu-toggle:checked ~ .menu {
  left: 0;
}
This technique is elegant because it leverages CSS's ability to respond to element states without requiring any scripting, making it lightweight and maintainable for simple navigation scenarios.