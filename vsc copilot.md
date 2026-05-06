1 - Install `Copilot Chat` from the Marketplace

<img width="345" height="83" alt="image" src="https://github.com/user-attachments/assets/2b882519-cfcc-4c62-9b8e-27c7b620c2fa" />


2 - Install `generic-copilot` Chat from the Marketplace

  - Configure `generic-copilot` by pressing `CTRL + SHIFT + P`
  - open its menu:
  - <img width="654" height="74" alt="image" src="https://github.com/user-attachments/assets/3a6ec3b8-cde5-44cf-be35-69f480d77469" />
  - open `settings.json`
<img width="576" height="731" alt="image" src="https://github.com/user-attachments/assets/bba55097-275f-42e0-b1e7-a99bb04d73e2" />


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
        "id": "glm-5.1",
        "slug": "glm-5.1",
        "provider": "z.ai",
        "model_properties": {},
        "model_parameters": {},
        "displayName": "glm-5.1"
    }
]
```
