# kiro-cli-openclaw-bridge

OpenClaw Skill：将 [OpenClaw](https://github.com/openclaw/openclaw) 连接到 [Kiro CLI](https://kiro.dev) 的 ACP 后端，支持流式响应和工具调用。

## 安装

### 通过 ClawHub 安装（推荐）

```bash
clawhub install kiro-cli-openclaw-bridge
```

### 手动安装

将 `SKILL.md` 复制到你的 skills 目录：

```bash
git clone https://github.com/LuoShiXi/kiro-cli-openclaw-skill.git
cp -r kiro-cli-openclaw-skill ~/.openclaw/skills/kiro-cli-openclaw-bridge/
```

## 前置条件

- [kiro-cli](https://kiro.dev) 已安装并完成认证（`kiro-cli auth`）
- [ACP-to-OpenAI Bridge](https://github.com/LuoShiXi/kiro-cli-openclaw-bridge) 已运行

## 工作原理

```
OpenClaw  ──HTTP──▶  Bridge (FastAPI :18788)  ──stdio──▶  kiro-cli acp
```

Bridge 作为本地代理，将 OpenAI 格式的请求翻译为 ACP JSON-RPC 协议，让 OpenClaw 可以直接使用 kiro-cli 作为 AI 后端。

## 相关项目

- [kiro-cli-openclaw-bridge](https://github.com/LuoShiXi/kiro-cli-openclaw-bridge) — Bridge 源码和预编译二进制
- [ClawHub 页面](https://clawhub.ai/luoshixi/kiro-cli-openclaw-bridge) — 在线查看和安装

## License

MIT-0
