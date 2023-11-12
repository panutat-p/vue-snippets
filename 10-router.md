# Vue Router

https://router.vuejs.org/installation.html

## $route

* Visiting `http://localhost:4000/products?page=4`

```vue
<template>
  <p>You are on {{ $route.query.page }}</p>
</template>
```

## useRoute

```vue
<script setup lang="ts">
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()

const page = computed(() => parseInt(<string>route.query.page) || 1)
</script>

<template>
  <p>Current page is {{ page }}</p>
</template>
```
