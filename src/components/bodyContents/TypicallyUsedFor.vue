<template>
  <div class="container">
    <div class="typically-container">
      <h3 class="title">Typically used for</h3>
      <div class="mostusedIcons">
        <div class="all-icons">
          <div class="icons-name" v-for="(image, index) in images" :key="index">
            <img :src="image.src" :alt="image.alt" class="image" />
            <P
              :v-for="(image, index) in images"
              key="index"
              class="image-name"
              >{{ image.name }}</P
            >
          </div>
        </div>
      </div>
      <div></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TypcalyUsedFor",
  components: {},
  data() {
    return {
      images: [
        {
          src: require("../../assets/icons/Bedding.svg"),
          alt: "Bedding",
          name: "bedding",
        },
        {
          src: require("../../assets/icons/Courtains.svg"),
          alt: "Image 2",
          name: "courtains",
        },
        {
          src: require("../../assets/icons/Hostpital.svg"),
          alt: "Image 3",
          name: "hospital & yachting",
        },
        {
          src: require("../../assets/icons/homeDecol.svg"),
          alt: "Image 4",
          name: "home decor",
        },
        {
          src: require("../../assets/icons/table.svg"),
          alt: "Image 5",
          name: "table",
        },
      ],
    };
  },
};
</script>

<style scoped>
.typically-container {
  padding-left: 90px;
  padding-right: 108px;
  padding-top: 44px;
}
.title {
 font-family: "Bodoni Moda";
    font-style: normal;
    font-weight: 600;
    font-size: 25px;
    line-height: 38px;
    color: #1e1e1e;
}
.mostusedIcons {
  padding-top: 56px;
  padding-bottom: 80px;
}
.image-name {
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  padding-top: 16px;
  padding-bottom: 14px;
  align-items: center;
}
.icons-name {
    display: flex;
    align-items: center;
    flex-direction: column;
    border-right: 0.5px solid rgba(30, 30, 30, 0.2);
    border-spacing: 2;
    padding-right: 40px;
    height: 70px;
}

.icons-name:after {
    display: none;
}

.all-icons{
  display: flex;
  justify-content: space-between;
}

.image{
  
}

@media screen and (max-width: 666px) {
  .container {
    display: block;
    width: 100%;
  }
  .mostusedIcons {
  
    display: flex;
    flex-direction: column;
  }
  .image-name {
  padding-left: 20px;
  }
  .icons-name {
    display: flex;
    flex-direction: row;
    border-top: 1px solid rgba(30, 30, 30, 0.2);
    padding: 10px;
    
  }
  .typically-container{
    padding-left: 15px;
    padding-right: 15px;
  }
  .image{
    width: 10%;
  }
  .all-icons{
    display: flex;
    flex-direction: column;
  }
}
</style>

