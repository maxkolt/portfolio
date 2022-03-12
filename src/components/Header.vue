<template>
  <v-app-bar style="padding: 0 90px"
             app
             color="grey lighten-3"
             light
             elevation="6"
             elevate-on-scroll
  >
    <v-toolbar-title>
      Резюме
    </v-toolbar-title>
    <v-spacer/>
    <v-list class="d-flex align-center grey lighten-3">
      <v-list-item link v-for="(menu, index) in menus" :key="index" :to="menu.route">
        <v-list-item-title>{{ menu.title }}</v-list-item-title>
      </v-list-item>
      <v-btn text>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-btn outlined color="success">Начать</v-btn>
    </v-list>
  </v-app-bar>

</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      menus: [
        {title: 'Home', route: 'home'},
        {title: 'Education', route: 'education'},
        {title: 'Portfolio', route: 'portfolio'},
        {title: 'Project', route: 'project'},
        {title: 'Gallery', route: 'gallery'},
        {title: 'Contact', route: 'contact'},
      ]
    }
  }
}
</script>

<style scoped>
.v-toolbar__title {
  font-size: 35px;
  font-weight: 700;
  font-family: cursive;
  color: #444444;
}
</style>
