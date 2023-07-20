<template>
  <div>
    <section class="featured">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="section-title">
              <h2>Movie List</h2>
            </div>
            <!-- Genre Component -->
            <movie-genre/>
          </div>
        </div>
        <!-- Movie List Component -->
        <movie-list :movies="movieData"/>
      </div>
    </section>
  </div>
</template>

<script>
import MovieGenre from '~/components/movies/MovieGenre.vue';
import MovieList from '~/components/movies/MovieList.vue';

export default {
  components: {
    'movie-genre': MovieGenre,
    'movie-list': MovieList
  },
  computed: {
    movieData() {
      return this.$store.state.movies;
    }
  }
};
</script>

<style>
.featured {
  padding-top: 30px;
  padding-bottom: 40px;
}
.section-title {
  margin-bottom: 20px;
  text-align: center;
}

.section-title h2 {
  color: #1c1c1c;
  font-weight: 700;
  position: relative;
}
</style>
