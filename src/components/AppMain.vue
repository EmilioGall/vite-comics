<script>
import { comicsArray } from "../assets/data/dc-comics.js";

export default {

  data() {
    return {

      comics: comicsArray,

    };
  },

};
</script>

<template>

  <div id="main-container">

    <!-- Cover Section -->
    <section>

      <img src="" alt="">

    </section>
    <!-- Cover Section -->

    <!-- Titles Grid Section -->
    <section class="wrapper">

      <h3>CURRENT SERIES</h3>

      <div>

      </div>

    </section>
    <!-- /Titles Grid Section -->

  </div>

</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

#main-container {
  color: $general-white;
  background-color: $general-black;
  padding: 10px 0;

  // Debug
  height: 250px;

}
</style>
