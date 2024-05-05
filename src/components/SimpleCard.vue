<script>
export default {

  props: {

    cardImage: String,
    cardTitle: String,

  },

};
</script>

<template>

  <div class="card" :class="cardType">

    <div class="img-container">

      <img :src="cardImage" :alt="cardTitle" />

    </div>

    <h4>{{ cardTitle }}</h4>

  </div>

</template>

<style scoped lang="scss">

@use "../style/partials/variables" as *;

.card {
  padding: 1rem;

  .img-container {
    height: calc($header-height * 2.5);
    position: relative;
    overflow: hidden;
    margin-bottom: 10px;

    img {
      object-fit: cover;
      position: absolute;
      margin: auto;

    }

  }



}
</style>