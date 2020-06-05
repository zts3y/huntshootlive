<style>
  #latest-content {
	display: flex;
	justify-content: space-evenly;
  }
  #latest-content > div {
	  width: 480px;
	  padding: 16px;
	  margin: 16px 0px;
	  background: #B3B6B9;
	  border-radius: 10px;
	  display: flex;
	  flex-direction: column;
  }
  .youtube-preview img {
    width: 480px;
    height: 268px;
    object-fit: cover;
  }
  .podcast-preview img {
	 
    height: 268px;
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
      src="https://d3t3ozftmdmh3i.cloudfront.net/production/podcast_uploaded/5180499/5180499-1588528501392-1d2f4507c8e23.jpg" />
  </div>
</div>
