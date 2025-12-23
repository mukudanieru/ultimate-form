<script lang="ts">
  import ThemeToggle from "./ThemeToggle.svelte";
</script>

<div class="flex flex-col justify-center items-center gap-4 w-fit">
  <h1 class="text-dark dark:text-light text-center text-2xl font-bold">
    Ultimate Form in Ohio
  </h1>

  <div class="flex justify-between items-center gap-1.5 w-full">
    <ThemeToggle />

    <div>
      <p class="text-sm text-primary-dark dark:text-primary text-right">
        Built by
        <a
          class="hover:underline underline-offset-4"
          href="https://github.com/mukudanieru"
          target="_blank"
          rel="noopener noreferrer"
        >
          mukudanieru
        </a>
      </p>

      <p class="text-sm text-primary-dark dark:text-primary text-right">
        Inspired by
        <a
          class="hover:underline underline-offset-4"
          href="https://github.com/bricesuazo/ultimate-form"
          target="_blank"
          rel="noopener noreferrer"
        >
          Brice Suazo
        </a>
      </p>
    </div>
  </div>
</div>
