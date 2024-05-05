<script>
import { menuFooterArray } from "../assets/data/menu-footer.js";
import { socialsFooterArray } from "../assets/data/socials-footer.js";

export default {

  data() {
    return {

      menu: menuFooterArray,
      socials: socialsFooterArray,

    };
  },

  methods: {

    getLogoImagePath(company) {

      return new URL(`../assets/img/footer-${company}.png`, import.meta.url).href;

    },

  },

};
</script>

<template>

  <footer>

    <div class="wrapper">

      <!-- Menu Section -->
      <div class="row">

        <!-- Menu List -->
        <div class="col-1">

          <div class="menu-block" v-for="title in menu">

            <div class="sub-menu">

              <h3> {{ title.name }}</h3>

              <ul>

                <li v-for="category in title.categories">

                  <a href="">

                    <p>

                      {{ category }}

                    </p>

                  </a>

                </li>

              </ul>

            </div>

          </div>

        </div>
        <!-- /Menu List -->

        <!-- Logo Footer -->
        <div class="col-2">

          <div class="img-container">

            <img src="../assets/img/dc-logo-bg.png" alt="">

          </div>

        </div>
        <!-- /Logo Footer -->

      </div>
      <!-- /Menu Section -->

    </div>

    <!-- Contacts Section -->
    <div class="row contacts">

      <div class="wrapper row">

        <!-- SignUp Link -->
        <div class="col-1 sign-up">
  
          <a href="">
            SIGN-UP NOW!
          </a>
  
        </div>
        <!-- /SignUp Link -->
  
        <!-- Socials Links -->
        <div class="col-2 socials">
  
          <h3>FOLLOW US</h3>
  
          <div class="social-logos">
  
            <a href="" v-for="logo in socials">
  
              <img :src="getLogoImagePath(logo)" :alt="logo">
  
            </a>
  
          </div>
  
        </div>
        <!-- /Socials Links -->

      </div>

    </div>
    <!-- /Contacts Section -->

  </footer>

</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

footer {
  color: $general-white;
  background-image: url(../assets/img/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;


  .row {
    @include flex(row, space-between, stretch, wrap);

    .col-1 {
      @include flex(row, space-between, start);
      width: calc(100% / 2);
      padding: 2rem 0;

      &.sign-up {

        a {
          border: 3px solid $general-lightblue;
          padding: 20px 40px;

        }
      }

      .menu-block {
        @include flex(row, space-between, center);
        width: calc(100% / 4);

        .sub-menu {

          h3 {
            padding-bottom: 10px;

          }

          p {
            padding: 5px;
            font-size: small;
            font-weight: 100;

          }

        }

      }

    }

    .col-2 {
      width: calc(100% / 2);
      position: relative;

      &.socials {
        @include flex(row, end, center);
        gap: 80px;

        h3 {
          color: $general-lightblue;

        }

        .social-logos {
          @include flex(row, end, center);
          gap: 10px;

        }

      }

      .img-container {
        height: 100%;
        position: relative;
        overflow: hidden;

        img {
          object-fit: cover;
          position: absolute;
          right: 0px;
          top: -40px;
          margin: auto;

        }

      }

    }

    &.contacts {
      background-color: $general-grey;

    }

  }



}
</style>
