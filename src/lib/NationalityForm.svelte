<script lang="ts">
  import { nationalities } from "./constants.svelte";

  let idx = $state(0);
  let nationality = $derived(nationalities[idx]);
</script>

<div class="flex flex-col w-full gap-2.5">
  <label for="nationality">Nationality: {nationality}</label>
  <input bind:value={idx} type="range" min="0" max={nationalities.length - 1} />
</div>
