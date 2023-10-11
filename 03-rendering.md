# Rendering

## Text Interpolation

https://vuejs.org/guide/essentials/template-syntax.html

```vue
<script setup>
import { ref } from 'vue'

const msg = ref("Click")
</script>

<template>
  <button>{{ msg }}</button>
</template>
```

## Conditional Rendering

```vue
<script setup>
import { ref } from 'vue'

const isShow = ref(true)
</script>

<template>
  <h1>Conditional Rendering</h1>
  <p v-if="isShow">Now you see me</p>
</template>
```
