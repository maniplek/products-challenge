<template>
  <div class="footer-container">
    <div class="footer-container-1">
      <div class="section-one">
        <div class="section-one-logo"></div>
        <div class="top-right">
          <a class="top-right-item contacti hide-on-mobile">contacti</a>
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
                    <div class="services">
                          <div class="services-description">
                            Dal 1947 lo spirito imprenditoriale
                            <strong>MARTINELLIGINETTO</strong> si fonda sulle competenze tecniche,
                            l’utilizzo delle tecnologie tessili più avanzate e sulla capacità di
                            mobilitare energie professionali e creative in grado di innovare il
                            prodotto a tutti i livelli.
                          </div>
                          <Services
                            :key="service"
                            v-for="service in services"
                            :service="service"
                          />
                    </div>
      <div class="separator" />
      <Clients />
      <div class="separator hide-on-mobile" />
      <div class="footer-bottom-part hide-on-mobile">
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
import Services from "@/components/footerContents/Services.vue";
import Clients from "@/components/footerContents/Clients.vue";
export default {
  name: "Footer",
  components: {
    Services,
    Clients,
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
.insta {
  fill: #ffffff;
}

.facebook {
  fill: #ffffff;
}

.section-one {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.footer-container {
  background-color: #1e1e1e;
  color: #ffffff;
  width: 100%;
}

.section-one-logo {
  background-image: url("../assets/logos/martineli-ginetto.logo.svg");
  min-width: 220px;
  height: 100px;
  background-repeat: no-repeat;
}

.footer-container-1 {
  width: 85%;
  margin: auto;
  padding-top: 4rem;
}

.top-right {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.top-right-item {
  padding: 10px;
}

.contacti {
  text-decoration: underline;
}

.services {
  display: flex;
  justify-content: space-between;
  padding-top: 32px;
  width: 100%;
}

.services-description {
  flex-basis: 20%;
  font-size: 12px;
  line-height: 20px;
  padding: 5px;
}

.separator {
  width: 100%;
  height: 2px;
  background-color: rgba(255, 255, 255, 0.3);
}

.footer-bottom-part {
  display: flex;
  justify-content: space-between;
  padding: 2rem 0rem;
  opacity: 0.8;
  font-size: 11px;
  line-height: 28px;
  font-weight: 400;
}
.link {
  text-decoration: underline;
}

.cookie {
  padding-left: 2rem;
}

.first-separator {
  visibility: hidden;
}

@media screen and (max-width: 666px) {
  .section-one-logo {
    min-width: 180px;
    height: 40px;
    background-repeat: no-repeat;
    background-image: url("../assets/logos/martineli-gineto-group.mobile.logo.svg");
  }

  .first-separator {
    visibility: visible;
  }

  .footer-container-1 {
    width: 85%;
    margin: auto;
    padding-top: 2rem;
  }

  .top-right-item {
    padding-top: 0px;
  }

  .services {
    flex-wrap: wrap;
  }

  .services-description {
    flex-basis: 100%;
    font-size: 12px;
    line-height: 20px;
    padding: 5px;
  }

  .hide-on-mobile {
    display: none;
  }
}
</style>
