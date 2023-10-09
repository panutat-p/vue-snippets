# Reactivity

## `ref`

https://vuejs.org/guide/essentials/reactivity-fundamentals.html#why-refs

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

## `reactive`

https://vuejs.org/guide/essentials/reactivity-fundamentals.html#reactive

* Converts the object deeply
* `reactive()` return a `Proxy` of the original object, which is not equal to the original object
* Only works for object types: array, map, set, object
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

* Only root-level properties are reactive
