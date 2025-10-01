<script lang="ts">
  import favicon from "$lib/assets/favicon.svg";
  import "../app.css";

  let { children } = $props();
</script>

<svelte:head>
  <title>北方工业大学日语社 | 北方工業大学日本語サークル</title>
  <meta name="description" content="我们是北方工大日语社！欢迎加入哦！" />
  <meta
    name="keywords"
    content="北方工业大学, 北方工大, 北方工業大学, NCUT,
    日语社, 日本語サークル, JLCC, Japanese Language and Culture Club"
  />
  <meta name="robots" content="index, follow" />
  <link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}
