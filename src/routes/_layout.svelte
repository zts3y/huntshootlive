<script>
  import Nav from "../components/Nav.svelte";
  let bgImage = "background.jpg";
  export let segment;
</script>

<style>
  main {
    position: relative;
    max-width: 100vw;
    height: calc(100vh);
    background-color: #21201F;
    margin: 0 auto;
    box-sizing: border-box;
  }
  header {
    display: flex;
    flex-direction: column;
    justify-items: center;
    min-height: 300px;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 100% 34%;
  }
  #hero {
	height: calc(300px - 53px);
	display: flex;
	justify-content: center;
  }
  #hero #logo{
	 
	  padding: 1em;
  }
</style>

<main>
  <header style="background-image: url('{bgImage}')">
    <Nav {segment} />
    <div id="hero">
      <img id="logo" alt="Hunt Shoot Live Logo" src="Badge.svg" />
    </div>
  </header>
  <slot />
</main>
