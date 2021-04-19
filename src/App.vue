<template>
  <div id="app">
    <Header msg="Gabriel" />
  </div>
</template>
<script src="https://kit.fontawesome.com/fe3e03610d.js" crossorigin="anonymous"></script>

<script>
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    Header,
  },
};
</script>