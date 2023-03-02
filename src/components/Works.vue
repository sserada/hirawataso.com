<template>
  <v-container>
    <v-row>
      <v-col>
        <v-card class="mx-auto" max-width="344">
          <v-img src="https://fightingsou.github.io/images/works.png" height="270px" cover></v-img>
          <div class="margin">
          </div>
        </v-card>
      </v-col>
      <v-col>
        <v-card class="mx-auto" max-width="344">
          <v-img src="https://fightingsou.github.io/images/portfolio.png" height="150px" cover></v-img>
          <v-card-title>
            Portfolio Site
          </v-card-title>
          <v-card-subtitle>
            Here.
          </v-card-subtitle>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn
              :icon="show1 ? 'mdi-chevron-up' : 'mdi-chevron-down'"
              @click="show1 = !show1"
            ></v-btn>
          </v-card-actions>
          <v-expand-transition>
            <div v-show="show1">
              <v-divider></v-divider>
              <v-card-text>
                This is my portfolio site, created using Vue.js.<br>
                <a href="https://github.com/fightingsou/my-portfolio/tree/master">GitHub</a>
              </v-card-text>
            </div>
          </v-expand-transition>
        </v-card>
      </v-col>
      <v-col>
        <v-card class="mx-auto" max-width="344">
          <v-img src="https://fightingsou.github.io/images/thinker.jpg" height="150px" cover></v-img>
          <v-card-title>
            The Thinker
          </v-card-title>
          <v-card-subtitle>
            A web application for environmental issues.
          </v-card-subtitle>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn
              :icon="show2 ? 'mdi-chevron-up' : 'mdi-chevron-down'"
              @click="show2 = !show2"
            ></v-btn>
          </v-card-actions>
          <v-expand-transition>
            <div v-show="show2">
              <v-divider></v-divider>
              <v-card-text>
                A web application that aims to raise questions about current perceptions of environmental issues.
                The presentation won the third place in the SD PBL course held at the university.
                Developed with Nuxt.js.<br>
                <a href="https://github.com/fightingsou/the-thinker">GitHub</a>
              </v-card-text>
            </div>
          </v-expand-transition>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Works',
  data: () => ({
    show1: false,
    show2: false,
  }),
}
</script>

<style lang="scss" scoped>
.v-card {
  margin-top: 40px;
  box-shadow: 0 1px 2px 2px rgba(0, 0, 0, 0.1);
  .margin {
    margin-top: 12px;
  }
  a {
    text-decoration: none;
    color: #3f51b5;
  }
}
</style>
