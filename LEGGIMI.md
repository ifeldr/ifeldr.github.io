# Sito Stampa 3D con il tema Chirpy

Sito Jekyll con il tema [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) 7.6:
barra laterale con menu, ricerca, modalità chiara/scura, categorie, tag e archivio.

- **Home**: presentazione, invito al simulatore ed elenco degli articoli (il blog)
- **Simulatore 3D**: il calcolatore del prezzo da file STL
- **Categorie, Tag, Archivio**: gli articoli organizzati in automatico
- **Chi sono**: la tua presentazione

## Pubblicarlo su GitHub Pages

Chirpy non viene costruito direttamente da GitHub Pages ma da una GitHub Action, già inclusa.
Il modo più semplice per avere tutto a posto è partire dal modello ufficiale di Chirpy:

1. Apri https://github.com/cotes2020/chirpy-starter, clicca **Use this template** →
   **Create a new repository**. Come nome usa `tuonome.github.io` (con il tuo nome utente),
   lascia **Public** e crea il repository.
2. Nel nuovo repository vai in **Settings → Pages** e in **Source** scegli **GitHub Actions**.
3. Torna alla pagina principale del repository, **Add file → Upload files**, e trascina tutto il
   contenuto di questo zip estratto. I file con lo stesso nome vengono sostituiti.
   Clicca **Commit changes**.
4. Apri `_config.yml` con la matita e imposta almeno `url`, `title`, `social` (nome ed email).
   Salva con **Commit changes**.
5. Nella scheda **Actions** attendi la spunta verde di "Build and Deploy" (2–4 minuti).
   Il sito è online all'indirizzo `https://tuonome.github.io`.

Se il repository ha un altro nome (per esempio `stampa3d`), l'indirizzo sarà
`https://tuonome.github.io/stampa3d`: in `_config.yml` imposta `baseurl: "/stampa3d"`.

## Cosa personalizzare

| Cosa | Dove |
|---|---|
| Nome, sottotitolo, descrizione, indirizzo, email | `_config.yml` |
| Immagine rotonda della barra laterale | `avatar` in `_config.yml` (file in `assets/img/`) |
| Icone social nella barra laterale | `_data/contact.yml` |
| Prezzi, materiali, qualità, email dei preventivi | `_data/calcolatore_3d.yml` |
| Presentazione in cima alla home | `_includes/intro-home.html` |
| Pagina "Chi sono" | `_tabs/about.md` (i testi segnaposto sono da sostituire) |
| Domande frequenti del simulatore | `_tabs/simulatore-3d.md` |
| Nomi delle voci del menu | `_data/locales/it-IT.yml`, sezione `tabs` |
| Stili aggiuntivi | `assets/css/jekyll-theme-chirpy.scss`, dopo il commento "Stili aggiuntivi" |

## Scrivere un articolo

Crea in `_posts` un file chiamato `AAAA-MM-GG-titolo-breve.md`, per esempio
`2026-10-05-stampare-pezzi-per-esterni.md`:

```
---
title: "Titolo dell'articolo"
description: "Una o due frasi: compaiono nell'elenco degli articoli e su Google."
categories: [Guide]
tags: [asa, esterni]
image:
  path: /assets/img/copertina.jpg
  alt: Descrizione dell'immagine
---

Testo dell'articolo in Markdown.
```

`image` è facoltativa. Categorie e tag creano da soli le rispettive pagine.
Per mettere un articolo sempre in cima alla home aggiungi `pin: true`.
Altre possibilità (riquadri colorati, immagini, video) sono spiegate nella guida del tema:
https://chirpy.cotes.page/posts/write-a-new-post/

## Note

- La versione del tema è bloccata sulla 7.6 (nel `Gemfile`) perché `_layouts/home.html`
  è una copia del layout del tema con in più la presentazione. Per passare a una versione
  più recente, ricopia `home.html` dal tema e reinserisci le righe con `intro-home.html`.
- Il simulatore analizza i file STL nel browser del visitatore: nessun file viene caricato
  sul sito. L'anteprima 3D usa three.js da cdnjs.cloudflare.com.
