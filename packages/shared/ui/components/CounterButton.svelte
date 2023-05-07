<script lang="ts">
  let count = 0;

  function handleClick(): void {
    count += 1;
  }
</script>

<button class="px-8 py-4 border border-radius" on:click={handleClick}>
  clicks: {count}
</button>
