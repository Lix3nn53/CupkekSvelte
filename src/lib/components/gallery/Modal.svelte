<script>
  import { onDestroy } from "svelte";
  import { fade } from "svelte/transition";
  import { modalStore, open, close } from "./modalStore.js";

  let state = {};
  let isOpen = false;
  let props = null;
  let Component = null;
  let background;
  let wrap;

  const handleKeyup = ({ key }) => {
    if (Component && key === "Escape") {
      event.preventDefault();
      close();
    }
  };
  const handleOuterClick = (event) => {
    if (event.target === background || event.target === wrap) {
      event.preventDefault();
      close();
    }
  };

  const unsubscribe = modalStore.subscribe((value) => {
    Component = value.Component;
    props = value.props;
    isOpen = value.isOpen;
  });

  onDestroy(unsubscribe);
</script>

<svelte:window on:keyup={handleKeyup} />

<div>
  {#if isOpen}
    <div
      class="bg"
      on:click={handleOuterClick}
      bind:this={background}
      transition:fade={{ duration: 200 }}
    >
      <div
        class="window-wrap"
        bind:this={wrap}
        transition:fade={{ duration: 200 }}
      >
        <div class="content">
          <div class="close">
            <button on:click={close}>
              <i class="fas fa-times" />
            </button>
          </div>
          <svelte:component this={Component} {...props} />
        </div>
      </div>
    </div>
  {/if}
  <slot />
</div>

<style>
  * {
    box-sizing: border-box;
  }
  .bg {
    position: fixed;
    z-index: 1000;
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100vw;
    height: 100vh;
    background: rgba(0, 0, 0, 0.66);
    transition: opacity 200ms ease-in-out 0s;
    top: 0;
    left: 0;
  }
  .window-wrap {
    position: relative;
  }
  .content {
    position: relative;
  }
  .close {
    position: fixed;
    top: 10px;
    right: 25px;
    font-size: 35px;
    font-weight: bold;
    background-color: transparent;
    padding: 20px;
  }
</style>
