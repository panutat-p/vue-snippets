# Reactivity

## `ref`

https://vuejs.org/guide/essentials/reactivity-fundamentals.html#why-refs

* For primitive types
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

## `reactive`

https://vuejs.org/guide/essentials/reactivity-fundamentals.html#reactive

* For object types
* Deep conversion, nested objects are also wrapped
* `reactive()` return a `Proxy` of the original object, which is not equal to the original object
* Destructure will lose the reactivity connection

```vue
<script setup>
import { reactive } from 'vue'

const state = reactive({ count: 0 })

function increment() {
  count++
}
</script>

<template>
  <button v-on:click="increment">
    {{ count }}
  </button>
</template>
```

## `shallowReactive`

https://vuejs.org/api/reactivity-advanced.html#shallowreactive

* For object types
* No deep conversion, only root-level properties are reactive

```vue
<script setup>
import { shallowReactive } from 'vue'

const state = shallowReactive({ count: 0 })

function increment() {
  count++
}
</script>

<template>
  <button v-on:click="increment">
    {{ count }}
  </button>
</template>
```
