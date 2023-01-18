<template>
  <div class="container">
    <div class="header-logo">
      <div class="header-log-container">
        <img src="../assets/logos/group.logo.svg" alt="" class="mobile-logo" />
        <img src="../assets/logos/martineli-logo.svg" class="desktop-logo" />
      </div>
    </div>

    <div class="login-section">
      <div class="login">
        <img class="icon" src="../assets/icons/person.icon.svg" />
        <h3 class="login-title">LOG IN</h3>
      </div>
      <div class="toggle-menu">
        <img src="../assets/icons/menu-toggle.svg" alt=" " />
      </div>
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
  width: 100%;
  background-color: #000000;
  font-family: "Montserrat", sans-serif;
  color: #ffffff;
  display: flex;
  justify-content: space-between;
  overflow: hidden;
  height: 70px;
}
.header-logo {
  display: flex;
  justify-content: center;
  height: 70px;
  background-repeat: no-repeat;
}

.login-section {
  gap: 50px;
  padding: 3px;
  display: flex;
  justify-content: flex-end;
}
.login {
  display: flex;
  justify-content: space-between;
  padding: 10px;
}

.login img {
  position: relative;
  top: 1.5px;
  height: 50%;
}
.toggle-menu {
  padding-right: 46.25px;
  padding-left: 2.5px;
}
.login-title {
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #ffffff;
}
.icon {
  padding-right: 13px;
}
.header-log-container {
  margin: 5px;
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
  .mobile-logo{
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
  }

  .login-title {
    display: none;
  }


}
</style>
