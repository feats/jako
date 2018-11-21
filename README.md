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

The name `jako` comes from "**JAK**e + **O**pinionated".

> Jake is the JavaScript build tool for NodeJS. Jake has been around since the very early days of Node, and is very full featured and well tested.

In essence, _jako_ is just a tiny but powerful wrapper around [jake](http://jakejs.com/). Under the hood, _jako_ combines the maturity of a battle-tested codebase with a modern architecture.

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

## Writting your first scripts/tasks

Let's create our first script together! To do so, let's imagine you want to have a script that clears all the `node_modules` folders in your repo.

1. create a `/scripts/clean` folder inside your project:
```bash
$ mkdir -p scripts/clean
```
2. write the logic inside an executable file inside the created folder:
```bash
$ printf "#\!/bin/bash\nfind . \( -type d -name 'node_modules' \) -exec rm -rf '{}' +" > scripts/clean/node_modules.sh
```
3. give it permission to run:
```bash
$ chmod +x **/*.sh
```

4. run it!
```bash
# both calls below should be equivalent:
$ jako clean:node_modules
# or
$ ./scripts/clean/node_modules.sh

# running `jako` with no arguments will list the available tasks
$ jako
```

Keep in mind that you can create `scripts` folder anywhere you want in your project and _jako_ will adapt to it.

Nesting `scripts` folders deep inside your project is not only possible but recommended!

![divider](.github/divider.png)

## Good practices

* always add [shebang](https://en.wikipedia.org/wiki/Shebang_%28Unix%29) to your scripts.
* always give your scripts permision to run: `chmod +x **/*.ext` (where `ext` is the extension of the files you want to make executable)

![divider](.github/divider.png)

**Credits**

Vector illustration credit: <a target="_blank" href="https://vecteezy.com">www.vecteezy.com</a>
