<script>
export default {
    name: "AppMain"
}
</script>

<template>
  <main>
    <div class="container-main">
      <div class="margin">
        <i class="fa-solid fa-arrow-right"></i>
      <span class="content">
        <a href="">Content goes here</a>
      </span>
      <i class="fa-solid fa-arrow-left-long"></i>
      </div>
      
    </div>
  </main>
</template>

<style scoped lang="scss">
@use "../style/partials/variables.scss";

.container-main {
  height: 200px;
  background-color: #1C1C1C;
  text-align: center;
  display: flex;
  align-items: center;
  color: white;
}
.content a{
  font-size: 1.4rem;
  color: white;
  font-weight: bold;
  text-decoration: none;
  padding: 5px;
}
</style>