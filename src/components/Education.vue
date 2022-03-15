<template>
  <v-container class="mt-10">
    <h2 class="text">Мое обучение</h2>
    <v-row>
      <v-col lg="6">
        <img alt="img" class="image" src="../assets/img/education-student.png">
      </v-col>
      <v-col class="mt-10" lg="6">
        <v-col lg="12">
          <v-card class="pa-6 rounded-xl " elevation="5">
            <div class="d-flex align-center justify-space-between">
              <div class="">
                <h3>TeachMeSkills</h3>
                <span>Апрель 2019 - Октябрь 2019</span>
              </div>
              <a href="https://teachmeskills.by/" target="_blank">
                <v-icon color="green">mdi-link</v-icon>
              </a>
            </div>
            <v-card-text>
              TeachMeSkills - это школа программирования, где учат востребованным сегодня знаниям. Все наши программы
              составлены Senior и Lead разработчиками ведущих IT компаний специально для новичков в IT.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col lg="12">
          <v-card class="pa-6 rounded-xl " elevation="5">
            <div class="d-flex align-center justify-space-between">
              <div class="">
                <h3>UDEMY</h3>
                <span>Сентябрь 2019 - По настоящее время</span>
              </div>
              <a href="https://www.udemy.com/" target="_blank">
                <v-icon color="green">mdi-link</v-icon>
              </a>
            </div>
            <v-card-text>
              Udemy
              Открытый онлайн-провайдер курсов,ориентированный на взрослых профессионалов и студентов.По состоянию на
              сентябрь 2022 насчитывает 175 000 курсов.
            </v-card-text>
          </v-card>
        </v-col>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Education"
}
</script>

<style scoped>
.image {
  margin-top: 5rem;
  width: 100%;
}

.text {
  margin-top: 2rem;
  padding-top: 5rem;
  font-size: 40px;
  font-family: cursive;
  font-weight: 700;
}
</style>
