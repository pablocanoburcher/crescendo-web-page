# Crescendo Labs — Operaciones sin fricción

Sitio estático rediseñado con navegación 3D por paneles deslizables (rueda, trackpad, swipe táctil o flechas del teclado). Mantiene los contenidos, paleta "Tierra Viva" y tipografías originales (Cormorant Garamond + Epilogue + DM Mono).

## Estructura

```
crescendo-redesign/
├── index.html      # sitio completo en un solo archivo
├── vercel.json     # configuración de despliegue
├── package.json    # scripts opcionales de dev local
├── .gitignore
└── README.md
```

## Probar localmente

```bash
# opción 1 — abrir directamente
open index.html

# opción 2 — servidor estático
npm run dev          # http://localhost:3000
# o
python3 -m http.server 3000
```

## Subir a GitHub

```bash
cd crescendo-redesign
git init
git add .
git commit -m "feat: rediseño 3D Crescendo Labs"
git branch -M main
git remote add origin https://github.com/<tu-usuario>/crescendo-labs.git
git push -u origin main
```

## Deploy en Vercel (1-click)

1. Entra a https://vercel.com/new
2. Importa tu repositorio `crescendo-labs`
3. Framework Preset: **Other** (Vercel detecta automáticamente que es un sitio estático)
4. Root Directory: `./`
5. Build Command: *vacío*
6. Output Directory: *vacío*
7. **Deploy**

El `vercel.json` ya incluye headers de seguridad y cache. Tras el primer despliegue tendrás una URL `*.vercel.app`. Para dominio propio: Settings → Domains.

## Controles del sitio

| Acción | Resultado |
|---|---|
| Rueda / trackpad | Desliza al siguiente panel |
| ← → ↑ ↓ | Navega entre paneles |
| Swipe (móvil) | Cambia de panel |
| Click en barra lateral | Salta a panel específico |
| Espacio | Avanza |
| Inicio / Fin | Primer / último panel |

## Stack

Solo HTML + CSS + JS vanilla. Sin build, sin frameworks, sin dependencias en runtime. Las fuentes se cargan desde Google Fonts.
