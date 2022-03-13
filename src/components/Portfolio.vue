<template>
  <v-container class="my-10">
    <v-row justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text justify-center">Мои работы</v-subheader>
        <p>Вашему вниманию представлены несколько моих работ, а также сертификаты об окончании обучения</p>
      </v-col>
      <v-col lg="12">
        <div class="text-center">

          <v-chip
              @click="activePortfolio = 'webapp'"
              class="ma-2"
              :color="activePortfolio === 'webapp' ? 'teal lighten-1' : '' "
              outlined
          >
            <v-icon left>
              mdi-server-plus
            </v-icon>
            Проекты
          </v-chip>

          <v-chip
              @click="activePortfolio = 'certificate'"
              class="ma-2"
              :color="activePortfolio === 'certificate' ? 'red lighten-1' : ''"
              outlined
          >
            Сертификаты
            <v-icon right>
              mdi-account-outline
            </v-icon>
          </v-chip>
        </div>

      </v-col>
      <slot v-if="activePortfolio === 'webapp' ">
        <v-col lg="3" v-for="(web, webindex) in webApps" :key="webindex">
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
      <slot v-if="activePortfolio === 'certificate' ">
        <v-col lg="3" v-for="(certificat, certificatindex) in certificateApps" :key="certificatindex">
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
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Portfolio",
  data() {
    return {
      activePortfolio: 'webapp',
      webApps: [
        {title: 'Project 1', image: 'https://avatars.mds.yandex.net/i?id=40847cb65e1af4fe306e7378f133ec9c-5887333-images-thumbs&n=13'},
        {title: 'Project 2', image: 'https://avatars.mds.yandex.net/i?id=40847cb65e1af4fe306e7378f133ec9c-5887333-images-thumbs&n=13'},
        {title: 'Project 3', image: 'https://avatars.mds.yandex.net/i?id=40847cb65e1af4fe306e7378f133ec9c-5887333-images-thumbs&n=13'},
        {title: 'Project 5', image: 'https://avatars.mds.yandex.net/i?id=40847cb65e1af4fe306e7378f133ec9c-5887333-images-thumbs&n=13'},
        {title: 'Project 5', image: 'https://avatars.mds.yandex.net/i?id=40847cb65e1af4fe306e7378f133ec9c-5887333-images-thumbs&n=13'},
        {title: 'Project 6', image: 'https://avatars.mds.yandex.net/i?id=40847cb65e1af4fe306e7378f133ec9c-5887333-images-thumbs&n=13'},
      ],
      certificateApps: [
        {title: 'Certificate 1', image: 'http://flash7.ru/images/img-for-site-dev-1/FL-Center-Certif01-rgb-small.jpg'},
        {title: 'Certificate 2', image: 'http://flash7.ru/images/img-for-site-dev-1/FL-Center-Certif01-rgb-small.jpg'},
        {title: 'Certificate 3', image: 'http://flash7.ru/images/img-for-site-dev-1/FL-Center-Certif01-rgb-small.jpg'},
        {title: 'Certificate 4', image: 'http://flash7.ru/images/img-for-site-dev-1/FL-Center-Certif01-rgb-small.jpg'},
        {title: 'Certificate 5', image: 'http://flash7.ru/images/img-for-site-dev-1/FL-Center-Certif01-rgb-small.jpg'},
      ]
    }
  }
}
</script>

<style scoped>
.text {
  margin-top: 5rem;
  font-size: 40px;
  font-family: cursive;
  font-weight: 700;
}
</style>
