# omkarmusale0910.github.io

Personal portfolio of Omkar Musale, Senior Data Engineer. Live at https://omkarmusale0910.github.io

A single static page in plain HTML, CSS and JavaScript, with no build step. `index.html` is what GitHub Pages serves.

## Editing

`src/body.html` is the source. After changing it, rebuild `index.html`:

```sh
{ printf '<!doctype html>\n<html lang="en">\n<head>\n<meta charset="utf-8">\n<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">\n'; sed -n '1,/<\/style>/p' src/body.html; printf '</head>\n<body>\n'; sed -n '/<\/style>/,$p' src/body.html | tail -n +2; printf '</body>\n</html>\n'; } > index.html
```
