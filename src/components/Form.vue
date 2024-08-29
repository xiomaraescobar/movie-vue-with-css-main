<script setup lang="ts">
import { ref } from "vue";

const movies = ref([

  {
    name: "Baturu Man",
    available: 8,
    quantity: 0,
  },
  {
    name: "Journey Rabbit",
    available: 2,
    quantity: 0,
  },
  {
    name: "panter pink",
    available: 3,
    quantity: 0,
  },
  {
    name: "River Gens, Mid Game",
    available: 5,
    quantity: 0,
  },
]);
</script>

<template>
  <form v-for="(movie, i) in movies" :key="i">
    <h4>{{ movie.name }}</h4>
    <button type="button" @click="movie.quantity--" :disabled="movie.quantity <= 0">
    -
    </button>
    {{ movie.quantity }}
    <button type="button" @click="movie.quantity++" :disabled="(movie.quantity >= movie.available)">
    +
    </button>
  </form>
</template>


<style lang="scss" scoped>
@import "../styles/_variables";

form {
  background: $bg;
  border: 1px solid $color;
  margin: 0 50px 25px;
  font-family: courier;
  padding: 10px 25px 25px;
  text-align: center;
  transform: scale(1);
  transition: 0.3s transform;

  &:hover {
    transform: scale(1.2);
  }
}

button {
  background: $color2;
  border: 1px solid $color;
  cursor: pointer;
  padding: 5px 10px;

  &:hover {
    border-color: $color2;
  }
}

button[disabled] {
  opacity: 0.5;
}
</style>
