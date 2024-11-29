<template>
  <div class="row">
    <div class="card col-md-3 m-1"  v-for="book in props.books">
      <img :src=book.img_url class="img-fluid">
      <div class="card-body">
        <h2 class="card-title">{{ book.title }}</h2>
        <p>{{ book.author }}</p>
        <p class="card-text">{{ book.description }}</p>
      </div>
    </div>
  </div>
</template>
<script setup>
  const props = defineProps(['books'])
</script>

<style scoped>

</style>
