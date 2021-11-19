<script>
  import { onMount } from 'svelte'

  let popMovies = []

  onMount(async () => {
    const res = await fetch(`https://api.themoviedb.org/3/movie/popular?api_key=20198fe77843ae9de92a02d9ce1e74c0&language=en-US&page=1`)
    let data = await res.json()
    popMovies = data.results
    console.log(popMovies)
  })
</script>

<div>
  {#each popMovies as movie}
    <div class="movie-card">
      <img src={`https://image.tmdb.org/t/p/original/${movie.poster_path}`} alt="movie poster">
      <h5>{movie.title}</h5>
      <div>

      </div>
    </div>
  {/each}
 
</div>
<style>
  .movie-card img{
    width: 300px;
  }
</style>
<!-- adult: false
backdrop_path: "/cinER0ESG0eJ49kXlExM0MEWGxW.jpg"
genre_ids: (3) [28, 12, 14]
id: 566525
original_language: "en"
original_title: "Shang-Chi and the Legend of the Ten Rings"
overview: "Shang-Chi must confront the past he thought he left behind when he is drawn into the web of the mysterious Ten Rings organization."
popularity: 10359.702
poster_path: "/1BIoJGKbXjdFDAqUEiA2VHqkK1Z.jpg"
release_date: "2021-09-01"
title: "Shang-Chi and the Legend of the Ten Rings"
video: false
vote_average: 7.9
vote_count: 2820 -->
  