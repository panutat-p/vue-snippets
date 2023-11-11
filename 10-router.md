# Vue Router

https://router.vuejs.org/installation.html

## $route

```vue
<script setup>
// current path is http://localhost:4000/products?page=4
</script>

<template>
  <p>You are on {{ $route.query.page }}</p>
</template>
```

## useRoute

```vue
<script setup>
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()
const page = computed(() => parseInt(route.query.page) || 1)

// current path is http://localhost:4000/products?page=4
</script>

<template>
  <p>You are on {{ page }}</p>
</template>
```
