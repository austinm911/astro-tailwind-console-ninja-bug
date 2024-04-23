# Astro Starter Kit: Basics

## Command Line History

```bash
 bun create astro@latest

 astro   Launch sequence initiated.

   dir   Where should we create your new project?
         ./astro-tailwind-console-ninja-bug

  tmpl   How would you like to start your new project?
         Include sample files

    ts   Do you plan to write TypeScript?
         Yes

   use   How strict should TypeScript be?
         Strict

  deps   Install dependencies?
         Yes

   git   Initialize a new git repository?
         Yes

      ✔  Project initialized!
         ■ Template copied
         ■ TypeScript customized
         ■ Dependencies installed
         ■ Git initialized

  next   Liftoff confirmed. Explore your project!

         Enter your project directory using cd ./astro-tailwind-console-ninja-bug
         Run bun run dev to start the dev server. CTRL+C to stop.
         Add frameworks like react or tailwind using astro add.

         Stuck? Join us at https://astro.build/chat

╭─────╮  Houston:
│ ◠ ◡ ◠  Good luck out there, astronaut! 🚀
╰─────╯
❯ cd astro-tailwind-console-ninja-bug
❯ bunx astro add tailwind
✔ Resolving packages...

  Astro will run the following command:
  If you skip this step, you can always run it yourself later

 ╭──────────────────────────────────────────────────────╮
 │ bun add @astrojs/tailwind@^5.1.0 tailwindcss@^3.4.3  │
 ╰──────────────────────────────────────────────────────╯

✔ Continue? … yes
✔ Installing dependencies...

  Astro will generate a minimal ./tailwind.config.mjs file.

✔ Continue? … yes

  Astro will make the following changes to your config file:

 ╭ astro.config.mjs ─────────────────────────────╮
 │ import { defineConfig } from 'astro/config';  │
 │                                               │
 │ import tailwind from "@astrojs/tailwind";     │
 │                                               │
 │ // https://astro.build/config                 │
 │ export default defineConfig({                 │
 │   integrations: [tailwind()]                  │
 │ });                                           │
 ╰───────────────────────────────────────────────╯

✔ Continue? … yes

   success  Added the following integration to your project:
  - @astrojs/tailwind
❯ cursor .
❯ bun dev
$ astro dev
✔ Console Ninja extension is connected to Astro, see https://tinyurl.com/2vt8jxzw
ENOENT: no such file or directory, read
  Stack trace:
    at Object.readFileUtf8 (/Users/xx/.cursor/extensions/wallabyjs.console-ninja-1.0.309/out/buildHook/index.js:1144:67469)
    at Module._extensions..js (node:internal/modules/cjs/loader:1397:18)
    at Module._load (node:internal/modules/cjs/loader:1023:12)
    at require (node:internal/modules/helpers:176:18)
    at Module._compile (node:internal/modules/cjs/loader:1376:14)
error: script "dev" exited with code 1
```

However, after deleting node modules and bun lock, this is the result of using pnpm

```bash
❯ pnpm i
Packages: +506
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Progress: resolved 565, reused 483, downloaded 23, added 506, done
node_modules/.pnpm/esbuild@0.19.12/node_modules/esbuild: Running postinstall script, done in 558ms
node_modules/.pnpm/sharp@0.32.6/node_modules/sharp: Running install script, done in 2.9s
node_modules/.pnpm/esbuild@0.20.2/node_modules/esbuild: Running postinstall script, done in 535ms

dependencies:
+ @astrojs/check 0.5.10
+ @astrojs/tailwind 5.1.0
+ astro 4.6.3
+ tailwindcss 3.4.3
+ typescript 5.4.5

Done in 9.4s
❯ pnpm dev

> astro-tailwind-console-ninja-bug@0.0.1 dev /Users/xx/Coding/repro/astro-tailwind-console-ninja-bug
> astro dev

✔ Console Ninja extension is connected to Astro, see https://tinyurl.com/2vt8jxzw

 astro  v4.6.3 ready in 381 ms

┃ Local    http://localhost:4321/
┃ Network  use --host to expose

07:52:10 watching for file changes...
```

ORIGINAL README below

```sh
npm create astro@latest -- --template basics
```

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/withastro/astro/tree/latest/examples/basics)
[![Open with CodeSandbox](https://assets.codesandbox.io/github/button-edit-lime.svg)](https://codesandbox.io/p/sandbox/github/withastro/astro/tree/latest/examples/basics)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/withastro/astro?devcontainer_path=.devcontainer/basics/devcontainer.json)

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

![just-the-basics](https://github.com/withastro/astro/assets/2244813/a0a5533c-a856-4198-8470-2d67b1d7c554)

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   └── Card.astro
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       └── index.astro
└── package.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).
