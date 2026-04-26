# 长期记忆

## Agent 配置（8个核心Agent分工）

| Agent | 昵称 | 技能 | 职责 |
|-------|------|------|------|
| 小戴 🧠 | 戴 | Alarm Memo Assistant Pro + wechat-clawbot-notify | 待办、闹钟、提醒、备忘录、每日推送、微信通知 |
| 小文 📄 | 文 | WeChat Article Save | 公众号文章抓取与存储 |
| 小静 🌱 | 静 | Life Principles | 人生原则管理与每日智慧推送 |
| 小林 💡 | 林 | Idea Capture | 灵感、想法快速记录 |
| 小红 📕 | 红 | 小红书助手 | 小红书运营推广、笔记发布、搜索、互动、博主分析 |
| 小风 🎨 | 风 | baoyu-cover-image | 文章封面图生成、视觉设计 |
| 小G 🐙 | G | GitHub + GitHub AI Trends | 代码仓库管理、Issues/PR/CI操作、AI趋势追踪 |
| 小图 🖼️ | 图 | Jimeng AI | 小红书封面生成、AI绘画、自媒体配图 |

> **2026-04-26 更新**：小图改用 Jimeng AI（即梦AI）Skill，通过 AI 绘画生成高质量小红书封面图。
> 
> **2026-04-26 更新**：新增小H Agent，使用 GitHub AI Trends Skill，追踪GitHub热门AI项目。

> **2026-04-25 更新**：用户已删除 book2skill skill，反馈"这个skill不好用"。book2skill 流程（阶段0→1→1.5→2→3→4）被认为过于繁琐、产出不够直接。后续如有书籍/文章拆解需求，改用更轻量的方式处理。

## 小红书助手 MCP 配置
- **安装完成**：2026-04-25，xiaohongshu-mcp Windows 预编译版 v2026.04.17.0444-c63748f
- **MCP 服务**：localhost:18060，已连接并登录成功
- **数据目录**：`~/.workbuddy/tools/xiaohongshu-mcp/`
- **功能验证**：登录状态检查、首页 feed 获取、搜索笔记、发布图文/视频、用户分析等

## baoyu-cover-image Skill 安装
- **安装时间**：2026-04-25
- **来源**：GitHub (JimLiu/baoyu-skills)
- **安全扫描**：✅ 已通过腾讯朱雀实验室 A.I.G 安全检测
- **功能**：文章封面图生成（5维度配置：类型/调色板/渲染/文本/情绪）
- **路径**：`~/.workbuddy/skills/baoyu-cover-image/`
- **特点**：纯文档型 skill，无脚本执行，提供风格指南和生成模板

## 业务相关
- **小红接定制skill的单**：用户要求在小红（可能是另一个AI客户端/智能体）接定制skill的订单

## 用户偏好
- 使用中文交流，语言简短直接
- 偏好本地桌面存储，文档以Markdown格式保存

## 自动化任务
- **早安待办推送**：每日 8:00，读取小戴的 todos.json + alarms.json，推送今日待办摘要
- **晚间完成总结**：每日 20:00，读取 todos.json，统计当日完成/未完成/完成率
- 数据文件路径：`~/.workbuddy/skills/alarm-memo-assistant-pro/data/`
- memos.md 尚未创建，推送暂不包含备忘录

## 合作项目
- 暂无进行中项目
