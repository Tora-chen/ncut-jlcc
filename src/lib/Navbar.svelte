<script>
  import Socials from "./Socials.svelte";
</script>

<div class="navbar bg-base-100 shadow-sm">
  <div class="flex-none">
    <label for="my-drawer" class="btn btn-square btn-ghost">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        class="inline-block h-5 w-5 stroke-current"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M4 6h16M4 12h16M4 18h16"
        ></path>
      </svg>
    </label>
  </div>

  <div class="flex-1">
    <div class="flex items-center gap-2">
      <a href="/">
        <img
          src="/src/lib/assets/logo.png"
          alt="logo"
          class="
           h-10 w-10 object-contain"
        />
      </a>
      <a href="/" class="hidden sm:inline">
        <p class="text-xl font-normal p-0 min-h-0">NCUT 日语社</p>
      </a>
    </div>
  </div>
  <div class="flex-none flex items-center gap-2">
    <span class="text-sm text-base-content/60 select-none italic"
      >在我们的社交媒体上了解更多! --&gt;</span
    >
    <nav>
      <Socials />
    </nav>
  </div>
</div>
