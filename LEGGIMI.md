# Sito Stampa 3D (Jekyll per GitHub Pages)

Sito completo con quattro pagine: **Home**, **Chi sono**, **Blog** e **Simulatore 3D**.
Non usa temi esterni: tutto ciò che serve è in questa cartella.

## Pubblicarlo su GitHub Pages

1. Crea un repository su GitHub e carica tutto il contenuto di questa cartella
   (dal sito di GitHub: "Add file" → "Upload files", trascinando file e cartelle).
2. Apri `_config.yml` e imposta `url` e `baseurl`:
   - repository chiamato `tuonome.github.io` → `url: "https://tuonome.github.io"` e `baseurl: ""`
   - qualsiasi altro nome, per esempio `stampa3d` → `url: "https://tuonome.github.io"` e `baseurl: "/stampa3d"`
3. Nel repository vai in **Settings → Pages**, alla voce "Build and deployment" scegli
   **Deploy from a branch**, poi il branch `main` e la cartella `/ (root)`, e salva.
4. Dopo un paio di minuti il sito è online all'indirizzo indicato nella stessa pagina.

Ogni volta che modifichi un file e fai commit, GitHub ricostruisce il sito da solo.

## Cosa personalizzare

| Cosa | Dove |
|---|---|
| Nome, ruolo, foto, social, indirizzo del sito | `_config.yml` |
| Email di contatto, prezzi, materiali, qualità | `_data/calcolatore_3d.yml` |
| Voci del menu | `_data/navigazione.yml` |
| Testi della home | `index.html` |
| Pagina "Chi sono" | `chi-sono.md` (i testi segnaposto sono da sostituire) |
| Domande frequenti del simulatore | `simulatore-3d.html` |
| Colori e caratteri | `assets/css/stile.css`, in cima al file |

**Foto:** carica un'immagine quadrata in `assets/img/` (per esempio `foto.jpg`) e scrivi
`foto: "/assets/img/foto.jpg"` in `_config.yml`. Finché il campo è vuoto, al suo posto
compaiono le iniziali del nome.

**Materiali:** i materiali elencati nella home sono gli stessi del simulatore. Aggiungine o
modificane uno in `_data/calcolatore_3d.yml` e si aggiornano entrambi. Il campo
`descrizione` è il testo che compare nella home.

## Scrivere un articolo

Crea un file in `_posts` con il nome nel formato `AAAA-MM-GG-titolo-breve.md`, per esempio
`2026-10-05-stampare-pezzi-per-esterni.md`, con questa intestazione:

```
---
title: "Titolo dell'articolo"
description: "Una o due frasi: compaiono nell'elenco del blog e nei risultati di Google."
---

Testo dell'articolo in Markdown.
```

Gli articoli con una data futura non vengono pubblicati finché quella data non arriva.
Le immagini vanno in `assets/img/` e si inseriscono con
`![Descrizione]({{ '/assets/img/nome.jpg' | relative_url }})`.

## Provare il sito sul computer (facoltativo)

Serve Ruby. Nella cartella del sito:

```
bundle install
bundle exec jekyll serve
```

poi apri http://localhost:4000 (con il baseurl, http://localhost:4000/nome-repository/).

## Note

- Plugin usati, tutti supportati da GitHub Pages: jekyll-feed (feed RSS del blog),
  jekyll-seo-tag (anteprime per Google e social) e jekyll-sitemap.
- Il simulatore analizza i file STL nel browser del visitatore: nessun file viene caricato
  sul sito. L'anteprima 3D usa three.js da cdnjs.cloudflare.com, i caratteri arrivano da
  Google Fonts.
