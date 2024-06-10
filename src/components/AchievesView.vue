<script>
  import anime from 'animejs/lib/anime.es.js';

  export default {
    name: 'AchievesPage',
    mounted() {
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            anime({
              targets: '#achieves-container',
              opacity: [0, 1],
              duration: 1000,
              easing: 'easeInOutQuad'
            });
          } else {
            anime({
              targets: '#achieves-container',
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
  <div id="achieves-container">
    <div id="achieves-header">
      <h1>Achievements</h1>
    </div>
    <div id="achieves-content">
      <h2>Projects</h2>
      <ProjectsView />
      <h2>Publications</h2>
      <PublicationsView />
      <h2>Presentations</h2>
      <PresentationsView />
    </div>
  </div>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Noto+Serif+JP:wght@200..900&display=swap');

  #achieves-container {
    opacity: 0;
  }

  #achieves-header {
    padding-top: 100px;
  }

  #achieves-content {
    width: 90%;
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
    font-family: 'Great Vibes', cursive;
    font-size: 30px;
    opacity: 0.6;
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

  @media (max-width: 768px) {
    #achieves-container {
      padding: 0;
    }

    #achieves-content {
      width: 100%;
    }

    #achieves-header {
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
