<script setup lang="ts">
import Form from "./components/Form.vue";
</script>

<template>
  <h2>Peliculas</h2>
  <Form />
</template>

<style lang="scss">
@import "./styles/variables";

html,
body {
  background: $bg;
  color: $color;
  margin: 0;
  font-family: sans-serif;
}

h2 {
  border-bottom:
    1px solid $color;
  padding-bottom: 10px;
}
</style>
