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

    <div>

      <img src="" alt="">

    </div>

    <div>

      <ul>

        <li v-for="element in menu">

          {{ element.title }}

        </li>

      </ul>

    </div>

  </header>

</template>

<style lang="scss" scoped></style>
