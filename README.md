# PersonalWebSite
# 🌐 Página Web Personal — Perfil Profesional

¡Bienvenido a mi repositorio! Este proyecto consiste en una página web personal estática diseñada desde cero, centrada en presentar mi perfil, datos de contacto, hobbies y redes sociales. El objetivo principal ha sido aplicar conceptos avanzados de **arquitectura de software, usabilidad y buenas prácticas de desarrollo** utilizando únicamente tecnologías web nativas.

---

## 🛠️ Tecnologías Utilizadas

* **HTML5:** Estructuración semántica y accesible del contenido.
* **CSS3 Moderno:** Flexbox, CSS Grid y Variables CSS (`:root`) para el diseño responsivo (Mobile-First) y estilos visuales sin depender de frameworks externos.

---

## 📐 Arquitectura de Software y Principios Aplicados

Aunque el proyecto se compone de archivos estáticos (HTML y CSS), el desarrollo se abordó desde una perspectiva de ingeniería de software, abstrayendo conceptos de **Clean Architecture / Onion Architecture** y principios de diseño:

### 1. Separación de Capas (Concepto Clean/Onion)
El código se ha dividido estrictamente respetando la separación de responsabilidades:
* **Capa de Dominio/Contenido (HTML Semántico):** Contiene la información pura del perfil (datos, texto, enlaces) aislada de cualquier regla de presentación.
* **Capa de Presentación (CSS UI):** Centraliza la lógica visual, tipografías y el comportamiento responsivo.
* **Capa de Infraestructura (Integración Externa):** El módulo del video de YouTube (`<iframe>`) se aisló en su propio contenedor responsivo para evitar que dependencias externas rompan la estabilidad visual de la UI.

### 2. Arquitectura CSS con Metodología BEM
Para garantizar un *Clean Code* mantenible y escalable, las clases de CSS siguen la convención **BEM (Block, Element, Modifier)**:
```css
/* Ejemplo del estándar utilizado */
.profile-card { }          /* Bloque (Componente principal) */
.profile-card__avatar { }  /* Elemento (Parte del componente) */
.profile-card--dark { }    /* Modificador (Variante de estilo) */
