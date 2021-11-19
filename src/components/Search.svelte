<script>


 let onSubmit = (e) => {
    const keyword = e.target.input.value
    console.log(keyword)
    searchQuery.update()
    
 }
</script>
<div class="search-bar">
    <form on:submit|preventDefault={onSubmit}>
        <div class="search-input">
            <label for="moviesearch">Look up a movie</label>
            <input
                type="text"
                id="search"
                name="search"
                value=""
            />
        </div>
        <button type="submit">Search</button>
    </form>
</div>