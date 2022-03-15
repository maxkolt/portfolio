<template>
  <v-container>
    <v-row justify="center">
      <v-col class="text-center" lg="12">
        <h2 class="text justify-center">Мои навыки</h2>
      </v-col>
    </v-row>
    <div class="mb-10">
      <h6>HTML</h6>
      <v-progress-linear
          buffer-value="0"
          color="orange darken-4"
          stream
          value="93"
      ></v-progress-linear>
      <br>
      <h6>CSS</h6>
      <v-progress-linear
          buffer-value="0"
          color="deep-purple accent-4"
          stream
          value="85"
      ></v-progress-linear>
      <br>
      <h6>JS</h6>
      <v-progress-linear
          buffer-value="80"
          color="yellow accent-3"
          stream
          value="75"
      ></v-progress-linear>
      <br>
      <h6>VUE</h6>
      <v-progress-linear
          buffer-value="76"
          color="teal lighten-1"
          stream
          value="65"
      ></v-progress-linear>
      <br>
      <h6>TypeScript</h6>
      <v-progress-linear
          buffer-value="87"
          color="cyan darken-3"
          stream
          value="73"
      ></v-progress-linear>
    </div>
  </v-container>
</template>

<script>

export default {
  name: "Skills"

}
</script>

<style lang="scss">
.text {
  margin-top: 5rem;
  font-size: 40px;
  font-family: cursive;
  font-weight: 700;
  color: #444444;
}

.mb-10 {
  margin-top: 4rem;
  font-size: 40px;
}
</style>
