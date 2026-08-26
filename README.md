# <img src="src/assets/images/kauai-logo.png" alt="Kaua'i" width="100"/> — Kaua'i: Where Jurassic Park Was Born

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![Sass](https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![npm](https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white)
![Parcel](https://img.shields.io/badge/Parcel-E7A93D?style=for-the-badge&logo=parcel&logoColor=white)
![Stylelint](https://img.shields.io/badge/Stylelint-263238?style=for-the-badge&logo=stylelint&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)

<sub>🗓️ Developed during the 2025-2026 academic year</sub>

This project is a **one-page website** dedicated to **Kaua'i**, the Hawaiian island that served as a filming location for *Jurassic Park*.

Developed using version 3.x of [UOC Boilerplate](https://github.com/uoc-advanced-html-css/uoc-boilerplate) as the starter template: a modern frontend development base that includes Parcel, a Sass compiler, an ES6 transpiler, minifiers, an image transformer, and development tools.

Created by Jordi Tarrida (jorditarrida@uoc.edu).

---

## ✅ Sections

- **Hero**: full-screen video with animated title.
- **The Garden Isle**: introduction to the island and its connection to *Jurassic Park*.
- **Filming Locations**: 4 real locations where JP was filmed, with links to Google Maps.
- **Interactive Map**: interactive map built with **Leaflet** and custom markers for each location.
- **Photo Gallery**: touch-enabled carousel built with **Swiper**, featuring photographs of Kaua'i.
- **Plan Your Trip**: practical travel information (how to get there, best time to visit, getting around).
- **Footer**: project credits.

---

## 🛠 Installation & Setup

### a0. Prerequisites
Make sure you have installed:
- **[Node.js](http://nodejs.org/) 20.x** or higher

Check the version:
```bash
node -v
```

### a1. Clone the repository
```bash
git clone https://github.com/marcturu/kauai-hawaii
cd https://github.com/marcturu/kauai-hawaii
```

### a2. Install dependencies
```bash
npm install
```

### a3. Run locally
```bash
npm run dev
```
The app will be available at **http://localhost:8123**, with live reload enabled.

### b1. Try the website
You can try the deployed version directly in the browser:

- **Netlify (browser testing):**
  WebApp: [https://kauai-hawaii.netlify.app/](https://kauai-hawaii.netlify.app/)

> ℹ️ **Deployment details:**
> The project is deployed on [Netlify](https://netlify.com) from the `main` branch.
> - **Build command:** `npm run build`
> - **Publish directory:** `dist`

---

## 🧩 Methodology

- **ITCSS**: style architecture (settings, tools, generic, elements, objects, components, utilities)
- **BEM**: CSS class naming convention
- **OOCSS**: reusable object classes (`o-container`, `o-section`)
- Responsive, *mobile-first* design

---

## 🧰 Built With

### Core

| Technology | Purpose |
| --- | --- |
| [Parcel v2](https://parceljs.org) | Bundler — development server, production build, asset pipeline |
| [Sass/SCSS](https://sass-lang.com) | CSS preprocessor — variables, nesting, functions, mixins, partials (`@parcel/transformer-sass`) |
| [PostCSS](https://postcss.org/) | CSS transpilation — vendor prefixes and compatibility with older browsers (`@parcel/transformer-postcss`, `postcss-preset-env`) |
| [PostHTML](https://github.com/posthtml/posthtml) | HTML partials via `posthtml-include` (`@parcel/transformer-posthtml`) |
| [Stylelint](https://stylelint.io/) | SCSS linting with custom BEM and SCSS rules (`stylelint-config-prettier-scss`, `stylelint-config-recommended-scss`, `stylelint-scss`), configured in `.stylelintrc` |

### Optimization (production build)

| Technology | Purpose |
| --- | --- |
| [`lightningcss`](https://github.com/parcel-bundler/lightningcss) | CSS minification and optimization (`@parcel/optimizer-css`) |
| [`htmlnano`](https://github.com/posthtml/htmlnano) | HTML minification (`@parcel/optimizer-htmlnano`) |
| [SWC](https://swc.rs/) | JavaScript minification (`@parcel/optimizer-swc`) |
| [Babel](https://babeljs.io/) | JavaScript transpilation for older browsers (`@parcel/transformer-babel`) |
| [`sharp`](https://sharp.pixelplumbing.com/) | Image transformation and WebP conversion (`@parcel/transformer-image`) |

### Dependencies

| Dependency | Purpose |
| --- | --- |
| [Lenis](https://lenis.studiofreight.com/) | Smooth scrolling `"lenis": "^1.3.21"` |
| [Leaflet](https://leafletjs.com/) | Interactive map `"leaflet": "^1.9.4"` |
| [Swiper](https://swiperjs.com/) | Touch carousel `"swiper": "^12.1.3"` |
| [AOS](https://michalsnik.github.io/aos/) | Scroll animations `"aos": "^2.3.4"` |
| [Font Awesome](https://fontawesome.com/) | Icons `"@fortawesome/fontawesome-free": "^7.2.0"` |

---

## 📜 Commands

| Command | Description |
| --- | --- |
| `npm run dev` | Starts the development server at http://localhost:8123 with live reload |
| `npm run build` | Compiles and optimizes the files for production into `dist/` |
| `npm run clean` | Removes the `dist/` folder and caches |
| `npm run stylelint` | Validates the SCSS files against the configured rules |

---

## 📂 Project Structure

```
src/
├── index.html
├── views/                  # PostHTML partials
│   ├── header.html
│   ├── hero.html
│   ├── about.html
│   ├── locations.html
│   ├── map.html
│   ├── gallery.html
│   ├── visit.html
│   └── footer.html
├── assets/
│   ├── fonts/              # Self-hosted fonts (Unbounded, DM Sans)
│   ├── images/             # Optimized images in WebP
│   ├── videos/             # Hero video (MP4)
│   ├── scripts/
│   │   ├── main.js
│   │   └── modules/        # JS modules (lenis, aos, swiper, leaflet, header)
│   └── styles/
│       ├── main.scss
│       ├── _dependencies.scss
│       ├── settings/       # Variables, fonts
│       ├── tools/          # Functions, mixins
│       ├── generic/        # Reset
│       ├── elements/       # Base styles
│       ├── objects/        # OOCSS objects
│       ├── components/     # BEM components
│       └── utilities/      # Utility classes
```

---

## 📷 Screenshots 

