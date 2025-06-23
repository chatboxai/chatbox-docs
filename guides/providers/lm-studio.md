# 如何将 Chatbox 连接到 LM Studio：分步指南

Chatbox 可以很好地连接到 LM Studio 服务，让你在使用本地模型时可以获取 Chatbox 提供的更多强大功能，比如 Artifact Preview、会话话题管理、Prompt 管理等。

你只需要简单几步就能连接到 LM Studio 服务：

### 1. 开启 LM Studio 服务

请先打开 LM Studio，按顺序开启以下选项：

1. 进入 Developer 模式
2. 进入 Developer 面板
3. 点击开关开启 Server（Status 显示为 running 即可）

![Chatbox connect LM Studio Guide 1](https://download.chatboxai.app/static/lm_studio_guide_1.png)

如果你希望使用 Chatbox 连接当前网络下另外一台机器上运行的 LM Studio 服务，或者你希望在 Chatbox 手机应用连接到你电脑上运行的 LM Studio 服务，那么你还需要完成下面两步设置：

4. 点击 Settings
5. 开启 Enable CORS
6. 开启 Serve on Local Network

![Chatbox connect LM Studio Guide 2](https://download.chatboxai.app/static/lm_studio_guide_2.png)

最后请复制 LM Studio 中显示的 API Host 地址。

### 2. 在 Chatbox 中连接 LM Studio 服务

打开 Chatbox 设置，在 Model Provider 中选择 LM Studio，然后输入对应的 API Host 即可。

![Chatbox connect LM Studio Guide 3](https://download.chatboxai.app/static/lm_studio_guide_3.png)

正常情况下你将在模型选项中看到 LM Studio 已经下载的模型列表，然后就能正常使用了。
