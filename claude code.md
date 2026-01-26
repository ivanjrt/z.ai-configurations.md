# Claude Code Configuration Guide

This guide will walk you through the installation and configuration of the Claude code command-line interface.

## 1. Prerequisites

Before you begin, ensure you open a new terminal window (like PowerShell or Command Prompt) with **Administrator rights**.

## 2. Installation

Execute the following command in your terminal to download and run the installer script:

```powershell
irm https://claude.ai/install.ps1 | iex
```


* Configuring Claude code
Modify this line with your own key: 
setx ANTHROPIC_AUTH_TOKEN your_zai_api_key

```
setx ANTHROPIC_AUTH_TOKEN "YOURAPI.TOKENGOESHERE"
setx ANTHROPIC_BASE_URL https://api.z.ai/api/anthropic
```

then edit / create this path: (change the USER-GOES-HERE to your username)
```
notepad C:\Users\USER-GOES-HERE\.claude\settings.json
```
Add this content:
```
{
  "env": {
    "ANTHROPIC_DEFAULT_HAIKU_MODEL": "glm-4.5-air",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "glm-4.7",
    "ANTHROPIC_DEFAULT_OPUS_MODEL": "glm-4.7"
  }
}
```

* Testing
you should now see the Model chosen:
`/status` this will tell you your information