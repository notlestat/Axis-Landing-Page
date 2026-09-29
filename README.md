# Axis landing page, historical project

A static landing-page design for the former Axis Studio business. It contains the earlier service packages and brand direction. Corey Kavanagh is the current practice; this repository preserves the older project.

## Preview locally

Requires Python 3. From the repository root:

```sh
git clone https://github.com/notlestat/Axis-Landing-Page.git
cd Axis-Landing-Page
python3 -m http.server 8000 --bind 127.0.0.1
```

Open [the main page](http://localhost:8000/index.html). Stop the server with Ctrl+C.

There is no package installation or build step. The pages load Tailwind CSS, Google Fonts and icon fonts from external services, so their intended styling needs an internet connection.

## Files

| File | Purpose |
|---|---|
| [index.html](index.html) | Main landing page |
| [code.html](code.html) | Earlier design variant |
| [DESIGN.md](DESIGN.md) | Design direction and visual rules |
| [AXIS_STUDIO.md](AXIS_STUDIO.md) | Historical business proposition and packages |
| `axis logo.png` | Local logo asset used by the main page |
| `screen.png` | Saved design image |

## Current state

The checked-in pages are static designs. They contain no lead-submission JavaScript, booking integration or backend connection. The service descriptions and prices are historical copy, not evidence that those workflows are running.

The separate [Axis-Studio repository](https://github.com/notlestat/Axis-Studio) contains the earlier backend implementation and requires access permission. This page is not automatically connected to it.

There is no automated test suite or deployment configuration in this repository. Preview the page and check its navigation, assets and responsive layout before using it elsewhere.
