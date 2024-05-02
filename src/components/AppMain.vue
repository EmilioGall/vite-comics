<script>

export default {



};

</script>

<template>

  <div id="main-container">

    <div class="wrapper">

      <h2>Main content</h2>

    </div>

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
