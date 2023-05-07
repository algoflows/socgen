<script lang="ts">
  import type { PageData } from "./$types";

  export let data: PageData;
</script>

<section>
  <img
    width="300"
    src="/src/assets/soc-gen-high-resolution-logo-color-on-transparent-background.png"
    alt="Logo"
  />
  {#each data.countries_countries ?? [] as country}
    <div>{country.name}</div>
  {/each}
</section>
