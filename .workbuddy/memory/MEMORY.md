# 项目长期记忆 · zhaiyingchang.com

## 项目
翟英昌（Kevin Zhai）的个人简历网站。暗黑紫罗兰设计、FDE 定位、CSV 驱动、单文件 HTML。
- 入口：`index.html`（由 `build.py` 生成，勿手改）；内容编辑 = 改 `data/*.csv` → 跑 `build.py`
- 构建命令：`/Users/apple/.workbuddy/binaries/python/envs/default/bin/python build.py`（venv 已装 jinja2）
- 目标发布方式：WorkBuddy 资料库轻应用（HTML 节点 + data/ 9 CSV + README + assets 子节点）

## 内容强制规则（改 CSV 时不可违反）
- 语言区：TypeScript 第 1、Rust 第 2；无 CSS
- 框架区：无 Vue/Vite/Storybook/Nuxt；Rails 固定第 4
- AI 工具区：WorkBuddy 第 1、Claude Code 第 2；无 Cursor
- 其它技能：无 Playwright/Docker/RESTful
- 整站无「工作经历」区块；简介含「前新东方讲师」与「英文工作语言」
- 头像圆形；Hero 大字 Kevin Zhai ≥2 次；Vue 可在项目经验中出现（真实历史栈）
- 中文 CSV 用 VSCode/Numbers/Python 编辑（Excel 会乱码）

## 关键技术决策
- 头像白底 → `mix-blend-mode: multiply` + `brightness(1.1)` 融入暗色
- reveal 渐进增强：`.reveal` 默认可见；JS 成功加 `html.anim` 才隐藏；IO + 900ms 保险 + 400ms 自终止 interval 兜底
- 所有动效只用 transform/opacity；prefers-reduced-motion + 页脚「减弱动效」开关
- jinja2 注意：dict 的 `items` 键须用 `g['items']`；CSS 选择器不用 `!=`
