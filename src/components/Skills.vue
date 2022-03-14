<template>
  <v-container class="mt-10">
    <v-row justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text justify-center">Мои навыки</v-subheader>
      </v-col>
    </v-row>
    <div class="mb-10">
      <h6>HTML</h6>
      <v-progress-linear
          color="orange darken-4"
          buffer-value="0"
          value="93"
          stream
      ></v-progress-linear>
      <br>
      <h6>CSS</h6>
      <v-progress-linear
          color="deep-purple accent-4"
          buffer-value="0"
          value="85"
          stream
      ></v-progress-linear>
      <br>
      <h6>JS</h6>
      <v-progress-linear
          color="yellow accent-3"
          buffer-value="80"
          value="75"
          stream
      ></v-progress-linear>
      <br>
      <h6>VUE</h6>
      <v-progress-linear
          color="teal lighten-1"
          buffer-value="76"
          value="65"
          stream
      ></v-progress-linear>
      <br>
      <h6>TypeScript</h6>
      <v-progress-linear
          color="cyan darken-3"
          buffer-value="87"
          value="73"
          stream
      ></v-progress-linear>
    </div>
  </v-container>
</template>

<script>

export default {
  name: "Skills"

}
</script>

<style scoped>
.text {
  margin-top: 5rem;
  font-size: 40px;
  font-family: cursive;
  font-weight: 700;
}

.mb-10 {
  margin-top: 5rem;
  font-size: 40px;
}
</style>
