---
description: 06 May 2026
---

# Supercharging Reverse Engineering: Using VS Code to Orchestrate Ghidra and HexStrike AI

[https://medium.com/@fxxmm/supercharging-reverse-engineering-using-vs-code-to-orchestrate-ghidra-and-hexstrike-ai-7d520d306da5](https://medium.com/@fxxmm/supercharging-reverse-engineering-using-vs-code-to-orchestrate-ghidra-and-hexstrike-ai-7d520d306da5)

### HexStrike AI Set-up:

#### Clone the Repository:

git clone https://github.com/0x4m4/hexstrike-ai.git

cd hexstrike-ai

#### Create a Virtual Environment:

python3 -m venv hexstrike-env

source hexstrike-env/bin/activate

#### Install Dependencies:

pip3 install -r requirements.txt

Launch the Server:

HexStrike usually runs on http://127.0.0.1:8889.

Verify it's healthy by running: curl http://127.0.0.1:8889/health

&#x20;

### Connect

#### Tab 1: Start the Core API Server This is the part that actually runs the hacking tools.

cd \~/hexstrike-ai

source hexstrike-env/bin/activate

python3 hexstrike\_server.py

&#x20;

#### Tab 2: Start the MCP Bridge Now that the core is alive, restart the bridge so it can find it.

cd \~/hexstrike-ai

source hexstrike-env/bin/activate

python3 hexstrike\_mcp.py



![](<.gitbook/assets/unknown (25).png>)

&#x20;

![](<.gitbook/assets/unknown (26).png>)



### Ghidra MCP

[![](https://images.gitbook.com/__img/dpr=1.25,width=32,onerror=redirect,height=32,fit=contain,format=auto,signature=-477128472/https%3A%2F%2Fgithub.com%2Ffluidicon.png)Releases · symgraph/GhidrAssistMCPGitHub](https://github.com/symgraph/GhidrAssistMCP/releases)

[![](https://images.gitbook.com/__img/dpr=1.25,width=32,onerror=redirect,height=32,fit=contain,format=auto,signature=-477128472/https%3A%2F%2Fgithub.com%2Ffluidicon.png)Releases · symgraph/GhidrAssistGitHub](https://github.com/symgraph/GhidrAssist/releases)

Target: http://localhost:9090/sse

![](<.gitbook/assets/unknown (27).png>)



In VS Code, click on the third button to manage MCP servers.

![](<.gitbook/assets/unknown (28).png>)

<figure><img src=".gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

Restart the MCP Server by letting Cline reload its configuration to see the new HexStrike Server. Click on the Manage MCP Servers button. If HexStrike does not show a green status light, click the Refresh or Restart button within that panel.

![](<.gitbook/assets/unknown (29).png>)

The green light next to hexstrike means the server is active and Cline is successfully connected to your pen-testing toolkit.



<figure><img src=".gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>



Get an API key from openrouter.ai.&#x20;

<figure><img src=".gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>



Feel free to try other models.​

Prompt Example:

What is the main function?

What is the password?

Password or flag found in the exe in the Ghidra project.



<figure><img src=".gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>
