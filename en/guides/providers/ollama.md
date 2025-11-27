# How to Connect Chatbox to Remote Ollama Service: Step-by-Step Guide

There are now more and more open-source models that allow you to run them on your own computer or server. Using local models has many advantages:

* Run completely offline, protecting your privacy and data security
* No need to pay for online API fees
* Completely offline, stable service, no network latency
* Freedom to adjust and customize model parameters

Chatbox connects seamlessly to Ollama services, allowing you to access more powerful features while using local models, such as Artifact Preview, file parsing, conversation topic management, Prompt management, and more.

(Note: Running local models requires certain hardware specifications, including RAM, GPU, etc. If you experience lag, try reducing model parameters.)

### Installing Ollama

Ollama is an open-source local model runtime tool that makes it easy to download and run various open-source models, such as Llama, Qwen, DeepSeek, etc. This tool supports Windows, MacOS, Linux, and other operating systems.

[Ollama Download](https://ollama.com/)

![Ollama Chatbox Guide](https://download.chatboxai.app/static/ollama_guide_1.png)

### Download and Run Local Models

After downloading and installing Ollama, open the command line terminal and enter the command to download and run local models. You can view all Ollama-supported models here: [Ollama Model List](https://ollama.com/models).

Example 1: Download and run the llama3.2 model

```bash
ollama run llama3.2
```

Example 2: Download and run the deepseek-r1:8b model (Note: DeepSeek R1 models on Ollama are actually distilled models)

```bash
ollama run deepseek-r1:8b
```

![Ollama Chatbox Guide](https://download.chatboxai.app/static/ollama_guide_2.png)

### Connect to Local Ollama Service in Chatbox

Open settings in Chatbox, select Ollama from the model provider, and you will see your running local model in the model dropdown.

![Ollama Chatbox Guide](https://download.chatboxai.app/static/ollama_guide_3.png)

Click save, and you can start chatting.

![Ollama Chatbox Guide](https://download.chatboxai.app/static/ollama_guide_4.png)

### Connect to Remote Ollama Service in Chatbox

In addition to easily connecting to local Ollama services, Chatbox also supports connecting to remote Ollama services running on other machines.

For example, you can run an Ollama service on your home computer and use the Chatbox client on your phone or another computer to connect to this service.

You need to ensure that the remote Ollama service is properly configured and exposed on your current network so that Chatbox can access it. **By default, you need to do some simple configuration for the remote Ollama service**.

#### How to Configure Remote Ollama Service?

By default, Ollama service only runs locally and does not provide external service. To enable the Ollama service to provide external service, you need to set the following two environment variables:

```bash
OLLAMA_HOST=0.0.0.0
OLLAMA_ORIGINS=*
```

#### Configuration on MacOS

1.  Open the command line terminal and enter the following commands:

    ```bash
    launchctl setenv OLLAMA_HOST "0.0.0.0"
    launchctl setenv OLLAMA_ORIGINS "*"
    ```
2. Restart the Ollama application for the configuration to take effect.

#### Configuration on Windows

On Windows, Ollama inherits your user and system environment variables.

1. Exit Ollama through the taskbar.
2. Open Settings (Windows 11) or Control Panel (Windows 10), and search for "environment variables".
3.  Click to edit environment variables for your account.

    Edit or create a new variable **OLLAMA\_HOST** for your user account with value **0.0.0.0**; Edit or create a new variable **OLLAMA\_ORIGINS** for your user account with value **\***.
4. Click OK/Apply to save the settings.
5. Launch the Ollama application from the Windows Start menu.

#### Configuration on Linux

If Ollama runs as a systemd service, you should use systemctl to set environment variables:

1. Run `systemctl edit ollama.service` to edit the systemd service configuration. This will open an editor.
2.  Add an Environment line for each environment variable under the \[Service] section:

    ```
    [Service]
    Environment="OLLAMA_HOST=0.0.0.0"
    Environment="OLLAMA_ORIGINS=*"
    ```
3. Save and exit.
4.  Reload systemd and restart Ollama:

    ```
    systemctl daemon-reload
    systemctl restart ollama
    ```

#### Service IP Address

After configuration, the Ollama service will be able to provide services within the current network (such as home WiFi). You can use the Chatbox client on other devices to connect to this service.

The IP address of the Ollama service is your computer's address on the current network, typically in the form:

```
192.168.XX.XX
```

In Chatbox, set the API Host to:

```
http://192.168.XX.XX:11434
```

#### Notes

* You may need to allow the Ollama service port (default 11434) in your firewall, depending on your operating system and network environment.
* To avoid security risks, do not expose the Ollama service to public networks. A home WiFi network is a relatively safe environment.

#### Reference

* [Ollama Service Configuration](https://github.com/ollama/ollama/blob/main/docs/faq.md#how-can-i-expose-ollama-on-my-network)
