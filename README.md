# Klárka stránky

Čistý statický základ webu Klárka vytažený z aktuální produkční verze webu Lucka.

## Soubory

- `index.html` - hlavní stránka
- `styles.css` - styly
- `script.js` - chování webu a načítání CMS obsahu
- `content/site.json` - obsah spravovaný přes CMS
- `admin/` - Sveltia CMS administrace
- `uploads/` - média nahraná přes CMS

## CMS a hosting

Administrace používá Sveltia CMS přes Netlify Identity + Git Gateway. Klientka se přihlašuje e-mailem a heslem, bez GitHub účtu.

GitHub repo zůstává technické úložiště:

`petmal10-droid/klarka-stranky-preview`

Plánovaná Netlify preview URL:

`https://klarka-stranky-preview.netlify.app/`

Repo je propojené s Netlify a Identity je zapnuté v režimu pozvánek. Před klientským používáním CMS je potřeba v Netlify UI zapnout Git Gateway a doplnit skutečné kontaktní, právní a případné doménové údaje.
