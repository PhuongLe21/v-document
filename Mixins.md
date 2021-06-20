### Mixins

#### Basics

Mixins is a way to re-use code for Vue components.
When a component uses a mixin, all options in the mixin will be "mixed" into the component's own options

#### Option Mergings

- The component's options will take priority.
- Hook functions with the same name are merged into an array

#### Global Mixin

```
Vue.mixin({
    //
})
```

It affects every Vue instance
