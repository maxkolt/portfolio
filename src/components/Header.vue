<template>
  <v-app-bar app
             color="grey lighten-3"
             elevate-on-scroll
             elevation="6"
             light
             style="padding: 0 90px"
  >
    <v-avatar class="mr-2">
      <img alt="Max" src="https://cdn.vuetifyjs.com/images/john.jpg">
    </v-avatar>
    <div class="text-header">
      Резюме
    </div>
    <v-spacer/>
    <v-list class="text-nav d-flex grey lighten-3" >
      <v-list-item v-for="(menu, index) in menus" :key="index" :to="menu.route" link>
        <v-list-item-title>{{ menu.title }}</v-list-item-title>
      </v-list-item>
      <div class="flex ml-3">
        <div :class="darkDark" class="mode-toggle" @click="modeToggle">
          <div class="toggle">
            <div id="dark-mode" type="checkbox"></div>
          </div>
        </div>
      </div>
    </v-list>
  </v-app-bar>

</template>

<script>
import MyComponent from "@/components/Main";

export default {
  name: "Header",
  components: {MyComponent},
  data() {
    return {
      menus: [
        {title: 'Главная', route: 'home'},
        {title: 'Обучение', route: 'education'},
        {title: 'Галерея', route: 'portfolio'},
        {title: 'Навыки', route: 'project'},
        {title: 'Контакт', route: 'contact'},
      ],
      darkMode: false
    }
  },
  methods: {
    dark() {
      document.querySelector('body').classList.add('dark-mode')
      this.darkMode = true
      this.$emit('dark')
    },

    light() {
      document.querySelector('body').classList.remove('dark-mode')
      this.darkMode = false
      this.$emit('light')
    },

    modeToggle() {
      if (this.darkMode || document.querySelector('body').classList.contains('dark-mode')) {
        this.light()
      } else {
        this.dark()
      }
    },
  },
  computed: {
    darkDark() {
      return this.darkMode && 'darkmode-toggled'
    }
  }
}
</script>

<style lang="scss">
.text-header {
  font-size: 2.3rem;
  font-weight: 700;
  font-family: cursive;
  color: #444444;
}
.text-nav {
  font-family: cursive;
  align-items: center;
}

$dark: #373637;
$mode-toggle-bg: #0a1e39;

body {
  background-color: #fff;
  color: $dark;
  transition: background-color .2s ease, color .2s ease;
}

body {
  &.dark-mode {
    background-color: lighten($dark, 5%);

    .flex {
      h2, h6, p {
        color: #d6d3d3;
      }
    }
  }
}

.mode-toggle {
  position: relative;
  padding: 10px;
  width: 55px;
  height: 24px;
  min-width: 36px;
  min-height: 20px;
  background-color: grey;
  border: 0;
  border-radius: 24px;
  outline: 0;
  overflow: hidden;
  cursor: pointer;
  z-index: 1;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
  -webkit-touch-callout: none;
  appearance: none;
  transition: background-color .5s ease;

  .toggle {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    margin: auto;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    border: 3px solid transparent;
    box-shadow: inset 0 0 0 2px #a5abba;
    overflow: hidden;
    transition: transform .5s ease;

    #dark-mode {
      position: relative;
      width: 100%;
      height: 100%;
      overflow: hidden;
      border-radius: 50%;

      &:before {
        content: '';
        position: relative;
        width: 100%;
        height: 100%;
        left: 50%;
        float: left;
        background-color: #a5abba;
        transition: border-radius .5s ease, width .5s ease, height .5s ease, left .5s ease, transform .5s ease;
      }
    }
  }
}

body.dark-mode {
  .mode-toggle {
    background-color: lighten($mode-toggle-bg, 5%);

    .toggle {
      transform: translateX(35px);

      #dark-mode {
        &:before {
          border-radius: 50%;
          width: 150%;
          height: 85%;
          left: 40%;
          transform: translate(-10%, -40%), rotate(-35deg);
        }
      }
    }
  }
}

html, body, #app, {
  width: 100%;
  height: 1%;
}
</style>
