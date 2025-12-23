<script lang="ts">
  let value = $state(20 / 2);
  let calculatedValue = $derived((value - 10) * 10);
</script>

<div class="flex flex-col w-full gap-2.5">
  <label for="gender">
    {#if calculatedValue < 0}
      Gender: {Math.abs(calculatedValue)}% Male
    {:else if calculatedValue > 0}
      Gender: {Math.abs(calculatedValue)}% Female
    {:else}
      Gender
    {/if}
  </label>

  <div class="flex flex-col gap-1">
    <input id="gender" bind:value type="range" min="0" max="20" />

    <div
      class="flex justify-between text-sm text-secondary-dark dark:text-secondary"
    >
      <span class="hover:cursor-default">Male</span>
      <span class="hover:cursor-default">Female</span>
    </div>
  </div>
</div>
