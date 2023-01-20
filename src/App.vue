<template>
  <div>
    <Header/>
    <NavBar/>
    <AllBodyContents/>
    <Footer/>
  </div>
</template>

<script>

import Header from './components/Header.vue'
import NavBar from './components/NavBar.vue'
import AllBodyContents from './components/AllBodyContents.vue'
import Footer from './components/Footer.vue'

export default {
  name: "App",
  components: {
    Header,
    NavBar,
    AllBodyContents,
    Footer
  },
};
</script>

<style>
* {
 margin:0;
 padding:0;
 box-sizing: border-box;
}
#app {
  overflow: hidden;
  font-family: Raleway, sans-serif;

}



</style>
