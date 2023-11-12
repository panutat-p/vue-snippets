# Vue Router

https://router.vuejs.org/installation.html

## $route

* Visiting `http://localhost:4000/products/2?year=2023`

```vue
<template>
  <p>Page {{ $route.params.page }}</p>
  <p>Year {{ $route.query.year }}</p>
</template>
```

## useRoute

* Visiting `http://localhost:4000/products/2?year=2023`

```vue
<script setup lang="ts">
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()

const page = computed(() => parseInt(<string>route.params.page) || 1)
const year = computed(() => parseInt(<string>route.query.year) || 2000)
</script>

<template>
  <h1>This is a product page</h1>

  <h2>$route</h2>
  <p>Page: {{ $route.params.page }}</p>
  <p>Year: {{ $route.query.year }}</p>

  <h2>computed</h2>
  <p>Page: {{ page }}</p>
  <p>Year: {{ year }}</p>
</template>
```
