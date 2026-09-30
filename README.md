# JihoČAS – web Jihočeské pobočky ČAS

Statický web postavený na [Jekyllu](https://jekyllrb.com/) s tématem
[Bulma Clean Theme](https://github.com/chrisrhymes/bulma-clean-theme).
Po pushi do větve `main` se automaticky sestaví a nasadí na GitHub Pages
(`.github/workflows/jekyll.yml`).

## Lokální spuštění

Potřebujete Ruby 3.2+ (CI používá Ruby 4.0).

```sh
bundle install
bundle exec jekyll serve --livereload
```

Web pak běží na <http://localhost:4000/JihoCAS-homepage/>.

## Kde co upravit

| Co | Kde |
|---|---|
| Hlavní menu | `_data/navigation.yml` |
| Menu v patičce | `_data/footer_menu.yml` |
| Tři dlaždice na úvodní stránce | `_data/home_callouts.yml` |
| Seznam hvězdáren | `_data/hvezdarny.yml` |
| Projekty (každý = jeden soubor) | `_projekty/*.md` |
| Aktuality / pozvánky | `_posts/RRRR-MM-DD-nazev.md` |
| Stránky | `o-nas.md`, `projekty.md`, `hvezdarny.md`, `clenstvi.md`, `casopis.md`, `kontakt.md` |
| Barvy a styly | `assets/css/app.scss` |

### Nový projekt

Vytvořte `_projekty/nazev.md`:

```yaml
---
title: Název projektu
subtitle: Krátký podtitulek
icon: fa-star        # ikona z https://fontawesome.com/icons (sada solid)
order: 5             # pořadí v rozcestníku
summary: Jedna až dvě věty na kartu v rozcestníku.
links:               # nepovinné
  - name: Web projektu
    url: https://...
---

Text stránky projektu v Markdownu.

{% include projekt-odkazy.html %}
```

a případně ho přidejte do rozbalovacího menu v `_data/navigation.yml`.

### Nová aktualita

Vytvořte `_posts/2026-10-15-nazev-akce.md` s hlavičkou `title:` (a volitelně `summary:`).

Místa, kde chybí údaje, jsou v souborech označená komentářem `TODO`.
