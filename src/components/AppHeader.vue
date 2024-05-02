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

  <header>

    <div class="logo-container">

      <img src="../assets/img/dc-logo.png" alt="">

    </div>

    <div class="menu-container">

      <ul class="menu-list">

        <li v-for="element in menu">

          <a href="">
            {{ element.title }}
          </a>

        </li>

      </ul>

    </div>

  </header>

</template>

<style lang="scss" scoped>

@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

header {
  @include flex(row, space-between, center);
  padding: 20px;

  // Debug
  background-color: lightcoral;

  img {
    width: 80px;

  }

  .menu-list {
    display: flex;

    li {
      margin-left: 10px;

    }

  }

}

</style>
