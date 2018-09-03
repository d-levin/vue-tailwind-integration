# vue-tailwind

> Example of [Vue.js](https://vuejs.org) and [Tailwind CSS](https://tailwindcss.com) integration

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn run serve
```

### Compiles and minifies for production
```
yarn run build
```

### Lints and fixes files
```
yarn run lint
```

## Integrate Tailwind CSS with Existing Projects

Source: https://flaviocopes.com/vue-tailwind/

### Install Tailwind
```bash
# Using npm
npm install tailwindcss --save-dev

# Using Yarn
yarn add tailwindcss --dev
```

### Create a Configuration File
```bash
./node_modules/.bin/tailwind init tailwind.js
```

### Configure PostCSS
Edit `postcss.config.js` or create one if it does not exist:
```javascript
module.exports = {
  'plugins': [
    require('tailwindcss')('./tailwind.js'),
    require('autoprefixer')()
  ]
}
```

### Remove PostCSS Configuration from Package.json
Remove the following lines from `package.json` if they exist (or `postcss.config.js` won't be read):
```bash
"postcss": {
  "plugins": {
    "autoprefixer": {}
  }
},
```

### Create a CSS File
Create a CSS file in `src/assets/css/tailwind.css` and add:
```bash
@tailwind preflight;
@tailwind components;
@tailwind utilities;
```

### Import the CSS File
Import Tailwind CSS in `src/main.js`:
```javascript
import 'src/assets/css/tailwind.css'
```

### Done!
Tailwind CSS is now ready to be used. Test it by adding some Tailwind classes on an element:
```html
<div class="bg-red text-white p-10">
  Test
</div>
```
