<template>
  <div id="app">Hello World!
  </div>
</template>

<script>
let numberOfFilms;

function start(){
  numberOfFilms = +prompt('How many films you watch?', '');

  while (numberOfFilms ==='' || numberOfFilms == null || isNaN(numberOfFilms)){
    numberOfFilms = +prompt('How many films you watch?', '');
  }
}

start();

let personalMovieDB = {
  count: numberOfFilms,
  movie: {},
  actors: {},
  genres: [],
  privat: false
}

function detectPersonalLevel() {
  if (personalMovieDB.count < 10) {
    confirm('Просмотрено довольно мало фильмов')
  } else if (personalMovieDB.count < 31) {
    confirm('Вы классический зритель')
  } else if (personalMovieDB.count > 30) {
    confirm('Вы киноман')
  } else {
    confirm('Произошла ошибка')
  }
}

detectPersonalLevel();

function rememberMyFilms() {
  for (let i = 1; i < 3; i++) {
    const a = prompt('What the last film?', ''),
        b = prompt('How you like it film?', '');
    if (b != null && a != null && b.length < 50 && a.length < 50 && b !== '' && a !== '') {
      personalMovieDB.movie[a] = b;
    } else {
      i--;
    }
  }
}

rememberMyFilms();

function writeYourGenres () {
  for (let i = 1; i < 4; i++) {
    personalMovieDB.genres[i - 1] = prompt(`Ваш любимый жанр под номером ${i}?`, '');
  }
}

writeYourGenres();

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
