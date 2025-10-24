<script>
  import { page } from "$app/stores";

  $: keyValue = $page.url.searchParams.get("key") ?? "";
  $: keyChars = keyValue ? keyValue.split("") : [];
</script>

<div class="min-h-screen bg-base-200 flex items-center justify-center">
  <div class="card bg-base-100 shadow-lg w-full max-w-lg">
    <div class="card-body">
      <h1 class="card-title text-2xl text-primary">Key</h1>

      {#if keyValue}
        <div class="flex flex-wrap gap-3 justify-center items-center py-4">
          {#each keyChars as char}
            <div
              class="w-14 h-16 rounded-lg flex items-center justify-center text-3xl font-extrabold border border-base-300"
            >
              {char}
            </div>
          {/each}
        </div>
      {:else}
        <p class="text-base-content/80 text-center">尚未提供 key 参数</p>
      {/if}
    </div>
  </div>
</div>
