<script>
  import anime from 'animejs/lib/anime.es.js';

  export default {
    name: 'AboutPage',
    mounted() {
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            anime({
              targets: '#about-container',
              opacity: [0, 1],
              duration: 1000,
              easing: 'easeInOutQuad'
            });
          } else {
            anime({
              targets: '#about-container',
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
  <div id="about-container">
    <div id="about-header">
      <h1>About</h1>
    </div>
    <div id="about-content">
      <div>
        <h2>平綿 素望 <span>So Hirawata</span></h2>
        <p>東京都市大学大学院 環境情報学研究科 環境情報学専攻 1年</p>
        <p>海洋研究開発機構 付加価値情報創生部門 地球情報科学センター 臨時研究補助員</p>
        <p class="en">Student at Tokyo City University</p>
        <p>Research Assistant at Japan Agency for Marine-Earth Science and Technology</p>
        <div class="icons">
          <a target="_brank" href="https://github.com/fightingso"><i class="fab fa-github"></i></a>
          <a target="_brank" href="https://x.com/fightingsou"><i class="fab fa-twitter"></i></a>
          <a target="_brank" href="https://instagram.com/hirawataso"><i class="fab fa-instagram"></i></a>

        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Noto+Serif+JP:wght@200..900&display=swap');

  #about-container {
    height: 100%;
    opacity: 0;
  }

  #about-header {
    padding-top: 200px;
  }

  #about-content {
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

  @media (min-width: 1000px) and (min-height: 1500px) {
    #about-header {
      padding-top: 50%;
    }
  }

  @media (max-width: 768px) {
    #about-container {
      padding: 0;
    }

    #about-content {
      width: 80%;
    }

    #about-header {
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
