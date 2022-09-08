<script>
  import Carousel from "svelte-carousel";

  /**
   * @type {any}
   */
  let carousel; // for calling methods of the carousel instance
  export let carouselItems;

  const handleNextClick = () => {
    carousel.goToNext();
  };
</script>

<Carousel bind:this={carousel} autoplay={true} autoplayDuration={2000}>
  {#each carouselItems as item}
    <li>
      <div class="background">
        <div class="text">{item.text}</div>
        <div class="image">
          <img src={item.image} alt="item" />
        </div>
      </div>
    </li>
  {/each}
</Carousel>

<style>
  .background {
    padding-top: 14px;
    padding-right: 6px;
    background: linear-gradient(rgb(255, 255, 255) 46%, #c8c4c4 100%),
      rgb(255, 255, 255);
    border-left-style: none;
    height: 360px;
  }

  .text {
    color: #b11226;
    width: 278px;
    height: 59px;
    margin-bottom: -14px;
    font-weight: bold;
    padding-left: 20px;
    padding-bottom: 20px;
  }

  .image {
    scale: 60%;
    margin-top: 0px;
    position: relative;
    top: -100px;
    left: -350px;
    /* padding-left: 20px; */
  }
</style>
