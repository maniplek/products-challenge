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
    padding: 0 19.75px 0 9%;
    align-items: center;
    gap: 0.5%;
}
.icon:hover{
  cursor: pointer;
}
.back{
   text-decoration-line: underline;
   color: #1E1E1E;
   text-decoration-color:DarkGray;
}
.back:hover{
cursor: pointer;
}
  @media screen and (max-width: 666px) {

  .icon{
    padding-right: 0px;
 padding-left: 3%;
   
}

   .back-section{
    display: flex;
    flex-direction: row;
    padding: 0px;
   }

}
</style>
