<script lang="ts">
  let random = Math.floor(Math.random() * 100);
  let guess = 50;
  let result = "TRY ?!";

  function handleSubmit(event) {
    console.log(random);
    result = guess === random 
      ? 'Bingo!' 
      : guess < random
        ? 'TRY BIGGER'
        : 'TRY LITTER'  
  }
</script>

<main>
  <p>A Template with swc</p>

  <h2>{result}</h2>
  
  <input bind:value={guess} type="number" placeholder="enter your guess">
  <button on:click={handleSubmit}>submit</button>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
