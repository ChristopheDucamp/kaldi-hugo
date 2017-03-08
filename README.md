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

Le template est basé sur des petits "partials" agnostiques-au-contenu qui peuvent être mélangés et combinés. Les pages pré-construites présentent quelques combinaisons possilbes. Réflérez-vous au répertoire `site/layouts/partials` pour tous les partials disponibles.

Utilisez la fonctionnalité `dict` de Hugo pour alimenter le contenu à l'intérieur des partials et pour éviter de vous répéter et de créer des divergences.

## CSS

Le template utilise un fork personnalisé de Tachyons et PostCSS avec cssnext et cssnano. Pour personnaliser le template pour votre marque, référez-vous à `src/css/imports/_variables.css` où sont stockées la plupart des variables globales importantes comme les couleurs et l'espacement.

## SVG

Toutes les icônes SVG stockées dans `site/static/img/icons` sont automatiquement optimisées avec SVGO (gulp-svgmin) et concaténées dans un sprite SVG unique sous forme d'un partiel appelé `svg.html`. Assurez-vous d'utiliser des icônes cohérentes en termes de viewport et de direction artistique pour des résultats optimaux. Référez vous à un SVG via la balise `<use>` comme suit :

```
<svg width="16px" height="16px" class="db">
  <use xlink:href="#SVG-ID"></use>
</svg>
```
