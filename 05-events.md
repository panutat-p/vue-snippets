# Events

https://vuejs.org/guide/essentials/event-handling.html

## Button event

```vue
<script setup>
import { ref } from 'vue'

const count = ref(0)
</script>

<template>
  <button v-on:click="count++">Add 1</button>
  <p>Count is: {{ count }}</p>
</template>
```
