<template>
 
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
                  <td class="first-col">{{ item.name }}</td>

                  <td>{{ item.descrption }}</td>
                </tr>
              </tbody>
            </table>
          </div>
        
        <div class="info-image">
          <img src="../../assets/images/Bitmap.png" alt="Snow" class="infoImage" />
        </div></div>
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
  padding-left: 90px;
  padding-top: 44px;
  background: #F5F5F4;
}

.information {
  display: flex;
  justify-content: space-between;
}

.info-image {
    width: 50%;
    height: 300px;
    padding-left: 55px;
}

.info-image img {
        margin-bottom: 9px;
    width: 100%;
}

.organic-cotton {
    display: flex;
    justify-content: space-between;
    gap: 5%;
    padding-top: 80px;
}
.oraganic-img {
  width: 100%;
  padding-top: 20px;
  padding-bottom: 64px;
}
.organic-cotton-section {
    padding-right: 53px;
    width: 50%;
}
.organic-text {
    font-family: 'Raleway';
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 150%;
    letter-spacing: 0.03em;
    color: #1E1E1E;
}
.organic-title {
    padding-top: 70px;
    padding-right: 164px;
    font-family: 'Bodoni Moda';
    font-style: normal;
    font-weight: 700;
    font-size: 30px;
    line-height: 50px;
    color: #1E1E1E;
}
.table {
    padding-right: 136px;
    display: flex;
    width: 50%;
    padding-top: 10px;
    font-family: 'Raleway';
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    color: #1E1E1E;
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

.first-col{
  font-family: 'Raleway';
font-style: normal;
font-weight: 700;
font-size: 16px;
line-height: 24px;
}
.main-title {
    text-transform: uppercase;
    font-size: 24px;
    line-height: 34px;
    letter-spacing: 2px;
    border-bottom: 1px solid black;

}
.horizontal-line {
  margin-top: 4px;
}

.head-title {
  display: flex;
  width: auto;
}
.organic-cotton-image {
  width: 50%;
}

@media screen and (max-width: 666px) {
  .container {
    display: flex;
    flex-direction: column;
    padding-left: 16px;
    padding-right:16px
  }
  .info-image{
    width: 100%;
    padding-left:0;
  }

  .info-image img{
width: auto;
}
  .organic-cotton{
    display: flex;
    flex-direction: column-reverse;
    padding-right: 0;
  }
  .information{
    width: 100%;
    display: flex;
    flex-direction: column;
  }
  .organic-cotton-image{
    width: 100%;
  }
  .organic-cotton-section{
    width:100%;
       padding-right: 0;
  }
  .organic-title{
       padding-right: 0;
    margin-bottom: 10%;
    font-size: 40px;
  }
  .table{
    display: flex;
    width: 100%;
    padding-top: 10px;
    padding-right: 1%;
    margin-bottom: 10%;
  }
  .table-row tr td:last-child {
    text-align: right;
  }
  .main-title{
    font-size: 16px;
    line-height: 24px;
  }
  .oraganic-img{
        padding-top: 35px;
  }
}
</style>
