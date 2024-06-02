<template>
  <div id="container">
    <Header />
    <div id="main-vis">
      <MainVisual />
      <ScrollDown />
    </div>
  </div>
</template>

<script lang="ts" setup>
</script>

<style>
  #container {
    height: 100%;
    text-align: center;
  }

  #main-vis {
    text-align: center;
    max-width: 1200px;
    height: auto;
    margin-left: auto;
    margin-right: auto;
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

