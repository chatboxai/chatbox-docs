---
icon: plug
---

# Use Chatbox AI in Third-Party Apps

Chatbox AI provides an OpenAI-compatible API interface, allowing you to use Chatbox AI services in third-party applications that support the OpenAI API.

## API Configuration

| Configuration | Value |
|---------------|-------|
| API Host | `https://ai.chatboxai.app` |
| API Key | Your Chatbox AI License Key |

## Getting Your API Key

1. Log in to your [Chatbox AI](https://chatboxai.app) account
2. Go to the Dashboard page
3. Copy your License Key

## Configuration in Common Apps

### Cursor

1. Open Cursor settings
2. Find **Models** > **OpenAI API Key** configuration
3. Enter your API Key
4. In **Override OpenAI Base URL**, enter: `https://ai.chatboxai.app/v1`

### Continue (VS Code Extension)

Add the following configuration to `~/.continue/config.json`:

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

1. Open Settings > Model Providers
2. Add a new provider, select **OpenAI API** type
3. Enter API address: `https://ai.chatboxai.app/v1`
4. Enter your API Key

### Open WebUI

1. Go to Admin Settings
2. Configure in **Connections** > **OpenAI API**
3. API Base URL: `https://ai.chatboxai.app/v1`
4. API Key: Enter your key

### Other OpenAI API Compatible Apps

Most applications that support the OpenAI API can be integrated as follows:

1. Find the OpenAI API or custom API configuration option
2. Set the API Base URL to: `https://ai.chatboxai.app/v1`
3. Enter your Chatbox AI API Key (License Key)
4. Select the model you want to use

## Available Models

Based on your subscription plan, you can use the following models:

**Advanced Models (Pro/Pro+ Plans)**
- `gpt-5` - GPT 5
- `claude-4.5-sonnet` - Claude 4.5 Sonnet
- `gemini-3-pro` - Gemini 3 Pro

**Standard Models (All Paid Plans)**
- `deepseek-chat` - DeepSeek V3
- `deepseek-reasoner` - DeepSeek R1
- `deepseek-v3.2` - DeepSeek V3.2
- `kimi-k2` - Kimi K2
- `gpt-5-mini` - GPT 5-mini
- `gemini-2.5-flash` - Gemini 2.5 Flash

> Note: Model names may be updated. Please refer to the official Chatbox AI website for the latest information.

## FAQ

### API Request Failed

- Check if the API Key is correct
- Confirm the API Host address is correct (note https and trailing slash)
- Confirm your subscription plan is valid

### Model Unavailable

- Check if your subscription plan supports this model
- Confirm the model name is correct

### Point Consumption

Using API integration consumes compute points from your account, just like using the Chatbox client. Please monitor your point usage.

## Related Links

- [Pricing Plans](plans.md)
- [Subscription Management](subscription-management.md)
