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
              <div class="color black"></div>
              <div class="color red"></div>
              <div class="color grey"></div>
              <div class="color green"></div>
              <div class="color red"></div>
              <div class="color grey"></div>
              <div class="color black"></div>
              <div class="color red"></div>
              <div class="color grey"></div>
              <div>+20</div>
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
  padding-left: 108px;
  padding-right: 108px;
  padding-top: 64px;
  padding-bottom: 64px;
}
.product {
  display: flex;
  justify-content: space-between;
}
.product-title {
  font-family: "Bodoni Moda";
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
}
.link {
  font-family: "Raleway";
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 150%;
  letter-spacing: 0.03em;
  text-decoration-line: underline;
  color: #1e1e1e;
  padding-top: 5px;
}

.product-image {
  width: 470px;
  height: auto;
  margin-right: 38px;
}

.color-selection {
  padding-top: 15px;
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
  padding: 1px;
}
.btn-log-in {
  margin: 20px;
  width: 150px;
  height: 35px;
  color: #ffffff;
  border-radius: 80px;
  background: #1e1e1e;
  border-radius: 80px;
}
.btn-Sign-up {
  margin: 20px;
  width: 150px;
  height: 35px;
  background: #ffffff;
  border-radius: 80px;
}

.color {
  display: flex;
  justify-content: space-between;
  gap: 10px;
  width: 10%;
  font-size: 14px;
  padding-bottom: 15px;
  margin: 1px;
  padding: 3px;
  height: 10px;
  width: 15px;
  border-radius: 100%;
  margin-bottom: 20px;
}
.red {
  background-color: rgb(142, 139, 139);
}

.grey {
  background-color: rgb(43, 32, 32);
}

.green {
  background-color: rgb(137, 168, 0);
}

.black {
  background-color: rgb(244, 168, 168);
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
  width: 20px;
  height: 20px;
}

.product-photo {
  position: relative;
}

@media screen and (max-width: 666px) {
  .product-image{
    width: 100%;

  }
  .product-photo{
    width: 100%;
  }
  .product {
    display: flex;
    flex-direction: column;
  }
  .products-container{
    padding-left: 10px;
    padding-right: 10px;
  }
}
</style>
