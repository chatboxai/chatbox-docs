# How to Connect Chatbox to LM Studio: Step-by-Step Guide

Chatbox connects seamlessly to LM Studio services, allowing you to access more powerful features while using local models, such as Artifact Preview, conversation topic management, Prompt management, and more.

You just need a few simple steps to connect to LM Studio:

### 1. Start LM Studio Service

First open LM Studio and enable the following options in order:

1. Enter Developer mode
2. Enter the Developer panel
3. Click the switch to enable Server (Status should show running)

![Chatbox connect LM Studio Guide 1](https://download.chatboxai.app/static/lm_studio_guide_1.png)

If you want to use Chatbox to connect to an LM Studio service running on another machine on the current network, or if you want to connect the Chatbox mobile app to LM Studio running on your computer, you need to complete the following two additional steps:

4. Click Settings
5. Enable CORS
6. Enable Serve on Local Network

![Chatbox connect LM Studio Guide 2](https://download.chatboxai.app/static/lm_studio_guide_2.png)

Finally, copy the API Host address displayed in LM Studio.

### 2. Connect to LM Studio Service in Chatbox

Open Chatbox settings, select LM Studio in Model Provider, then enter the corresponding API Host.

![Chatbox connect LM Studio Guide 3](https://download.chatboxai.app/static/lm_studio_guide_3.png)

Under normal circumstances, you will see the list of models already downloaded in LM Studio in the model options, and then you can use it normally.
