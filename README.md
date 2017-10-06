# Displaying Data in Vue.js Templates
> A project to practice working with data in templates.

This project provides you with a simulated data set pulled from
[The Movie Database](https://www.themoviedb.org). The goal of the project is to
create a "Search Results" page that shows the most popular movies of the 20th
Century. We only have the first page of data to work with in this project, but
our goal will be to process the data for this page into our template just like
we would do if we were using a real API call.

(**Please note:** Although this data
is originally pulled from [TMDb](https://www.themoviedb.org), this
project does not use a live API connection. No additional data or upddated
information will be pulled in unless you register on TMDb and implement a real
API request).

In order to complete this project, you will need to complete the Basic
Requirements outlined below. Additional help and information about how to
complete the project is available in [Section 7 of the Practical JavaScript 2:
Building Applications](https://shawnr.gitbooks.io/practical-javascript-2-building-applications/working-with-templates/) book. Please refer to the text for background, context,
and detailed instructions.

For the most part, the requirements ask you to fill the provided template with
data from the template context (the simulated API results). This will require
you to use many features of Vue.js templates, and you will need to edit the
template in the `Results.vue` file in order to accomplish these goals. You will
use various directives to loop through parts of the data and/or conditionals to
modulate the display.

Be sure to look at the `src/apiresults.js` file in order to see the JSON object
that you will be working with for this project. This is a captured response from
TMDb, and you can see more about the different data points on the
documentation page for the [TMDb Discover API endpoint](https://developers.themoviedb.org/3/discover).

Refer to the TODOs in the `src/components/Results.vue` file for additional
information about where data goes and what to do in this project.

## Basic Requirements
Fulfill the following requirements in order to successfully complete this
assignment.

* Fill in the template for the Results component (`src/components/Results.vue`) with dynamic data
* Populate the `curent-page` value
* Populate the `total-pages` value
* Populate the `total-results` value
* Create a loop that processes each of the items in the `results` Array
* Display the following information to the user in the appropriate locations of the template:
    * Title
    * Overview
    * Poster image (note that the base URL for poster images is: `https://image.tmdb.org/t/p/w150_and_h225_bestv2/`)
    * Release date (no need to format the date in a different way)
* Use a conditional to determine whether this is a "Critic's Choice", "Well-Liked", or "Stinker"
    * "Critics Choice" are movies where the `vote_average` is over 8
    * "Well Liked" are movies where the `vote_average` is between 7 and 8
    * "Stinkers" are movies where the `vote_average` is lower than 5
    * Display the `vote_average` and `vote_count` in the proper locations
* Use another loop to display a genre list with each movie
* Link the title back to the proper movie info page on TheMovieDatabase.org using the base URL (`https://www.themoviedb.org/movie/`) and the movie ID

## Stretch Goals
* Figure out how to apply the "backdrop" image in some appealing way as a background for each movie
* [Look up how to write a filter](https://vuejs.org/v2/guide/filters.html) to format the Release Date value and make it look nicer
* Create a better simulation of pagination than the existing metadata at the top of the page
* Alter the base URL of the poster images to pull larger or smaller images (be sure to keep them in proper scale)
* Enhance some of the styles to give this project a nicer visual appeal
* Modify the template to make the ratings information be displayed as a percentage bar (or as a circle diagram, or something else).

## Build Setup
This project was created with the Vue-CLI. In order to get it running, use the following commands.

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## Credits
This project uses data originally retreived from [The Movie Database](https://www.themoviedb.org). Their API is easy to use and has liberal terms, making it fun for education and experimentation. You can see how this data is used on their site by looking up [movies like this](https://www.themoviedb.org/movie/335984-blade-runner-2049).