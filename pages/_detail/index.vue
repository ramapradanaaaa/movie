<template>
    <div>
      <movie-detail/>
    </div>
</template>

<script>
    import MovieDetail from '~/components/movies/MovieDetail.vue';
    export default {
        components: {
          'movie-detail': MovieDetail
        }
    }
</script>
