<template>
  <header class="header">
    <nav class="nav">
      <ul class="nav__list">
        <li class="nav__item">
          <a class="nav__link" href="/">Home</a>
        </li>
        <li class="nav__item">
          <a class="nav__link" href="/about">About</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
export default ({
  name: 'Header',
});
</script>

<style lang="scss" scoped>
.header {
  padding: 1rem;
}

.nav__list {
  display: flex;
  list-style: none;
  padding: 0;
  margin: 0;
}

.nav__item {
  margin-right: 1rem;
}

.nav__link {
  color: #555;
  font-family: sans-serif;
  text-decoration: none;
  transition: color 0.3s;
}

.nav__link:hover {
  color: #ccc;
}
</style>
