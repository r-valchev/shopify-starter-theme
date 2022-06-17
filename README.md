# Shopify starter theme for OnlineStore 2.0

[Getting started](#getting-started) |
[Developer tools](#developer-tools) |
[License](#license)

This starter template is based on Dawn theme.
Dawn represents a HTML-first, JavaScript-only-as-needed approach to theme development. It's Shopify's first source available theme with performance, flexibility, and [Online Store 2.0 features](https://www.shopify.com/partners/blog/shopify-online-store) built-in and acts as a reference for building Shopify themes.

## Getting started

We use Shopify CLI to develop themes.\
[Learn more about Shopify CLI](https://shopify.dev/themes/tools/cli/getting-started). \
[Link to all shopify theme commands](https://shopify.dev/themes/tools/cli/theme-commands)

### Login to the Shopify CLI

```bash
shopify login
```

### Make sure you are logged in the correct store

Check which store and account you are logged in. If not the correct one, use switch to change to the desired store.

```bash
shopify whoami
shopify switch --store name-of-store
```

<sub>In this case the store will be name-of-store.myshopify.com</sub>

### Developing themes:

#### Starting Shopify CLI server

```bash
shopify theme serve
```

When you start a server, all of the changes are applied locally and into a shadow theme called Development(XXXXXXXXX).\
**All of the content changes done in the shadow Customizer will be removed when the server is stopped.** \
If you want to have those changes to be saved locally, you have to pull them, before you stop your server.

#### Pull changes from store theme:

To pull changes from store theme into your local theme use the command and select the theme you want to pull from.

```bash
shopify theme pull
```

#### Push your local changes to shopify store

To push your local changes to a theme in the store use the command and choose the theme you want to overwrite:

```bash
shopify theme push
```

## Developer tools

There are a number of really useful tools that the Shopify Themes team uses during development. Dawn is already set up to work with these tools.

### Shopify CLI

[Shopify CLI](https://github.com/Shopify/shopify-cli) helps you build Shopify themes faster and is used to automate and enhance your local development workflow. It comes bundled with a suite of commands for developing Shopify themes—everything from working with themes on a Shopify store (e.g. creating, publishing, deleting themes) or launching a development server for local theme development.

You can follow this [quick start guide for theme developers](https://github.com/Shopify/shopify-cli#quick-start-guide-for-theme-developers) to get started.

### Theme Check

We recommend using [Theme Check](https://github.com/shopify/theme-check) as a way to validate and lint your Shopify themes.

We've added Theme Check to Dawn's [list of VS Code extensions](/.vscode/extensions.json) so if you're using Visual Studio Code as your code editor of choice, you'll be prompted to install the [Theme Check VS Code](https://marketplace.visualstudio.com/items?itemName=Shopify.theme-check-vscode) extension upon opening VS Code after you've forked and cloned Dawn.

You can also run it from a terminal with the following Shopify CLI command:

```bash
shopify theme check
```

### Continuous Integration

Dawn uses [GitHub Actions](https://github.com/features/actions) to maintain the quality of the theme. [This is a starting point](https://github.com/Shopify/dawn/blob/main/.github/workflows/ci.yml) and what we suggest to use in order to ensure you're building better themes. Feel free to build off of it!

#### Shopify/lighthouse-ci-action

We love fast websites! Which is why we created [Shopify/lighthouse-ci-action](https://github.com/Shopify/lighthouse-ci-action). This runs a series of [Google Lighthouse](https://developers.google.com/web/tools/lighthouse) audits for the home, product and collections pages on a store to ensure code that gets added doesn't degrade storefront performance over time.

#### Shopify/theme-check-action

Dawn runs [Theme Check](#Theme-Check) on every commit via [Shopify/theme-check-action](https://github.com/Shopify/theme-check-action).

## License

Copyright (c) 2021-present Shopify Inc. See [LICENSE](/LICENSE.md) for further details.
