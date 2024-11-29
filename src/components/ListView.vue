<script setup>
  import { ref } from 'vue';
  const props = defineProps(['books'])
</script>
<template>
  <table class="table">
    <thead>
      <tr>
        <th>Author</th>
        <th>Title</th>
        <th>Decription</th>
        <th>Image</th>
      </tr>
    </thead>
    <tbody>
      <tr  v-for="book in props.books">
        <td>{{ book.author }}</td>
        <td>{{ book.title }}</td>
        <td>{{ book.description }}</td>
        <td>
          <img :src=book.img_url class="img-fluid" style="height:50px">
        </td>
      </tr>
    </tbody>
  </table>
</template>

<style scoped>

</style>
