# Changelog

All notable changes to this project are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and the project uses [Semantic Versioning](https://semver.org/).

## [Unreleased]

### Planned
- Update personal details: name, intro, bio, contact email and social links.
- Link the "Download CV" button to a real resume.
- Refresh skills, experience and projects.
- Deploy to Render.

## [1.1.0] - 2026-11-20

Recreated the site from the live Netlify deployment after the original source and hosting account were lost, and moved it to this repository.

### Added
- `README.md` describing the project, its structure, local setup and deployment.
- `CHANGELOG.md`.
- `render.yaml` so the site can be deployed as a Render static site.
- `aria-label`s on icon-only links and buttons.
- `target="_blank"` with `rel="noopener"` on external project and social links.
- `required` attributes on the contact form's name, email and message fields.

### Changed
- Renamed image assets to descriptive names (`profile.png`, `about.jpg`, `project-*.jpg`).
- Re-captured the project screenshots and photos at display resolution, which shrinks total image size from about 5.4 MB to about 400 KB.
- The contact form's Subject field now sets the email subject line, through FormSubmit's `_subject` field.
- Skill bar widths are now set inline per skill instead of by one CSS class per skill.
- Tidied the formatting of the CSS and JavaScript.

### Fixed
- Skills accordion: the backend section never opened, because an extra class broke the open/close check.
- The JavaScript/jQuery and React skill bars showed 10% while their labels said 30%.
- Typos in the section subtitle, project descriptions and work history.
- A stray double semicolon in the font-family declaration.

### Removed
- The phone number in the Contact section.
- An empty qualification tabs container left over from the template.

## [1.0.0] - 2022

### Added
- First version of the portfolio, built from Bedimcode's responsive portfolio template and hosted on Netlify.
- Sections: Home, About, Skills, Qualification, Portfolio (LMS, Valley Talley, Sunridge HOA and this site) and Contact.
- Light/dark theme toggle, a project carousel and a FormSubmit contact form.
