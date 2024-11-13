<template>
  <div class="input-area">
    <input type="text" v-model="newMovie" :class="{ 'red-glow': newMovie.length < 4, 'green-glow': newMovie.length >= 4 }" placeholder="Enter Movie Title">
    <button @click="addMovie" :disabled="newMovie.length < 4">Add Movie</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newMovie: ''
    };
  },
  methods: {
    addMovie() {
      this.$emit('add', this.newMovie);
      this.newMovie = '';
    }
  }
}
</script>

<style>
</style>
