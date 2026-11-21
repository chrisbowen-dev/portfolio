# Portfolio

The source for my personal portfolio website: a single responsive page that introduces me, my skills, my education and experience, and projects I've built.

It's plain HTML, CSS and JavaScript, with no framework and no build step.

## Features

- **Responsive layout.** Works on phones, tablets and desktops. On mobile the nav moves to a bottom menu.
- **Light and dark themes.** A toggle in the header, and the choice is remembered between visits.
- **Skills accordion.** Frontend and backend skill groups that expand and collapse.
- **Project carousel.** A swipeable slider of projects with screenshots and demo links, built on Swiper.
- **Contact form.** Sends messages to my inbox through FormSubmit, with no backend needed.
- **Scroll extras.** The nav highlights the current section, and a back-to-top button appears as you scroll.

## Tech stack

| Purpose | Tool |
| --- | --- |
| Markup and styling | HTML5, CSS3 (custom properties, Grid, Flexbox) |
| Interactivity | Vanilla JavaScript |
| Carousel | [Swiper](https://swiperjs.com) 6.5.8 (bundled locally) |
| Icons | [Unicons](https://iconscout.com/unicons) (CDN) |
| Fonts | [Poppins](https://fonts.google.com/specimen/Poppins) (Google Fonts) |
| Contact form | [FormSubmit](https://formsubmit.co) |
| Hosting | [Render](https://render.com) static site (planned) |

## Project structure

```
.
├── index.html                  # The whole page
├── assets/
│   ├── css/
│   │   ├── style.css           # Site styles and theme variables
│   │   └── swiper-bundle.min.css
│   ├── js/
│   │   ├── main.js             # Menu, accordion, carousel, theme toggle, scroll effects
│   │   └── swiper-bundle.min.js
│   └── img/                    # Profile photo, about photo and project screenshots
├── render.yaml                 # Render static-site config
├── CHANGELOG.md
└── README.md
```

## Running locally

Nothing to install. Either open `index.html` in a browser, or serve the folder so links behave the way they will in production:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Customizing

- **Theme color:** change `--hue-color` at the top of `assets/css/style.css`. Try 340 for pink (current), 250 for purple, 230 for blue or 142 for green.
- **Content:** every section lives in `index.html`, marked with a comment banner such as `<!-- ABOUT -->`.
- **Skill levels:** each bar's fill is set with an inline `style="width: N%"` in `index.html`.
- **Projects:** each slide is a `.portfolio-content` block inside `.swiper-wrapper`. Copy one to add a project, and put its screenshot in `assets/img/`.

## Deployment

The site is set up to deploy on Render as a **Static Site**:

1. In Render, choose **New → Static Site** and connect this repo, or use **Blueprint**, which reads `render.yaml`.
2. Leave the build command empty and set the publish directory to `.`.
3. Every push to `main` then redeploys automatically.

## History

I first built this site in 2022 and hosted it on Netlify. When I lost access to that account and the original source, I recreated it from the live deployment. See [CHANGELOG.md](CHANGELOG.md) for what's changed since.

## Credits

The layout is adapted from Bedimcode's "Responsive Portfolio Website" tutorial template. Swiper is © Vladimir Kharlampidi, MIT License.
