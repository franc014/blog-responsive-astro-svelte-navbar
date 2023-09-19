<script>
  import { createEventDispatcher } from "svelte";
  export let navIsOpen;

  const dispatch = createEventDispatcher();

  function toggleNavbar(e) {
    dispatch("openNavigation");
  }
</script>

<button class:navIsOpen class="block" on:click={toggleNavbar}
  ><svg
    xmlns="http://www.w3.org/2000/svg"
    fill="none"
    viewBox="0 0 24 24"
    stroke-width="1.5"
    stroke="currentColor"
    class="w-10 h-10 text-slate-200"
  >
    <path
      stroke-linecap="round"
      stroke-linejoin="round"
      d="M3.75 5.25h16.5m-16.5 4.5h16.5m-16.5 4.5h16.5m-16.5 4.5h16.5"
    />
  </svg>
</button>

<style>
  .navIsOpen {
    @apply hidden;
  }
</style>
