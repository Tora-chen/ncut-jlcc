<script>
  import Navbar from "$lib/Navbar.svelte";
  import Drawer from "$lib/Drawer.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<!-- 导航栏 -->
<Navbar />

<!-- 左侧栏 -->
<Drawer />

<!-- Hero -->
<div class="hero min-h-screen" style="background-image: url('/sushe.webp');">
  <div
    class="hero-content text-left p-0 flex justify-start items-start w-full h-full"
  >
    <div
      class="max-w-md pl-8 pt-8 sm:pl-12 sm:pt-12 md:pl-16 md:pt-16 text-left"
    >
      <h1 class="mb-3 text-4xl md:text-5xl font-bold tracking-tight">
        <span
          class="bg-gradient-to-r from-primary to-secondary bg-clip-text text-transparent drop-shadow-md"
          >北方工大日语社</span
        >
      </h1>
      <h2
        class="text-lg md:text-xl font-medium text-primary-content drop-shadow"
      >
        北方工大日本語サークル
      </h2>
      <h2
        class="mb-4 text-lg md:text-xl font-medium text-primary-content drop-shadow"
      >
        Japanese Language and Culture Club at North China University of
        Technology
      </h2>
      <blockquote
        class="mb-6 text-base md:text-lg italic text-primary-content border-l-4 border-primary pl-4"
      >
        语言是我们所知的最庞大、最广博的艺术，是一代代人无意识地创造出的宏伟而无名的作品。<br
        />
        <span class="block mt-2 text-sm text-primary-content"
          >——《语言论》( Edward Sapir 著 )</span
        >
      </blockquote>
    </div>
  </div>
</div>

<!-- 第二个 Hero -->
<section
  class="w-full bg-gradient-to-br from-blue-50 to-accent py-12 px-4 md:px-0"
>
  <div class="max-w-2xl mx-auto">
    <h2 class="text-4xl font-bold m-10 text-primary">在这里，你可以——</h2>
    <ul
      class="list-disc pl-6 space-y-6 text-lg md:text-md mx-10 text-base-content/90"
    >
      <li class="rounded transition hover:-translate-y-1 cursor-pointer p-1">
        <span class="font-semibold text-secondary">找到同好，成为社牛！</span
        ><br />
        日语社的同学们多才多艺，来这里交到和你一样或是热爱唱歌、或是喜欢配音、或是痴迷日剧的知心朋友吧！
      </li>
      <li class="rounded transition hover:-translate-y-1 cursor-pointer p-1">
        <span class="font-semibold text-secondary">一起学习，变成大佬！</span
        ><br />
        社团提供多方面的日语学习指导与实际应用场景，在这里入门或是进阶日语吧！
      </li>
      <li class="rounded transition hover:-translate-y-1 cursor-pointer p-1">
        <span class="font-semibold text-secondary">唱歌配音，不在话下！</span
        ><br />
        和大家一起学唱好听的日语歌、一起学念感人的台词！
      </li>
      <li class="rounded transition hover:-translate-y-1 cursor-pointer p-1">
        <span class="font-semibold text-secondary">练好口语，秀出口才！</span
        ><br />
        在每周的日语角和同好或留学生交流，练出你落落大方、出口成章的口语能力！
      </li>
      <li class="rounded transition hover:-translate-y-1 cursor-pointer p-1">
        <span class="font-semibold text-secondary">实用技能，统统 get ！</span
        ><br />
        想要更好的口才？想更擅长人际交往？想掌握某项工作技能？各种能力都可以在社团有锻炼自己的机会！
      </li>
    </ul>
  </div>
</section>

<Footer />
