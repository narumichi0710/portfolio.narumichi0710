<template>
  <h2 class="title">
    {{ title }}
  </h2>
</template>

<script>
export default {
  props: ["title"],
}
</script>

<style scoped>
.title {
  text-align: center;
  padding-bottom:8px;
  border-bottom: solid 3px black;
  width: 50%;
  margin: 0 auto 50px;
  font-size: 40px;
  opacity:0.8;
}
@media screen and (max-width: 480px) {
  .title {
    font-size: 30px;
  }
}
</style>
