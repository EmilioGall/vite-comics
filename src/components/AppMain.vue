<script>
import { comicsArray } from "../assets/data/dc-comics.js";
import SimpleCard from "./SimpleCard.vue";

export default {

  data() {
    return {

      comics: comicsArray,

    };
  },

  components: {

    SimpleCard,

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

          <div class="col" v-for="title in comics">

            <SimpleCard :cardImage="title.thumb" :cardTitle="title.series" />

          </div>

        </div>

        <button>LOAD MORE</button>

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

    .wrapper {
      position: relative;
      display: flex;
      flex-direction: column;
      align-items: center;

      h3 {
        display: inline-block;
        padding: 10px 20px;
        background-color: $general-lightblue;
        position: absolute;
        top: -40px;
        left: 0px;

      }

      .row {
        @include flex(row, space-between, stretch, wrap);
        margin-top: 15px;

        .col {
          width: calc(100% / 6);
          margin-bottom: 1rem;

          // Debug
          // border: 2px solid white;

        }

      }

      button {
        width: 20%;
        display: inline-block;
        padding: 10px 20px;
        background-color: $general-lightblue;

      }

    }

  }

}
</style>
