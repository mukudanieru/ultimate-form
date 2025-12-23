<script lang="ts">
  let age = $state(69);
</script>

<div class="flex flex-col w-full gap-2.5">
  <label for="age">Age: {age}</label>

  <div class="grid grid-cols-10 gap-2">
    {#each { length: 100 }, number}
      <div class="flex items-center gap-1">
        <input
          id="age-{number}"
          type="radio"
          value={number}
          name="age"
          bind:group={age}
        />
        <label
          class="font-medium! text-sm! text-secondary-dark! dark:text-secondary!"
          for="age-{number}">{number}</label
        >
      </div>
    {/each}
  </div>
</div>
