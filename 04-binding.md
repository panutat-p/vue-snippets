# Binding

https://vuejs.org/guide/essentials/class-and-style.html

## ref

```vue
<script setup lang="ts">
import { ref } from 'vue';

const isHighlighted = ref<boolean>(false);

const textClass = ref('normal-text');

const toggleClass = () => {
  isHighlighted.value = !isHighlighted.value;
  textClass.value = isHighlighted.value ? 'highlighted-text' : 'normal-text';
};
</script>

<template>
  <div>
    <button @click="toggleClass">Toggle Class</button>
    <p :class="textClass">Hello, Vue with Composition API!</p>
  </div>
</template>

<style scoped>
.normal-text {
  color: white;
  font-size: 25px;
}

.highlighted-text {
  color: red;
  font-weight: bold;
  font-size: 50px;
}
</style>

```

## reactive

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
