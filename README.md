# decaying-durians
###### *Not* a Rotten Tomatoes 🤢🍅 production.

![mockup1](https://user-images.githubusercontent.com/110003885/198463762-80d4f03a-c798-4ccb-8d2a-8f2693360830.png)

This is a movie searching 🔎 and filtering system 🗃 built using HTML, CSS & CSS Bootstrap and JavaScript.

### How we get our movies to insert themselves into our website!
``` javascript
function getAllMovies() {
    var moviesOutput = document.getElementById('movieOutput');
    for(var i = 0; i < movies.length; i++) {
        var movie = movies[i];
        moviesOutput.innerHTML += 
            `<div class="col-12 col-md-4 mb-5">
                    <div class="card">
                        <img ${movie.poster} class="card-img-top" alt="${movie.title} Poster">
                        <div class="card-body">
                        <h5 class="card-title">${movie.title}</h5>
                        <h6 class="card-text">${movie.year}</h6>
                        <p class="card-text">${movie.rating}</p>
                        <a href="#" class="btn" value="${i}" data-bs-toggle="modal" data-bs-target="#movieModal">Read More</a>
                        </div>
                    </div>
                </div>
            `
    }
}
```
We simply add all of our movie details into an array and run a function, that goes through each iterations of our array and inserts the appropriate information into our HTML.




### How we get our website to filter by who's starring in our movies!
``` javascript
function filterStarring() {
    var moviesOutput = document.getElementById('movieOutput');
    moviesOutput.innerHTML = " ";
    for(var i = 0;i < movies.length; i++) {
        for(j = 0; j < movies[i].starring.length; j++) {
            var movie = movies[i];
            var stars = movies[i].starring[j];
            if(starring.value === stars) {
            moviesOutput.innerHTML += 
                `
                <div class="col-4 p-2">
                        <div class="card">
                            <img ${movie.poster} class="card-img-top" alt="Movie Poster">
                            <div class="card-body">
                                <h5 class="card-title">${movie.title}</h5>
                                <h6 class="card-text">${movie.year}</h6>
                                <p class="card-text">${movie.rating}</p>
                                <a href="#" class="btn">Read More</a>
                            </div>
                        </div>
                </div>
            `
            }
        }
    }
}
```


