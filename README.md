# Image Gallery React / Pixabay

Install instructions:

npx create-react-app .

npm i -D tailwindcss postcss-cli autoprefixer

npx tailwind init tailwind.js --full

```
Create postcss config file:

    touch postcss.config.js

add following to it:
```

const tailwindcss = require('tailwindcss');

module.exports = {
plugins: [tailwindcss('./tailwind.js'), require('autoprefixer')],
};

```
Also add build css to package.json:

```

    "start": "npm run watch:css && react-scripts start",
    "build": "npm run watch:css && react-scripts build",
    "build:css": "postcss src/assets/tailwind.css -o src/assets/main.css",
    "watch:css": "postcss src/assets/tailwind.css -o src/assets/main.css"

```

```
