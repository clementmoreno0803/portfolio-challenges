<template>
  <div class="container">
    <navbar></navbar>
    <presentation></presentation>
    <mapAdress></mapAdress>
    <section class="advance_link"></section>
  </div>
</template>

<script>
import mapAdress from "./components/map.vue";
import navbar from "./components/nav.vue";
import presentation from "./components/pres.vue";
export default {
  name: "App",
  components: {
    mapAdress,
    navbar,
    presentation,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@500;700&display=swap');
:root {
  --primary: rgb(42, 207, 207);
}
#app {
  display: flex;
  justify-content: center;
  box-sizing: border-box;
}
.container {
  width: 75%;
}
.titre {
  width: 50%;
}
h1{
  font-family: "Poppins";
  font-size: 4rem;
  margin: 0;
}
h2{
  font-family: "Poppins";
  font-size: 1rem;
  opacity: 0.4;
  font-weight: 500;
}
.advanced_link{
  background : rgb(158, 154, 167);
}
</style>
