# sandbox-tailwind-css

## About

Debug, Test standalone [Tailwind CSS](https://tailwindcss.com/)
- Check other branches for older versions.
- Compare the same example in multiple (version) branches.

## Installation

😞 The [`tailwindcss`](https://tailwindcss.com/blog/standalone-cli) CLI DX was not great (many unanswered questions for the time spent, e.g. can you use it to install different TW versions? Why it does not scaffold for you?).

Moving to [installing with postCSS](https://v3.tailwindcss.com/docs/installation/using-postcss).  
[postCSS](https://postcss.org) is a tool for transforming CSS with JavaScript plugins.  
[postCSS](https://postcss.org) is not a CSS preprocessor like Sass or LESS but as the name suggests a **postprocessor**—meaning it processes your CSS after you've written it, often enhancing, optimizing, or modifying it.

Sidenote: Tailwind CSS is a postCSS sponsor.

1. Read 👉 [3.4.x docs](https://v3.tailwindcss.com/docs/installation/using-postcss) **WATCH FOR VERSIONS**

2. Run `npm run init` it creates the following files:

```js
// postcss.config.js
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  }
}
```

```js
//tailwind.comfig.js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

3. Build and watch for changes: `npm run start`

## Version

3.4.17

TIP: See all npm available versions: `npm view tailwindcss versions`
