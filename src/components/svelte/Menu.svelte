<script>
  import { navIsOpen } from "./stores";
  import MenuBtn from "./MenuBtn.svelte";
  import CloseBtn from "./CloseBtn.svelte";
  import { fly, fade } from "svelte/transition";
  import { sineIn } from "svelte/easing";
</script>

<div class="ml-auto p-4">
  <MenuBtn />
  <CloseBtn />
</div>
{#key $navIsOpen}
  <nav
    in:fly={{ y: -200, duration: 1000, easing: sineIn }}
    out:fly={{ x: -200 }}
    class:navIsOpen={$navIsOpen}
    class="w-full hidden py-8"
  >
    <ul class="text-center text-2xl tracking-wider text-slate-200">
      <li><a href="/">About</a></li>
      <li><a href="/">Products</a></li>
      <li><a href="/">Reviews</a></li>
      <li><a href="/">Contact</a></li>
    </ul>
  </nav>
{/key}

<style>
  .navIsOpen {
    @apply block;
  }
  nav li {
    @apply py-4  border-b border-b-violet-400;
  }
</style>
