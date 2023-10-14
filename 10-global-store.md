# Global Stores

We keep on building our store from scratch.
We will use `effectScope()`` to properly collect all the reactive effects associated to a store.

```typescript
import { effectScope } from 'vue'

let effect
let count

function useCount() {
  if (!effect) {
    count = effectScope().run(() => ref(0))
  }
  return { count }
}
```
