# NCUT 日语社

北方工业大学日语社网站, 使用 [`svelte`](https://svelte.dev/) 开发。

## 快速开始

你可以使用云开发环境，也可以在本地搭建开发环境。

### A. 使用云开发环境（更简单）
1. 注册 [腾讯云原生构建（CNB）](https://cnb.cool)；
2. 联系项目管理者，邀请你加入本项目组织；
3. 选择本项目仓库，点击`云原生开发`；
4. 等待环境初始化完成后，即可开始开发！


### B. 搭建本地开发环境（更可靠）

#### 1. 下载编辑器
  
编辑器是你编写代码的工具，推荐使用 [Visual Studio Code↗](https://code.visualstudio.com/)。

#### 2. 安装Git和Node.js
参照[Git官网↗](https://git-scm.com/)和[Node.js官网↗](https://nodejs.org/)的说明安装`Git`和`Node.js`。

#### 3. 克隆项目代码
打开终端，执行以下命令克隆项目代码到本地：
```sh
git clone https://github.com/Tora-chen/ncut_jlcc.git

cd ncut_jlcc

code .
```

执行完之后，你应该可以在VS Code中看到项目代码了。

#### 4. 安装依赖
打开终端，执行以下命令安装项目依赖：
```sh
npm install
```

### 本地开发
启动本地开发服务器：
```sh
npm run dev
```

打开浏览器，访问 `http://localhost:5173` ，你应该就可以看到我们的网站了。


不过，开发服务器的预览，有时并不能代表你部署后看到的网站的样子。在你准备好发布网站时，执行以下命令预览生产版本：
```sh
npm run build
```
```sh
npm run preview
```

## 目录结构

项目主要目录和文件说明如下：

```
.
├── .devcontainer/      # VS Code 远程开发配置
├── .github/            # GitHub 相关配置
├── .svelte-kit/        # SvelteKit 构建输出（自动生成）
├── docs/               # 项目文档
├── node_modules/       # 项目依赖
├── src/                # 源代码目录
│   ├── routes/         # 路由页面（每个页面一个文件夹或文件）
│   ├── lib/            # 可复用组件
│   └── assets/         # 图片等静态资源
├── static/             # 直接暴露的静态文件（如 logo、robots.txt）
├── .editorconfig       # 代码风格配置
├── .gitignore          # Git 忽略文件，记录哪些文件不纳入版本控制
├── svelte.config.js    # Svelte 配置
├── vite.config.js      # Vite 配置
├── tsconfig.json       # TypeScript 配置
├── package.json        # 项目依赖和脚本（自动生成）
└── README.md           # 项目说明
```

参考[Svelte 项目结构↗](https://svelte.dev/docs/kit/project-structure)了解更多。

## 发布/部署

本项目为纯静态网站，可以部署到 GitHub Pages、Vercel、Edge One 等静态网站托管平台。

参考：

[SvelteKit 部署文档↗](https://svelte.dev/docs/kit/building-your-app)

[GitHub Pages↗](https://pages.github.com/)

[Vercel↗](https://vercel.com/)

[Edge One↗](https://www.tencentcloud.com/products/edgeone)


