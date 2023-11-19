# Lifecycle Hooks

https://vuejs.org/guide/essentials/lifecycle.html

* Lifecycle hooks allow us to add code at specific stages
* The most commonly hooks are `onMounted`, `onUpdated`, and `onUnmounted`

## onMounted

```vue
<script setup lang="ts">
import { onMounted } from 'vue'

onMounted(() => {
  alert('hello')
})
</script>
```

## onUpdated

## onUnmounted
