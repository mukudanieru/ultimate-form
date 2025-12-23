<script lang="ts">
  let theme = localStorage.getItem("theme");
  let isDark = $state(theme === "dark" ? true : false);
  let bodyClass = $derived(isDark ? "dark" : "");

  $effect(() => {
    document.body.classList.toggle("dark", bodyClass === "dark");
    localStorage.setItem("theme", bodyClass === "dark" ? "dark" : "light");
  });
</script>

<button
  onclick={() => (isDark = !isDark)}
  class="flex size-8 items-center justify-center hover:bg-primary-dark/10 hover:dark:bg-primary/10 rounded-md"
  title="theme-toggle"
>
  <span class="size-4 text-primary hidden dark:block">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 24 24"
      fill="none"
      stroke="currentColor"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round"
    >
      <circle cx="12" cy="12" r="4" />
      <path d="M12 2v2" />
      <path d="M12 20v2" />
      <path d="m4.93 4.93 1.41 1.41" />
      <path d="m17.66 17.66 1.41 1.41" />
      <path d="M2 12h2" />
      <path d="M20 12h2" />
      <path d="m6.34 17.66-1.41 1.41" />
      <path d="m19.07 4.93-1.41 1.41" />
    </svg>
  </span>

  <span class="size-4 text-primary-dark block dark:hidden">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 24 24"
      fill="none"
      stroke="currentColor"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round"
    >
      <path d="M12 3a6 6 0 0 0 9 9 9 9 0 1 1-9-9Z" />
    </svg>
  </span>
</button>
