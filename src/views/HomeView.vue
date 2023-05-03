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
          Here is my portfolio site.
        </p>
        <p>
          Have a look around!
        </p>
      </v-col>
      <v-col>
        <img src="@/assets/img/my-face.png" alt="Sou Hirawata">
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
  max-width: 1300px;
  height: 95%;
  text-align: center;
  margin: 0 auto;
  padding-top: 100px;
  .v-row {
    height: 100%;
    .v-col {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      img {
        width: 100%;
        border-radius: 50%;
        margin-right: 220px;
      }
      h1 {
        z-index: 1;
        color: #A7A7A7;
        font-size: 7rem;
        margin-left: 140px;
        .period {
          color: #888;
        }
      }
      p {
        z-index: 1;
        color: #666;
        font-size: 1.2rem;
        font-family: 'Playfair Display', serif;
        margin-left: 140px;
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
    max-width: 500px;
    max-height: 1000px;
    .v-row {
      flex-direction: column-reverse;
      position: relative;
      .v-col {
        img {
          position: absolute;
          top: 50px;
          width: 80%;
          margin: 0;
        }
        h1 {
          font-size: 3rem;
          margin: 0;
        }
        p {
          font-size: 0.8rem;
          max-width: 250px;
          margin: 0;
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
