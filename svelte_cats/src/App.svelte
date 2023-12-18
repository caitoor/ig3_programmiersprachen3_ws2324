<script>
  import Cat from "./Cat.svelte";

  let catBreeds = [];
  let selectedBreeds = [];

  // Function to fetch all cat breeds
  async function fetchCatBreeds() {
    try {
      const response = await fetch("https://api.thecatapi.com/v1/breeds");
      const data = await response.json();
      catBreeds = data.map((breed) => ({ id: breed.id, name: breed.name }));
    } catch (error) {
      console.error("Failed to fetch cat breeds:", error);
    }
  }

  // Function to select 3 random breeds
  function selectRandomBreeds() {
    for (let i = 0; i < 3; i++) {
      const randomIndex = Math.floor(Math.random() * catBreeds.length);
      selectedBreeds = [...selectedBreeds, catBreeds[randomIndex]];
    }
  }

  // Function to fetch images for selected breeds
  async function fetchBreedImage(breedId) {
    const response = await fetch(
      `https://api.thecatapi.com/v1/images/search?breed_ids=${breedId}`,
    );
    const data = await response.json();
    return data[0].url;
  }

  async function start() {
    await fetchCatBreeds();
    selectRandomBreeds();
    for (let breed of selectedBreeds) {
      breed.imageUrl = await fetchBreedImage(breed.id);
    }
    selectedBreeds = [...selectedBreeds];
    console.log(selectedBreeds);
  }

  start();
</script>

<header>
  <h1>Random Cat Breed Images</h1>
</header>
<main>
  <div class="cat-cage">
    {#each selectedBreeds as breed}
      <Cat url={breed.imageUrl} breed={breed.name} />
    {/each}
  </div>
</main>

<style>
  .cat-cage {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
  }
</style>
