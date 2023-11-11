# Lifecycle Hooks

https://vuejs.org/guide/essentials/lifecycle.html

* Lifecycle hooks allow us to add code at specific stages
* The most commonly hooks are `onMounted`, `onUpdated`, and `onUnmounted`

## onMounted

```vue
<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  console.log(`the component is now mounted.`)
})
</script>
```

## onUpdated

## onUnmounted
