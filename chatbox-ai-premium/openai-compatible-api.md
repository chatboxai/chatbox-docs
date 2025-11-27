---
icon: plug
---

# 在第三方应用中接入 Chatbox AI

Chatbox AI 提供 OpenAI 兼容的 API 接口，您可以在支持 OpenAI API 的第三方应用中使用 Chatbox AI 服务。

## API 配置信息

| 配置项 | 值 |
|--------|-----|
| API Host | `https://ai.chatboxai.app` |
| API Key | 您的 Chatbox AI License Key |

## 获取 API Key

1. 登录 [Chatbox AI](https://chatboxai.app) 账户
2. 进入Dashboard页面
3. 复制你的 License Key

## 在常见应用中配置

### Cursor

1. 打开 Cursor 设置
2. 找到 **Models** > **OpenAI API Key** 配置项
3. 填入您的 API Key
4. 在 **Override OpenAI Base URL** 中填入：`https://ai.chatboxai.app/v1`

### Continue (VS Code 插件)

在 `~/.continue/config.json` 中添加配置：

```json
{
  "models": [
    {
      "title": "Chatbox AI",
      "provider": "openai",
      "model": "gemini-3-pro",
      "apiKey": "your-chatbox-license-key",
      "apiBase": "https://ai.chatboxai.app/v1"
    }
  ]
}
```

### Cherry Studio

1. 打开设置 > 模型服务商
2. 添加新的服务商，选择 **OpenAI API** 类型
3. API 地址填入：`https://ai.chatboxai.app/v1`
4. 填入您的 API Key

### Open WebUI

1. 进入管理员设置
2. 在 **Connections** > **OpenAI API** 中配置
3. API Base URL：`https://ai.chatboxai.app/v1`
4. API Key：填入您的密钥

### 其他支持 OpenAI API 的应用

大多数支持 OpenAI API 的应用都可以通过以下方式接入：

1. 找到 OpenAI API 或自定义 API 配置选项
2. 将 API Base URL 设置为：`https://ai.chatboxai.app/v1`
3. 填入您的 Chatbox AI API Key（License Key）
4. 选择需要使用的模型

## 可用模型

根据您的订阅方案，可以使用以下模型：

**高级模型（Pro/Pro+ 方案）**
- `gpt-5` - GPT 5
- `claude-4.5-sonnet` - Claude 4.5 Sonnet
- `gemini-3-pro` - Gemini 3 Pro

**标准模型（所有付费方案）**
- `deepseek-chat` - DeepSeek V3
- `deepseek-reasoner` - DeepSeek R1
- `deepseek-v3.2` - DeepSeek V3.2
- `kimi-k2` - Kimi K2
- `gpt-5-mini` - GPT 5-mini
- `gemini-2.5-flash` - Gemini 2.5 Flash

> 注意：模型名称可能更新，请以 Chatbox AI 官网为准。

## 常见问题

### API 请求失败

- 检查 API Key 是否正确
- 确认 API Host 地址是否正确（注意 https 和末尾是否有斜杠）
- 确认您的订阅方案是否有效

### 模型不可用

- 检查您的订阅方案是否支持该模型
- 确认模型名称是否正确

### 点数消耗

使用 API 接入与在 Chatbox 客户端中使用相同，都会消耗您账户中的计算点数。请注意监控您的点数使用情况。

## 相关链接

- [付费方案说明](plans.md)
- [订阅管理](subscription-management.md)
