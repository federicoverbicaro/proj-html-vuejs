<template>

  <header>
    <AppHeader/>
  </header>

  <main>
    <AppMain/>
  </main>

  <footer>
    <AppFooter/>
  </footer>


</template>

<script>
import AppHeader from './components/header/AppHeader.vue';
import AppMain from './components/main/AppMain.vue';
import AppFooter from './components/footer/AppFooter.vue';



//inserimento tag creazione componenti 
export default {

  components : {
    AppHeader,
    AppMain,
    AppFooter,
  
},
data() {
  return {
    
  }
},
  
}

</script>


<style lang="scss">
/* Stili del componente radice */
@use "../src/styles/general.scss" //collegamento a file general.scss per utilizzare styles
</style>
