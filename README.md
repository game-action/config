# 🛠️ GameAction config files

This repository contains the common configuration files for GameAction projects.

## 💻 Usage

Install the package as a dev dependency from [npm](https://www.npmjs.com/package/@game-action/config):

```bash
npm install --save-dev @game-action/config
```
or
```bash
yarn add -D @game-action/config
```

### Prettier

Our Prettier configuration keeps all defaults with the exception of print width, which is set at 120 characters rather than 80. To use this configuration, create a Prettier config file `.prettierrc.cjs` in the project root:

```js
module.exports = require("@game-action/config").prettier;
```

### Semantic Release

We use [Semantic Release](https://github.com/semantic-release/semantic-release) for automated deployments of our packages. Our configuration adds support for [Gitmoji](https://gitmoji.carloscuesta.me) commits, creating release notes with a `CHANGELOG.md`, and publishing to GitHub and npm.

Create a Semantic Release config file `release.config.js` in the project room. If you want to release the `master` or `production` branches, you can use the import directly:

```js
module.exports = require("@game-action/config").master;
```

Alternately, you can specify the branch you want to release:

```js
module.exports = require("@game-action/config").release("branch-name");
```

## 📄 License

- Code: [MIT](./LICENSE) © [Rémy BRUYERE](https://remy.ovh)

<p align="center">
  <sub>An open source project by <a href="https://remy.ovh">rem42</a></sub>
</p>
