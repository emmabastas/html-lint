> # ⚠️ This repository is a mirror of [a Codeberg repository](https://codeberg.org/emmabastas/html-lint)
>
> There are many reasons to prefer a community-run platform like Codeberg over something like GitHub which is a for-profit company part of a soft power apparatus. I think [this blogpost](https://seanfobbe.com/posts/2025-04-10_migrating-open-source-code-from-github-to-codeberg/) articulates some of those reasons well.
>
> Please feel free to open issues here! But if you want to have a look at the code then head on over to Codeberg :-)
> [codeberg.org/emmabastas/html-lint](https://codeberg.org/emmabastas/html-lint)
# `html-lint` — Your one-stop shop for HTML linting activities

Whether you're using a templating engine for your server-side rendering, a frontend framework for your SPA, or making a good ol static website: If there's HTML involved, you can lint it using `html-lint`!

There are two ways of using `html-lint`
  1) In the terminal: Give the cli-app files to lint and it will give you a report.
  2) In the browser: `html-lint` can analyses the HTML in the website itself.

## Why not use <my favorite HTML linter> instead?

There are many nice HTML linters out there, however `html-lint` tries to be something I have not seen elsewhere:
  - **Universal.** Many html linters are tied to a specific ecosystem: [djlint](https://github.com/djlint/djlint) is tied to `pip` and is for HTML templates only, [html-eslint](https://github.com/yeonjuan/html-eslint?tab=readme-ov-file) is tied to NodeJS and HTML-in-JS. With `html-lint` you can install it with `pip` for your templates one day, and then use the same tool via `npm` for React.
  - **zero-config, works for you.** `html-lint` comes with sane defaults so you can focus on making good accessible HTML and not fuss about with configuration. There is always the option of customizing though.
  - **Use it everywhere.** The mix of simultaneously working in the terminal and on the browser isn't something I've seen elsewhre.

## Use in the CLI

### Installing

- **Prebuilt binaries** in the [dist/cli](TODO) folder.
- **npm** `npm install --save-dev @emmabastas/html-lint-cli`
- **pip** `pip install html-lint`

### Usage

Lint all HTML and handlebars files in `src`.

```bash
html-lint src/**/*.html src/**/*.html src/**/*.hbs
```

More options with `html-lint --help`.

## Use in the browser

### Fastest: Use the reverse proxy

Go to [html-lint.notadev.net](html-lint.notadev.net) to lint any website.

### Add `<script>` tag

Add `<script src="https://cdnjs.cloudflare.com/TODO"></script>` inside the `<head>` of any page you want linted in the browser. You can conditionally include the script tag in development only. Te above script tag uses `cdnjs.com` to deliver the JS, if you want to host it yourself you can find minified JS bundles in [dist/jsbundles](TODO).

### npm package

If you're working on a frontend with npm you can install the npm package with `npm install --save-dev @emmabastas/html-lint-browser`, you then run it with

```js
TODO
```

You only want this to run in development, and so how you do that depends on what bundler you're using.

### Configuring

TODO

## Contributing

Please contribute <3. There are many ways to do so
- Let me know you appreciate this tool: Send me an email or star this repo, makes me really happy!
- Open issues with bugs or things that you want implemented.
- Add/improve linting rules. See [/rules/rules.yaml](TODO) for further information.
- Work on the CLI. See [/cli/README.md](TODO) for further information.
- TODO more.

## License

The following files belong to the [duktape.org](https://duktape.org) project and are licensed under the MIT license.
- [cli/src/duk_config.h](TODO)
- [cli/src/duk_source_meta.json](TODO)
- [cli/src/duktape.c](TODO)
- [cli/src/duktape.h](TODO)

All other code in this repository is owned by each respective contributor and licensed under the GNU Affero General Public License version 3 or later (AGPL-3.0-or-later). The license is found in [LICENSE](TODO).
