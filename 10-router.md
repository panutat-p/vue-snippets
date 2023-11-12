# Vue Router

https://router.vuejs.org/installation.html

## $route

* Visiting `http://localhost:4000/products/2?year=2023`

```typescript
const router = createRouter({
  history: createWebHistory(import.meta.env.BASE_URL),
  routes: [
    {
      path: '/product/:page',
      name: 'product',
      component: ProductView,
    },
  ],
})
```

```vue
<template>
  <p>Page {{ $route.params.page }}</p>
  <p>Year {{ $route.query.year }}</p>
</template>
```

## useRoute

* Visiting `http://localhost:4000/products/2?year=2023`

```typescript
const router = createRouter({
  history: createWebHistory(import.meta.env.BASE_URL),
  routes: [
    {
      path: '/product/:page',
      name: 'product',
      component: ProductView,
    },
  ],
})
```

```vue
<script setup lang="ts">
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()

const page = computed(() => parseInt(<string>route.params.page) || 1)
const year = computed(() => parseInt(<string>route.query.year) || 2000)
</script>

<template>
  <p>Page: {{ page }}</p>
  <p>Year: {{ year }}</p>
</template>
```

## Props Object Mode

```javascript
const routes = [
  {
    path: "/",
    name: "Home",
    component: Home,
    props: { showExtra: true },
  },
```

```vue
<script setup>
defineProps(['showExtra'])
</script>

<template>
  <div class="home">
    <h1>This is a home page</h1>
    <div v-if="showExtra">Extra stuff</div>
  </div>
</template>
```

## Props Function Mode

```javascript
const routes = [
  {
    path: "/",
    name: "Home",
    component: Home,
    props: route => {
      return { showExtra: route.query.e }
    }
  },
```

```vue
<script setup>
defineProps(['showExtra'])
</script>

<template>
  <div class="home">
    <h1>This is a home page</h1>
    <div v-if="showExtra">Extra stuff</div>
  </div>
</template>
```
