<script lang="ts">
  function getRandomMobile() {
    const digits = Math.floor(Math.random() * 1e9)
      .toString()
      .padStart(9, "0");

    return `+63 9${digits.slice(0, 2)} ${digits.slice(2, 5)} ${digits.slice(5)}`;
  }

  let mobileNumber = $state(getRandomMobile());
  let hasConfirmed = $state(false);
</script>

<div class="flex {hasConfirmed ? 'flex-row' : 'flex-col'} w-full gap-2.5">
  {#if !hasConfirmed}
    <label for="mobile">Mobile Number:</label>

    <div class="flex flex-col gap-2.5">
      <p class="text-secondary-dark dark:text-secondary font-bold">
        {mobileNumber}

        <span class="text-muted-dark dark:text-muted-dark font-medium"
          >&lt;-- Is this your phone number?</span
        >
      </p>

      <div class="flex gap-2">
        <button
          onclick={() => {
            hasConfirmed = !hasConfirmed;
          }}
          class="btn flex-1">Yes</button
        >

        <button
          onclick={() => (mobileNumber = getRandomMobile())}
          class="btn flex-1">No</button
        >
      </div>
    </div>
  {:else}
    <label for="mobile"
      >Mobile Number:
      <span class="text-muted-dark dark:text-muted-dark font-medium"
        >{mobileNumber}</span
      >
    </label>

    <button
      onclick={() => {
        hasConfirmed = !hasConfirmed;
      }}
      class="btn rounded-full px-2! py-1! text-xs">Clear</button
    >
  {/if}
</div>
