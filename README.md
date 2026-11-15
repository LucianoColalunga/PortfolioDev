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

### Dominio y Cloudflare

El dominio está registrado en NIC Argentina y delegado a los nameservers de **Cloudflare** (plan gratis), que va adelante de GitHub Pages:

- Los registros `A` y `AAAA` del dominio apuntan a las IP de GitHub Pages, y `www` es un `CNAME` a `lucianocolalunga.github.io`. Todos tienen el **proxy activado** (nube naranja).
- El HTTPS lo da el certificado de Cloudflare, con el modo SSL/TLS en **Full** y **Always Use HTTPS** activado. Por eso, en GitHub Pages, *Enforce HTTPS* queda desactivado: con el proxy no está disponible y no hace falta.
- GitHub Pages no permite headers personalizados, así que los agrega Cloudflare. La regla **"Encabezados de seguridad"** (en Rules, del tipo *Response Header Transform Rule*) pone los mismos que tenía `vercel.json`:
  - Content-Security-Policy
  - X-Frame-Options
  - X-Content-Type-Options
  - Referrer-Policy
  - Permissions-Policy
  - Strict-Transport-Security (HSTS)
- Cloudflare guarda copias de los archivos, así que después de un push un cambio puede tardar unos minutos en verse.

> La CSP está en dos lugares: el `<meta>` de `index.html` y la regla de Cloudflare. El navegador aplica las dos, así que cualquier recurso externo nuevo hay que permitirlo en ambas.

`vercel.json`, `netlify.toml` y `_headers` quedan como referencia, por si algún día se vuelve a un host que los use.

---

© Luciano Colalunga
