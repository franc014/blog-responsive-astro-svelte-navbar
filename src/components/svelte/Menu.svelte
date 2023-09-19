<script>
  import MenuBtn from "./MenuBtn.svelte";
  import CloseBtn from "./CloseBtn.svelte";

  let navIsOpen = false;

  function toggleNavbar() {
    navIsOpen = !navIsOpen;
  }
</script>

<div class="ml-auto p-4 ">
  <MenuBtn {navIsOpen} on:openNavigation={toggleNavbar} />
  <CloseBtn {navIsOpen} on:openNavigation={toggleNavbar} />
</div>
<nav class:navIsOpen class="w-full hidden py-8">
  <ul class="text-center text-2xl tracking-wider text-slate-200 ">
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
  nav li {
    @apply py-4  border-b border-b-violet-400;
  }
</style>
