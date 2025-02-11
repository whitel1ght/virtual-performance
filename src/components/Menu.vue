<template>
  <nav>
    <ul>
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/pros">About</router-link></li>
      <li><router-link to="/cons">Contact</router-link></li>
    </ul>
  </nav>
</template>

<script setup>
</script>

<style scoped>
nav {
  background-color: #f8f9fa;
  padding: 1rem;
}

ul {
  list-style: none;
  padding: 0;
  display: flex;
  gap: 1rem;
}

li {
  margin: 0;
}

a {
  text-decoration: none;
  color: #007bff;
}

a:hover {
  text-decoration: underline;
}
</style>
