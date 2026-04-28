# Learn Hermes Agent — 源码讲解

> 本教程的页面设计参考自 [Learn Claude Code](https://learn.shareai.run/zh/s05/)（19 章节、4 个阶段，带你从 0 到 1 手搓一个结构完整的 Claude Code-like Agent），
> 内容聚焦于 **Hermes Agent 源码架构**，重点对比 **Hermes 与 Claude Code 的设计差异**。

**在线访问：** [https://fairy2021.github.io/Hermes-learning/](https://fairy2021.github.io/Hermes-learning/)（启用 GitHub Pages 后可用）

---

## 这是什么

一份对照 Claude Code 设计哲学、深入 Hermes Agent 源码的交互式学习页面。

**核心视角：** 学 Hermes 源码最好的方式，不是读每行代码，而是理解它在"什么问题上做了和 Claude Code 不同的设计选择"。

## 覆盖内容

共 18 章，按 4 个阶段组织：

| 阶段 | 章节 | 主题 |
|------|------|------|
| 🔵 **核心架构** | s00–s06 | Agent 循环、Provider 抽象、工具系统、子代理、技能系统、上下文压缩 |
| 🟢 **系统加固** | s07–s10 | 提示词系统、记忆系统、插件机制、权限安全 |
| 🟡 **多平台网关** | s11–s14 | Gateway 架构、平台适配器、定时调度、Webhook |
| 🩷 **高级特性** | s15–s18 | Credential Pool、Profiles 隔离、Checkpoints、MCP 集成 |

## Hermes vs Claude Code 核心差异速览

| 维度 | Hermes | Claude Code |
|------|--------|-------------|
| Provider | 20+ 个 LLM，5 种传输模式 | 仅 Anthropic |
| 运行平台 | CLI + 15+ 消息平台 | 纯 CLI |
| 工具注册 | 自注册 + 21 个工具集 + 条件启用 | 硬编码 |
| 技能系统 | 动态自进化，Agent 可自动维护 | 静态 CLAUDE.md |
| 记忆系统 | 可插拔（内置/Honcho/Mem0） | 内置不可扩展 |
| API Key 管理 | 多 Key 池 + 自动轮换 + Fallback | 单 Key |
| 安全 | 注入检测+密钥脱敏+PII脱敏+Cron 扫描 | 基本审批 |
| 扩展性 | 插件/MCP/Cron/Webhook/Profiles | 有限 |

## 技术栈

- 纯 HTML + CSS + JavaScript（无框架依赖）
- 暗色/亮色模式自动适配
- 侧边栏导航 + 标签页切换
- 移动端适配

## 相关链接

- **Hermes Agent 源码：** [https://github.com/NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent)
- **Hermes Agent 文档：** [https://hermes-agent.nousresearch.com/docs/](https://hermes-agent.nousresearch.com/docs/)
- **Learn Claude Code (参考)：** [https://learn.shareai.run/zh/s05/](https://learn.shareai.run/zh/s05/)
- **本项目仓库：** [https://github.com/Fairy2021/Hermes-learning](https://github.com/Fairy2021/Hermes-learning)
