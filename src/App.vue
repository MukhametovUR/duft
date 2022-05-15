<template>
  <v-app>
    <Register />
  </v-app>
</template>

<script>
import Register from "./views/Register.vue";
export default {
  components: {
    Register,
  },
  name: "App",

  data: () => ({
    //
  }),
};
</script>
<style scoped>
body {
  background-color: #000;
}
</style>
