<template>
  <v-btn class="form-btn white--text my-10">
    <slot></slot>
  </v-btn>
</template>

<script>
export default {
  name: "MyButton",
};
</script>

<style scoped>
.form-btn {
  background: linear-gradient(90deg, #ff00b1 0%, #b423c1 100%);
  box-shadow: 0px 0px 10px #d70e93;
  border-radius: 4px;
  position: left;
  padding: 30px 0;
}
</style>