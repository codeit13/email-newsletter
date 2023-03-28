<template>
  <EmailLayout />
</template>

<script>
import EmailLayout from "./components/EmailLayout.vue";

export default {
  name: "App",
  components: {
    EmailLayout,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: auto;
}

@media only screen and (min-width: 768px) {
  #app {
    width: 26%;
  }
}
</style>
