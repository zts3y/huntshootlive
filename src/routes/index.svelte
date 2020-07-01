<script>
  import Image from 'svelte-image';
  let HSLSocial = "HSLSocial.jpg";
</script>

<style>
  #latest-content {
	display: flex;
	justify-content: space-evenly;
  }
  #latest-content > div {
	  width: 430px;
	  padding: 16px;
	  margin: 16px 0px;
	  background: var(--light-grey);
	  border-radius: 10px;
	  display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .youtube-preview img {
    width: 430px;
    height: 218px;
    object-fit: cover;
  }
  .podcast-preview img {
	 
    height: 218px;
    object-fit: contain;
  }
</style>

<svelte:head>
  <title>Hunt Shoot Live</title>
</svelte:head>

<div id="latest-content">
  <div class="youtube-preview">
    <h2>Latest Video</h2>
    <h3>Groundhog Killshot Compilation...Exploding Varmints Vol. 2!!!</h3>
    <img alt="" src="https://i.ytimg.com/vi/AS7Orz3TI6I/hqdefault.jpg" />
  </div>
  <div class="podcast-preview">
    <h2>Latest Podcast</h2>
    <h3>Custom AR Builds - Tips and Tricks</h3>
    <img
      alt=""
      src={HSLSocial} />
  </div>
</div>
