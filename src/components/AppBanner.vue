<script>

export default {

  data() {
    return {

      menu: [
        {
          category: "DIGITAL COMICS",
          icon: "comics-digital-comics.png",
        },
        {
          category: "DC MERCHANDISE",
          icon: "comics-merchandise.png",
        },
        {
          category: "SUBSCRIPTION",
          icon: "comics-subscriptions.png",
        },
        {
          category: "COMIC SHOP LOCATOR",
          icon: "comics-shop-locator.png",
        },
        {
          category: "DC POWER VISA",
          icon: "dc-power-visa.svg",
        },
      ],

    };
  },

  methods: {

    getImagePath(imageName) {

      return new URL(`../assets/img/buy-${imageName}`, import.meta.url).href;

    },
  },

};

</script>

<template>

  <div id="banner-container">

    <div class="wrapper">

      <a v-for="element in menu">

        <img :src="getImagePath(element.icon)" alt="">

        <h3> {{ element.category }}</h3>

      </a>

    </div>

  </div>

</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

#banner-container {
  @include flex(row, space-between, center);
  color: $general-white;
  background-color: $general-lightblue;
  padding: 50px 0;

  // Debug
  // height: 250px;

  .wrapper {
    @include flex(row, space-between, center);

    a {
      @include flex(row, space-between, center);

      img {
        height: 50px;
        

      }

      &:last-child {

        img {
          height: auto;
          width: 50px;

        }

      }

      h3 {
        font-size: small;
        padding-left: 10px;

      }

    }

  }

}
</style>
