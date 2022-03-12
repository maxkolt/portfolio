<template>
  <v-app>
    <Header/>
    <v-main>
      <MyComponents/>
      <Education/>
    </v-main>
  </v-app>
</template>

<script>


import Header from "@/components/Header";
import MyComponents from "@/components/MyComponent";
import Education from "@/components/Education";

export default {
  name: 'App',
  components: {Education, MyComponents, Header},
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
};
</script>
