<template>
  <div class="products-container">
    <div class="product">
      <div class="product-photo">
        <img
          class="product-image"
          src="../../assets/images/Captura-de-pantalla-las.png"
          alt="Snow"
        />
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
      </div>

      <div>
        <h1 class="product-title">Canapone</h1>
        <p class="product-text">
          Full-bodied and resistant double-width fabric in 100% linen. Thanks to
          linen's abrasion resistance and its pleasant feel to the touch.
        </p>
        <a class="link" href="#"> See more </a>

        <div class="color-selection">
          <h3 class="color-selection-title">Color selection</h3>

          <div>
            <div class="color">
              <div class="color one"></div>
              <div class="color two"></div>
              <div class="color three"></div>
              <div class="color four"></div>
              <div class="color five"></div>
              <div class="color six"></div>
              <div class="color seven"></div>
              <div class="color eight"></div>

              <p class="more-colors">+20</p>
            </div>

            <div class="sign-up">
              <p class="to-customize">
                To discover personalized products and custom designs log in or
                sign up
              </p>
              <div class="btn">
                <button class="btn-Sign-up">Sign up</button>
                <button class="btn-log-in">Log in</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Products",
  components: {},
  data: () => ({
    services: [
      {
        title: "SETTORI",
        contents: ["Filati", "Tessuti", "Nobilitazione", "Editoria"],
      },
      {
        title: "INNOVAZIONE",
        contents: [
          "Creatività e Design",
          "Realtà produttiva",
          "Vision Digitale",
        ],
      },
      {
        title: "Responsabilità",
        contents: ["Economica", "Ambientale", "Sociale"],
      },
      {
        title: "CARRIERA",
        contents: ["Giovani", "Scuola lavoro", "Lavora con noi"],
      },
    ],

    colors: [
      "red",
      "orange",
      "yellow",
      "green",
      "blue",
      "indigo",
      "violet",
      "purple",
    ],
  }),
};
</script>

<style scoped>
.products-container {
  background: #f5f5f4;
  padding-left: 88px;
  padding-right: 108px;
  padding-top: 64px;
  padding-bottom: 64px;
}
.product {
  display: flex;
  justify-content: space-between;
}
.product-title {
  font-family: "Bodoni Moda", serif;
  font-style: normal;
  font-weight: 700;
  font-size: 45px;
  line-height: 85px;
  color: #1e1e1e;
}

.product-text {
  font-family: "Raleway";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0.03em;
  color: rgba(30, 30, 30, 0.75);
  width: 400px;
  padding-bottom: 10px;
}
.link {

    font-family: "Raleway";
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 150%;
    letter-spacing: 0.03em;
    text-decoration-line: underline;
    color: #1e1e1e;
    padding-top: 5px;
    text-decoration-color: #1e1e1e;
}

.product-image {
  width: 570px;
  height: auto;
  margin-right: 50px;
}

.color-selection {
     padding-top: 32px;
}
.color-selection-title {
  font-family: "Raleway";
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  display: flex;
  align-items: center;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  color: #000000;
}
.more-colors{
  text-decoration: underline;
}

.sign-up {
  margin-top: 5px;
  background-color: #ffffff;
}
.to-customize {
  font-family: "Raleway";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 19px;
  color: rgba(30, 30, 30, 0.75);
  padding: 15px;
}

.btn {
display: flex;
    padding-left: 5%;
    gap: 5%;
    padding-bottom: 20px;
}
.btn-log-in {
    width: 150px;
    height: 45px;
    color: #ffffff;
    border-radius: 80px;
    background: #1e1e1e;
    border-radius: 80px;
}
.btn-Sign-up {
     width: 150px;
    height: 45px;
    background: #ffffff;
    border-radius: 80px;
  
    border: 1px solid black;
}

.color {
  display: flex;
  justify-content: space-between;
  gap: 10px;
  margin: 1px;
  padding: 3px;
  height: 18px;
  width: 276px;
  border-radius: 100%;
  margin-bottom: 20px;
}
.one {
  background: #4e6071;
  border: 2px solid #d8d8d8;
}

.two {
  background: #7b6350;
  border: 2px solid #d8d8d8;
}

.three {
  background: #a58a71;
  border: 2px solid #d8d8d8;
}

.four {
  border: 1px solid #d8d8d8;
  border: 2px solid #d8d8d8;
}
.five {
  background: #80857a;
  border: 2px solid #d8d8d8;
}

.six {
  background: #808080;
  border: 2px solid #d8d8d8;
}

.seven {
  background: #9a9ea3;
  border: 2px solid #d8d8d8;
}

.eight {
  background: #bfbfbf;
  border: 2px solid #d8d8d8;
}

.left-right-icons {
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-10);
}
.left-right-icons img {
  width: 60px;
  height: 26px;
}

.product-photo {
  position: relative;
}

@media screen and (max-width: 666px) {
  .product-image {
    width: 100%;
  }
  .product-photo {
    width: 100%;
  }
  .product {
    display: flex;
    flex-direction: column;
  }
  .products-container {
    padding-left: 10px;
    padding-right: 10px;
  }
}
</style>
