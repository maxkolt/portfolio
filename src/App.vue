<template>
  <v-app>
    <Header/>
    <v-main>
      <MyComponent/>
      <Education/>
      <Portfolio/>
      <Skills/>
      <Contacts/>
    </v-main>
  </v-app>
</template>

<script>


import Header from "@/components/Header";
import MyComponent from "@/components/MyComponent";
import Education from "@/components/Education";
import Portfolio from "@/components/Portfolio";
import Skills from "@/components/Skills"
import MyComponents from "@/components/MyComponent";
import Contacts from "@/components/Contacts";
export default {
  name: 'App',
  components: {Contacts, MyComponents, Portfolio, Education, MyComponent, Header, Skills},
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
