<script lang="ts">
  export let imgUrl = "";
  export let links = [];
</script>

<header class="sticky bottom-0 top-0 flex items-center justify-between">
  <div class="flex-1">
    <a href="/" class="flex-2 cursor-pointer">
      <img width="150" src={imgUrl} alt="logo" class="h-auto cursor-pointer" />
    </a>
  </div>
  <div class="flex-3">
    <ul class="flex min-h-full">
      {#each links as link}
        <li class="custom-padding">
          <a
            href={link.href}
            class="nav-link text-xs text-gray-800 hover:text-gray-700"
            >{link.label}</a
          >
        </li>
      {/each}
    </ul>
  </div>
</header>

<style>
  .custom-padding {
    padding-left: 0.7rem;
    padding-right: 0.7rem;
  }
</style>
