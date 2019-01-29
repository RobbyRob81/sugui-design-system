# SugUI Design System

This package works together with the [sugui](https://github.com/gazpachu/sugui) UI component library.

If you decide to fork it, to make your custom design system, you might want to setup your local environment to have both packages working together with hot reloading. If you don't want to change the components and their examples, then you probably will be fine just running `yarn run styleguide`, otherwise continue reading...

## Local env. setup

If you want to modify the components and their examples and see the changes in real-time in the styleguidist website, then you will need to create a symbolic link to the `sugui` library.

You can use [yarn link](https://yarnpkg.com/lang/en/docs/cli/link/) or [npm link](https://docs.npmjs.com/cli/link.html).

First, clone the [sugui](https://github.com/gazpachu/sugui) package into your computer.

Go to your cloned `sugui` folder and type:

```cmd
yarn link
```

Then go to `/sugui-design-system/node_modules` folder and type:

```cmd
yarn link sugui
```

Done!, now your `sugui` folder in `node_modules` will reference your cloned `sugui` folder, rather than the one downloaded from npm.

Now you can run the styleguide and it will trigger the Hot Reload everytime you change anything in `sugui` or in `sugui-design-system`.

```cmd
yarn run styleguide
```

## Production build

Type:

```cmd
yarn run styleguide:build
```

## Deploy to Github pages

```cmd
yarn run deploy
```
