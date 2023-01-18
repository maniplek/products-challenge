<template>
  <div class="footer-container">
    <div class="footer-container-all">
      <div class="upper-section">
        <div class="upper-section-logo"></div>
                    <div class="contact">
                      <a ref="#" class="top-right-item contact-name hide-on-mobile">
                        contacti
                      </a>
                      <img
                        class="insta top-right-item"
                        src="../assets/logos/instagram.logo.svg"
                      />
                      <img
                        class="facebook top-right-item"
                        src="../assets/logos/facebook.logo.svg"
                      />
                    </div>
      </div>
      <div class="separator first-separator" />
      <div class="section-two">
              <div class="decription">
                <p class="description-words">
                  Dal 1947 lo spirito imprenditoriale
                  <strong>MARTINELLIGINETTO</strong> si fonda sulle competenze
                  tecniche, l’utilizzo delle tecnologie tessili più avanzate e sulla
                  capacità di mobilitare energie professionali e creative in grado di
                  innovare il prodotto a tutti i livelli.
                </p>
              </div>
          <div class="services">
                  <Service
                    :key="service.title"
                    v-for="service in services"
                    :service="service"
                  />
          </div>
      </div>
      <div class="section-three">
        <div class="line-separator"></div>

        <div class="companies">
          <Clients />
        </div>

        <div class="line-separator"></div>
      </div>

      <div class="last-section hide-on-mobile">
        <div>
          <a class="link privacy">Privacy</a>
          <a class="link cookie">Cookie policy</a>
        </div>
        <div>
          Martinelli Ginetto S.p.A - C.F. e Partita Iva 03403660164 Cap.Sociale
          10.000.000 I.v. REA: BG – 375519
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Service from "./footerContents/Services.vue";
import Clients from "./footerContents/Clients.vue";
export default {
  name: "Footer",
  components: {
    Clients,
    Service,
  },
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
  }),
};
</script>

<style scoped>
.footer-container {
  background-color: #1e1e1e;
  padding-left: 108px;
  padding-right: 114.35px;
}
.upper-section {
  padding-top: 56.31px;
  display: flex;
  justify-content: space-between;
}

.upper-section-logo {
  background-image: url("../assets/logos/martineli-ginetto.logo.svg");
  min-width: 220px;
  height: 100px;
  padding-bottom: 10px;
  background-repeat: no-repeat;
}
.contact {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.contact-name {
  color: white;
  padding: 20px;
  text-decoration: underline;
}

.footer-container-all {

  padding-top: 4rem;
}

.top-right-item {
  padding: 10px;
}
img {
  padding: 20px;
}
.separator {
  width: 100%;
  height: 2px;
  background-color: rgba(255, 255, 255, 0.3);
}

.decription {
  color: white;
  font-size: 12px;
  font-family: "Raleway";
  font-style: normal;
  font-weight: 300;
  font-size: 12px;
  line-height: 20px;
  width: 30%;
  padding-right: 110px;
}

.first-separator {
  visibility: hidden;
}
.section-two {
  display: flex;
  justify-content: space-between;
}

.services {
  display: flex;
  justify-content: space-between;
  gap: 10%;
  padding-right: 25%;
}
.line-separator {
 
  border-top: 2px solid rgba(255, 255, 255, 0.3);
  
}
.last-section {
  display: flex;
  justify-content: space-between;
  padding: 2rem 0rem;
  opacity: 0.8;
  font-size: 11px;
  line-height: 28px;
  font-weight: 400;
  color: #ffffff;
}

.link {
  text-decoration: underline;
}

.cookie {
  padding-left: 2rem;
}

@media screen and (max-width: 666px) {
  .footer-container{
display: block;
width: 100%;
padding: 0;
  }
  .upper-section-logo {
    min-width: 180px;
    height: 40px;
    background-repeat: no-repeat;
    background-image: url("../assets/logos/martineli-ginetto.logo.svg");
  }

  .first-separator {
    visibility: visible;
  }

  .footer-container-all {
    width: 85%;
    margin: auto;
    padding-top: 2rem;
  }

  .top-right-item {
    padding-top: 0px;
  }

  .section-two {
    flex-wrap: wrap;
  }

  .decription {
    flex-basis: 1000%;
    font-size: 12px;
    line-height: 20px;
    padding: 5px;
  }

  .hide-on-mobile {
    display: none;
  }
  .section-two{
  padding-right: 10px;
  padding-left: 10px;
  width: 100%;
  }
}
</style>
