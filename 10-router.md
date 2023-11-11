# Vue Router

https://router.vuejs.org/installation.html

## $route

```vue
<script setup>
// current path is http://localhost:4000/products?page=4
</script>

<template>
  <p>Your are on {{ $route.query.page }}</p>
</template>
```
