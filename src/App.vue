<template>
  <div id="app">
    <Header msg="Gabriel" />
    <Menu />
    <Content />
    <Footer />
  </div>
</template>
<script src="https://kit.fontawesome.com/fe3e03610d.js" crossorigin="anonymous"></script>

<script>
import Header from "./components/Header.vue";
import Menu from "./components/Menu.vue";
import Content from "./components/Content.vue";
import Footer from "./components/Footer.vue";


export default {
  name: "App",
  components: {
    Header,
    Menu,
    Content,
    Footer
  },
};
</script>