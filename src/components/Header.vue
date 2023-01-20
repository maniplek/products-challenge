<template>
  <div class="container">
    <div class="header-log-container">
      <img src="../assets/logos/group.logo.svg" alt="" class="mobile-logo" />
      <img src="../assets/logos/martineli-logo.svg" class="desktop-logo" />
    </div>

    <div class="login-section">
      <div class="login">
        <img class="icon" src="../assets/icons/person.icon.svg" />
        <h3 class="login-title">LOG IN</h3>
      </div>

      <img src="../assets/icons/menu-toggle.svg" alt=" " class="toggle-menu" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
@import url("https://fonts.cdnfonts.com/css/montserrat");
.container {
  background-color: #000000;
  font-family: "Montserrat", sans-serif;
  color: #ffffff;
  align-items: center;
  display: flex;
  justify-content: space-between;
}
.header-logo {
  display: flex;
  justify-content: center;
  height: 70px;
  background-repeat: no-repeat;
}
.desktop-logo {
  width: 80%;
}

.login-section {
    display: flex;
    justify-content: space-between;
    padding-right: 4%;
    gap: 20px;
}
.login {
  display: flex;
  align-items: center;
}

.login img {
  position: relative;
  height: 69%;
}
.toggle-menu {
  width: 20%;
}
.login-title {
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #ffffff;
}
.icon {
  margin-right: 13px;
  width: 17%;
}
.header-log-container {
  margin: 5px;
  padding-left: 5%;
}
.mobile-logo {
  display: none;
}

@media screen and (max-width: 666px) {
  .container {
    padding-right: 0;
    padding-right: 0;
  }
  .desktop-logo {
    display: none;
  }
  .mobile-logo {
    display: block;
  }
  .header-logo {
    height: 100%;
    padding-left: 0;
    display: block;
  }
  .header-log-container {
    padding-top: 5px;
  }
  .login-section {
    padding-left: 0;
    padding-right: 0;
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }

  .icon {
    padding-right: 0px;
    width: 0;
  }

  .login-title {
    display: none;
  }
}
</style>
