<script lang="ts">
  import { Navbar, CounterButton } from "shared/ui";

  import type { PageData } from "./$types";

  export let data: PageData;
</script>

<div class="bg-slate-100">
  <Navbar
    imgUrl="/src/assets/soc-gen-high-resolution-logo-color-on-transparent-background.png"
  />
  <CounterButton />
  {#each data.countries_countries ?? [] as country}
    <div>{country.name}</div>
  {/each}
</div>
