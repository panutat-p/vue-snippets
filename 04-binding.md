# Binding

https://vuejs.org/guide/essentials/class-and-style.html

## Class binding

```vue
<script setup>
import { ref } from 'vue'

const isRed = ref(true)
</script>

<template>
  <div v-bind:class="{ 'text-red': isRed }">
    <h1>Hello</h1>
  </div>
</template>

<style>
.text-red {
  color: red;
}
</style>
```
