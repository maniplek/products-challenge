<template>
  <div class="nav-container">
    <div class="logo">
      <img src="../assets/logos/brignoli.svg" class="image-log" alt=" " />
    </div>

    <div class="item-selection">
      <div class="menu">CATALOG</div>

      <div class="nav-options">
        <ScrollNav :options="options" />
      </div>
    </div>
  </div>
</template>

<script>

import ScrollNav from './ScrollNav.vue'

export default {
  name: "NavBar",
  components: {
    ScrollNav,
  },
  data() {
    return {options: ["SOLUTIONS", "NEWS", "PROJECTS", "ABOUT", "PRESS", "CONTACT", "TEXTURES", "INSPIRATION"]};
  },
};
</script>

<style scoped>
@import url("https://fonts.cdnfonts.com/css/montserrat");
.nav-container {
  width: 100%;
  background-color: #a3846b;
  font-family: "Montserrat", sans-serif;
  color: #ffffff;
  display: flex;
  justify-content: space-between;
  overflow: hidden;
  height: 70px;
}
.menu {
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 29px;
  display: flex;
  justify-content: space-between;
  color: #ffffff;
  padding-bottom: 30px;
  padding-right: 38.75px;
}
.logo {
  padding-left: 80px;
  padding-top: 10px;
  padding-bottom: 90px;
  width: 1%;
}
.image-log {
  height: auto;
  width: 1000%;
}

  .nav-options {
    width: 80%;
    padding-bottom: 30px;
  }

.item-selection {
    padding: 19px 80px;
    height: 72px;
    width: 40%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

@media screen and (max-width: 666px) {
  .item-selection {
    padding: 0px;
    flex-direction: column;
    flex-basis: 10%;
 
  }

  .logo {
    padding: 5px;
    flex-basis: 10%;
    display: flex;
    align-items: center;

  }
  .image-log{
    height: 180%;
  }

  .nav-container {
    padding: 20px 0px;
    font-size: 18px;
 
  }

.nav-options{
  flex-basis: 10%;
}
  }
</style>
