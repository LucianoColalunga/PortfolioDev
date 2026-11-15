# Portfolio — Luciano Colalunga

Portfolio profesional de **Luciano Colalunga**, Desarrollador Full Stack, QA Manual & Automation y Arquitecto de Software.

🌐 **Sitio:** [lucianocolalungadev.com.ar](https://lucianocolalungadev.com.ar)

## Contenido

- **Sobre mí y competencias clave:** desarrollo Full Stack, arquitectura de software, QA, diseño UI/UX con Figma y ciberseguridad.
- **Tecnologías y herramientas:** Frontend, Backend, Bases de Datos, QA & Testing, Metodologías, Seguridad & IA.
- **Proyectos destacados:** AlkyWallet, Ecommerce Fullstack (Teclab) y premios en hackathons.
- **Certificaciones y formación.**
- **Contacto:** WhatsApp, LinkedIn, GitHub, correo y formulario de mensaje rápido.

## Tecnologías

Sitio estático hecho con **HTML, CSS y JavaScript** (módulos ES), sin frameworks ni proceso de build.

```
index.html
css/        estilos (variables, base, componentes)
js/
  app.js    punto de entrada
  data/     contenido: perfil, proyectos, stack, certificaciones
  modules/  navegación, formulario de contacto, portapapeles, seguridad
assets/     imágenes y CV
```

## Correr en local

Basta con servir la carpeta con cualquier servidor estático, por ejemplo:

```bash
npx serve .
```

## Deploy

Publicado gratis en **GitHub Pages**, directo desde la rama `main` (carpeta raíz): cada push a `main` actualiza el sitio solo.

- `CNAME` define el dominio propio `lucianocolalungadev.com.ar`.
- `.nojekyll` hace que GitHub publique los archivos tal cual, sin procesarlos con Jekyll.
- GitHub Pages no permite headers personalizados, así que la CSP y la Referrer-Policy van como `<meta>` en `index.html`. `vercel.json`, `netlify.toml` y `_headers` quedan por si algún día se vuelve a un host que los use.

---

© Luciano Colalunga
