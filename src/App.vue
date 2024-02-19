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
<!-- 
<AppButton yellow :button-text="'bella'" :icon="yellowIcon"/> -->

</template>

<script>
import AppHeader from './components/header/AppHeader.vue';
import AppMain from './components/main/AppMain.vue';
import AppFooter from './components/footer/AppFooter.vue';
import AppButton from './components/Button/AppButton.vue';
// import yellowIcon from './assets/img/Speaker-icon.png';


//inserimento tag creazione componenti 
export default {

  components : {
    AppHeader,
    AppMain,
    AppFooter,
    AppButton,
},
data() {
  return {
    // yellowIcon: yellowIcon
  }
},
  
}

</script>


<style lang="scss">
/* Stili del componente radice */
@use "../src/styles/general.scss" //collegamento a file general.scss per utilizzare styles
</style>
