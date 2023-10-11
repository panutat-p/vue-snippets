# Template

https://vuejs.org/guide/essentials/template-syntax.html

## Bind

```vue
<div v-bind:id="dynamicId"></div>
```

```vue
<button :disabled="isButtonDisabled">Button</button>
```

## If

```vue
<p v-if="isShow">Now you see me</p>
```

## On Click

```vue
<a v-on:click="doSomething"> ... </a>
```

## Form submit

```vue
<form @submit.prevent="onSubmit">...</form>
```
