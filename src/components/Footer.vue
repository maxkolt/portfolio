<template>
  <v-footer padless>
    <v-col lg="12" >
      <v-row justify="center">
        <v-col lg="4" class="text-center">
          <v-toolbar-title>Frontend-developer</v-toolbar-title>
          <v-card-text>
            <v-btn
                v-for="icon in icons"
                :key="icon"
                class="mx-4 black--text"
                icon
            >
              <v-icon size="24px">
                {{ icon }}
              </v-icon>
            </v-btn>
          </v-card-text>
        </v-col>
      </v-row>
      <div class="mt-5">
        <v-divider></v-divider>
        <v-subheader>
          {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
          <v-spacer/>
          <strong>Максим Колтович</strong>
        </v-subheader>
      </div>
    </v-col>

  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  data: () => ({
    icons: [
      'mdi-facebook',
      'mdi-twitter',
      'mdi-linkedin',
      'mdi-instagram',
    ],
  }),
}
</script>

<style scoped>
.v-toolbar__title {
  font-size: 25px;
  font-weight: 700;
  font-family: cursive;
  color: #555555;
}
</style>
