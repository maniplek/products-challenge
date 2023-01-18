<template>
  <div class="container">
    <h4 class="title service-element">{{service.title.toUpperCase()}}</h4>
    <div class="service-element" :key="element" v-for="element in service.contents">{{element}}</div>
  </div>
</template>

<script>
export default {
  name: "Services",
  props: {
    service: Object
  }
}
</script>

<style scoped>
  .title {
    font-size: 12px;
    font-weight: 700;
    line-height: 28px;
  }

  .service-element {
    font-size: 12px;
    line-height: 28px;
    padding: 5px;
  }

  @media screen and (max-width: 666px) {
    .container {
    flex-basis: 50%;
    padding: 0px;
  }
  .service-element {
    padding: 3px;
  }
  }

</style>