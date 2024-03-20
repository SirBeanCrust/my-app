<script>
  let degrees = 0;
  let celcius = 0;
  let selcection = degrees;

  switch (selcection) {
    case degrees:
      console.log("hguj");

    case "celsius":
      console.log("hguj");
  }

  function increaseCounter() {
    celcius += 1;
  }
  function decreaseCounter() {
    celcius -= 1;
  }
  $: flameHeight = `${celcius}%`;
</script>

<!-- +page.svelte -->
<link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css"
/>

<h1>Welcome to SvelteKit</h1>

<button on:click={increaseCounter}> <i class="fas fa-arrow-up"></i> </button>

<button on:click={decreaseCounter}> <i class="fas fa-arrow-down"></i></button>

<button on:click={swap}> {celcius}°C </button>

<button on:click={swap}> {degrees} deg</button>

<button on:click={Start}> Start </button>

<div class="image-container">
  <!-- svelte-ignore a11y-img-redundant-alt -->
  <img src="/Furnace.jpeg" alt="Example Image" class="base-furnace" />
  <img
    src="/Flame.gif"
    alt="Live GIF"
    class="overlay-flame"
    style="height: {flameHeight};"
  />
</div>

<style>
  .image-container {
    position: relative;
    width: 200px;
    height: auto;
  }
  .base-furnace {
    position: relative;
    z-index: 1;
    width: 100%;
    height: auto;
  }

  .overlay-flame {
    position: absolute;
    bottom: 4%;
    left: 14%;
    z-index: 2;
    width: 67%;
  }
  .fas fa-heart {
  }
</style>
