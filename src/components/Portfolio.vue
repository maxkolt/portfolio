<template>
  <v-container class="my-10">
    <v-row justify="center">
      <v-col class="text-center" lg="12">
        <h2 class="text justify-center">Моё портфолио</h2>
        <p style="font-family: cursive">Вашему вниманию представлены несколько моих работ, а также сертификаты об окончании обучения</p>
      </v-col>
      <v-col lg="12">
        <div class="text-center">
          <v-chip
              :color="activePortfolio === 'certificate' ? 'red lighten-1' : ''"
              class="ma-2"
              outlined
              @click="activePortfolio = 'certificate'"
          >
            Сертификаты
            <v-icon right>
              mdi-account-outline
            </v-icon>
          </v-chip>

          <v-chip
              :color="activePortfolio === 'webapp' ? 'teal lighten-1' : '' "
              class="ma-2"
              outlined
              @click="activePortfolio = 'webapp'"
          >
            <v-icon left>
              mdi-server-plus
            </v-icon>
            Проекты
          </v-chip>
        </div>
      </v-col>

      <slot v-if="activePortfolio === 'certificate' ">
        <v-col v-for="(certificat, certificatindex) in certificateApps" :key="certificatindex" lg="3">
          <v-card>
            <v-img
                :src="certificat.image"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                height="200px"
            >
              <v-card-title>{{ certificat.title }}</v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </slot>
      <slot v-if="activePortfolio === 'webapp' ">
        <v-col v-for="(web, webindex) in webApps" :key="webindex" lg="3">
          <v-card>
            <v-img
                :src="web.image"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                height="200px"
            >
              <v-card-title>{{ web.title }}</v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </slot>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Portfolio",
  data() {
    return {
      activePortfolio: 'certificate',
      certificateApps: [
        {title: '', image: 'https://udemy-certificate.s3.amazonaws.com/image/UC-1825da82-b92d-4725-b582-41091fff0d86.jpg'},
        {title: '', image: 'https://udemy-certificate.s3.amazonaws.com/image/UC-DZCJ1KD4.jpg'},
        {title: '', image: 'https://udemy-certificate.s3.amazonaws.com/image/UC-c91a29d0-f43b-48df-b290-a0aa9cd46c1c.jpg'},
        {title: '', image: 'https://udemy-certificate.s3.amazonaws.com/image/UC-YSVYRISC.jpg'},
        {title: '', image: 'https://udemy-certificate.s3.amazonaws.com/image/UC-8083af02-8a18-4098-8300-a318d2480c99.jpg'},
        {title: '', image: 'file:///C:/Users/Администратор/Downloads/diploma_page-0001.jpg'},
      ],
      webApps: [
        {title: 'Project 1', image: 'https://github.com/maxkolt/portfolio/raw/master/src/assets/img/project.png'},
        {title: 'Project 2', image: 'https://avatars.mds.yandex.net/i?id=40847cb65e1af4fe306e7378f133ec9c-5887333-images-thumbs&n=13'},
        {title: 'Project 3', image: 'https://avatars.mds.yandex.net/i?id=40847cb65e1af4fe306e7378f133ec9c-5887333-images-thumbs&n=13'},
        {title: 'Project 5', image: 'https://avatars.mds.yandex.net/i?id=40847cb65e1af4fe306e7378f133ec9c-5887333-images-thumbs&n=13'},
        {title: 'Project 5', image: 'https://avatars.mds.yandex.net/i?id=40847cb65e1af4fe306e7378f133ec9c-5887333-images-thumbs&n=13'},
        {title: 'Project 6', image: 'https://avatars.mds.yandex.net/i?id=40847cb65e1af4fe306e7378f133ec9c-5887333-images-thumbs&n=13'},
      ],
    }
  }
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
</style>
