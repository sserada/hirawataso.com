<template>
  <Header />
  <v-container class="about">
    <h1>
      <span>Sou</span> Hirawata
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

  </v-container>
</template>

<script>
import Header from '@/components/Header.vue'

export default {
  name: 'About',
  components: {
    Header
  }
}
</script>

<style lang="scss" scoped>
.about {
  padding: 100px 100px;
  h1 {
    font-size: 4.0rem;
    font-weight: 700;
    margin-bottom: 40px;
    span {
      color: #ff4081;
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
