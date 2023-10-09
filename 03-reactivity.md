# Reactivity

https://vuejs.org/guide/essentials/reactivity-fundamentals.html

* When a component is rendered for the first time, Vue tracks every `ref`
* When a `ref` is mutated, it will trigger a re-render for components that are tracking it.
* Vue automatically detects the change and updates the DOM accordingly

```vue
<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  count.value++
}
</script>

<template>
  <button v-on:click="increment">
    {{ count }}
  </button>
</template>
```
