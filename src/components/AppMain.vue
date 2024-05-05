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
    <section class="cover-banner">

      <img src="../assets/img/jumbotron.jpg" alt="">

    </section>
    <!-- Cover Section -->

    <!-- Titles Grid Section -->
    <section class="titles-grid">

      <div class="wrapper">

        <h3>CURRENT SERIES</h3>

        <div class="row">

          <div class="col" v-for="prod in comics">

            <h1>hello</h1>
            <!-- <ProductCard 
            :cardImage="prod.src" 
            :cardTitle="prod.titolo" 
            :cardType="prod.tipo" /> -->

          </div>

        </div>

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

  // Debug
  // height: 250px;

  .cover-banner {
    height: calc($header-height * 4);
    position: relative;
    overflow: hidden;

    img {
      object-fit: cover;
      position: absolute;
      margin: auto;

    }

  }

  .titles-grid {
    padding: 1rem 1rem;

    @include flex(column, center, center);

    .row {
      @include flex(row, space-between, stretch, wrap);

      .col {
        width: calc(100% / 6);
        margin-bottom: 1rem;
        border: 2px solid white;
      }
    }
  }

}
</style>
