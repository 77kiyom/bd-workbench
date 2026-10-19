# 修改与部署指南

仓库地址：https://github.com/77kiyom/bd-workbench

## 项目结构

```
bd-workbench/
├── workbench.html      # 工作台主页面（单文件，所有样式和脚本都在里面）
├── README.md           # 项目说明
├── GITHUB_SETUP.md     # 本文档
└── .gitignore          # Git 忽略配置
```

整个工作台就是一个 `workbench.html` 单文件，没有构建步骤、没有依赖，双击即可在浏览器打开。

## 怎么修改

### 方式一：在 GitHub 网页上直接改（最快）

1. 打开 https://github.com/77kiyom/bd-workbench
2. 点击 `workbench.html`
3. 点右上角铅笔图标进入编辑
4. 改完点 `Commit changes`

适合改文字、链接、颜色这类小改动。

### 方式二：本地改完再推（推荐，可预览）

```bash
cd "C:/Users/wujie15/WorkBuddy AI/2026-10-19-11-53-41"

# 改完 workbench.html 后
git add .
git commit -m "更新: 说明这次改了什么"
git push
```

改完直接在浏览器打开 `workbench.html` 就能看到效果，不用等推送。

### 方式三：换台电脑用

```bash
git clone https://github.com/77kiyom/bd-workbench.git
```

然后在克隆下来的目录里打开 `workbench.html` 即可。

## 常用改动位置速查

打开 `workbench.html`，按注释找位置：

| 想改什么 | 找什么 |
|---|---|
| 页面标题 | `<h1>寄样工作台</h1>` |
| 功能卡片 | 每个 `div class="card"` 块 |
| 卡片点击后的提示语 | 文件底部 script 里的 `runOrganize()` / `runBatchEntry()` / `runTracking()` |
| 快捷链接 | `ul class="link-list"` 里的 `li class="link-item"` |
| 整体配色 | `body` 的 `background` 和 `.card-action` 的 `background`（改 `#667eea` / `#764ba2` 两个色值） |
| 卡片图标 | 每个卡片里的 `div class="card-icon"` |

## 用 GitHub Pages 托管（可选）

想直接用一个网址打开工作台，不用下载文件：

1. 仓库页 → **Settings** → 左侧 **Pages**
2. **Source** 选 `Deploy from a branch`
3. **Branch** 选 `main`，目录选 `/ (root)`，点 **Save**
4. 等 1~2 分钟，访问：`https://77kiyom.github.io/bd-workbench/workbench.html`

之后每次 push，网页会自动更新。

## 工作台与 WorkBuddy 的分工

这个页面本身只是**导航入口**，不执行实际任务。点卡片会提示你去 WorkBuddy AI 对话里输入对应指令：

| 卡片 | 在 WorkBuddy 里输入 |
|---|---|
| 寄样信息整理 | 帮我跑寄样整理 |
| 批量录入生成 | 帮我跑寄样录入 |
| 快递单号同步 | 帮我同步快递单号 |

真正干活的脚本在 `~/.workbuddy-ai/skills/feishu-sample-matcher/` 下，跟这个仓库是分开的。

## 定时任务

已有三条自动化在跑（无需手动触发）：

- 寄样批量录入 — 每天 11:30
- 寄样批量录入 — 每天 18:00
- 快递单号同步 — 每天 10:30

## 遇到问题

推代码报 `Authentication failed`：GitHub 不再支持账号密码，需要用 Personal Access Token。
生成地址：https://github.com/settings/tokens → `Generate new token (classic)` → 勾 `repo` → 生成后当密码用。

其他问题直接把报错发我。
