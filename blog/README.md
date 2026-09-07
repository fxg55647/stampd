# Blogi

Jekyll-pohjainen blogi, joka julkaistaan GitHub Pagesilla `.github/workflows/blog-pages.yml`-workflowlla.

## Uusi postaus

Lisää tiedosto `_posts/`-kansioon muodossa `VVVV-KK-PP-otsikko.md`:

```markdown
---
layout: post
title: "Otsikko"
date: 2026-01-01 12:00:00 +0300
categories: yleista
---

Postauksen sisältö tähän.
```

## Paikallinen kehitys

```bash
cd blog
bundle install
bundle exec jekyll serve
```

Sivusto aukeaa osoitteessa `http://localhost:4000/leima/`.

## Julkaisu

Workflow käynnistyy automaattisesti kun `blog/`-kansioon pushataan muutoksia `main`-haaraan.
Jotta julkaisu toimii, GitHub-repon asetuksista **Settings → Pages → Build and deployment →
Source** täytyy olla kertaluontoisesti asetettu arvoon **GitHub Actions**.
