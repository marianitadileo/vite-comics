<script>
export default {
    name: "AppMain"
}
</script>

<template>
  <main>
    <div class="container-main">
      <i class="fa-solid fa-arrow-right"></i>
      <a href="" class="content">Content goes here</a>
      <i class="fa-solid fa-arrow-left-long"></i>
    </div>
  </main>
</template>

<style scoped lang="scss">
@use "../style/partials/variables.scss" as *;

main {
  width: 100%;
  height: 150px;
  background-color: #1C1C1C;
  font-size: 1.4rem;
  font-weight: bold;
}
.container-main {
  @include margin;
  line-height: 140px;
  color: white;
}
.content {
  color: white;
  text-decoration: none;
  padding: 5px;
}

</style>