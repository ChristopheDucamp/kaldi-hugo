# Netlify CMS template small-business

Ceci est un template small business construit avec [Victor Hugo](https://github.com/netlify/victor-hugo) et [Netlify CMS](https://github.com/netlify/netlify-cms).

## Pour démarrer

Utiliser notre bouton "deploy" pour disposer de votre propre copie du repository :

[![Déployer vers Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/netlify-templates/kaldi-hugo-cms-template)

Une fois que c'est fait, vous devez régler l'intégration GitHub pour le CMS Netlify.

Allez sur https://github.com/settings/developers et enregistrez une nouvelle application.

Puis, allez sur l'onglet "Access" dans votre site Netlify et ajoutez un fournisseur d'authentification GitHub.

Une fois que c'est fait, vous pourrez rentrer dans le CMS en allant à l'URL de votre nouveau site et en ajoutant `/admin`

## Développement Local

Clonez ce repository, et lancez `yarn` ou `npm install` à partir du nouveau répertoire pour installer toutes les dépendances requises.

Puis lancez le serveur de développement avec `yarn start` ou `npm start`.

## Layouts

The template is based on small, content-agnostic partials that can be mixed and matched. The pre-built pages showcase just a few of the possible combinations. Refer to the `site/layouts/partials` folder for all available partials.

Use Hugo’s `dict` functionality to feed content into partials and avoid repeating yourself and creating discrepancies.

## CSS

The template uses a custom fork of Tachyons and PostCSS with cssnext and cssnano. To customize the template for your brand, refer to `src/css/imports/_variables.css` where most of the important global variables like colors and spacing are stored.

## SVG

All SVG icons stored in `site/static/img/icons` are automatically optimized with SVGO (gulp-svgmin) and concatenated into a single SVG sprite stored as a a partial called `svg.html`. Make sure you use consistent icons in terms of viewport and art direction for optimal results. Refer to an SVG via the `<use>` tag like so:

```
<svg width="16px" height="16px" class="db">
  <use xlink:href="#SVG-ID"></use>
</svg>
```
