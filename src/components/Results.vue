<template>
  <div class="results">
    <h1>Top Movies from the 20<sup>th</sup> Century</h1>
    <p class="search-meta">
      <span class="current-page"><b>Current Page:</b> 1</span>
      <span class="total-pages"><b>Pages:</b> 777</span>
      <span class="total-results"><b>Count:</b> 3232</span>
    </p>

    <ul>
      <li class="movie-item">
        <img src="https://image.tmdb.org/t/p/w150_and_h225_bestv2/p64TtbZGCElxQHpAMWmDHkWJlH2.jpg" alt="Title of Movie Poster" class="poster-image">
        <h2 class="title"><a href="https://www.themoviedb.org/movie/78">Movie Title Goes Here</a></h2>
        <div class="ratings">
          <span class="rating-category critics-choice">Critic's Choice</span>
          <span class="rating-category well-liked">Well Liked</span>
          <span class="rating-category stinker">Stinker</span>
          <span class="vote-average">8.4</span> with <span class="vote-count">3676</span> votes
        </div>
        <p class="overview">
          Movie overivew goes here. Aenean tellus metus, bibendum sed, posuere ac, mattis non, nunc. Cras dapibus. Praesent porttitor, nulla vitae posuere iaculis, arcu nisl dignissim dolor, a pretium mi sem ut ipsum.
        </p>
        <p class="release-date">Original Release: 1999-12-31</p>
        <ul class="genre-list">
          <li>genre</li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>
import apiresults from '../apiresults.js'
export default {
  name: 'results',
  data () {
    return apiresults
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  margin: 0 0 1rem 0;
}

ul {
  list-style-type: none;
  padding: 0;
}
.search-meta {
  text-align: right;
}

.movie-item {
  margin: 10px 0;
  padding: 2rem;
  box-shadow: 4px 4px 10px rgba(0,0,0,0.2);
}

.movie-item img {
  float: left;
  margin-right: 1rem;
}

.release-date {
  font-weight: 600;
  font-size: 12px;
  color: #333;
}

.rating-category {
  font-size: 12px;
  color: #fff;
  font-weight: 800;
  background: #ccc;
  padding: 0.5rem;
  border-radius: 4px;
}


.rating-category.critics-choice {
  background: goldenrod;
}

.rating-category.well-liked {
  background: green;
}

.rating-category.stinker {
  background: brown;
}

.genre-list li {
  border-radius: 4px;
  background: #666;
  color: #fff;
  font-weight: 800;
  font-size: 12px;
  padding: 0.5rem;
  display: inline-block;
  margin-right: 10px;
}

a {
  color: #42b983;
}
</style>
