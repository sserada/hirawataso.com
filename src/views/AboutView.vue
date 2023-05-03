<template>
  <Header />
  <v-container class="about">
    <h1>
      So Hirawata
    </h1>
    <v-row>
      <v-col cols="12" md="5">
        <img src="../assets/img/my-face.png" alt="so" />
      </v-col>
      <v-col cols="12" md="7">
        <p>
          東京都市大学メディア情報学部4年生．修士課程進学予定．
          <br />
          自動作曲に関する研究をしています．
          <br />
          <br />
          2018年4月 ~ 2020年3月 日本大学藤沢高等学校
          <br />
          2020年4月 ~ 現在 東京都市大学 メディア情報学部 情報システム学科
          <br />
          2022年9月 ~ 現在 株式会社SQIP アルバイト
          <br />
          <br />
          GitHub : <a href="https://github.com/fightingsou">fightingsou</a>
          <br />
          Twitter : <a href="https://twitter.com/fightingsou">fightingsou</a>
        </p>
      </v-col>
    </v-row>
  </v-container>
  <Footer />
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'About',
  components: {
    Header,
    Footer,
  }
}
</script>

<style lang="scss" scoped>
.about {
  max-width: 1200px;
  height: 90%;
  padding: 100px 100px;
  h1 {
    color: #A7A7A7;
    font-size: 5.5rem;
    font-weight: 700;
    margin-top: 30px;
    width: 100%;
  }
  p {
    font-size: 1.0rem;
    font-family: 'Playfair Display', serif;
    color: #666;
    margin-top: 80px;
  }
  a {
    color: #666;
    text-decoration: none;
    &:hover {
      color: #666;
      text-decoration: underline;
    }
  }
  img {
    width: 300px;
    height: 300px;
    border-radius: 50%;
    margin-top: 40px;
    margin-left: 60px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
  }
}

@media screen and (max-width: 768px) {
  .about {
    padding: 100px 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
    h1 {
      font-size: 3.0rem;
      .btn {
        width: 50px;
        height: 50px;
        font-size: 1rem;
      }
    }
  }
  img {
    width: 200px;
    height: 200px;
    margin: 0 auto;
  }
}
</style>
