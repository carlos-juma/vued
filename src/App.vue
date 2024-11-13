<script >
import MovieInput from './components/MovieInput.vue';
import MovieList from './components/MovieList.vue';
import Logo from './components/Logo.vue';

export default {
  components: {
    MovieInput,
    MovieList
  },
  data() {
    return {
      movies: ['Lorem ipsum: The Movie', 'Ted 2', 'Scarface']
    };
  },
  methods: {
    addMovieToList(newMovie) {
      this.movies.push(newMovie);
    }
  }
}
</script>


<template>
  <div class="main-div">
    <div class="logo">
      LOGO.
    </div>
    <MovieInput @add="addMovieToList" />
    <MovieList :movies="movies" /> 
  </div> 
</template>


<style>
</style>
