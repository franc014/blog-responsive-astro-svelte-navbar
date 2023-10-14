<script>
  import { navIsOpen } from "./stores";
  import { scale } from "svelte/transition";

  function toggleNavbar() {
    navIsOpen.update((open) => !open);
  }
</script>

{#key $navIsOpen}
  <button
    class="absolute right-2 -top-1"
    transition:scale
    on:click={toggleNavbar}
  >
    <slot />
  </button>
{/key}
