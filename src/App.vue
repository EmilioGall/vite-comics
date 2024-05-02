<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {

  components: {

    AppHeader,
    AppMain,
    AppFooter
    
  },

};

</script>

<template>

  <div class="wrapper">

    <AppHeader />
  
    <AppMain />
  
    <AppFooter />

  </div>


</template>

<style lang="scss" scoped>

.wrapper {
  margin: 0 auto;
  width: 80%;

  // Debug
  background-color: lightcoral;

}

</style>
