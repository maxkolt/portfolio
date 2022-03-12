<template>
  <v-app>
<Header/>
    <v-main>
<MyComponents/>
    </v-main>
  </v-app>
</template>

<script>


import Header from "@/components/Header";
import MyComponents from "@/components/MyComponent";
export default {
  name: 'App',
  components: {MyComponents, Header},
  data() {
    return {
      menus: [
        {title: 'Home',      route: 'home'},
        {title: 'About',     route: 'about'},
        {title: 'Portfolio', route: 'portfolio'},
        {title: 'Project',   route: 'project'},
        {title: 'Gallery',   route: 'gallery'},
        {title: 'Contact',   route: 'contact'},
      ]
    }
  }
};
</script>
