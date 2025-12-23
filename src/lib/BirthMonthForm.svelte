<script lang="ts">
  import { months } from "./constants.svelte";

  let month = $state("");
</script>

<div class="flex flex-col w-full gap-2.5">
  <label for="birth-month">Birth Month: {month}</label>

  <select bind:value={month} name="birth month" id="birth-month">
    <option value="" disabled hidden></option>
    {#each months as month}
      <option value={month}>{month}</option>
    {/each}
  </select>
</div>
