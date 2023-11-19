# Rendering

## Text Interpolation

https://vuejs.org/guide/essentials/template-syntax.html

```vue
<script setup>
import { ref } from 'vue'

const msg = ref("Hello Vue")
const num = ref(43)
</script>

<template>
  <h1>{{ msg }}</h1>
  <h1>{{ num }}</h1>
</template>
```

## Conditional Rendering

https://vuejs.org/guide/essentials/conditional.html

```vue
<script setup>
import { ref } from 'vue'

const toggle = ref(true)
</script>

<template>
  <h1 v-if="toggle">isShow is true</h1>
  <h1 v-else>isShow is false</h1>
  <button v-on:click="toggle=!toggle">
    Change
  </button>
</template>
```

## List Rendering

https://vuejs.org/guide/essentials/list.html

```vue
<script setup>
import { ref } from 'vue'

const items = ref(
  [
    { message: 'Foo' },
    { message: 'Bar' },
  ]
)
</script>

<template>
  <li v-for="item in items">
    {{ item.message }}
  </li>
</template>
```
