<template>
  <div class="slider-container">
    <div class="title-container">
      <h2 class="title">Products you might like</h2>
      <div class="next-prev-image">
        <img
          class="prev-image"
          src="../../assets/icons/keyboard_backspace.svg"
          alt="Snow"
        />

        <img class="next-image" src="../../assets/icons/east.svg" alt="Snow" />
      </div>
    </div>

    <div class="image-slide">
      <div
        class="slide"
        v-for="(image, index) in images"
        :key="index"
        v-bind:class="{ active: index === currentSlide }"
      >
        <div class="left-right-icons">
          <img
            class="product-image"
            src="../../assets/icons/GroupLeft.svg"
            alt="Snow"
          />

          <img
            class="product-image"
            src="../../assets/icons/GroupRight(1).svg"
            alt="Snow"
          />
        </div>
        <div class="overlay">
          <h4 class="overlay-title">Lorem Ipsum dollar</h4>
          <div class="ovalay-colors">
            <div class="colors-sections">
              <div class="colors-section red"></div>
              <div class="colors-section grey"></div>
              <div class="colors-section green"></div>
              <div class="colors-section black"></div>
              <div>+20</div>
            </div>
          </div>
        </div>
        <img :src="image.src" :alt="image.alt" />
      </div>
    </div>
    <div class="nav-container">
      <div class="nav-btn left">
        <img
            class="product-image"
            src="../../assets/icons/Left.svg"
            alt="Snow"
        />
      </div>
      <div class="nav-labels">
        <p class="nav active">1</p>
        <p class="nav">2</p>
        <p class="nav">3</p>
        <p class="nav">4</p>
      </div>
      <div class="nav-btn right">
        <img
            class="product-image"
            src="../../assets/icons/Right.svg"
            alt="Snow"
        />
      </div>
    </div>
  </div>
</template>

<script>
import ScrollNav from "../ScrollNav.vue";

export default {
  name: "ProductYouMightLike",
  components: {
    ScrollNav,
  },
  data() {
    return {
      // isMobile: window.matchMedia("(max-width: 768px)").matches,
      images: [
        {
          src: require("../../assets/images/Captura-de-pantalla1.png"),
          alt: "Image 1",
        },
        {
          src: require("../../assets/images/Captura-de-pantalla-2.png"),
          alt: "Image 2",
        },
        {
          src: require("../../assets/images/Captura-de-pantalla2.png"),
          alt: "Image 3",
        },
        {
          src: require("../../assets/images/Captura-de-pantalla-(1).png"),
          alt: "Image 4",
        },
        {
          src: require("../../assets/images/Captura-de-pantalla(1).png"),
          alt: "Image 5",
        },
      ],
      currentSlide: 0,
    };
  },

  // mounted() {
  //   window.addEventListener("resize", this.handleResize);
  // },

  methods: {
    handleResize() {
      this.isMobile = window.matchMedia("(max-width: 666px)").matches;
    },

    prevSlide() {
      if (this.currentSlide > 0) {
        this.currentSlide--;
      }
    },
    nextSlide() {
      if (this.currentSlide < this.images.length - 1) {
        this.currentSlide++;
      }
    },
  },
};
</script>

<style scoped>
.slider-container {
  padding: 64px 0px 64px 90px;
  background: #edeae6;
  overflow: hidden;
}

.slide {
  width: 100%;
  float: left;
  position: relative;
}

.slide:hover > .overlay {
  opacity: 1;
}

.slide:hover > .left-right-icons {
  opacity: 1;
}

.image-slide {
  display: flex;
  gap: 16px;
  overflow: hidden;
  justify-content: space-between;
  flex-direction: row;
}

.title-container {
  display: flex;
  justify-content: space-between;
}
.title {
  font-family: "Bodoni Moda";
  font-style: normal;
  font-weight: 700;
  font-size: 33px;
  line-height: 50px;
  padding-bottom: 10px;
  color: #000000;
}
.next-icon {
  float: left;
}

.left-right-icons {
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  opacity: 0;
  height: 40%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: absolute;
  left: 0;
  right: 0;
  top: 22%;
  transform: translateY(-10);
}

.left-right-icons img {
  width: 20px;
  height: 20px;
}

.overlay {
  background: white;
  position: absolute;
  left: 0;
  right: 0;
  padding-top: 30px;
  bottom: 0;
  opacity: 0;
  height: 50%;
}

.colors-sections {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 50%;
  margin: auto;
  font-size: 14px;
  padding-bottom: 1px;
}

.colors-section {
  height: 20px;
  width: 20px;
  border-radius: 80%;
}

.overlay-title {
  text-align: center;
  padding-bottom: 20px;
}

.red {
  background-color: maroon;
}

.grey {
  background-color: grey;
}

.green {
  background-color: rgb(13, 66, 13);
}

.black {
  background-color: black;
}

.next-prev-image {
  padding-right: 6%;
}

.nav-container {
  display: none;
}

@media screen and (max-width: 666px) {
  .title-container {
    display: flex;
  }
  .next-prev-image {
    display: none;
  }
  .product-image {
    display: block;
    width: 100%;
  }
  .slider-container {
    padding-left: 16px;
  }
  .image-loop-on-mobile {
    display: block;
  }
.title{
      font-size: 50px;
      padding-bottom: 24px;
}
.slide > .overlay {
  opacity: 1;
}

.slide > .left-right-icons {
  opacity: 1;
}

.overlay {
  height: 25%;
  padding-top: 20px;
}

.nav-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 32px;
  padding-right: 16px;
}

.nav-btn {
  width: 36px;
  height: 36px;
}

.nav-btn img {
  width: 100%;
  height: 100%;
}

.nav-labels {
  display: flex;
  align-items: center;
  gap: 22px;
}

.nav {
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0.03em;
  font-weight: 600;
  color: #1E1E1E;
  opacity: 0.3;
}

.nav.active {
  opacity: 1;
}

}
</style>
