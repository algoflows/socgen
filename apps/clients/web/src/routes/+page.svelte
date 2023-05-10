<script lang="ts">
  import type { PageData } from "./$types";

  export let data: PageData;
</script>

<div>
  <h1>Hi there.</h1>
  {#each data.countries_countries ?? [] as country}
    <div>{country.name}</div>
  {/each}
</div>
