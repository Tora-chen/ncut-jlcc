<script>
  import { onMount } from "svelte";
  // onMount 是 Svelte 的生命周期函数，它会在组件被渲染到 DOM 后执行。
  onMount(() => {
    // 此时 guardContainer 元素已经存在于页面上
    // GuardFactory 是由我们在 app.html 中引入的脚本所创建的全局变量
    let guard = new GuardFactory.Guard({
      appId: "6717834b204b7b910e18ffe8", // 替换成你的 App ID
    });

    // 挂载 Authing Guard 到我们绑定的 div 元素上
    guard.start("#authing-guard-container");

    guard.on("login", (userInfo) => {
      console.log(userInfo);
    });
  });
</script>

<div id="authing-guard-container"></div>
