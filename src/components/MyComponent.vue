<template>
  <v-container class="mt-16">
    <v-row>
      <v-col lg="6">
        <h2 class="intro-text">Привет! Я Frontend-разработчик</h2>
        <p class="description">В настоящее время фрилансер.
          Вы можете увидеть меня на GitHub,
          а так-же несколько моих работ с кодом.
          </p>
        <v-btn target="_blank" href="https://github.com/maxkolt?tab=repositories" class="white--text mr-7" color="red lighten-1" rounded>
          <v-icon left size="20">mdi-github</v-icon>
          GitHub
        </v-btn>
        <v-btn color="teal lighten-2" class="white--text" rounded>
          <v-icon left>mdi-cloud-upload</v-icon>
          Скачать резюме
        </v-btn>
      </v-col>
      <v-col lg="6">
        <img width="100%" src="../assets/img/Web-Design-Development-PNG-Image-1024x872.png" alt="img"/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "MyComponents"
}
</script>

<style scoped>
h2.intro-text{
  font-size: 50px;
  line-height: 3rem;
  font-weight: bold;
  font-family: cursive;
  color: #444;
  margin-top: 7rem;
}
p.description{
  font-size: 19px;
  font-family: cursive;
  margin: 30px 0;
  color: #444444ba;
}
</style>
