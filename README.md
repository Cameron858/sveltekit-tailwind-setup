# sveltekit x tailwindcss

This has been written inline with the tutorial found [here](https://www.youtube.com/watch?v=A93LogPsEv8&ab_channel=simonswiss)

## Creating the project
---

The project skeleton was set up as follows:
```
npm svelte@latest tailwindcss-tutorial
cd ./tailwindcss-tutorial
npm install
npm install -D tailwindcss postcss autoprefixer
```

## Setup
---
Init tailwind config file. include `-p` for postcss config file.
```
npx tailwind init -p
```
Update the tailwind config file to the `src` folder.
```
content: [
    'src/**/*.{svelte, html, js, ts}
]
```

Add `app.css` file to src
```
src
|    - routes
|    - app.css
|    - app.html
```

Import the tailwind directives into `app.css`
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

In svelte's base layout, import `app.css`
```
<script>
    import "../app.css";
</script>
```

## Styles

Start a local development server
```
npm run dev
```

Add classes from [the docs](https://tailwindcss.com/docs)
```
<h1 class="text-3xl font-bold underline text-green-500">
```
