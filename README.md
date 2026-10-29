# Static landing-page prototype

A static HTML landing-page design with a second design variant. The checked-in copy includes proposed service packages and prices. Those figures do not establish current services or a working sales process.

## Preview locally

Download or clone this repository using GitHub's **Code** menu. With Python 3 installed, open a terminal in the checkout and run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open [the main page](http://localhost:8000/index.html) or [the design variant](http://localhost:8000/code.html). Stop the server with Ctrl+C.

There is no package installation or build step. The pages load Tailwind CSS, Google Fonts, and icon fonts from external services. Their intended styling requires an internet connection.

## Project files

| File | Purpose |
| --- | --- |
| [index.html](index.html) | Main page |
| [code.html](code.html) | Earlier design variant |
| [DESIGN.md](DESIGN.md) | Design direction and visual rules |
| [AXIS_STUDIO.md](AXIS_STUDIO.md) | Business proposition and service packages behind the page copy |
| `axis logo.png` | Logo image loaded by the main page |
| `screen.png` | Saved design image |

## Implementation limits

The pages contain no lead-submission JavaScript, booking integration, or backend connection. There is no automated test suite or deployment configuration.

Before reusing the design, review the copy and prices, then preview navigation, assets, and responsive layouts.
