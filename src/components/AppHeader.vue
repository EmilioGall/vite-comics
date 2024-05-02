<script>

export default {

  data() {
    return {

      menu: [
        {
          title: "CHARACTERS",
          isActive: false,
        },
        {
          title: "COMICS",
          isActive: true,
        },
        {
          title: "MOVIES",
          isActive: false,
        },
        {
          title: "TV",
          isActive: false,
        },
        {
          title: "GAMES",
          isActive: false,
        },
        {
          title: "COLLECTIBLES",
          isActive: false,
        },
        {
          title: "VIDEOS",
          isActive: false,
        },
        {
          title: "FANS",
          isActive: false,
        },
        {
          title: "NEWS",
          isActive: false,
        },
        {
          title: "SHOP",
          isActive: false,
        },
      ],

    };
  },

};

</script>

<template>

  <header class="wrapper">

    <!-- Logo Section -->
    <section class="logo-container">

      <img src="../assets/img/dc-logo.png" alt="">

    </section>
    <!-- /Logo Section -->

    <!-- Menu Section -->
    <section class="menu-container">

      <ul class="menu-list">

        <li v-for="element in menu" :class="{ active: element.isActive }">

          <a href="">
            {{ element.title }}
          </a>

        </li>

      </ul>

    </section>
    <!-- /Menu Section -->

  </header>

</template>

<style lang="scss" scoped>

@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

header {
  @include flex(row, space-between, center);
  height: $header-height;

  // Debug
  // border: 1px solid lightcoral;

  .menu-container {

    img {
      aspect-ratio: 1;
      width: 80px;

    }

  }

  .menu-container {

    .menu-list {
      @include flex(row, end, center);

      li {
        padding: 10px;
        @include flex(row, end, center);
        height: $header-height;
        border-bottom: 5px solid rgba($color: #000000, $alpha: 0);

        &:last-child {
          padding-right: 0px;

        }

        &.active {
          color: $general-lightblue;
          border-bottom: 5px solid $general-lightblue;

        }

      }

    }

  }

}

</style>
