<script>
  export let name;
  import Nav from "./components/Nav.svelte";
  import Search from "./components/Search.svelte"
  import MovieCarousel from './components/MovieList.svelte'
  import { searchTerm } from './stores.js'

 let searchQuery

 searchTerm.subscribe(value => {
	 searchQuery = value
 })
 
</script>

<main>
  <Nav />
  <Search/>
  <MovieCarousel/>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
