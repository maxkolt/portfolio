<template>
  <v-container class="mt-10">
    <v-row justify="center">
      <v-col lg="12" class="text-center mt-5">
        <v-subheader class="text justify-center">Контакт</v-subheader>
      </v-col>
      <v-col lg="6" class="mt-12">
        <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d577336.7638984495!2d36.82513038949304!3d55.5807480820225!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46b54afc73d4b0c9%3A0x3d44d6cc5757cf4c!2z0JzQvtGB0LrQstCw!5e0!3m2!1sru!2sru!4v1647197872032!5m2!1sru!2sru"
            width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
      </v-col>
      <v-col lg="6" class="mt-12">
        <v-form ref="form">
          <v-text-field
              v-model="contactInfo.name"
              :counter="10"
              label="Name"
              required
          ></v-text-field>

          <v-text-field
              v-model="contactInfo.email"
              :rules="emailRules"
              label="E-mail"
              required
          ></v-text-field>

          <v-textarea label="Massage" v-model="contactInfo.massage">

          </v-textarea>

          <v-btn color="teal lighten-2" class="mr-4">
            Отправить
          </v-btn>

        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Contacts",
  data(){
    return {
      contactInfo: {}
    }
  }
}
</script>

<style scoped>
.text {
  margin-top: 1rem;
  font-size: 40px;
  font-family: cursive;
  font-weight: 700;
}
</style>
