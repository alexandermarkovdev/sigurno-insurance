# Застраховки гр.Стамболийски - Пловдив

Bulgarian insurance office website. Static HTML, CSS and JavaScript; no dependencies or build step.

## Run locally

```sh
python -m http.server 8080 --directory dist
```

Open http://localhost:8080/. Serve `dist/` as the website root so navigation and asset paths work correctly.

## Pages

Homepage, six individual insurance products, claims guidance and contact information. The menu uses Гражданска отговорност, Каско, Имуществени, Медицински, Живот and Пенсионни, with full titles on each product page. The earlier /kontakti/ contact route is retained.

Business: бул. „Марица“ 20, Стамболийски 4210, Пловдивска област, България. Phone: 089 597 0516. Hours: every day 08:00–19:00.

Forms are demonstrations: they validate inputs and show a local review, with an optional download. They do not transmit requests, issue policies or accept payments.

## Updates

This repository is the public website mirror. A local post-commit hook on the source project copies the current `dist/`, commits changes and pushes to `main`. Project references, credentials, hosting configuration and private source history are excluded. Ordinary edits made in a clone of this public repository can be committed and pushed normally.

Live mobile-test website: https://alexandermarkovdev.github.io/sigurno-insurance/

The local sync step pushes the source to `main` and the prepared website to `gh-pages`, which GitHub Pages publishes automatically. `scripts/build-pages.py` prepares project-relative asset and navigation paths in `_site/`; the original `dist/` stays compatible with the existing website hosting.
