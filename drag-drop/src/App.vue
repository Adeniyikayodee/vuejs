<script setup>
import { ref } from 'vue';
import draggable from 'vuedraggable';
const meals = ref([
  'Hamburger',
  'Pizza',
  'Spaghetti',
  'Tacos',
  'Teriyaki Chicken',
]);
</script>

<template>
  <h1>Favorite Foods</h1>
  <draggable v-model="meals" tag="ul">
    <template #item="{ element: meal }">
      <li>{{ meal }}</li>
    </template>
  </draggable>
</template>




