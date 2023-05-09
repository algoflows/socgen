<script lang="ts">
  export let imgUrl = "";
  export let links = [];

  let innerWidth = 0;
  let innerHeight = 0;

  $: condition = innerWidth * 1.8 <= innerHeight;
</script>

<svelte:window bind:innerWidth bind:innerHeight />

<header class="sticky top-0 bottom-0 flex items-center justify-between">
  <div class="flex-1">
    <a href="/" class="cursor-pointer flex-2">
      <img
        width="200"
        class:image-conditional={condition}
        src={imgUrl}
        alt="logo"
        class="w-full h-auto cursor-pointer"
      />
    </a>
  </div>
  <div class="flex-3">
    <ul class="flex min-h-full">
      {#each links as link}
        <li class="custom-padding">
          <a
            href={link.href}
            class="text-xs text-gray-800 hover:text-gray-700 nav-link"
            >{link.label}</a
          >
        </li>
      {/each}
    </ul>
  </div>
</header>

<style>
  .image-conditional {
    width: 120px;
  }
  .custom-padding {
    padding-left: 0.7rem;
    padding-right: 0.7rem;
  }
</style>
