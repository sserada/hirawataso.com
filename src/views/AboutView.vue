<template>
  <Header />
  <v-container class="about">
    <h1>
      <span>Sou</span> Hirawata
      <v-btn class="btn github" href="https://github.com/fightingsou" target="_blank">
        <v-icon>mdi-github</v-icon>
      </v-btn>
      <v-btn class="btn twitter" href="https://twitter.com/fightingsou" target="_blank">
        <v-icon>mdi-twitter</v-icon>
      </v-btn>
    </h1>
    <v-row>
      <v-col sm="3">
        <img src="@/assets/img/myface.jpg" alt="myface" />
      </v-col>
      <v-col sm="9">
        <p>
          This is my face 18 years ago. Where has the cuteness of those days gone?
          <br>
          I am now a junior at the university.
          In university, I majored in computer science and am doing research on automatic composition.
          I also enjoy competitive programming and web development.
        </p>
      </v-col>
    </v-row>
    <History />
    <Works />
  </v-container>
  <Footer />
</template>

<script>
import Header from '@/components/Header.vue'
import History from '@/components/History.vue'
import Footer from '@/components/Footer.vue'
import Works from '@/components/Works.vue'

export default {
  name: 'About',
  components: {
    Header,
    History,
    Footer,
    Works
  }
}
</script>

<style lang="scss" scoped>
.about {
  padding: 100px 100px;
  h1 {
    font-size: 3.4rem;
    font-weight: 700;
    margin-bottom: 40px;
    span {
      color: #ff4081;
    }
    .btn {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      font-size: 1.2rem;
      box-shadow: 0 0 5px rgba(0, 0, 0, 0);
      transition: all 0.3s;
      &:hover {
        background-color: #ff4081;
        color: #fff;
      }
      &.github {
        color: #333;
      }
      &.twitter {
        color: #1da1f2;
      }
    }
  }
  p {
    font-size: 1.3rem;
    font-weight: 300;
    font-family: 'Playfair Display', serif;
    color: #666;
    margin-top: 40px;
  }
  img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
  }
}
</style>
