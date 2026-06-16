# Klárka stránky - projektový kontext

Aktualizováno: 2026-06-16

## Projekt

- Název pracovního projektu: Klárka stránky
- Typ: statický microsite web
- Téma: BEMER terapie, osobní konzultace, mikrocirkulace
- Lokální složka: `C:\Users\malp\Documents\Klárka stránky`
- Základ projektu: čistý výběr z produkční verze webu Lucka
- Zdrojová produkční verze: commit `c486417` ze složky `C:\Users\malp\Documents\Lucka stránky`
- Ověření zdroje: commit `c486417` se shodoval s aktuálním živým webem `https://www.bemer-lucie.cz/`
- Plánované GitHub repo: `petmal10-droid/klarka-stranky-preview`
- Plánovaný preview hosting: Netlify
- Plánovaná preview URL: `https://klarka-stranky-preview.netlify.app/`
- Produkční doména Klárka webu: zatím nedoplněna
- Hlavní soubory: `index.html`, `styles.css`, `script.js`, `content/site.json`, `admin/config.yml`

## Co bylo přeneseno

Do nového projektu byly přeneseny jen soubory nutné pro aktuální produkční web:

- `index.html`
- `styles.css`
- `script.js`
- `admin/index.html`
- `admin/config.yml`
- `content/site.json`
- `uploads/.gitkeep`
- `logo.png`
- `01_zasobeni_bunek.png`
- `02_latkova_vymena.png`
- `03_regenerace_vykon.png`
- `PROJECT_CONTEXT.md`, přepsaný pro Klárku

Záměrně nebyly přeneseny staré varianty, porovnávací stránky, Pastel soubory, screenshoty, logy, testovací JSON výstupy, původní `.git`, původní `CNAME` ani nepoužívané assety.

## CMS

Administrace používá Sveltia CMS přes Netlify Identity + Git Gateway. Klientka se má přihlašovat e-mailem a heslem, bez GitHub účtu.

- CMS vstup: `admin/index.html`
- CMS konfigurace: `admin/config.yml`
- Obsah webu: `content/site.json`
- Upload složka: `uploads`
- Backend Git Gateway bude zapisovat do repo `petmal10-droid/klarka-stranky-preview`
- `site_url` a `display_url` směřují na Netlify preview Klárka projektu

Před ostrým použitím je potřeba:

- propojit GitHub repo `klarka-stranky-preview` s Netlify,
- zapnout Netlify Identity,
- zapnout Git Gateway,
- doplnit skutečný kontaktní e-mail, telefon, lokalitu a právní údaje provozovatele,
- pokud se použije vlastní doména, přidat nový `CNAME` s Klárka doménou a aktualizovat `site_url`, `display_url` a reCAPTCHA domény.

## Pravidla práce

- Zdrojový projekt Lucka je pouze referenční a nesmí se měnit.
- Tento projekt je samostatný lokální git repozitář.
- Při změnách obsahu držet pohromadě `content/site.json`, `admin/config.yml`, `index.html` a `script.js`.
- CSS používat jen pro prezentaci, ne jako náhradu CMS stavu.
- Nepřenášet zpět staré pracovní soubory z Lucka projektu, pokud nejsou nově vědomě potřeba.

## Poznámky k prvnímu stavu

Tento základ stále obsahuje velkou část textace a vizuální identity převzatou z Lucka webu jako výchozí šablonu pro Klárku. Viditelné osobní údaje jsou nastavené jako pracovní placeholdery a mají se před spuštěním nahradit finálními údaji klientky.
