# Basic

## Set up

https://vuejs.org/guide/quick-start.html

```shell
npm create vue@latest
```

## Entry point

`main.ts`
```typescript
import { createApp } from 'vue'
import App from "@/App.vue";

const app = createApp(App)
app.mount('#app')
```

`index.html`
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vite</title>
  </head>
  <body>
    <div id="app"></div>
    <script type="module" src="/src/main.ts"></script>
  </body>
</html>
```
