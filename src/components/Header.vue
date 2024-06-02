<template>
  <header>
    <ul>
      <li><a href="#">About</a></li>
      <li><a href="#">Works</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </header>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');

  header {
    position: absolute;
    margin-top: 10px;
    right: 0;
    padding: 10px 50px;
  }

  ul {
    display: flex;
    gap: 50px;
    padding: 0;
    margin: 0;
  }

  li {
    list-style: none;
  }

  a {
    text-decoration: none;
    font-family: 'Great Vibes', cursive;
    font-size: 24px;
    color: #eee;
    transition: color 0.3s ease, transform 0.3s ease;
  }

  a:hover {
    color: #ff6347;
    transform: scale(1.1);
  }
</style>

