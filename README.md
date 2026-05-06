# Git Portfolio

A personal portfolio website built with Vue 3 and Vite, designed to showcase resume details, experience, skills, and contact information.

## Built with

- **Vue 3** — modern reactive UI using `<script setup>` single-file components
- **Vite** — fast development server and build pipeline
- **Tailwind CSS** — utility-first styling support (configured for the project)
- **JavaScript (ESM)** — app logic and theme switching
- **CSS** — custom layout and responsive styling

## Features

- Responsive portfolio layout
- Light / dark theme toggle
- Downloadable resume button
- Experience and skills sections
- Contact and education details
- Simple and modern UI design

## Getting Started

### Install dependencies

```bash
npm install
```

### Run locally

```bash
npm run dev
```

Open the local URL shown in the terminal to view the portfolio.

### Build for production

```bash
npm run build
```

## Customize the portfolio

Update the content in these files to personalize your portfolio:

- `src/components/Header.vue` — site title, navigation, resume button
- `src/components/Hero.vue` — name, title, personal info, summary
- `src/components/Projects.vue` — experience history
- `src/components/Skills.vue` — skills and characteristics
- `src/components/Contact.vue` — education and contact links
- `src/style.css` — theme colors, layout, and visual styles

## Resume download

The download button links to `public/resume.pdf`. Replace that file with your actual resume PDF to make the download work.

## GitHub Pages deployment

This repository includes a GitHub Actions workflow at `.github/workflows/deploy.yml`. When you push to `main` or `master`, the site will be built and published automatically to the `gh-pages` branch.

If your repository is hosted at `https://github.com/<username>/git-portfolio`, your site will be available at:

- `https://<username>.github.io/git-portfolio/`

## Notes

This project is intended as a simple portfolio starter that you can extend with more sections, animations, or project cards.
