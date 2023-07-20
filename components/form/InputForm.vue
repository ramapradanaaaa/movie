<template>
  <form>
    <div class="row">
      <div class="col-lg-4 col-md-4">
        <input type="text" placeholder="Movie Name" v-model="movieData.name">
      </div>
      <div class="col-lg-4 col-md-4">
        <input type="text" placeholder="Image Link" v-model="movieData.link">
      </div>
      <div class="col-lg-4 col-md-4">
        <input type="number" placeholder="Release Year" v-model="movieData.year">
      </div>
      <div class="genre__input__checkbox">
        <label v-for="item in genres" :key="item">
          <input
            type="radio"
            name="genre"
            v-model="movieData.genre"
            :value="item"
          />
          {{item}}
        </label>
      </div>
      <div class="col-lg-12 text-center">
        <textarea
          placeholder="Your Review"
          v-model="movieData.review"
        ></textarea>
        <button type="submit" class="site-btn" v-on:click.prevent="newData">
          Add Review
        </button>
      </div>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      movieData: {
        name: "",
        link: "",
        genre: "",
        year: "",
        review: "",
      }
    };
  },
  computed: {
    genres() {
      return this.$store.state.genres
    }
  },
  methods: {
    newData() {
      this.$store.commit('addNewMovie', this.movieData);
      this.$router.push('/')
    }
  }
};
</script>


<style>
input[type="text"], input[type="number"] {
  width: 100%;
  height: 50px;
}

.genre__input input.genre__input__add {
  margin-bottom: 20px;
}

.genre__input input::placeholder {
  color: #b2b2b2;
}

.genre__input__checkbox {
  margin-bottom: 10px;
}

.genre__input__checkbox label {
  position: relative;
  font-size: 16px;
  color: #1c1c1c;
  padding-left: 30px;
  cursor: pointer;
}

.genre__input__checkbox label input {
  width: 20px;
  height: 20px;
}
</style>
