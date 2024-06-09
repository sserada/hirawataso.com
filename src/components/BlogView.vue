<script>
  import anime from 'animejs/lib/anime.es.js';
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

  export default {
    name: 'BlogPage',
    mounted() {
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            anime({
              targets: '#blog-container',
              opacity: [0, 1],
              duration: 1000,
              easing: 'easeInOutQuad'
            });
          } else {
            anime({
              targets: '#blog-container',
              opacity: [1, 0],
              duration: 1000,
              easing: 'easeInOutQuad'
            });
          }
        });
      }, { threshold: 0.1 });

      observer.observe(this.$el);
    }
  }
</script>

<template>
  <div id="blog-container">
    <div id="blog-header">
      <h1>Blog</h1>
    </div>
    <div id="blog-content">
      <h3>Under Construction</h3>
    </div>
  </div>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Noto+Serif+JP:wght@200..900&display=swap');

  #blog-container {
    height: 100%;
    opacity: 0;
  }

  #blog-header {
    padding-top: 200px;
  }

  #blog-content {
    width: 60%;
    text-align: center;
    margin: 0 auto;
    height: auto;
  }

  h1 {
    font-size: 100px;
    font-family: 'Great Vibes', cursive;
    color: #ff6347;
    opacity: 0.3;
  }

  h2 {
    font-family: "Noto Serif JP", serif;
    font-size: 30px;
    opacity: 0.8;
    margin-top: 40px;
    margin-bottom: 30px;
  }

  span {
    font-size: 20px;
    opacity: 0.4;
  }

  p {
    font-family: "Noto Serif JP", serif;
    opacity: 0.7;
  }

  .en {
    margin-top: 50px;
  }

  .icons {
    display: flex;
    justify-content: center;
    margin-top: 3vh;
  }

  .icons a {
    font-size: 1.5rem;
    color: #aaa;
    margin: 0 1vw;
  }

  .icons a:hover {
    color: #ff6347;
    transition: 0.3s;
  }

  @media (max-width: 768px) {
    #blog-container {
      padding: 0;
    }

    #blog-content {
      width: 80%;
    }

    #blog-header {
      padding-top: 40%;
    }

    h1 {
      font-size: 80px;
    }

    h2 {
      font-size: 30px;
    }

    span {
      font-size: 20px;
    }

    p {
      font-size: 14px;
    }

    .icons a {
      font-size: 1.4rem;
      margin: 0 5vw;
      padding-bottom: 30%;
    }
  }
</style>
