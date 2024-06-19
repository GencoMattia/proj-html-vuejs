<script>
import AppHeader from "./components/AppHeader.vue"
import AppMain from "./components/AppMain.vue"
import AppFooter from "./components/AppFooter.vue"

export default {
components: {
  AppHeader,
  AppMain,
  AppFooter,
},

    data() {
        return {
        
        };
    }
};
</script>

<template>
  <AppHeader/>
  <AppMain />
  <AppFooter />
  
  <main>
    
  </main>
</template>

<style lang="scss">
  @use "../node_modules/bootstrap/scss/bootstrap.scss";
  @use "./styles/general.scss";
</style>
