<template>
  <v-footer color="grey lighten-3">
    <v-col class="mt-5" lg="12">
      <v-row justify="center">
        <v-col class="text-center" lg="12">
          <v-toolbar-title>Frontend-developer</v-toolbar-title>
          <v-card-text>
            <v-btn
                v-for="icon in icons"
                :key="icon"
                class="mx-2 grey--text"
                icon
            >
              <v-icon size="24px">
                {{ icon }}
              </v-icon>
            </v-btn>
          </v-card-text>
        </v-col>
      </v-row>
      <div class="mt-2">
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

<style lang="scss">
.v-toolbar__title {
  font-size: 25px;
  font-weight: 700;
  font-family: cursive;
  color: #555555;
}
</style>
