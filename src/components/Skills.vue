<template>
  <v-container class="my-10">
    <v-row justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text justify-center">Мои навыки</v-subheader>
      </v-col>
    </v-row>
    <v-card class="mx-auto mt-5" max-width="960">
      <v-card-title
          class="grey lighten-2 white--text"
      >
        <span class="text-h4">Skills</span>
        <v-spacer></v-spacer>
        <v-btn
            :outlined="interval == null"
            :color="interval == null ? 'teal lighten-2' : 'red lighten-1'"
            dark
            depressed
            @click="interval == null ? start() : stop()"
        >
          Начать просмотр/Стоп
        </v-btn>
      </v-card-title>
      <v-card-text class="py-0">
        <v-timeline dense>
          <v-slide-x-reverse-transition
              group
              hide-on-leave
          >
            <v-timeline-item
                v-for="item in items"
                :key="item.id"
                :color="item.color"
                small
                fill-dot
            >
              <v-alert
                  :value="true"
                  :color="item.color"
                  :icon="item.icon"
                  class="white--text"
              >
               <img src="../assets/img/language-html5.png" alt="html">
              </v-alert>
            </v-timeline-item>
          </v-slide-x-reverse-transition>
        </v-timeline>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
const COLORS = [
  'orange accent-3',
  'warning',
  'error',
  'success',
]
const ICONS = {
  html: 'mdi-language-html5',
  css: 'mdi-language-css3',
  JS: 'mdi-language-javascript',
  vue: 'mdi-vue-js',
  bootstrap:'mdi-bootstrap',
  vuetify: 'mdi-vuetify',

}
export default {
  name: "Skils",
  data: () => ({
    interval: null,
    items: [
      {
        id: 1,
        color: 'orange accent-3',
        icon: ICONS.html,
      },
      {
        id: 2,
        color: 'red accent-3',
        icon: ICONS.css,
      },
    ],
    nonce: 1,
  }),

  beforeDestroy() {
    this.stop()
  },

  methods: {
    addEvent() {
      let {color, icon} = this.genAlert()

      const previousColor = this.items[0].color

      while (previousColor === color) {
        color = this.genColor()
      }

      this.items.unshift({
        id: this.nonce++,
        color,
        icon,
      })

      if (this.nonce > 6) {
        this.items.pop()
      }
    },
    genAlert() {
      const color = this.genColor()

      return {
        color,
        icon: this.genIcon(color),
      }
    },
    genColor() {
      return COLORS[Math.floor(Math.random() * 4)]
    },
    genIcon(color) {
      return ICONS[color]
    },
    start() {
      this.interval = setInterval(this.addEvent, 2500)
    },
    stop() {
      clearInterval(this.interval)
      this.interval = null
    },
  },
}
</script>

<style scoped>
.text {
  margin-top: 5rem;
  font-size: 40px;
  font-family: cursive;
  font-weight: 700;
}
.text-h4{
  color: grey;
}
</style>
