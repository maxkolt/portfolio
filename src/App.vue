<template>
  <v-app class="flex">
    <v-main>
      <Header/>
      <MainPage/>
      <Education/>
      <Portfolio/>
      <Skills/>
      <Contacts/>
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>


import Header from "@/components/Header";
import MainPage from "@/components/MainPage";
import Education from "@/components/Education";
import Portfolio from "@/components/Portfolio";
import Skills from "@/components/Skills"
import Contacts from "@/components/Contacts";
import Footer from "@/components/Footer";

export default {
  name: 'App',
  components: {Footer, Contacts, Portfolio, Education, MainPage, Header, Skills},
  data() {
    return {}
  },

}
</script>

<style lang="scss">
</style>
