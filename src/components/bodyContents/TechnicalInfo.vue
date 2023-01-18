<template>
  <div class="fullcontainer">
    <div class="container">
      <div>
        <div class="head-title">
          <h3 class="main-title">Technical information</h3>
        </div>

        <div class="information">
          <div class="table">
            <table class="table-row">
              <thead>
                <tr>
                  <th></th>
                  <th></th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="item in items" :key="item.id">
                  <td>{{ item.name }}</td>

                  <td>{{ item.descrption }}</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
        <div class="info-image">
          <img src="../../assets/images/Bitmap.png" alt="Snow" class="infoImage" />
        </div>
      </div>

      <div class="organic-cotton">
        <div class="organic-cotton-image">
          <img
            class="oraganic-img"
            src="../../assets/images/image12.png"
            alt="Snow"
          />
        </div>
        <div class="organic-cotton-section">
          <h2 class="organic-title">Organic cotton</h2>
          <p class="organic-text">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc
            vulputate libero et velit interdum, ac aliquet odio mattis. Class
            aptent taciti sociosqu ad litora torquent per conubia nostra, per
            inceptos himenaeos. Curabitur tempus urna at turpis condimentum
            lobortis.
          </p>
          <br />
          <p class="organic-text">
            Class aptent taciti sociosqu ad litora torquent per conubia nostra,
            per inceptos himenaeos. Curabitur tempus urna at turpis condimentum
            lobortis.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TechnicalInfo",
  data() {
    return {
      items: [
        { id: 1, name: "Pattern", descrption: "Plain" },
        { id: 2, name: "With(cm)", descrption: "29500" },
        { id: 3, name: "structure", descrption: "Sateen" },
        { id: 4, name: "Composition", descrption: "100% Cotton" },
        { id: 5, name: "Thread Count(T.C)", descrption: "600" },
        { id: 6, name: "Weight(g/m2)", descrption: "28500" },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  padding-left: 108px;
  padding-top: 44px;
}

.information {
  display: flex;
  justify-content: space-between;
}

.info-image {
  width: 50%;
  height: 300px;

  padding-left: 30px;
}

.info-image img {
margin-top:24px;
}

.organic-cotton {
  display: flex;
  justify-content: space-between;
  gap: 5%;
  padding-right: 108px;
  padding-top: 108px;
}
.oraganic-img {
  width: 100%;
  padding-top: 20px;
  padding-bottom: 64px;
}
.organic-cotton-section {
  padding-right: 20px;
  width: 50%;
}
.organic-text {
  font-weight: 500;
  font-size: 16px;
  line-height: 150%;
  letter-spacing: 0.03em;
  color: #1e1e1e;
}
.organic-title {
  font-weight: 700;
  font-size: 40px;
  line-height: 50px;
  color: #1e1e1e;
  padding-top: 70px;
  padding-right: 172px;
}
.table {
  padding-right: 20px;
  display: flex;
  width: 50%;
  padding-top: 10px;
}
.table-row td {
  border-bottom: 1px solid rgba(30, 30, 30, 0.1);
}
.table-row td {
  padding: 10px 0;
}

.table-row {
  page-break-after: always;
  border-collapse: collapse;
  border-spacing: 10px;
  width: 100%;
}
.main-title {
  text-transform: uppercase;
  text-decoration: underline;
  font-size: 24px;
  line-height: 34px;
  letter-spacing: 2px;

}
.horizontal-line {
  margin-top: 4px;
}

.head-title {
  display: block;
  width: auto;
}
.organic-cotton-image {
  width: 50%;
}

@media screen and (max-width: 666px) {
  .fullcontainer {
    display: block;
    width: 100%;
  }
  .container {
    display: flex;
    flex-direction: column;
    width: 100%;
    padding-left: 10px;
  }
  .infoImage{
    width: 100%;
  }
  .organic-cotton{
    display: flex;
    flex-direction: column-reverse;
  }
}
</style>
