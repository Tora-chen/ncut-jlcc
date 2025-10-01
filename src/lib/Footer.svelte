<script>
  import Socials from "./Socials.svelte";
</script>

<footer class="footer sm:footer-horizontal bg-base-100 text-base-content p-10">
  <aside class="flex items-center gap-4">
    <img src="/logo.png" alt="logo" class="h-14 w-14 object-contain" />
    <p>
      <span>© 2025 NCUT 日语社</span><br />
      <span class="text-sm"
        >Japanese Language and Culture Club at North China University of
        Technology</span
      >
    </p>
  </aside>
  <nav>
    <span class="text-sm text-base-content/60 select-none italic"
      >在我们的社交媒体上了解更多!</span
    >
    <div class="grid grid-flow-col gap-4"></div>
    <Socials />
  </nav>
</footer>
