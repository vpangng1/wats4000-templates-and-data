<template>
  <div class="results">
    <h1>Top Movies from the 20<sup>th</sup> Century</h1>
    <p class="search-meta">
      <span class="current-page"><b>Current Page:</b> 1</span><!-- TODO: Fill in current page value from data. -->
      <span class="total-pages"><b>Pages:</b> 777</span><!-- TODO: Fill in total pages value from data. -->
      <span class="total-results"><b>Count:</b> 3232</span><!-- TODO: Fill in results count value from data. -->
    </p>

    <ul>
      <li class="movie-item"><!-- TODO: Use a for loop to iterate through each result in the results array. -->
        <img src="https://image.tmdb.org/t/p/w150_and_h225_bestv2/p64TtbZGCElxQHpAMWmDHkWJlH2.jpg" alt="Title of Movie Poster" class="poster-image"><!-- TODO: Combine base URL with poster_path value in data to make the image src URL (Hint: Use v-bind.). -->
        <h2 class="title"><a href="https://www.themoviedb.org/movie/78">Movie Title Goes Here</a></h2><!-- TODO: Combine base URL with movie ID value in data to make the link href URL (Hint: Use v-bind.). -->
        <div class="ratings">
          <span class="rating-category critics-choice">Critic's Choice</span><!-- TODO: Use a conditional to determine if the vote_average is over 8. -->
          <span class="rating-category well-liked">Well Liked</span><!-- TODO: Use a conditional to determine if the vote_average is between 7 and 8. -->
          <span class="rating-category stinker">Stinker</span><!-- TODO: Use a conditional to determine if the vote_average is under 7. -->
          <span class="vote-average">8.4</span> with <span class="vote-count">3676</span> votes <!-- TODO: Fill in the vote_average and vote_count values accordingly. -->
        </div>
        <p class="overview"><!-- TODO: Fill in the movie overview from the data. -->
          Movie overivew goes here. Aenean tellus metus, bibendum sed, posuere ac, mattis non, nunc. Cras dapibus. Praesent porttitor, nulla vitae posuere iaculis, arcu nisl dignissim dolor, a pretium mi sem ut ipsum.
        </p>
        <p class="release-date">Original Release: 1999-12-31</p><!-- TODO: Fill in the release date from the data. -->
        <ul class="genre-list"><!-- TODO: Use a loop to iterate through all of the genres for this movie. -->
          <li>genre</li><!-- TODO: Fill in the genre name from the data. -->
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
