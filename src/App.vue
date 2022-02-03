<template>
  <div id="app">Hello World!
  </div>
</template>

<script>
// const result = confirm("Are you here?");
// console.log(result);
const numberOfFilms = +prompt('How many films you watch?', '');
let personalMovieDB = {
  count: numberOfFilms,
  movie: {},
  actors: {},
  genres: [],
  privat: false
}
const a = 'What the last film?',
      b = 'How you like it film?',
      c = prompt('What the last film?', ''),
      d = prompt('How you like it film?', '');
 personalMovieDB.movie[a] = c;
 personalMovieDB.movie[b] = d;
console.log(personalMovieDB);
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0;
}
</style>
