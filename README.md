# GitHub Pages starter
> Fast rendering, live reload, GitHub Pages ready

* Jekyll is great - but slow at compiling assets (images, SASS).
* This setup uses high performance gulp tasks to generate assets.

## Installation
1. Clone/download repo
2. `yarn install`
3. Edit `_config.yml`, change values for `url` and `custom_settings`.

## Development
Open 3 terminals and run the following commands (they need to be run in parallel).

1. `yarn run jekyll-dev` - Generates site on changes to `/_site`.
2. `gulp watch` - Compiles SASS and images on changes to `/_site/assets`.
3. `yarn run browser-sync` - Hosts content from `/_site` at `http://localhost:3000` and injects asset changes.

## Production
`gulp build` - Cleans, builds and minifies assets to `/assets`.
