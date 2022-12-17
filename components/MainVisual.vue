<template>
  <section id="main-visual">
    <div class="message">
      <h1>
        Hello
        <span class="period">.</span>
      </h1>
      <p>My name is Sou Hirawata.I'm a college student and heres is my portfolio.Have a look.</p>
    </div>
    <div class="visual">
      <img src="~/assets/img/main_visual.jpg" alt="main_visual" />
    </div>
  </section>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "MainVisual"
});
</script>

<style lang="scss" scoped>
#main-visual {
  display: flex;

  .message {
    width: 40%;
    margin: 0 auto;
    margin-top: 8%;
    margin-left: 10%;

    h1 {
      font-size: 150px;
      white-space: nowrap;
      font-family: Georgia, "Times New Roman", Times, serif;
      font-weight: 900;
      .period {
        font-size: 100px;
        color: #ff0000;
      }
    }
    p {
      color: #555555;
      font-size: 15px;
      line-height: 1.2;
      letter-spacing: 0.1em;
    }
  }

  .visual {
    width: 45%;
    margin-right: 7%;
    img {
      width: 100%;
    }
  }
}
</style>
