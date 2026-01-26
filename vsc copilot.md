1 - Install `Copilot Chat` from the Marketplace
2 - Install `generic-copilot` Chat from the Marketplace
  - Configure `generic-copilot` by pressing `CTRL + SHIFT + P`
  - open its menu:
  - <img width="654" height="74" alt="image" src="https://github.com/user-attachments/assets/3a6ec3b8-cde5-44cf-be35-69f480d77469" />
  - open `settings.json`
  - <img width="527" height="234" alt="image" src="https://github.com/user-attachments/assets/00c1b490-6077-45ef-aa8f-6b2cad66a809" />

- Edit the apikey with yours:
- OPTIONAL: change the model: `ID, SLUG`
- 
```javascript
"generic-copilot.providers": [
    {
        "id": "z.ai",
        "baseUrl": "https://api.z.ai/api/coding/paas/v4",
        "displayName": "z.ai",
        "vercelType": "openai-compatible",
        "apiKey": "YOURKEY.GOESHERE"
    }
],
"generic-copilot.models": [
    {
        "id": "GLM-4.7",
        "slug": "glm-4.7",
        "provider": "z.ai",
        "model_properties": {},
        "model_parameters": {},
        "displayName": "GLM-4.7"
    }
]
```
