<p align="center"><img src="./.github/logo.png" width="215" /><p>
<br>

<p align="center">
<strong>Translucent opinionated scripts runner.</strong><br />
<sub>jako is a minimalist toolbelt choice for monorepo projects compatible with whatever languages you are using.</sub>
</p>

<p align="center">
  [ <a href="#getting-started">Getting started 🤓</a> | <a href="https://www.npmjs.com/package/jako">Check it on NPM 👌</a> ]
</p>
<br />

* **Zero setup:** There is no need to configure _jako_, and setting it up is as easy as moving your current scripts to a folder.

* **Polyglot:** You are free to write your scripts using any language you want.

* **Translucent:** Forget about build tools that force you to write code that only work for that specific runner. As a principle, all the scripts run by _jako_ need to be executable also without _jako_. No vendor lock, less API to keep track of.

* **Extensible and modular:** _jako_ doesn't hold you back while your project is growing. Encapsulate as many independent projects as you want in a single repo and _jako_ will let you run all your scripts from a centralized place.

<br />
<br />

The name `jako` comes from "**jak**e + **o**pinionated". Under the hood, it combines the maturity of a battle-tested codebase with a modern architecture.

> Jake is the JavaScript build tool for NodeJS. Jake has been around since the very early days of Node, and is very full featured and well tested.

In essence, _jako_ is just a tiny but powerful wrapper around jake.

![divider](.github/divider.png)

## Getting started

### Installing it

You can install it from one of these 3 options:

#### globally, with NPM

```bash
  $ npm install -g jako
```

#### globally, with Yarn

```bash
  $ yarn global add jako
```

#### locally
you may also install it as a development dependency in a package.json file:

```json
    // package.json
    "devDependencies": {
      "jako": "latest"
    }
```

Then install it with either `npm install` or `yarn install`

### Basic usage

    jako [options ...] [env variables ...] target

for the full list of available `options`, please check [jake's options](https://github.com/jakejs/jake/blob/master/docs/overview.md#options).

![divider](.github/divider.png)

**Credits**

Vector illustration credit: <a target="_blank" href="https://vecteezy.com">www.vecteezy.com</a>
