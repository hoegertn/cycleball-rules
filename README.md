# Radball-Reglement

Radball-Reglements als Markdown, mit Skripten zur PDF-Erzeugung.

## Inhalt

| Datei | Inhalt |
|---|---|
| [cycle-ball.md](cycle-ball.md) | Reglement Zweier-Radball, gültig ab 01.01.2027 |
| [cycle-ball-5er.md](cycle-ball-5er.md) | Reglement Fünfer-Radball |
| [CHANGELOG.md](CHANGELOG.md) | Änderungen am Reglement |
| [sources/](sources/) | Original-PDFs von UCI, BDR und Swiss Cycling |
| [scripts/](scripts/) | PDF-Erzeugung |

## PDF erzeugen

Voraussetzungen: `pandoc`, `weasyprint`, für Diffs zusätzlich Node.js (`npx pandiff`).

```bash
brew install pandoc
pip install weasyprint
```

Reglement als PDF (`cycle-ball.pdf`):

```bash
scripts/md2pdf
```

Änderungen gegenüber einem Commit als PDF (`cycle-ball-diff.pdf`):

```bash
scripts/md2diff <commit>
```

Beide Skripte verarbeiten nur `cycle-ball.md`.
