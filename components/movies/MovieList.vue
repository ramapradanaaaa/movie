<template>
    <div class="row featured__filter">
      <!-- Component Item Here -->
      <app-movie-item v-for="item in movies" :data="item"></app-movie-item>
  </div>
</template>

<script>
import MovieItem from "./MovieItem.vue"

export default {
  props: ['movies'],
  components: {
    "app-movie-item": MovieItem
  },
}
</script>
