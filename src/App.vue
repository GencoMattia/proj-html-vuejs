<script>
import AppHeader from "./components/AppHeader.vue"
import AppMain from "./components/AppMain.vue"
import AppFooter from "./components/AppFooter.vue"
import EventsPage from "./components/EventsPage.vue"

import { store } from "./store";

import "@fontsource/montserrat";
import "@fontsource/montserrat/400.css";
import "@fontsource/montserrat/400-italic.css";

export default {
components: {
  AppHeader,
  AppMain,
  AppFooter,
  EventsPage,
},

    data() {
        return {
          
        };
    },
    
    computed: {
      activePageComponent() {
        return store.pressedLink;
      }
    }
};
</script>

<template>
  <AppHeader/>
  <component :is="activePageComponent" />
  <AppFooter />
  
  <main>
    
  </main>
</template>

<style lang="scss">
  @use "../node_modules/bootstrap/scss/bootstrap.scss";
  @use "./styles/general.scss";

  // body {
  //   font-family: "Montserrat";
  // }
</style>
