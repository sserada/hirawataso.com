<template>
  <Header />
  <v-container>
    <v-row>
      <v-col>
        <h1>Hello<span class="period">.</span></h1>
        <p>
          I'm So Hirawata, a university student in Japan.
        </p>
        <p>
          Here is my portfolio site. Have a look around!
        </p>
        <div class="btns">
          <v-btn class="btn github" href="https://github.com/fightingsou" target="_blank">
            <v-icon>mdi-github</v-icon>
          </v-btn>
          <v-btn class="btn twitter" href="https://twitter.com/fightingsou" target="_blank">
            <v-icon>mdi-twitter</v-icon>
          </v-btn>
        </div>
      </v-col>
      <v-col>
        <img src="@/assets/img/profile.png" alt="Sou Hirawata">
      </v-col>
    </v-row>
  </v-container>
  <Footer />
</template>

<script>
import { defineComponent } from 'vue';
import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue';

export default defineComponent({
  name: 'HomeView',

  components: {
    Header,
    Footer,
  },
});
</script>

<style lang="scss" scoped>
.v-container {
  max-width: 1000px;
  height: 95%;
  text-align: center;
  margin: 0 auto;
  padding-top: 70px;
  .v-row {
    height: 100%;
    .v-col {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      img {
        width: 500px;
        height: 500px;
        border-radius: 50%;
        margin-bottom: 20px;
      }
      h1 {
        font-size: 5rem;
        .period {
          color: #ff4081;
        }
      }
      p {
        color: #666;
        font-size: 1.1rem;
        font-family: 'Playfair Display', serif;
      }
      .btn {
        box-shadow: 0 0 0 0;
        border-radius: 50%;
        width: 60px;
        height: 60px;
        margin-top: 10px;
        &:hover {
          background-color: #eee;
          box-shadow: 0 0 0 0;
        }
        .v-icon {
          font-size: 2rem;
          &.mdi-twitter {
            color: #1da1f2;
          }
        }
      }
    }
  }
}

@media screen and (max-width: 768px) {
  .v-container {
    .v-row {
      flex-direction: column-reverse;
      position: relative;
      .v-col {
        img {
          position: absolute;
          top: 70px;
          width: 350px;
          height: 350px;
        }
        h1 {
          font-size: 3rem;
        }
        p {
          font-size: 1rem;
          max-width: 250px;
        }
        .btn {
          width: 40px;
          height: 40px;
          .v-icon {
            font-size: 1.5rem;
          }
        }
      }
    }
  }
}
</style>
