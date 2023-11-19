# Events

https://vuejs.org/guide/essentials/event-handling.html

## Button event

```vue
<script setup lang="ts">
import { ref } from 'vue'

const count = ref<number>(0)
</script>

<template>
  <button v-on:click="count++">Add</button>
  <p>Count is: {{ count }}</p>
</template>
```
