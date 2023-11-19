# Binding

https://vuejs.org/guide/essentials/class-and-style.html

## Class binding

```vue
<script setup lang="ts">
import { ref } from 'vue'

const isRed = ref<boolean>(true)
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

```vue
<script setup lang="ts">
import { reactive } from 'vue'

const titleStyle = reactive({
  color: 'yellow',
  fontSize: '50px',
})
</script>

<template>
  <div>
    <h1 v-bind:style="titleStyle">Hello</h1>
  </div>
</template>
```
