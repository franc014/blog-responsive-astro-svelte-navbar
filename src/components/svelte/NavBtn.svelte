<script>
  import { navIsOpen } from "./stores";

  function toggleNavbar() {
    navIsOpen.update((open) => !open);
  }
</script>

<button on:click={toggleNavbar}>
  <slot />
</button>
