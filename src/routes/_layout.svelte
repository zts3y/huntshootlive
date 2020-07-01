<script>
  import Nav from "../components/Nav.svelte";
  import Image from 'svelte-image';
  let bgImage = "background.jpg";
  export let segment;
</script>

<style>
  main {
    position: relative;
    max-width: calc(100vw);
    height: calc(100vh);
    background-color: var(--dark-grey);
    margin: 0;
    box-sizing: border-box;
  }
  header {
    display: flex;
    flex-direction: column;
    justify-items: center;
    min-height: 300px;
    background-image: url('/background.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 100% 34%;
  }
  #hero {
  height: calc(300px - 53px);
  max-width: 100vw;
	display: flex;
	justify-content: center;
  }
  #hero #logo{
    max-width: calc(100vw - 2em);
	  padding: 1em 0 1em 0;
  }
</style>

<main>
  <header>
    <Nav {segment} />
    <div id="hero">
      <img id="logo" alt="Hunt Shoot Live Logo" src="Badge.svg" />
    </div>
  </header>
  <slot />
</main>
