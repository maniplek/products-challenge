<template>
  <div class="service-container">
    <h2>{{ service.title }}</h2>
    <div
      class="service-content"
      :key="content"
      v-for="content in service.contents"
    >
      {{ content }}
    </div>
  </div>
</template>

<script>
export default {
  name: "Service",
  props: {
    service: Object,
  },
};
</script>

<style scoped>
h2 {
  color: white;
  font-family: "Raleway";
  font-style: normal;
  font-weight: 700;
  font-size: 12px;
  line-height: 28px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  letter-spacing: 2px;
  text-transform: uppercase;
}
.service-content{
font-family: 'Raleway';
font-style: normal;
font-weight: 400;
font-size: 12px;
line-height: 28px;
display: flex;
align-items: center;
letter-spacing: 2px;
color: #FFFFFF
}
</style>
