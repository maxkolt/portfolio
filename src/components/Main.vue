<template class="">
  <v-container class="mt-16">
    <v-row>
      <v-col lg="6">
        <h2 class="intro-text">Привет! Я Frontend-разработчик</h2>
        <p class="description">В настоящее время фрилансер.
          Вы можете увидеть меня на GitHub,
          а так-же несколько моих работ с кодом.
        </p>
        <v-btn class="white--text mr-7" color="red lighten-1" href="https://github.com/maxkolt?tab=repositories"
               rounded target="_blank">
          <v-icon left size="20">mdi-github</v-icon>
          GitHub
        </v-btn>
        <v-btn class="white--text" color="teal lighten-2" rounded>
          <v-icon left>mdi-cloud-upload</v-icon>
          Скачать резюме
        </v-btn>
      </v-col>
      <v-col lg="6">
        <img alt="img" src="../assets/img/Web-Design-Development.png" width="100%"/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Main"
}
</script>

<style lang="scss">
.intro-text {
  font-size: 50px;
  line-height: 4rem;
  font-weight: bold;
  font-family: cursive;
  color: #444444;
  margin-top: 10rem;
}

p.description {
  font-size: 19px;
  font-family: cursive;
  margin: 30px 0;
  color: #444444ba;
}
</style>
