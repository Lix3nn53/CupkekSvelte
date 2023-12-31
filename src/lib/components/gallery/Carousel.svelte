<script>
  import Image from "./Image.svelte";
  import { fade } from "svelte/transition";
  import { close } from "./modalStore";
  import { debounce } from "./util.js";
  import ClickOutside from "svelte-click-outside";

  export let images;
  export let curr_idx = 0;
  let left_nav_button;
  let right_nav_button;
  const image_elements = new Array(images.length);
  let translateX = -curr_idx * window.innerWidth;

  function increment(num) {
    return num >= images.length - 1 ? 0 : num + 1;
  }

  function decrement(num) {
    return num == 0 ? images.length - 1 : num - 1;
  }

  function right() {
    curr_idx = increment(curr_idx);
    updatePosition();
  }

  function left() {
    curr_idx = decrement(curr_idx);
    updatePosition();
  }

  function updatePosition() {
    translateX = -curr_idx * window.innerWidth;
  }

  const debouncedClose = debounce(close, 100, true);

  function handleClose() {
    debouncedClose();
  }
</script>

<svelte:window on:resize={updatePosition} />
<div class="container">
  <div class="nav">
    <button class="left" on:click={left} bind:this={left_nav_button}>
      <svg role="presentation" viewBox="0 0 24 24">
        <path
          d="M15.422 16.078l-1.406 1.406-6-6 6-6 1.406 1.406-4.594 4.594z"
        />
      </svg>
    </button>
    <button class="right" on:click={right} bind:this={right_nav_button}>
      <svg role="presentation" viewBox="0 0 24 24">
        <path d="M9.984 6l6 6-6 6-1.406-1.406 4.594-4.594-4.594-4.594z" />
      </svg>
    </button>
  </div>
  <div
    class="carousel"
    style={`transform: translate3d(${translateX}px, 0, 0);`}
  >
    {#each images as image, i}
      <div class="img-container flex flex-col">
        <img {...image} bind:this={image_elements[i]} />
        <p class="text-center pt-4 text-xl font-semibold">{image.alt}</p>
      </div>
    {/each}
  </div>
</div>

<style>
  .container {
    position: relative;
  }
  .carousel {
    position: relative;
    overflow: hidden;
    display: inline-flex;
    transition: transform 100ms cubic-bezier(0.4, 0, 0.2, 1),
      opacity 100ms cubic-bezier(0.4, 0, 0.2, 1);
  }
  .nav {
    display: flex;
    box-sizing: border-box;
    -webkit-box-align: center;
    align-items: center;
    -webkit-box-pack: justify;
    justify-content: space-between;
    position: absolute;
    width: 100vw;
    height: 100%;
    z-index: 4;
  }
  .carousel img {
    height: auto;
    max-width: 80vw;
    max-height: 85vh;
    margin: auto;
    user-select: none;
  }
  :global(.carousel .click-outside-wrapper) {
    display: flex;
  }
  .img-container {
    display: flex;
    justify-content: center;
    width: 100vw;
  }
  .nav button {
    cursor: pointer;
    background: transparent;
    border: none;
    outline: none !important;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 50%;
    width: 5em;
    height: 5em;
    position: fixed;
    color: white;
    margin: 0 17px;
    bottom: 50%;
  }
  .nav button:hover {
    background: rgba(255, 255, 255, 0.3);
  }
  .nav svg {
    display: inline-block;
    fill: currentcolor;
    height: 5em;
    width: 5em;
    stroke: currentcolor;
    stroke-width: 0;
  }

  .left {
    left: 0;
  }

  .right {
    right: 0;
  }

  @media (max-width: 800px) {
    :global(.carousel img) {
      max-width: 75vw;
    }
    .nav button {
      margin: 0 12px;
      width: 4em;
      height: 4em;
      bottom: 10%;
    }
    .nav svg {
      width: 4em;
      height: 4em;
    }
  }
  @media (max-width: 550px) {
    :global(.carousel img) {
      max-width: 100vw;
    }
    .nav button {
      margin: 0 10px;
      width: 3em;
      height: 3em;
      bottom: 15%;
    }
    .nav svg {
      width: 3em;
      height: 3em;
    }
  }
</style>
