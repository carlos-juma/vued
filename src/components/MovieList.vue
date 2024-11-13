<template>
    <div>
      <MovieItem v-for="(movie, index) in movies" :key="index" :movie="movie" @delete="deleteMovie(index)" />
    </div>
  </template>
  
  <script>
  import MovieItem from './MovieItem.vue';
  
  export default {
    components: {
      MovieItem
    },
    props: ['movies'],
    methods: {
      deleteMovie(index) {
        this.movies.splice(index, 1);
      }
    }
  }
  </script>
  