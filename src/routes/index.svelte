<script>
  import Image from "svelte-image";
  import { Carousel, CarouselItem, CarouselControl, CarouselIndicators } from "sveltestrap";
  let HSLSocial = "HSLSocial.jpg";
  let activeIndex = 0;

  let items = [
    {
      title: "Latest Video",
      caption: "Groundhog Killshot Compilation...Exploding Varmints Vol. 2!!!",
      img: "https://i.ytimg.com/vi/AS7Orz3TI6I/hqdefault.jpg",
      type: "youtube",
    },
    {
      title: "Latest Podcast",
      caption: "Custom AR Builds - Tips and Tricks",
      img: HSLSocial,
      type: "podcast",
    },
  ];
  /*let items = [<div class="slide-content" bind:activeIndex itemIndex={0}>
        <h2>Latest Video</h2>
        <h3>Groundhog Killshot Compilation...Exploding Varmints Vol. 2!!!</h3>
        <img alt="" src="https://i.ytimg.com/vi/AS7Orz3TI6I/hqdefault.jpg" />
      </div>,
      <div>
        <h2>Latest Podcast</h2>
        <h3>Custom AR Builds - Tips and Tricks</h3>
        <img alt="" src={HSLSocial} />
      </div>]*/
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
  .carousel-inner { 
    min-width: 100vw;
    background-color: rgba(128,128,128,0.6);
    padding: 25px;
  }
  .carousel-item > div {
    display: flex;
    flex-direction: row;
    justify-content: center;

  }
</style>

<svelte:head>
  <title>Hunt Shoot Live</title>
</svelte:head>

<div id="latest-content">
  <Carousel {items} ride bind:activeIndex interval={100} class='carousel'>
    <CarouselIndicators bind:activeIndex {items} />
    <div class="carousel-inner">
      {#each items as item, index}
        <CarouselItem bind:activeIndex itemIndex={index}>
          <div
            class={item.type === 'youtube' ? 'youtube-preview' : 'podcast-preview'}>
            <img src={item.img} alt={`${item.title}`} />
            <div class='card-content'>
              <h2>{item.title}</h2>
              <h3>{item.caption}</h3>
            </div>
          </div>
        </CarouselItem>
      {/each}
    </div>
    <CarouselControl direction="prev" bind:activeIndex {items} />
    <CarouselControl direction="next" bind:activeIndex {items} />
  </Carousel>
</div>
