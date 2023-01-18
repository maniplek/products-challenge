<template>
  <div class='body-container'>
    <div class='back-section'>
       <img class='icon' src="../assets/icons/Caretright.svg" alt=" " />
        <a class="back">Back</a>
    </div>

    <Products/>
    <TypcalyUsedFor />
    <TechnicalInfo/>
    <ProductYouMightLike/>
  </div>
</template>


<script>

import Products from './bodyContents/Products.vue'
import TypcalyUsedFor from './bodyContents/TypicallyUsedFor.vue'
import TechnicalInfo from './bodyContents/TechnicalInfo.vue'
import ProductYouMightLike from './bodyContents/ProductYouMightLike.vue'


export default {
  name: "AllBodyContents",
  components: {
    Products,
    TypcalyUsedFor,
    TechnicalInfo,
    ProductYouMightLike
  },
};
</script>

<style scoped>

.back-section{
display: flex;
padding: 3px 19.75px 3px 118.75px ;

}
.icon{
    padding-right: 15px;
    width: 10px;
    height: auto;

}

.icon:hover{
  cursor: pointer;
}
.back{
   text-decoration-line: underline;
}
.back:hover{
cursor: pointer;
}
  
</style>
