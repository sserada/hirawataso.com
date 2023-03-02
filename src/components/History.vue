<template>
  <v-timeline direction="horizontal">
    <v-timeline-item>
      <template v-slot:opposite>
        ~2020
      </template>
      <div>
        <div class="text-h6">Nihon University Fujisawa High School</div>
        <p>
          I was a member of the tennis club and served as vice president.
        </p>
      </div>
    </v-timeline-item>

    <v-timeline-item>
      <template v-slot:opposite>
        2020~
      </template>
      <div>
        <div class="text-h6">Tokyo City University</div>
        <p>
          I majored in computer science at university.
          And, I was the president of a tennis club until last year, and I am currently a member of the Otani Laboratory, where I am doing research on automatic composition.
        </p>
      </div>
    </v-timeline-item>
  </v-timeline>
</template>

<script>
export default {
  name: 'History',
};
</script>

<style lang="scss" scoped>
.v-timeline {
  color: #666;
  font-family: 'Playfair Display', serif;
  padding-top: 60px;
  background-color: #fff;
  margin: 0 auto;
  max-width: 800px;
  position: relative;
  width: 100%;
}
</style>
