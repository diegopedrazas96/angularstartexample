# Angular 2/TypeScript/Webpack Starter

This is the initial version of our starter project using Angular 2.x, TypeScript and Webpack to tie it all together.

## npm scripts

> To see all available scripts:
```bash
$ npm run
```

### Dev
```bash
$ npm run dev
```

This runs a development mode server with live reload etc.

Open `http://localhost:8080` in your browser.

### Production

```bash
$ npm install
$ npm start
```
or
```bash
$ npm run build
$ npm start
```
This runs a production-ready express server that serves up a bundled and
minified version of the client.

Note: AoT is enabled by default. To disable AoT, use `npm run build:jit`.

Open `http://localhost:8080` in your browser.

### Tests

#### Single Run (with linting and coverage)
```bash
$ npm test
# or
$ npm t
```

#### Watch Files
```bash
$ npm run test:watch
```

#### Coverage
```bash
$ npm run cover
```

## Webpack

Configurations:
- For dev & jit: `webpack.config.js`
- For production & AoT: `webpack-aot.config.js`

The webpack directory consists of:
- `loaders.js`: definitions for all the loaders used in this project
- `plugins.js`: definitions for all the plugins used in this project. These are grouped based on `process.env`.
- `postcss.js`: configuration for the postcss plugin.

### Bundle Profiling

If you want to analyze the contents and size of the production bundles you can run one of the following commands:
- `npm run profile-build` for AoT builds
- `npm run profile-build:jit` for JiT builds

These commands produce a `stats.json` manifest in the project root and also opens a web page using `webpack-bundle-analyzer` so that you can parse it visually.

#### Connecting to remote APIs

Both the devmode and production servers provide a way to proxy requests to
remote HTTP APIs.  This can be useful for working around CORS issues when
developing your software.

Edit [this file](server/proxy-config.js) to mount such APIs at a given path.

## License

Copyright (c) 2016 rangle.io

[MIT License][MIT]

[MIT]: ./LICENSE "Mit License"
