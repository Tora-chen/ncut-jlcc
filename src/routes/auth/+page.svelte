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
      handleLogin(userInfo);
    });
  });

  let secretKey = "";
  let errorMessage = "";
  let isLoading = false;

  async function handleLogin(userInfo) {
    isLoading = true;
    try {
      // 从登录成功返回的用户信息中获取 token
      const token = userInfo.token;

      // 发送 GET 请求到你的 Cloudflare Worker
      const response = await fetch(
        "https://ncut-jlcc-woker.interactionchen.workers.dev/",
        {
          method: "GET",
          headers: {
            // 将 token 放入 Authorization 请求头
            Authorization: `Bearer ${token}`,
          },
        },
      );

      // 检查响应是否成功
      if (response.ok) {
        // 如果成功 (HTTP 状态码 200-299), 读取响应体中的文本作为密钥
        const key = await response.text();
        secretKey = key;
      } else {
        // 如果服务器返回错误 (例如 401 Unauthorized)
        const errorText = await response.text();
        errorMessage = `获取密钥失败: ${response.status} - ${errorText}`;
        console.error(errorMessage);
      }
    } catch (error) {
      // 处理网络请求本身发生的错误
      errorMessage = `网络请求异常: ${error.message}`;
      console.error(errorMessage);
    } finally {
      // 请求结束后，无论成功或失败，都取消加载状态
      isLoading = false;
    }
  }
</script>

<div id="authing-guard-container"></div>
<div class="result-container">
  {#if isLoading}
    <p>正在从服务器获取密钥...</p>
  {/if}

  {#if secretKey}
    <div class="success-box">
      <h2>✅ 成功获取密钥：</h2>
      <pre><code>{secretKey}</code></pre>
    </div>
  {/if}

  {#if errorMessage}
    <div class="error-box">
      <h2>❌ 发生错误：</h2>
      <p>{errorMessage}</p>
    </div>
  {/if}
</div>
