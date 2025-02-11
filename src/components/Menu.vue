<template>
  <nav>
    <ul>
      <li v-for="link in links" :key="link.to">
        <router-link :to="link.to">{{ link.text }}</router-link>
      </li>
    </ul>
  </nav>
</template>

<script setup>
const links = [
  { to: '/', text: 'Lists' },
  { to: '/usual-list', text: 'Usual' },
  { to: '/default-example', text: 'Virtual Example' },
  { to: '/virtual-list-types', text: 'Virtual Types' },
  { to: '/custom-virtual-scroll', text: 'Custom Dynamic' },
  { to: '/vuetify', text: 'Vuetify Dynamic' },
  { to: '/recycle-scroll', text: 'Recycle Scroll' },
  { to: 'pros', text: 'Pros' },
  { to: 'cons', text: 'Cons' },
]
</script>

<style lang="scss" scoped>
nav {
  padding: 1rem;
}

ul {
  list-style: none;
  padding: 0;
  display: flex;
  justify-content: space-evenly;
  gap: 1rem;
}

li {
  margin: 0;
}

a {
  text-decoration: none;
  color: #000000;
}

a:hover {
  font-weight: bold;
}
</style>
