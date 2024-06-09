<template>
  <div id="container">
    <a id="home" />
    <Header />
    <div id="main-vis">
      <MainVisual />
      <ScrollDown id="scroll-down" />
    </div>
    <a id="about" />
    <div id="about-view">
      <AboutView />
    </div>
    <a id="achieves" />
    <div id="achieves-view">
      <AchievesView />
    </div>
  </div>
</template>

<script lang="ts" setup>
</script>

<style>
  html {
    scroll-behavior: smooth;
  }

  #container {
    max-width: 2000px;
    margin: 0 auto;
    text-align: center;
  }

  #main-vis {
    position: relative;
    text-align: center;
    max-width: 1200px;
    height: 100vh;
    margin-left: auto;
    margin-right: auto;
  }

  #scroll-down {
    position: absolute;
    width: 100%;
    bottom: 30px;
  }

  #about-view {
    height: 100vh;
  }

  #achieves-view {
    height: auto;
  }

  @media (max-width: 1024px) {
    #main-vis {
      max-width: 900px;
    }
  }

  @media (max-width: 768px) {
    #main-vis {
      max-width: 700px;
    }
  }

  @media (max-width: 480px) {
    #main-vis {
      max-width: 90%;
    }
  }
</style>

