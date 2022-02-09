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
if (personalMovieDB.count < 10) {
  confirm('Просмотрено довольно мало фильмов')
} else if (personalMovieDB.count <31) {
  confirm('Вы классический зритель')
} else if (personalMovieDB.count > 30) {
  confirm('Вы киноман')
} else {
  confirm('Произошла ошибка')
}
 for (let i = 1; i < 3; i++) {
   const a = prompt('What the last film?', ''),
         b = prompt('How you like it film?', '');
   if (b != null && a != null && b.length < 50 && a.length < 50 && b !== '' && a !== '') {
     personalMovieDB.movie[a] = b;
   } else {
     i--;
   }
}
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
