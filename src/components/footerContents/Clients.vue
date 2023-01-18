<template>
  <div class="client-container">
    <img :key="logo" v-for="logo in logos" :src="logo" />
  </div>
</template>

<script>
export default {
  name: "Clients",
  data: () => ({
    logos: [
      require("../../assets/logos/martinelli-ginetto-italy.logo.svg"),
      require("../../assets/logos/brignoli-italy.logo.svg"),
      require("../../assets/logos/kohro.logo.svg"),
      require("../../assets/logos/nord-ciniglia.logo.svg"),
      require("../../assets/logos/ms3.logo.svg"),
    ],
  }),
};
</script>

<style scoped>
.client-container {
  display: flex;
  justify-content: space-between;
  padding-top: 1rem;
  margin: 2rem 0rem;
  opacity: 0.5;
}

@media screen and (max-width: 666px) {
  .client-container {
    
  }

  .container img {
  }
}
</style>
