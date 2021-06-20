### Slot
```
<navigation-link url="/profile">
  Your Profile
</navigation-link>

=> template for <navigation-link>
<a v-bind:href="url">
  <slot></slot>
</a>

```
#### Default content
#### Named Slot
```
<div class="container">
  <header>
    <slot name="header"></slot>
  </header>
  <footer>
    <slot name="footer"></slot>
  </footer>
</div>
```
To provide content to named slots, we can use the v-slot directive on a <template>
```
  <template v-slot:header>
    <h1>Here might be a page title</h1>
  </template>

  <template v-slot:footer>
    <p>Here's some contact info</p>
  </template>

```

#### Scoped slot
- Khi parent component muon access bien trong child component thì:
child component: 
```
<template>
  <span>
    <slot v-bind:user1="user">
      {{ user.lastName }}
    </slot>
  </span>
<template>

data() {
  return {
    user: {
      lastName: 'Le',
      firstName: 'Phuong'
    }
  }
}

```
parent component:
```
<template>
  <span>
    <template v-slot:default="slopProps">
      {{ slopProps.user1.firstName }}
    </template>
  </span>
<template>

data() {
  return {
    // no data
  }
  }
}
```

=> Nó sẽ nhận {{ slopProps.user1.firstName }} từ cha => giá trị là Phương