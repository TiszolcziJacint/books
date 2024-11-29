<script setup>
  import { ref } from 'vue';
  import ListView from './components/ListView.vue';
  import CardView from './components/CardView.vue';
  import books from './assets/bookdata.js';

  const card = ref(false);
  let changeView = () => card.value = !card.value;
</script>
<template>
  <div class="container vw-100">
    <button class="btn btn-primary" @click="changeView">
      <span v-if="!card">Card</span>
      <span v-if="card">Table</span>
    </button>
    <ListView v-if="!card" :books="books"/>
    <CardView v-if="card" :books="books"/>
  </div>
</template>

<style scoped>

</style>
