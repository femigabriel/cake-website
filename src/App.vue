<template>
  <div class="app">
    <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/line-awesome/1.3.0/line-awesome/css/line-awesome.min.css"
  />
  <Header />
  <Main />
  <AboutPage />
  <StorePage />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import AboutPage from './components/AboutPage.vue'
import StorePage from './components/StorePage.vue'

export default {
  name: "App",
  components: {
    Header,
    Main,
    AboutPage,
    StorePage,
  },
};
</script>

<style>
@import url("http://fonts.cdnfonts.com/css/kaushan-script");
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
:root {
  --mainPink: #ef7998;
  --mainYellow: rgb(249, 228, 148);
  --mainWhite: #fff;
  --mainBlack: #000;
  --yellowTrans: rgba(249, 228, 148, 0.5);
  --mainGrey: rgb(238, 238, 238);
}
body {
  font-family: "Kaushan Script", cursive;
  overflow-x: hidden;
}
@media (max-width: 820px) {
  body {
  overflow-x: hidden;
}
.app{
  overflow-x: hidden;
}
}

</style>
