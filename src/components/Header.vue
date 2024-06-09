<template>
  <div>
    <header>
      <div class="menu-icon" @click="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
      </div>
      <ul :class="{ open: menuOpen }">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#achieves">Achievements</a></li>
        <li><a href="#blog">Blog</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </header>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');

header {
  position: fixed;
  padding: 20px 100px;
  display: flex;
  width: 100%;
  justify-content: flex-end;
  align-items: center;
  z-index: 100;
}

.menu-icon {
  display: none;
  flex-direction: column;
  cursor: pointer;
}

.menu-icon span {
  width: 30px;
  height: 3px;
  background-color: #eee;
  margin: 4px 0;
  transition: all 0.3s ease;
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

@media (max-width: 768px) {
  header {
    padding: 20px;
  }

  .menu-icon {
    display: flex;
    opacity: 0.7;
    z-index: 10;
  }

  ul {
    position: fixed;
    top: 0;
    right: 0;
    flex-direction: column;
    background-color: #222;
    width: 100%;
    height: 100vh;
    transform: translateX(100%);
    transition: transform 0.5s ease;
    z-index: 9;
    overflow-y: auto;
  }

  ul.open {
    transform: translateX(0);
  }

  li {
    text-align: center;
    padding: 10px;
  }

  li:first-child {
    margin-top: 100px;
  }

  a {
    font-size: 24px;
  }
}
</style>
