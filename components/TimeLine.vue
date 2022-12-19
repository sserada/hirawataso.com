<template>
      <v-timeline
        align-top
        dense
      >
        <v-timeline-item
          color="white"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3">
              <strong>Now</strong>
            </v-col>
            <v-col>
              <strong>OtaniLab</strong>
            </v-col>
          </v-row>
        </v-timeline-item>

        <v-timeline-item
          color="white"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3">
              <strong>Now</strong>
            </v-col>
            <v-col>
              <strong>SQIP Inc.</strong>
            </v-col>
          </v-row>
        </v-timeline-item>

        <v-timeline-item
          color="white"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3">
              <strong>2020~</strong>
            </v-col>
            <v-col>
              <strong>Tokyo City University</strong>
            </v-col>
          </v-row>
        </v-timeline-item>

        <v-timeline-item
          color="white"
          small
        >
          <v-row class="pt-1">
            <v-col cols="3">
              <strong>~2020</strong>
            </v-col>
            <v-col>
              <strong>Nihon University Fujisawa High School</strong>
            </v-col>
          </v-row>
        </v-timeline-item>
      </v-timeline>
</template>

<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
  name: 'TimeLine',
})
</script>
