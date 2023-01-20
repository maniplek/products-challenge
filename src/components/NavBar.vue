<template>
  <div class="nav-container">
    <img src="../assets/logos/brignolilogo.svg" class="image-log" alt=" " />

    <div class="item-selection">
      <div class="menu">CATALOG</div>

      <div class="nav-options">
        <ScrollNav :options="options" />
      </div>
    </div>
  </div>
</template>

<script>
import ScrollNav from "./ScrollNav.vue";

export default {
  name: "NavBar",
  components: {
    ScrollNav,
  },
  data() {
    return {
      options: [
        "SOLUTIONS",
        "NEWS",
        "PROJECTS",
        "ABOUT",
        "PRESS",
        "CONTACT",
        "TEXTURES",
        "INSPIRATION",
      ],
    };
  },
};
</script>

<style scoped>
@import url("https://fonts.cdnfonts.com/css/montserrat");
.nav-container {
  background-color: #a3846b;
  font-family: "Montserrat", sans-serif;
  color: #ffffff;
  display: flex;
  justify-content: space-between;
  overflow: hidden;
}
.image-log{
      width: 20%;
    padding-left: 80px;
}

.nav-options {
  width: 80%;
}

.item-selection {
  padding: 19px 50px;
  height: 72px;
  width: 48%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.menu{
      font-family: 'Montserrat';
    font-style: normal;
    font-weight: 666;
    font-size: 20px;
    line-height: 29px;
    color: #FFFFFF;
}

@media screen and (max-width: 666px) {
  .item-selection {
    padding: 0px;
    flex-direction: column;
    flex-basis: 60%;
  }

  .nav-options {
    flex-basis: 10%;
  }
}
</style>
