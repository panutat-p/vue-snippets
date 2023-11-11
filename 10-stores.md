# Stores

We keep on building our store from scratch.
We will use `effectScope` to properly collect all the effects associated to a store.
* `effectScope()` can be disposed by a component
* `effectScope(true)` cannot be disposed by a component

```typescript
import { effectScope } from 'vue'

let effect
let count

function useCount() {
  if (!effect) {
    count = effectScope(true).run(() => ref(0))
  }
  return { count }
}
```
