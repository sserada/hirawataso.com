<template>
  <v-app dark>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>

<style>
.v-application--wrap {
  background-color: #eee;
  padding-top: 0;
  min-height: 100vh;
}
</style>
