<script>
  import { navIsOpen } from "./stores";
  import NavBtn from "./NavBtn.svelte";
</script>

<NavBtn>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    fill="none"
    viewBox="0 0 24 24"
    stroke-width="1.5"
    stroke="currentColor"
    class="w-10 h-10 text-slate-200 hidden"
    class:navIsOpen={$navIsOpen}
  >
    <path
      stroke-linecap="round"
      stroke-linejoin="round"
      d="M9.75 9.75l4.5 4.5m0-4.5l-4.5 4.5M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
    />
  </svg>
</NavBtn>

<style>
  .navIsOpen {
    @apply block;
  }
</style>
