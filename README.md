# Project catalog

A catalog of public projects, tools, and training resources by beardofedu.

## Updating the catalog

Edit `index.html` to update a project. Keep each description to two sentences,
link the project title to its repository, and maintain alphabetical order within
each topic. Styling lives in `styles.css`.

## Publishing

In repository **Settings → Pages**, select **GitHub Actions** as the source.
The workflow builds and deploys the site when changes reach `main`, or when
manually started from the Actions tab. It downloads the pinned official Primer
CSS package at build time and publishes the stylesheet with the site; visitors
do not need a third-party stylesheet or JavaScript. The project site is expected
at `https://beardofedu.github.io/project-catalog/` after a successful deployment.

For a local preview with Primer, install Node.js and run:

```sh
npm install --no-save --no-package-lock --ignore-scripts @primer/css@22.1.0 @primer/primitives@11.3.1
mkdir -p assets
cp node_modules/@primer/css/dist/primer.css assets/primer.css
```

Then open `index.html` in a browser. The generated `assets/` and `node_modules/`
directories are not committed.

## Accessibility

The site is designed for keyboard navigation, narrow screens, and browser zoom.
Automated checks cannot establish WCAG conformance on their own; also review the
site with keyboard and assistive technologies after changes.
