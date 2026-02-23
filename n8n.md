- OpenAI uses a very generic schema that is compatible with z.ai, so will be using that.

Save this snippet as json:
```json
{
  "name": "z.ai Agent",
  "nodes": [
    {
      "parameters": {
        "agent": "conversationalAgent",
        "promptType": "define",
        "text": "={{ $json.message || $json.text || $json.input }}",
        "options": {
          "systemMessage": "You are a helpful AI assistant. When given data or content, process it thoughtfully: summarize if it's long, answer questions if asked, and always be concise and clear in your response."
        }
      },
      "id": "ai-agent",
      "name": "AI Agent",
      "type": "@n8n/n8n-nodes-langchain.agent",
      "typeVersion": 1.7,
      "position": [500, 300]
    },
    {
      "parameters": {
        "model": "GLM-4.7",
        "options": {}
      },
      "id": "zai-chat-model",
      "name": "z.ai Chat Model",
      "type": "@n8n/n8n-nodes-langchain.lmChatOpenAi",
      "typeVersion": 1.2,
      "position": [440, 500],
      "credentials": {
        "openAiApi": {
          "id": "YOUR_ZAI_CREDENTIAL_ID",
          "name": "z.ai API"
        }
      }
    }
  ],
  "connections": {
    "z.ai Chat Model": {
      "ai_languageModel": [
        [
          {
            "node": "AI Agent",
            "type": "ai_languageModel",
            "index": 0
          }
        ]
      ]
    }
  },
  "settings": {
    "executionOrder": "v1"
  },
  "staticData": null,
  "tags": ["ai", "z.ai"],
  "meta": {
    "templateCredsSetupCompleted": false,
    "n8nVersion": "1.0.0"
  }
}
```
Create a new Canvas in n8n,  import the file

<img width="150" height="312" alt="image" src="https://github.com/user-attachments/assets/b57df9ec-6d6d-416c-a20b-2aa0ad220b0c" />


If you did it correctly, you should have this:

<img width="507" height="406" alt="image" src="https://github.com/user-attachments/assets/472f1487-a2bb-4c27-859b-2fdd956d5907" />

Double-click on the `model` , you can now change your model ie. 4.7 but this is up to you as long your accounts supports it
```
GLM-4.7
```

<img width="523" height="335" alt="image" src="https://github.com/user-attachments/assets/d0dc4219-9140-4309-950d-8bdc844203b9" />

Add your Model, API key, and the base URL

```
https://api.z.ai/api/coding/paas/v4
```
<img width="1193" height="744" alt="image" src="https://github.com/user-attachments/assets/a3850349-2ed5-4fb2-bb8e-c8d7f022b66a" />

That's it! 

You can create a webhook to test things out

