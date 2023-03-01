<template>
  <section id="about">
    <div class="title">
      <h2>
        About
        <span class="period">.</span>
      </h2>
    </div>

    <div class="profile">
      <v-avatar size="400px">
        <img src="~/assets/img/main_visual.jpg" alt="profile" />
      </v-avatar>
      <div class="profile-text">
        <h3>Sou Hirawata</h3>
        <p>I'm currently a third-year university student doing reseach on deep learning. I also do front-end development using Nuxt.js.</p>
        <TimeLine />
      </div>
    </div>

  </section>
</template>

<script lang="ts">
import Vue from "vue";
import TimeLine from "~/components/TimeLine.vue";

export default Vue.extend({
  name: "About",
  components: {
    TimeLine
  }
});
</script>

<style lang="scss" scoped>
#about {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  height: 100vh;
  .title {
    display: block;
    margin: 0 auto;
    margin-top: 7%;
    margin-left: 10%;
    h2 {
      padding-top: 8%;
      font-size: 50px;
      font-weight: 900;
      font-family: Georgia, "Times New Roman", Times, serif;

      .period {
        color: #ff0000;
      }
    }
  }
  .profile {
    margin-top: 6%;
    margin-left: 12%;
    width: 80%;
    display: flex;

    .v-avatar {
      width: 40%;
      height: 40%;
      margin-right: 5%;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }

    .profile-text {
      margin-top: 2%;
      h3 {
        font-size: 30px;
        font-weight: 900;
        font-family: Georgia, "Times New Roman", Times, serif;
      }
      p {
        color: #555555;
        font-size: 15px;
        line-height: 1.2;
        letter-spacing: 0.1em;
        margin-bottom: 5%;
      }
    }
  }
}
</style>
