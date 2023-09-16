<script>
  import MenuBtn from "./MenuBtn.svelte";
  import CloseBtn from "./CloseBtn.svelte";

  const navIsOpen = true;
</script>

<div class="self-end pt-2 pr-4 bg-violet-200">
  <MenuBtn />
  <CloseBtn />
</div>
<nav class:navIsOpen class="bg-pink-50 w-full opacity-0">
  <ul class="text-center">
    <li><a href="/">About</a></li>
    <li><a href="/">Products</a></li>
    <li><a href="/">Reviews</a></li>
    <li><a href="/">Contact</a></li>
  </ul>
</nav>

<style>
  .navIsOpen {
    opacity: 1;
  }
</style>
