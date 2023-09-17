<script>
  import MenuBtn from "./MenuBtn.svelte";
  import CloseBtn from "./CloseBtn.svelte";

  let navIsOpen = false;

  function toggleNavbar() {
    navIsOpen = !navIsOpen;
  }
</script>

<div class="self-end pt-2 pr-4 bg-violet-200">
  <MenuBtn {navIsOpen} on:openNavigation={toggleNavbar} />
  <CloseBtn {navIsOpen} on:openNavigation={toggleNavbar} />
</div>
<nav class:navIsOpen class="bg-pink-50 w-full hidden">
  <ul class="text-center">
    <li><a href="/">About</a></li>
    <li><a href="/">Products</a></li>
    <li><a href="/">Reviews</a></li>
    <li><a href="/">Contact</a></li>
  </ul>
</nav>

<style>
  .navIsOpen {
    @apply block;
  }
</style>
