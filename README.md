# Portfolio

My personal portfolio site: a single static page built with plain HTML, CSS and JavaScript.

## Stack

- HTML / CSS / vanilla JavaScript, no build step
- [Swiper](https://swiperjs.com) 6.5.8 for the project carousel
- [Unicons](https://iconscout.com/unicons) for icons
- [FormSubmit](https://formsubmit.co) for the contact form
- Light/dark theme toggle (remembered in `localStorage`)

## Structure

```
index.html
assets/
  css/  style.css, swiper-bundle.min.css
  js/   main.js, swiper-bundle.min.js
  img/  profile, about and project screenshots
render.yaml   Render static-site config
```

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploy

Deployed on [Render](https://render.com) as a Static Site. There's no build command, the publish directory is `.`, and every push to `main` redeploys.

## Credits

Layout adapted from Bedimcode's "Responsive Portfolio Website" tutorial template.
