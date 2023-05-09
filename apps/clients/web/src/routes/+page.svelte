<script lang="ts">
  import type { PageData } from "./$types";

  export let data: PageData;
</script>

<div>
  {#each data.countries_countries ?? [] as country}
    <div>{country.name}</div>
  {/each}
</div>
