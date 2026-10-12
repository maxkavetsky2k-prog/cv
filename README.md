# CV site

Static site: `index.html` (hero + CV), `resume.html` (print layout), `assets/` (video, poster, PDFs).

Rebuild PDFs after editing `resume.html`:

```
for l in en ru uk; do "/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --disable-gpu --no-pdf-header-footer --virtual-time-budget=8000 --print-to-pdf="$PWD/assets/cv_$l.pdf" "http://localhost:8791/resume.html?lang=$l"; done
```
