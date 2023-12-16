<script lang="ts">
  let tiers = ["S", "A", "B", "C", "D"];
  let stripLength = tiers.length

  //todo: make importing of files possible, change the css so that the whole vertical space gets used, change colors, style the buttons
</script>

<main>
  <div>
    <button>Import files</button>
    <button>How does it work?</button>
  </div>

  <div class="grid">
    <div>
      {#each tiers as tier, _}
        <div class="box">
          {tier}
        </div>
      {/each}
    </div>
    <div>
      {#each Array(stripLength) as _,i}
        <div class="stripe">
        </div>
      {/each}
    </div>
  </div>
  
</main>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@100;300&display=swap" rel="stylesheet">

<style>
  :root{
    --height: 200px;
  }

  main{
    font-family: "Roboto", sans-serif;
  }

  .grid {
    display: grid;
    grid-template-columns: 1fr 13fr;
    grid-gap: 0px;
    height: 100vh;
  }

  .box {
    width: var(--height);
    height: var(--height);
    border: solid 2px black;
    background-color: white;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .stripe {
    width: 100%;
    height: var(--height);
    border: solid 2px black;
    background-color: lightgrey;
    margin: 0px;
  }
</style>
