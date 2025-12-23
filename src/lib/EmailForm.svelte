<script lang="ts">
  const letters = Array.from({ length: 26 }, (_, i) =>
    String.fromCharCode(97 + i)
  );

  let email = $state([""]);
</script>

<div class="flex flex-col w-full gap-2.5">
  <label for="email">Email: {email.join("")}</label>

  <div class="grid grid-cols-4 gap-1">
    {#each { length: email.length }, n}
      <select
        bind:value={email[n]}
        onchange={() => {
          email.push("");
          console.log(email.join(""));
        }}
        name="letter"
        id="letter"
      >
        <option value="" disabled hidden></option>

        {#if n > 0}
          <option value="@">@</option>
          <option value="@">.</option>
        {/if}

        {#each letters as letter}
          <option value={letter}>{letter.toUpperCase()}</option>
        {/each}
      </select>
    {/each}
  </div>

  {#if email.length > 1}
    <button
      class="btn"
      onclick={() => {
        email = [""];
      }}>Clear</button
    >
  {/if}
</div>
