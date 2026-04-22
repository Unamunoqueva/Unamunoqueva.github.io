# unamunoqueva.github.io

Portfolio personal de José Luis Lupiáñez Serrano (lupi).

> DevOps Engineer en Málaga. Infraestructura, CI/CD, automatización e IA
> aplicada al ciclo de vida operativo.

## Stack del sitio

- [Astro](https://astro.build) 5 (SSG, zero-JS por defecto)
- [Tailwind CSS](https://tailwindcss.com) 4 vía `@tailwindcss/vite`
- Desplegado con [GitHub Pages](https://pages.github.com/) + GitHub Actions

## Desarrollo local

```bash
npm install
npm run dev      # http://localhost:4321
npm run build    # genera ./dist
npm run preview  # sirve ./dist localmente
```

## Despliegue

Cada `git push` a `main` lanza el workflow de `.github/workflows/deploy.yml`:
build con Node 20 → artifact → Pages. La URL de producción es
<https://unamunoqueva.github.io>.

## Estructura

```
src/
├── layouts/Layout.astro     # <html>, fuentes, meta, IntersectionObserver de reveals
├── pages/index.astro        # single-page: hero + secciones
├── components/
│   ├── TerminalHero.astro   # fake terminal con typing animado
│   ├── NavBar.astro
│   ├── Section.astro        # wrapper con label tipo prompt + título
│   ├── Stack.astro          # grid de tecnologías por categoría
│   ├── Projects.astro       # cards de proyectos
│   ├── CV.astro             # timeline de experiencia + formación
│   ├── Contact.astro        # bloque tipo contact.sh
│   └── Footer.astro
└── styles/global.css        # tema en variables CSS (OKLCH) + utilidades
```

## Licencia

Código del sitio: MIT. Contenido (textos, proyectos): derechos reservados.
